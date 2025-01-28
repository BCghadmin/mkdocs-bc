## Signing a Direct Channel Agreement with the Bank Gateway

To use the bank interface in Business Central, you need to sign a *gateway* direct channel agreement with your bank and order a certificate. The bank will provide instructions for ordering the certificate after the agreement is signed. The certificate file format must be .p12 and password-protected.

### Swedbank

<https://www.swedbank.ee/business/d2d/ebanking/gateway>

Supported services:

-   Sending payments to the bank (unsigned payments)
-   Account statement -- automatically retrieves the previous day's statement
-   Query for the current day's account statement

### LHV

<https://www.lhv.ee/et/connect>

Supported services:

-   Sending payments to the bank (unsigned payments)
-   Account statement -- automatically retrieves the previous day's statement

### SEB

<https://www.seb.ee/ariklient/igapaevapangandus/elektroonilised-kanalid/baltic-gateway>

Supported services:

-   Sending payments to the bank (unsigned payments)
-   Query for the current day's account statement (the queue must be configured with sufficient frequency to avoid missing transactions at the end of the day)

### COOP Bank

<https://www.cooppank.ee/gateway>

Supported services:

-   Sending payments to the bank (unsigned payments)
-   Account statement -- automatically retrieves the previous day's statement

### Security Certificate

To use the bank interface in Business Central, you need to configure a security certificate. After signing the agreement, the bank will send instructions for ordering the certificate. As the steps involve technical details, it is recommended to seek assistance from your IT department or contact your BC partner.

Steps required:

-   Generate a certificate request for ordering the certificate.
-   Merge the certificate and private key files into a pfx/p12 file and generate a password.
-   Configure the pfx/p12 file and password in BC.

Swedbank guide:  
<http://dev.swedbankgateway.net/content/general-info/doc/How-to-generate-CSR-and-convert-private-key-to-p12.pdf>  
<https://www.swedbank.com/openbanking/swedbank-gateway-go-live.html>

LHV guide:  
<https://partners.lhv.ee/en/connect/#certificates>

SEB guide:  
<https://developer.baltics.sebgroup.com/bgw/documentation/authentication>

Coop Bank guide:  
<https://www.cooppank.ee/s3fs-public/juhendid/Gateway_votmete_genereerimise_juhend.pdf>

## Configuring the Bank Interface

Open Bank Interface settings in Business Central and select the bank to be integrated from the Bank Channels block. The fields to be configured differ by bank.

![Conf Bank Interface][13]

For **SWED SGW**, fill in the Agreement ID, API Key (Client ID), and Password fields, then upload the certificate using the Add Certificate button on the menu bar:

![SWED SGW configuration example][1]

For **SEB BGW**, fill in the Agreement ID field and add the certificate.

For **LHV CONNECT**, only the certificate needs to be added.

For **COOP CPGW**, details will be clarified later.

### Bank Account Configuration

Open the Bank Accounts list and access the card for the bank account to be integrated. Fill in the Bank Interface block:

![Bank account configuration example][2]

The following fields must be completed on the bank account card:

-   Payment instruction message numbers
-   Bank account posting group
-   SWIFT code
-   IBAN
-   Bank statement import format
-   Payment export format

### Queue Entries

Set the queue entries for the respective bank to the ready state.

![Queue entry example][3]

## Exporting Payments to the Bank

In the Payment Journal worksheet, check **Allow Payment Export** to enable sending the payment file to the bank and **Check Payment Statuses Before Posting** to verify the payment status before posting.

![Payment Journal example][4]

Complete the Payment Journal with payments to be made, either manually or by suggesting payments for a vendor.

To send the payment file to the bank, select **Bank -- Send to Bank...** from the menu bar.

![Send to Bank example][5]

Payments are sent to the bank in an unsigned state. They must be separately approved and executed in the bank.

After the payment file is sent to the bank, the Payment Journal factbox will display payment status information after a short while.

![Payment status example][6]

Possible payment statuses:

- **RJCT** -- Rejected -- the payment was rejected by the bank
- **ACTC** -- Pending -- awaiting approval and execution in the bank
- **PDNG** -- Pending -- awaiting confirmation
- **PART** -- Partially approved -- at least one payment is approved
- **ACSP** -- Approved -- the payment is approved but not yet executed
- **ACSC** -- Executed -- the payment has been executed
- **ACWC** -- Accepted with changes -- changes were made and accepted, but the payment is not yet executed
- **Pending** -- the payment import file is being verified (SEB)
- **File check successful** -- the payment import file verification was successful (SEB)
- **Rejected** -- the payment import file verification was unsuccessful (SEB)

## Importing Bank Statements

### Manual Import

In the Payment Matching Journal, select **Import Payments from Bank Interface**:

![Import Payments example][7]

In the window that opens, choose the type of statement to import for the desired bank:

![Statement type selection][8]

- **End-of-day statement** -- only the end date can be specified. All unimported bank transactions for this date will be retrieved into BC.
- **Statement** -- specify a period for retrieving the bank statement into BC.
- **Intraday statement** -- retrieves the BC working day's statement.

After setting the filters, a message will appear:

![Import query notification][14]

This means the query has been sent to the bank and it will take some time for the bank statement to appear in BC. SEB statements appear immediately.

## Automatic Import of Bank Statements

To automatically import the previous day's bank statement, configure the **Queue Entries** for an automatic task.

Go to **Queue Entries** and click **New**.

Fill in the **Executable Object Type** with **Report** and **Executable Object ID** with **79901**, and set the **Earliest Start Date/Time**:

![Queue entry configuration example][9]

Set the desired time for retrieving the previous day's statement into BC.

Then check the box for **Report Request Page Options**:

![Report request options example][10]

A view identical to **Import Payments from Bank Interface** in the Payment Matching Journal will open.

Fill in the **Bank** field for the bank statement to be imported automatically and select **End-of-Day Statement** in the Statement Type field. Leave the **Start Date** and **End Date** fields blank.

![Automatic import configuration example][11]

In the **Recurrence** block, specify which days the query should run and set the **Interval Between Runs (in minutes)** to **1440** to ensure the query is run daily.

![Recurrence settings example][12]

A separate queue entry must be created for each bank account.

  [1]: ./media/image2.png
  [2]: ./media/image3.png
  [3]: ./media/image4.png
  [4]: ./media/image5.png
  [5]: ./media/image6.png
  [6]: ./media/image7.png
  [7]: ./media/image8.png
  [8]: ./media/image9.png 
  [9]: ./media/image11.png
  [10]: ./media/image12.png
  [11]: ./media/image13.png
  [12]: ./media/image14.png
  [13]: ./media/image1.png
  [14]: ./media/image10.png
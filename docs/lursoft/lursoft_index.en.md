Through the Lursoft interface, it is possible to import the data of Estonian, Latvian and Lithuanian companies from the Lursoft company database into Dynamics 365 Business Central, including:

-   Company name

-   Address

-   Registration number

-   VAT number

To start the service, it is necessary to sign a contract with the database administrator.

Contacts: 
**SIA "LURSOFT IT"**

Matīsa street 8, Rīga, LV-1001

https://www.lursoft.lv/

[mailto:info@lursoft.lv]

## Setup

On the "Lursoft Business Register Setup" page, fill in the fields required for the connection.

-   Apply Default Settings - the Lursoft Query URL and Access Token URL will be added.

-   The query and token credentials will be sent by Lursoft after the contract is signed.

-   "Query Response" specifies Lursoft Business Register search country. The default language is Latvian.

![][1]

After the setup is done you can also test the connection by clicking "Test Connection." In the opening window "Lursoft Business Register Query," you can add the name or Reg. No. of the company you are looking for and the country you are looking for. If the connection is available, the imported data will be displayed in the left Business Register block.

![][2]

## Vendor Data Query

When creating a new vendor:

-   Open a new vendor card

-   Click "Query Lursoft Business Register"

-   In the opening window, enter the "Name to Search" (does not have to be exact) or "Reg. No. to Search" and fill in the "Search Region" with the name of the country where the company you are looking for is registered.

-   The data obtained from the register will be displayed in the left "Business Register" block.

-   By clicking on the "three dots box," you can add the data to Business Central either one by one or all at once.

-   The data added to Business Central can be modified on the same page or later on the vendor card.

-   Click OK - the data will be added to the vendor card.

Checking Existing Vendor Data

-   Open the vendor card to be checked

-   Click "Query Lursoft Business Register"

-   In the opening window, the reg code is pre-filled

-   The register data is displayed, and you can check it against the data in BC. If necessary, copy it by clicking on the "three-star box" either one by one or all at once.

![][3]

## Customer Data Query

This is done similarly to the vendor but from the customer card.

[mailto:info@lursoft.lv]: mailto:info@lursoft.lv

[1]: ./media/image1.en.png
[2]: ./media/image2.en.png
[3]: ./media/image3.en.png

The solution enables signing of bank payments in Business Central and sending the signed payments to the bank.

## Setup

To sign bank payments, it is necessary to set up default signers for the bank account.
To do this, go to Bank Accounts, open the bank account card, and select Bank Account - **Default Payment File Signer** from the menu bar.

![][1]

Enter the signer's name and select the BC user.

![][2]

Signers do not have to be BC users.

## Signing the Payment Journal

Open the Payment Journal, add the required payments, and select **Bank - Sign and Send to Bank** from the menu bar

![][3]

In the window that opens, the default signers set up for the bank account are displayed. In the Sign Payment File window, it is possible to change the signers - add or remove them.

![][4]

When you click OK, you will be asked: "Do you want to open the created signing container?"

![][5]

Click Yes if you are the signer yourself. The Signing Container will open, where you can download the payment file, add more documents for signing if needed, change signers, and sign.

![][6]

In the Signing Container Documents section, you can download (Download) or view (View) the payment file. Through the Upload files menu item, you can add files for signing.

![][7]

In the \"Signing Container Signers\" section, you can add (New Line) and remove signers (Delete Line) and sign (Sign).

Possible statuses during signing:

- Draft - waiting for signing

- Signing - signing in progress

- Signed - signed

- Rejected - signer has refused

- Skipped

When all signers have signed the payment file, the Container Status in the header changes to "Signed".

![][8]

A Signing Container with the status "Signed" can be sent to the bank using the "Send to Bank" button in the menu bar or you can set up a workflow entry that automatically sends signed payments to the bank.

  [1]: ./media/image1eng.png
  [2]: ./media/image2eng.png
  [3]: ./media/image3eng.png
  [4]: ./media/image4eng.png 
  [5]: ./media/image5eng.png
  [6]: ./media/image6eng.png
  [7]: ./media/image7eng.png
  [8]: ./media/image8eng.png

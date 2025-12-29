This solution enables you to send the VAT declaration electronically to the Estonian Tax and Customs Board through X-Road from Dynamics 365 Business Central.

Managers of companies and institutions registered in the Estonian Business Register can join X-Road via X-Road Self-Service Portal: [X-tee iseteenindus]

To use this functionality in Business Central, the service must be enabled by the Tax and Customs Board. More information: [\[X-tee services \| Estonian Tax and Customs Board\]](https://www.emta.ee/en/business-client/e-services-training-courses/how-use-e-services/x-tee-services)

# Sending the VAT Report to the Tax and Customs Board via the X-Road Interface

## Setup

On page **XRoad Setup**, upload a certificate: Actions -\> Upload Certificate. Enter the certificate password in the Password field and press ENTER.

In the field **Submitter Person Code**, add the personal identification code of the user who has permission to submit the declaration in the Tax and Customs Board.

To send a confirmed VAT report to the Tax and Customs Board, select **Submit with Confirmation** on the **XRoad Setup** page.

![][1]

## Using the Functionality

The VAT report is generated according to Estonian localization on the VAT Return page.

Once the declaration lines are created and checked, Release the document.

To send the declaration: **Home -\> Send via X-Road**.

![][2]

Fields for monitoring status have been created:

- **XRoad Log Entry No**. - filled with the entry number after sending

- **XRoad status** - displays the status of the declaration:

- **Sent** - KMD has been sent to the Tax and Customs Board

- **Received** - KMD not confirmed in BC has been received by the Tax and Customs Board

- **Accepted** - KMD confirmed in BC has been received by the Tax and Customs Board

- **Error** - The Tax and Customs Board has rejected the KMD due to errors

The **Job Queue Entry** 24014760 Update XRoad Message Status retrieves responses from the Tax and Customs Board.

## Message Logs

Clicking the XRoad Log Entry No -\> number value opens the **XRoad Message Log**.

![][3]

You can view both Request Messages and Response Messages by clicking Yes in the respective column.

**Open Message Status Log** opens the XRoad Message Status Log page. Here you can open both Request Messages and Response Messages in text format. Also, Operation Accepted or Rejected XML messages.

You can also manually request responses from the Tax and Customs Board by clicking **Ask response** on the XRoad Message Status Log page. The comment "No pending messages found" means that all response messages from the Tax and Customs Board have been received.

  [X-tee iseteenindus]: https://x-tee.ee/en/home
  [X-tee services \| Estonian Tax and Customs Board]: https://www.emta.ee/en/business-client/e-services-training-courses/how-use-e-services/x-tee-services
  [1]: ./media/image1eng.png
  [2]: ./media/image2eng.png
  [3]: ./media/image3eng.png

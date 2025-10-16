Before installing the extension, the following extensions need to be added:

- Smart Item Codes

- VAT Reporting Localization for Estonia

## User rights

For a user with limited rights (not SUPER), assign the user rights set CPC-BSE CENTRALPLUS.

## Reports

Document designs based on Estonian legislation have been added to the following documents:

- Purchase order

- Posted sales credit memo

- Invoice draft

- Posted sales invoice

- Sales order - order confirmation and pro forma

- Sales quote

- Posted sales shipment

- Blanket purchase order

- Blanket sales order

Layouts are created as extensions to BC standard reports.

### Report setup

To apply all the above layouts, go to Company Information, select Actions - Report Selection - Apply Suno365 Layouts:

![][1]

For individual documents, follow these instructions to assign Suno Layouts:

1\.  Search for Report Selection and select the report selection for the respective module.

![][2]

2\.  Select the document you want to change the printout for from the Usage menu.

![][3]

3\.  Click on the Report Layout field.

![][4]

4\.  Select the desired report design by marking the row and clicking OK.

![][5]

The names of Suno365 printouts start with CPC-BSE.

## Dimension Corrector

The BC standard dimension corrector (for general ledger entries) has been supplemented with the ability to change dimensions in value/item, customer, and vendor ledger entries.

To correct dimensions in entries, search for Dimension Corrections and create a New one.

Select the ledger entries where the dimension value needs to be changed. By default, the update of all ledger entries is enabled.

![][6]

## Copying General Ledger Entries to Journal

Search for the general ledger entry you want to copy to the journal. Only general ledger entries related to the same document number are copied to the journal.

Then select Actions from the menu bar -> Functions -> Copy Transaction to Journal...

![][7]

If the selected general ledger entry is related to other ledgers, a warning is given that entries from other ledgers are not included in the copy.

The Copy Transaction Entries page opens, showing a preview of the entry to be copied to the journal.

To create the journal, click the Create Journal button in the header.

![][8]

After clicking Create Journal, you will be asked whether to copy the entry with the original document number or assign a new document number.

![][9]

Then you can choose which journal template and worksheet to copy the entry to.

![][10]

Go to the journal where you copied the entry. Make changes if necessary and post the journal.

![][11]

## Location Locking

If the location used in the document line is locked, an error message "Posting to Location is blocked" is displayed during posting and posting preview.

### Setup

Go to Inventory Setup, where you enable the Allow to Block Locations marker:

![][12]

When the Allow to Block Locations marker is enabled, a Blocked field is added to the Location Card, which must be enabled to lock the location.

![][13]

### Usage

When making a transaction with goods located in a locked location, an error message is displayed during posting preview and posting.

![][14]

## Automatic Reservation of Goods on Transfer Order

An automatic reservation setting for transfer order lines has been added to the Inventory Setup in the Suno Base section.

![][15]

When the setting is enabled, the goods on the transfer order lines are automatically reserved. In the standard, the reservation of goods must be done manually.

## Modifying Posted Sales Documents

The ability to change certain fields on posted sales invoices and posted sales shipments has been added.

Open the posted document that needs to be modified and select Home from the menu bar -> Edit Document.

![][16]

The Edit Posted Document page opens, showing all the fields that can be changed on the posted sales invoice.

![][17]

The following fields can be changed on the posted sales shipment:

![][18]

## Additional costs

Adding additional costs (e.g., transport) to the item on a line-by-line basis. The additional cost is linked to the item specified in the item ledger entries.

### Setup

To assign an additional cost to a sales document line, specify the Additional Cost marker in the Sales & Receivables Setup. Up to 3 additional cost markers can be specified.

![][19]

### Usage

After setting the additional cost marker, an Additional Cost field appears on the sales order and sales invoice lines.

![][20]

The additional cost is only reflected in the value entries related to the sales shipment.

![][21]

## Posting Entries on Invoice

### Sales Setup

In the Sales & Receivables Setup, it is possible to set up the posting of invoices by item lines and the copying of the item line description to the PR entry.

![][22]

When the setting Invoice Posting per lines (Item) is enabled, lines with the same item code are posted separately (summed up in the standard) and the description on the document line is copied as the entry description.

### Purchase Setup

A setting for posting invoices by item lines has been added to the Purchases & Payables Setup.

![][23]

When the setting Invoice Posting per Line is enabled, a separate general ledger entry line is created for each item and fixed asset line on the purchase invoice, and the description of the purchase invoice line is copied as the entry description.

## Mandatory Fields for Items

Mandatory fields can be set for items through the item category.

### Setup

In the Inventory Setup, enable the Item Mandatory Fields.

![][24]

Go to the Item Categories list, select the row for which you want to set mandatory fields. Then select Mandatory Fields for Items from the menu that opens from the arrow next to New.

![][25]

On the Item Category Mandatory Fields page that opens, mark the fields that are mandatory.

![][26]

### Usage

When the Item Mandatory Fields is enabled in the Inventory Setup, an item category must be assigned to each item.

When creating a new item card, a Blocked field is activated on the card.

![][27]

The Blocked field can be deactivated when all mandatory fields set through the item category are filled in on the item card.

![][28]

## Creating a Transfer Order from a Sales Order

### Setup

The prerequisite for creating a transfer order directly from a sales order is that a Requisition Worksheet template and Requisition Worksheet name are specified in the Inventory Setup, and transfer routes are set up or the Default Direct Transfer setting is enabled.

![][29]

### Usage

While on the sales order, select Actions from the menu bar - Functions - Create Transfer Order.

![][30]

You will be asked whether to create a transfer order for all lines or only for selected lines (lines marked on the sales order).

![][31]

On the page that opens, specify the Transfer-from Code.

![][32]

## Salesperson from Buyer Customer Card

In standard BC, the salesperson field on the sales document is overwritten with the salesperson of the payer customer when another customer is specified as the payer.

Enable the Take Salesperson Always From Sell-to Customer setting in the Suno Base section of the Sales & Receivables Setup to prevent the salesperson field on the sales document from being overwritten when adding a payer customer.

![][33]

## Obsolete Items Report

The purpose of the Obsolete Items report is to get an overview of items in the warehouse that have not moved or are moving slowly.

You can find the Obsolete Items report through the search.

![][34]

Up To Posting Date - specify the date until which the purchase transactions of the item are included in the report.

Up To Last Transaction Date - specify the date as of which you want to see the transactions. The date when the item was last consumed or transferred from one warehouse to another.

Last Transaction Entry Type Filter - the type of entry to be considered for the last transaction. If the filter is empty, the last transaction that is not a purchase is searched for.

The report is issued in Excel.

![][35]

## Inventory Valuation (SUNO) Report

The Inventory Valuation (SUNO) report is a copy of the BC standard Inventory Valuation report, supplemented with the following options:

![][36]

## Additional Fields on Documents, Cards, Lists

#### Rating QMS on Vendor Card

A numeric field Rating QMS has been added to the Vendor Card.

![][37]

#### Balance at Date for Vendors in the Register

Fields Balance at Date and Balance at Date (LCY) have been added to the Vendors register, where the balance as of today\'s date is displayed by default. Using the date filter, it is possible to see the balance of the vendor as of the specified date.

![][38]

#### Exclusion from ECSL Report

A field No Declaration on ECSL has been added to the VAT Posting Setup page:

![][39]

By checking the box on the line with the combination of VAT Bus. Posting Droup and VAT Prod. Posting Group, the VAT entries are excluded from the EU sales list reports (VD) when compiling these VAT entries.

#### Source fields in Item Ledger Entries List

Fields Source Type, Source No., and Source Name have been added to the Item Ledger Entries list.

Source fields in item ledger entries provide a better overview of which companies the item movements have been made with.

![][40]

#### Internal Reference on Documents

A field Internal Reference (text field, 250 characters) has been added to purchase and sales documents and lists, intended for internal communication between different parties or for storing necessary information about the document.

![][41]

![][42]

The Internal Reference field has been added to the following documents and lists:

- Sales invoice, sales invoices list

- Posted sales invoice, posted sales invoices list

- Purchase invoice, purchase invoices list

- Posted purchase invoice, posted purchase invoices list

- Purchase order

- Posted purchase receipt

- Purchase return order

- Posted return shipment

- Purchase orders archive

- Purchase return orders archive

- Purchase credit memo

- Posted purchase credit memo

#### Document Creator/Modifier and Time Fields

Fields document Created At, Author, Modified At, and Modifier have been added to the document register, providing a quicker overview of who created the document and who last modified it. The last modifier on the posted document is the person who posted the document.

![][43]

#### Profit and Profit % Fields on Sales Order

Fields Line Profit % and Line Profit (LCY) have been added to the sales order lines, and fields Total Profit (LCY) and Total Profit % have been added below the lines.

![][44]

Formulas for calculating profit:

- Line Profit (LCY) = Line Amount - (Unit Price \* Quantity)

- Line Profit % = (Line Amount - (Unit Price \* Quantity)) \* 100 / Line Amount

- Total Profit (LCY) = Sum of Line Profit (LCY) values - Total Invoice Discount Amount excluding VAT

- Total Profit % = Total Profit (LCY) / Total excluding VAT \* 100

#### Posting Date of Item Ledger Entries in Value Entries Register

The posting date of the related item ledger entry has been added to the value entries register.

![][45]

Item Ledger Entry Posting Date in the value entries allows checking if there are items that have been delivered and invoiced in different months.

#### Fields in Sales Lines and Purchase Lines List

The following fields have been added to the sales lines list:

- Bill-to Customer Name

- Sell-to Customer Name

- Document Date

- Ship-to Name

The following fields have been added to the purchase lines list:

- Document Date

- Buy-from Vendor Name

- Pay-to Name

- Ship-to Name

#### Sales Order Factbox Enhancements

The Sales Order Factbox has been enhanced with the Item Ledger Entries, and Posted Sales Invoice Lines.

![][46]

Clicking on the Item Ledger Entries opens the item ledger entries with the customer filter, where it is possible to see which items have been sold to the customer on the sales order.

Clicking on the Posted Sales Invoice Lines opens the posted sales invoice lines list, where it is possible to see the items sold to the customer with quantities, prices, and discounts.

![][47]

Posted Sales Invoice Lines have been added to Sales Line Details, where clicking on the posted sales invoice lines opens the posted sales invoice lines list for the active sales order line item, showing the items sold to the customer with quantities, prices, and discounts.

  [1]: ./media/image1eng.png
  [2]: ./media/image2eng.png
  [3]: ./media/image3eng.png
  [4]: ./media/image4eng.png
  [5]: ./media/image5eng.png
  [6]: ./media/image6eng.png
  [7]: ./media/image7eng.png
  [8]: ./media/image8eng.png
  [9]: ./media/image9eng.png
  [10]: ./media/image10eng.png
  [11]: ./media/image11eng.png
  [12]: ./media/image12eng.png
  [13]: ./media/image13eng.png
  [14]: ./media/image14eng.png
  [15]: ./media/image15eng.png
  [16]: ./media/image16eng.png
  [17]: ./media/image17eng.png
  [18]: ./media/image18eng.png
  [19]: ./media/image19eng.png
  [20]: ./media/image20eng.png
  [21]: ./media/image21eng.png
  [22]: ./media/image22eng.png
  [23]: ./media/image23eng.png
  [24]: ./media/image24eng.png
  [25]: ./media/image25eng.png
  [26]: ./media/image26eng.png
  [27]: ./media/image27eng.png
  [28]: ./media/image28eng.png
  [29]: ./media/image29eng.png
  [30]: ./media/image30eng.png
  [31]: ./media/image31eng.png
  [32]: ./media/image32eng.png
  [33]: ./media/image33eng.png
  [34]: ./media/image34eng.png
  [35]: ./media/image35eng.png
  [36]: ./media/image36eng.png
  [37]: ./media/image37eng.png
  [38]: ./media/image38eng.png
  [39]: ./media/image39eng.png
  [40]: ./media/image40eng.png
  [41]: ./media/image41eng.png
  [42]: ./media/image42eng.png
  [43]: ./media/image43eng.png
  [44]: ./media/image44eng.png
  [45]: ./media/image45eng.png
  [46]: ./media/image46eng.png
  [47]: ./media/image47eng.png

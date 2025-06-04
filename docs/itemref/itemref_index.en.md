### Purchase configurations

The configurations related to the purchases are on the "Purchase & Payables Setup" page in the "Suno Item References" block

![][1]

**Item numbers on purchace documents**

![][2]

**Item reference numbers on purchase orders**

![][3]

### Sales configurations

The configurations related to sales are on the "Sales & Receivables Setup" page in the "Suno Item References" block

![][4]

**Item numbers on sales documents**

![][5]

**Item reference numbers on sales orders**

![][6]

### Vendor configurations

Configurations related to the vendor are on the vendor card in the "Suno item references" block.

![][7]

### Customer configurations

Configurations related to the customer are on the custromer card in the "Suno item references" block.

![][8]

## Functionality

The functionalities used are related to the following tables and fields. With the table entries in the "Item Reference List" table.

![][9]

With the fields "Vendors item no." on the items card.

![][10]

Vendor and customer card in the drop-down menu "Item code on purchase (sales on customer card) documents".

![][11]

## Item number on purchase or sales documents 

Use of different item numbers on the printout of purchase or sales documents. The extension does not affect Microsoft Base printouts, and to use it, a dependency on Suno Item Ref must be added to the corresponding printout extension (for example, Suno Base). An example of a printout where the item number is changed on the printout.

![][12]

It is possible to choose between 5 different options in the purchase or sale configuration: Empty (BC standard), Item, Barcode/vendor/Item, Vendor/barcode/item, Vendor\'s item no./item. In the case of sales documents, it is the customer instead of the vendor.

![][13]

It is possible to choose between 5 different options in the purchase or sale configuration: Empty (BC standard), Item, Barcode/vendor/Item, Vendor/barcode/item, Vendor\'s item no./item. In the case of customer card, it is the customer instead of the vendor.

![][14]

The general logic applies that if an option is selected on the vendor or customer card, it only applies to the given vendor's or customer's documents and also does not depend on what is specified in the purchase or sales configuration.

For all the selections, the logic is that the first match found in the sequence is used. For example: Barcode/Vendor/Item.

![][15]

![][16]

For such a purchase order, the barcode reference number found in the "Item Reference List" table is used for document printouts. If this value was not found in the table, then the vendor code associated with the item would have been searched, and if it had not been found, then the item number specified on the item would have been used. If none of these searches yield a result, then the BC standard value is used.

![][17]

## Item reference number on purchase or sales order 

Using different reference numbers on a purchase or sales order. Example of a purchase order field item reference number.

![][18]

It is possible to choose between 4 different options in the purchase or sale configuration: Blank (BC standard), Vendor/Barcode, Vendor/Barcode/Unspecified, Barcode/Vendor. In the case of sales order, it is the Customer instead of the Vendor.

![][19]

For all the selections, the logic is that the first match found in the sequence is used. For example: Vendor/Barcode/Unspecified.

![][20]

![][21]

In the case of such a purchase order, the supplier's reference number found in the "Item reference list" table, is used in the purchase order line "Item Reference No". If this value was not found in the table, then the barcode related to the item would have been searched, and if it had not been found, then the item code without specifying field "Reference type" would have been searched in the table. If none of these searches yield a result, then the BC standard value is used.

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
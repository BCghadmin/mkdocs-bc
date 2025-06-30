Depends on Estonian Bank Formats Localization.

The extension includes the configuration for mandatory vendor reference numbers and the calculation of customer reference numbers.

### Mandatory vendor Reference Number

On the vendor card, there is a setting for Reference Mandatory.

![][1]

When this settings is enabled, a check is performed during the preview and posting of purchase orders and purchase invoices to ensure that the "Payment Reference" field is filled in. In the payment journal and payment matching journal, a check is performed to ensure that invoices with different reference numbers are not linked to a single payment. If they are, an error message is displayed, asking if you want to use the reference number specified on the supplier card.

### Customer Reference Numbers

With the Estonian Bank Formats Localization development, it is possible to set up the generation of reference numbers for newly created customers. In this solution, it is possible to generate a reference number for existing customers in BC. The reference number is created from the BC customer number and a check digit is added.

There are two options for generating a reference number for a customer:

1. From the customer card menu bar, Home - Calculate Reference No.

![][2]
2. Estonian Bank Formats Setup - Calculate Cust. Payment Ref. Nos.

![][3]

In the Estonian Bank Formats Setup, you can select the customers for whom a reference number needs to be created. If no selection is made, reference numbers are calculated for all customers.

  [1]: ./media/image1eng.png
  [2]: ./media/image2eng.png
  [3]: ./media/image3eng.png

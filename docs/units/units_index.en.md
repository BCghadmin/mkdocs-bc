## Setting Up Alternative Units of Measure

Alternative units are units that have defined mathematical relationships between them, allowing conversion from one unit to another within the same physical quantity.

To set up alternative units of measure, go to the **Inventory Setup** page. In the **Suno Units** section, specify the unit symbols between which conversion is allowed. To use this functionality, enable the following flags:

- **Keep Line Base Quantity** - ensures that the quantity in the base unit of measure is maintained during unit conversion.

- **Item UOM Conversion Log** - a log that records the values used for unit conversions in item transactions.

![][1]

## Managing Alternative Units of Measure

This functionality simplifies calculations between units. A new field, **Relational Quantity**, is added to the relationships between item units of measure. The value calculated in this field represents the quantity of the respective unit per one base unit.

You can find this information by navigating to the item card header: **Related → Item → Units of Measure**.

![][2]

![][3]

Open **Units of Measure** and mark the units for which the **Relational Quantity** should be used to preserve the base quantity. On the same page, you can define the **Rounding Tolerance**, which indicates the rounding rule used in unit conversions. Currently, Business Central applies rounding to the fifth decimal place.

![][4]

Conversions between different quantity units are recorded in the **Item Unit of Measure Log** table after the first use. For each subsequent use of the same quantity and unit, the system retrieves the required conversion value from the log.

![][5]

## Using Alternative Units of Measure

Once the functionality is enabled, alternative units and their quantities are displayed on the following documents: blanket purchase order, purchase order, purchase return, blanket sales order, sales order, sales return, and transfer order lines. All referenced documents include factboxes titled **Quantities in Alternative Units**, which provide quick information on the conversion of quantities from the base unit to available alternative units.

![][6]

![][7]

  [1]: ./media/image1eng.png
  [2]: ./media/image2eng.png
  [3]: ./media/image3eng.png
  [4]: ./media/image4eng.png
  [5]: ./media/image5eng.png
  [6]: ./media/image6eng.png
  [7]: ./media/image7eng.png

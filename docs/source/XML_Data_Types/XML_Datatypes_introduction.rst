XML Data Types
==============

In XML, data types define the **kind of data** that an element or attribute can hold.  
XML provides a range of **built-in data types** that help ensure the validity of XML content.

### Key Data Types in XML:

- 🧮 **String**: Represents textual data. Example: `<name>John</name>`
- 📅 **Date/Time**: Represents dates or times. Example: `<date>2025-04-26</date>`
- 🔢 **Integer**: Represents whole numbers. Example: `<age>25</age>`
- 💵 **Decimal**: Represents real numbers or floating-point values. Example: `<price>19.99</price>`
- ✔️ **Boolean**: Represents `true` or `false` values. Example: `<active>true</active>`
- 📏 **QName**: A qualified name, used in XML to refer to elements or attributes with namespaces. Example: `<ex:address>1234 Elm St</ex:address>`

### XML Schema Data Types:
When using **XSD (XML Schema Definition)**, you can specify data types for XML elements and attributes.  
This ensures that the data matches the expected format and constraints.

Example of defining a data type in XSD:

.. code-block:: xml

   <xs:element name="age" type="xs:int"/>

This defines the `age` element to only accept integer values.

### Why Use Data Types?

- **Validation**: Ensures that the data is in the correct format.
- **Consistency**: Guarantees uniformity across different systems using the same XML structure.
- **Precision**: Allows specific rules for data formats, such as date formats or currency precision.

----

> 📌 **Reminder:** When creating XML files, it's important to define appropriate data types to ensure data integrity and consistency.


XSD Introduction
=================

**XSD** stands for **XML Schema Definition**.  
It is a powerful way to define the structure, content, and data types of XML documents.

With XSD, you can:

-  Define **element names**, **attributes**, and **data types**
-  Set **rules and constraints** (like required fields or value ranges)
-  Support **reusable types** and **complex structures**
- Validate whether an XML file is well-formed **and** valid

Here’s why XSD matters:

- It provides a **blueprint** for XML data exchange.
- It ensures data consistency across systems or platforms.
- It's more expressive and type-safe than older DTD (Document Type Definition).

XSD files usually end with `.xsd` and are written in XML syntax themselves.

Example usage:

.. code-block:: xml

   <xs:element name="price" type="xs:decimal"/>

This line defines an XML element `<price>` that must contain a decimal value.


**Tip:** Always validate your XML against an XSD when working with structured data formats like APIs, config files, or business forms.

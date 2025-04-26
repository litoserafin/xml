====================================================================================================
                                      XML Schema (XSD)
====================================================================================================
XML Schema (XSD) defines the structure and content of XML documents. It provides a set of rules for the
XML data, specifying the types of elements and attributes, the relationships between them, and any
constraints on their content.

----------------------------------------------------------------------------------------------------
                                      Key Components:
----------------------------------------------------------------------------------------------------
- **Element**: Defines the structure and content of XML data.
- **Attribute**: Specifies additional properties or characteristics of elements.
- **Complex Types**: A combination of elements and/or attributes that can be nested.
- **Simple Types**: Define individual data types (e.g., string, integer, date).
- **Data Types**: Define the kind of data the elements can hold (e.g., string, integer, date, etc.).

----------------------------------------------------------------------------------------------------
                                XML Schema Syntax Example:
----------------------------------------------------------------------------------------------------
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
  
  <!-- Define a simple type -->
  <xs:element name="name" type="xs:string"/>
  
  <!-- Define a complex type -->
  <xs:complexType name="addressType">
    <xs:sequence>
      <xs:element name="street" type="xs:string"/>
      <xs:element name="city" type="xs:string"/>
    </xs:sequence>
  </xs:complexType>

  <!-- Define an element using a complex type -->
  <xs:element name="address" type="addressType"/>
  
</xs:schema>

----------------------------------------------------------------------------------------------------
                                    Why Use XML Schema (XSD)?
----------------------------------------------------------------------------------------------------
- **Data Validation**: Ensures XML documents conform to a predefined structure and data types.
- **Interoperability**: Allows systems to understand and share XML data across platforms and languages.
- **Automation**: Tools can automatically generate code or other artifacts based on XSD definitions.
- **Consistency**: Enforces consistent structure and rules across XML documents.
====================================================================================================

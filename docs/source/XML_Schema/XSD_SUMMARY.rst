XSD Schema SUMMARY!
==================

XSD Introduction
----------------
**XML Schema Definition (XSD)** is a way to define the structure and data types of an XML document. It ensures that XML data adheres to a specified format, and it is the most commonly used method for defining XML document structures. XSD provides more features and control over XML validation than DTDs.

XSD How To
-----------
XSD is usually defined using XML syntax itself. To create a valid XML schema, you must use the `<schema>` element and define the structure, data types, and constraints for your XML data.

Basic structure of an XSD document:

.. code-block:: xml

   <xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
     <!-- Define elements and attributes here -->
   </xs:schema>

XSD `<schema>`
--------------
The `<xs:schema>` element is the root element of an XSD document. It defines the namespace and serves as a container for all other elements, attributes, and data type definitions.

Example of an XSD schema declaration:

.. code-block:: xml

   <xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
     <xs:element name="book" type="xs:string"/>
   </xs:schema>

XSD Elements
------------
Elements in XSD define the structure of the data. You can define simple or complex elements and specify their data types (e.g., `xs:string`, `xs:int`).

Example of defining an element:

.. code-block:: xml

   <xs:element name="title" type="xs:string"/>

This defines a `title` element with a `string` data type.

XSD Attributes
--------------
Attributes define additional properties for elements. They are used to provide more details or characteristics about an element.

Example of defining an attribute:

.. code-block:: xml

   <xs:attribute name="category" type="xs:string"/>

This defines an attribute `category` with a `string` data type.

XSD Restrictions
----------------
**Restrictions** are used to apply constraints to an element or attribute's data type. You can restrict a data type to certain values, lengths, or patterns.

Example of a restriction:

.. code-block:: xml

   <xs:element name="price" type="xs:decimal">
     <xs:restriction base="xs:decimal">
       <xs:minInclusive value="0"/>
     </xs:restriction>
   </xs:element>

This restricts the `price` element to only accept decimal values greater than or equal to `0`.

XSD Complex Elements
--------------------
A **complex element** contains other elements or attributes within it. It is defined using the `complexType` element in XSD.

Example of a complex element:

.. code-block:: xml

   <xs:element name="book">
     <xs:complexType>
       <xs:sequence>
         <xs:element name="title" type="xs:string"/>
         <xs:element name="author" type="xs:string"/>
       </xs:sequence>
     </xs:complexType>
   </xs:element>

XSD Empty
---------
An **empty element** contains no child elements or text. It can be defined with an empty `complexType`.

Example of an empty element:

.. code-block:: xml

   <xs:element name="note">
     <xs:complexType/>
   </xs:element>

XSD Elements-only
-----------------
**Elements-only** content model means the element can only contain other elements and no text.

Example:

.. code-block:: xml

   <xs:element name="library">
     <xs:complexType>
       <xs:sequence>
         <xs:element name="book" minOccurs="0" maxOccurs="unbounded"/>
       </xs:sequence>
     </xs:complexType>
   </xs:element>

XSD Text-only
-------------
**Text-only** content model means the element can only contain text and no other elements.

Example:

.. code-block:: xml

   <xs:element name="description" type="xs:string"/>

This element can only contain text (a string).

XSD Mixed
----------
A **mixed content model** allows an element to contain both text and other elements.

Example of mixed content:

.. code-block:: xml

   <xs:element name="note">
     <xs:complexType>
       <xs:mixed/>
     </xs:complexType>
   </xs:element>

XSD Indicators
--------------
**Indicators** like `minOccurs` and `maxOccurs` define the number of occurrences an element can have in the XML document.

Example:

.. code-block:: xml

   <xs:element name="book" minOccurs="1" maxOccurs="unbounded"/>

This means the `book` element must appear at least once, but it can appear any number of times.

XSD `<any>`
-----------
The `<xs:any>` element allows for any content to be included within the specified element. It provides flexibility in your XML schema to accept elements from other schemas.

Example:

.. code-block:: xml

   <xs:element name="additionalContent">
     <xs:complexType>
       <xs:sequence>
         <xs:any/>
       </xs:sequence>
     </xs:complexType>
   </xs:element>

XSD `<anyAttribute>`
-------------------
The `<xs:anyAttribute>` element allows any attribute to be present within the specified element.

Example:

.. code-block:: xml

   <xs:element name="book">
     <xs:complexType>
       <xs:attribute name="category" type="xs:string"/>
       <xs:anyAttribute/>
     </xs:complexType>
   </xs:element>

XSD Substitution
----------------
The **substitution** group in XSD allows you to define a set of elements that can be substituted for one another in the XML document.

Example:

.. code-block:: xml

   <xs:element name="book">
     <xs:complexType>
       <xs:sequence>
         <xs:element ref="title"/>
         <xs:element ref="author"/>
       </xs:sequence>
     </xs:complexType>
   </xs:element>

   <xs:element name="bookReplacement" substitutionGroup="book"/>

XSD Example
-----------
Complete example of a book schema:

.. code-block:: xml

   <xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
     <xs:element name="book">
       <xs:complexType>
         <xs:sequence>
           <xs:element name="title" type="xs:string"/>
           <xs:element name="author" type="xs:string"/>
           <xs:element name="price" type="xs:decimal"/>
         </xs:sequence>
       </xs:complexType>
     </xs:element>
   </xs:schema>

This defines a `book` element with `title`, `author`, and `price` sub-elements.

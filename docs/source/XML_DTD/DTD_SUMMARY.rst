XML DTD SUMMARY!
================

DTD Introduction
----------------
A **Document Type Definition (DTD)** defines the structure and rules for an XML document. It specifies the elements, attributes, and entities that can appear in the document, ensuring that XML data adheres to a predefined structure.

DTD is used to validate the structure of an XML document. It can be included within the XML file (internal DTD) or referenced externally (external DTD).

DTD Building Blocks
-------------------
The building blocks of a DTD include:
- **Elements**: Define the structure of XML tags.
- **Attributes**: Define the attributes of XML elements.
- **Entities**: Represent reusable pieces of text or data.
- **Declarations**: Specify the rules for the elements, attributes, and entities.

DTD Elements
------------
An **element** in a DTD defines a tag and its content model. The content model specifies the allowed content within an element.

Example of a DTD declaring elements:

.. code-block:: xml

   <!ELEMENT book (title, author, price)>
   <!ELEMENT title (#PCDATA)>
   <!ELEMENT author (#PCDATA)>
   <!ELEMENT price (#PCDATA)>

This example declares a `book` element that contains `title`, `author`, and `price` as child elements, and each of these child elements holds parsed character data (`#PCDATA`).

DTD Attributes
--------------
An **attribute** in a DTD defines an attribute for an element. It specifies the name and possible values of the attribute.

Example of a DTD declaring an attribute:

.. code-block:: xml

   <!ATTLIST book category CDATA #REQUIRED>

This example declares an attribute `category` for the `book` element. The attribute type is `CDATA` (character data), and the attribute is required.

DTD Elements vs Attr
---------------------
**Elements** and **attributes** serve different purposes in an XML document:
- **Elements**: Represent the main content or structure of an XML document (e.g., `<book>`).
- **Attributes**: Provide additional information about elements (e.g., `<book category="fiction">`).

When deciding whether to use an element or an attribute:
- Use elements for data that may have multiple occurrences or needs to contain complex data.
- Use attributes for data that is simple and unlikely to have multiple values.

DTD Entities
------------
Entities in DTD are used to define reusable pieces of content, like text or other elements. They can be used to represent special characters, external files, or common values within the document.

Example of an entity declaration:

.. code-block:: xml

   <!ENTITY author "J.K. Rowling">

You can then use the `author` entity in your XML document as follows:

.. code-block:: xml

   <book>
     <title>Harry Potter</title>
     <author>&author;</author>
   </book>

DTD Examples
-------------
Here’s an example of an external DTD that validates an XML document describing books:

External DTD file (books.dtd):

.. code-block:: xml

   <!ELEMENT library (book+)>
   <!ELEMENT book (title, author, price)>
   <!ELEMENT title (#PCDATA)>
   <!ELEMENT author (#PCDATA)>
   <!ELEMENT price (#PCDATA)>
   <!ATTLIST book category CDATA #REQUIRED>

XML document using the external DTD:

.. code-block:: xml

   <?xml version="1.0"?>
   <!DOCTYPE library SYSTEM "books.dtd">
   <library>
     <book category="fiction">
       <title>Harry Potter</title>
       <author>J.K. Rowling</author>
       <price>29.99</price>
     </book>
     <book category="science">
       <title>A Brief History of Time</title>
       <author>Stephen Hawking</author>
       <price>15.50</price>
     </book>
   </library>

This XML document refers to the `books.dtd` file to validate the structure of the document.

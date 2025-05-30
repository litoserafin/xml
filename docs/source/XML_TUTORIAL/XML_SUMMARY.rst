XML Tutorial Summary!
=============

XML HOME
--------
Welcome to the XML tutorial! Here you'll find everything you need to understand XML, from basic concepts to advanced technologies like XPath, XSLT, and XQuery.

XML Introduction
----------------
**XML (eXtensible Markup Language)** is a flexible text format designed to store and transport data. It allows users to define their own tags and structure. XML is both human-readable and machine-readable, making it ideal for data exchange.

XML How to Use
---------------
To use XML, simply define your custom tags and structure the data hierarchically. XML data is enclosed within opening and closing tags and can include text, attributes, and other elements.

Basic XML Example:

.. code-block:: xml

   <note>
     <to>Tove</to>
     <from>Jani</from>
     <heading>Reminder</heading>
     <body>Don't forget me this weekend!</body>
   </note>

XML Tree
--------
The **XML tree structure** represents the hierarchical organization of elements in an XML document. It starts with a root element and branches out to child elements, forming a tree-like structure.

Example of an XML Tree structure:

.. code-block:: xml

   <library>
     <book>
       <title>Harry Potter</title>
       <author>J.K. Rowling</author>
     </book>
   </library>

XML Syntax
-----------
XML follows a specific syntax:
- Tags must be closed properly.
- Elements are case-sensitive.
- Attribute values must be enclosed in quotes.
- Special characters like `<`, `>`, and `&` must be escaped.

Example:

.. code-block:: xml

   <book category="fiction">
     <title>Harry Potter</title>
     <author>J.K. Rowling</author>
   </book>

XML Elements
-------------
An **element** is a fundamental part of an XML document, containing a start tag, content, and an end tag.

Example:

.. code-block:: xml

   <title>Harry Potter</title>

XML Attributes
--------------
**Attributes** provide additional information about elements. They are included in the start tag and are defined as name-value pairs.

Example:

.. code-block:: xml

   <book category="fiction">
     <title>Harry Potter</title>
     <author>J.K. Rowling</author>
   </book>

XML Namespaces
---------------
**XML Namespaces** avoid element name conflicts by qualifying element names with a unique identifier. Namespaces are defined using the `xmlns` attribute.

Example:

.. code-block:: xml

   <book xmlns="http://www.example.com/books">
     <title>Harry Potter</title>
   </book>

XML Display
-----------
XML data can be displayed using **XSLT (Extensible Stylesheet Language Transformations)** to transform XML into other formats like HTML.

Example of XSLT for displaying XML as HTML:

.. code-block:: xml

   <xsl:template match="/">
     <html>
       <body>
         <h2>Books</h2>
         <xsl:for-each select="library/book">
           <p><xsl:value-of select="title"/> by <xsl:value-of select="author"/></p>
         </xsl:for-each>
       </body>
     </html>
   </xsl:template>

XML HttpRequest
---------------
**XMLHttpRequest** is a browser-based API that allows web pages to request data from a server asynchronously without reloading the page. It is commonly used in AJAX applications.

Example of using `XMLHttpRequest`:

.. code-block:: html

   <script>
     var xhttp = new XMLHttpRequest();
     xhttp.onreadystatechange = function() {
       if (this.readyState == 4 && this.status == 200) {
         console.log(this.responseText);
       }
     };
     xhttp.open("GET", "data.xml", true);
     xhttp.send();
   </script>

XML Parser
-----------
An **XML Parser** is a tool used to read and validate XML documents. Parsers process the XML structure and extract data based on rules defined in a schema or DTD.

Example:

.. code-block:: text

   var parser = new DOMParser();
   var xmlDoc = parser.parseFromString(xmlString, "application/xml");

XML DOM
--------
**XML DOM (Document Object Model)** represents an XML document as a tree structure, allowing programs to manipulate the document programmatically.

Example of accessing XML DOM elements using JavaScript:

.. code-block:: javascript

   var x = xmlDoc.getElementsByTagName("title")[0].childNodes[0].nodeValue;

XML XPath
----------
**XPath (XML Path Language)** is a query language used to navigate XML documents. It allows you to select nodes based on attributes, text content, or structure.

Example of an XPath query:

.. code-block:: text

   /library/book/title

XML XSLT
---------
**XSLT** is used for transforming XML documents into other formats like HTML, plain text, or other XML structures. It allows you to style and process XML content dynamically.

Example of using XSLT to transform XML:

.. code-block:: xml

   <xsl:template match="/">
     <html>
       <body>
         <h2>Books</h2>
         <xsl:for-each select="library/book">
           <p><xsl:value-of select="title"/> by <xsl:value-of select="author"/></p>
         </xsl:for-each>
       </body>
     </html>
   </xsl:template>

XML XQuery
-----------
**XQuery** is a language used to query and manipulate XML data. It is often used for retrieving data from XML documents and databases.

Example of an XQuery:

.. code-block:: text

   for $book in doc("library.xml")//book
   return $book/title

XML XLink
----------
**XLink** is a standard for creating links in XML documents, enabling the linking of elements in various ways, including simple, extended, and locator links.

Example of using XLink:

.. code-block:: xml

   <link xlink:type="simple" xlink:href="http://www.example.com">Visit Example</link>

XML Validator
-------------
An **XML Validator** checks the correctness and validity of XML documents based on a DTD or XML Schema. It ensures the document adheres to the defined rules and structure.

XML DTD
--------
**XML DTD (Document Type Definition)** defines the legal structure and rules for an XML document. It can be embedded within the document or referenced externally.

Example of a simple DTD:

.. code-block:: xml

   <!ELEMENT book (title, author)>
   <!ELEMENT title (#PCDATA)>
   <!ELEMENT author (#PCDATA)>

XML Schema
-----------
**XML Schema** (XSD) is a more powerful and flexible way of defining the structure and data types for XML documents, providing validation and data-type constraints.

Example of an XML Schema:

.. code-block:: xml

   <xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
     <xs:element name="book" type="xs:string"/>
   </xs:schema>

XML Server
----------
An **XML Server** can be used to handle XML data requests, validate XML documents, and transform XML content. It can serve as an intermediary between the client and the database, making XML-based data available over the web.

Example of using a server-side script to handle XML requests:

.. code-block:: php

   <?php
     $xml = simplexml_load_file("data.xml");
     echo $xml->book[0]->title;
   ?>

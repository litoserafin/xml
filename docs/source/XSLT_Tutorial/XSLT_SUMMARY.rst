XSLT Tutorial
=============

XSLT Introduction
-----------------
XSLT (eXtensible Stylesheet Language Transformations) is used to transform XML documents into other formats like HTML, plain text, or another XML structure. It allows for flexible reformatting, filtering, and rearranging of data stored in XML.

XSL Languages
-------------
- **XSLT**: Used for transforming XML documents.
- **XPath**: Used inside XSLT for navigating XML trees.
- **XSL-FO** (Formatting Objects): Used for formatting documents for output (e.g., PDFs).

XSLT Transform
--------------
An XSLT stylesheet defines a set of rules (templates) to transform XML. You apply an XSLT transformation to an XML source to generate output (HTML, another XML, etc.).

Basic structure:

.. code-block:: xml

   <xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform">
     <xsl:template match="/">
       <html><body><h2>My Library</h2></body></html>
     </xsl:template>
   </xsl:stylesheet>

XSLT `<template>`
------------------
The `<xsl:template>` defines rules to apply to matching XML nodes. 
Templates use a `match` attribute to specify which part of the XML to transform.

Example:

.. code-block:: xml

   <xsl:template match="/library/book">
     <p><xsl:value-of select="title"/></p>
   </xsl:template>

XSLT `<value-of>`
------------------
The `<xsl:value-of>` element extracts and outputs the value of a selected node.

Example:

.. code-block:: xml

   <xsl:value-of select="author"/>

This outputs the value of the `<author>` element.

XSLT `<for-each>`
------------------
The `<xsl:for-each>` element loops over a set of nodes.

Example:

.. code-block:: xml

   <xsl:for-each select="library/book">
     <p><xsl:value-of select="title"/></p>
   </xsl:for-each>

XSLT `<sort>`
--------------
The `<xsl:sort>` element sorts the nodes selected inside `<xsl:for-each>` or `<xsl:apply-templates>`.

Example:

.. code-block:: xml

   <xsl:for-each select="library/book">
     <xsl:sort select="title"/>
     <p><xsl:value-of select="title"/></p>
   </xsl:for-each>

XSLT `<if>`
------------
The `<xsl:if>` element defines a conditional test.

Example:

.. code-block:: xml

   <xsl:if test="price > 20">
     <p>Expensive Book</p>
   </xsl:if>

XSLT `<choose>`
----------------
The `<xsl:choose>` element is like a switch-case statement. It contains `<xsl:when>` and `<xsl:otherwise>`.

Example:

.. code-block:: xml

   <xsl:choose>
     <xsl:when test="price > 20">
       <p>Expensive</p>
     </xsl:when>
     <xsl:otherwise>
       <p>Affordable</p>
     </xsl:otherwise>
   </xsl:choose>

XSLT Apply
-----------
The `<xsl:apply-templates>` element applies templates to selected nodes. It is used for recursive and flexible processing.

Example:

.. code-block:: xml

   <xsl:apply-templates select="library/book"/>

XSLT on the Client
-------------------
XSLT transformations can be applied directly in the browser (e.g., Chrome, Firefox) using an XML document linked to an XSL stylesheet.

Example XML linking to XSL:

.. code-block:: xml

   <?xml-stylesheet type="text/xsl" href="library.xsl"?>

XSLT on the Server
-------------------
Server-side XSLT transformations are done using languages like PHP, Java, .NET, or Node.js. 
The server processes the XML and XSLT, then sends the transformed result (e.g., HTML) to the client.

Example (PHP):

.. code-block:: php

   $xml = new DOMDocument;
   $xml->load('library.xml');

   $xsl = new DOMDocument;
   $xsl->load('library.xsl');

   $proc = new XSLTProcessor;
   $proc->importStyleSheet($xsl);
   echo $proc->transformToXML($xml);

XSLT Edit XML
-------------
XSLT can also modify the structure of XML during transformation:
- Adding or removing elements
- Changing attribute values
- Reorganizing content

Example (adding an attribute):

.. code-block:: xml

   <xsl:template match="book">
     <book status="new">
       <xsl:apply-templates/>
     </book>
   </xsl:template>

XSLT Examples
-------------
Full Example:

Input XML:

.. code-block:: xml

   <library>
     <book>
       <title>Harry Potter</title>
       <author>J.K. Rowling</author>
     </book>
   </library>

XSLT:

.. code-block:: xml

   <xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform">
     <xsl:template match="/">
       <html>
         <body>
           <h2>Library Books</h2>
           <xsl:for-each select="library/book">
             <p><xsl:value-of select="title"/> by <xsl:value-of select="author"/></p>
           </xsl:for-each>
         </body>
       </html>
     </xsl:template>
   </xsl:stylesheet>

Result:

.. code-block:: html

   <html>
     <body>
       <h2>Library Books</h2>
       <p>Harry Potter by J.K. Rowling</p>
     </body>
   </html>

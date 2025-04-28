XPath SUMMARY!
==============

XPath Introduction
-------------------
XPath (XML Path Language) is a query language for selecting nodes from an XML document. It provides a way to navigate through elements and attributes in XML documents efficiently. XPath is widely used in technologies like XSLT, XQuery, and DOM parsing.

XPath Nodes
-----------
In XPath, the XML document is treated as a tree of nodes:
- **Element nodes** (e.g., `<book>`)
- **Attribute nodes** (e.g., `category="fiction"`)
- **Text nodes** (text content inside elements)
- **Namespace nodes**
- **Processing instruction nodes**
- **Comment nodes**
- **Root node** (entire document)

Example XML:

.. code-block:: xml

   <library>
     <book category="fiction">
       <title>Harry Potter</title>
     </book>
   </library>

XPath Syntax
------------
XPath expressions are used to select nodes or node sets.

Common syntax:
- `/` selects from the root node
- `//` selects nodes anywhere in the document
- `@` selects attributes
- `[]` applies conditions

Example XPath expressions:

.. code-block:: text

   /library/book/title          -> Selects the title of the book
   //title                       -> Selects all title elements
   /library/book[@category='fiction'] -> Selects books with category "fiction"
   //@category                   -> Selects all category attributes

XPath Axes
----------
Axes define the node relationships:
- `child::` selects all children
- `parent::` selects the parent
- `ancestor::` selects all ancestors
- `descendant::` selects all descendants
- `following-sibling::` selects siblings after the current node
- `preceding-sibling::` selects siblings before the current node
- `attribute::` selects attributes

Example:

.. code-block:: text

   child::book          -> Selects all child book elements
   descendant::title    -> Selects all title descendants

XPath Operators
---------------
Operators in XPath allow complex queries:
- `|` (Union) — combine results
- `+`, `-`, `*`, `div`, `mod` — arithmetic
- `=`, `!=`, `<`, `>`, `<=`, `>=` — comparison
- `and`, `or` — logical operations

Example:

.. code-block:: text

   /library/book[price > 30]     -> Select books with price greater than 30
   //title | //author            -> Select all title and author elements

XPath Examples
--------------
Here are some full XPath examples based on the XML below:

.. code-block:: xml

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

Examples:

.. code-block:: text

   /library/book/title
   -> Selects all title elements of books.

   /library/book[@category='science']/title
   -> Selects the title of the science category book.

   //price[text() > 20]
   -> Selects price elements with values greater than 20.

   /library/book[author='J.K. Rowling']/title
   -> Selects the title of the book written by J.K. Rowling.

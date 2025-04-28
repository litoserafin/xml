XQuery SUMMARY!
===============

XQuery Introduction
-------------------
XQuery (XML Query Language) is a powerful language for querying and manipulating XML data. It is designed to query, transform, and manipulate XML documents, and is used widely in databases, web services, and data integration.

XQuery Example
--------------
A simple XQuery expression can be used to retrieve data from an XML document.

Example XML:

.. code-block:: xml

   <library>
     <book>
       <title>Harry Potter</title>
       <author>J.K. Rowling</author>
       <price>29.99</price>
     </book>
     <book>
       <title>A Brief History of Time</title>
       <author>Stephen Hawking</author>
       <price>15.50</price>
     </book>
   </library>

Example XQuery to select all titles:

.. code-block:: text

   for $book in doc("library.xml")//book
   return $book/title

This query retrieves the `<title>` element for each `<book>` in the document.

XQuery FLWOR
------------
FLWOR (For, Let, Where, Order by, Return) is the core expression in XQuery, used for selecting, filtering, and transforming data.

Example of FLWOR expression:

.. code-block:: text

   for $book in doc("library.xml")//book
   where $book/price > 20
   order by $book/title
   return <result>
            <title>{ $book/title }</title>
            <author>{ $book/author }</author>
          </result>

This selects books with a price greater than 20 and sorts them by title.

XQuery HTML
-----------
XQuery can also be used to generate HTML content from XML data, making it useful for web applications.

Example XQuery to generate HTML:

.. code-block:: text

   for $book in doc("library.xml")//book
   return <html>
             <body>
               <h1>{ $book/title }</h1>
               <p>Author: { $book/author }</p>
               <p>Price: { $book/price }</p>
             </body>
           </html>

This will generate an HTML page for each book.

XQuery Terms
------------
- **For**: Iterates over a set of nodes.
- **Let**: Binds a variable to a value.
- **Where**: Filters the data based on a condition.
- **Order by**: Sorts the results.
- **Return**: Specifies the output.

XQuery Syntax
-------------
XQuery syntax is similar to XPath, but with the added power of variables and operations like `for`, `let`, `where`, `order by`, and `return`.

Basic structure of an XQuery:

.. code-block:: text

   for $variable in $sequence
   return $expression

Where `$sequence` is a set of XML nodes and `$expression` is what will be returned for each node.

XQuery Add
----------
XQuery allows you to add new elements or nodes to the XML document.

Example XQuery to add a new book element:

.. code-block:: text

   let $newBook := <book>
                     <title>New Book</title>
                     <author>Author Name</author>
                     <price>25.00</price>
                   </book>
   return doc("library.xml")/*,$newBook

This will add the new `<book>` element to the XML document.

XQuery Select
-------------
The `select` clause in XQuery is used to retrieve specific parts of an XML document.

Example XQuery to select books with a price greater than 20:

.. code-block:: text

   for $book in doc("library.xml")//book
   where $book/price > 20
   return $book

XQuery Functions
----------------
XQuery supports various built-in functions like:
- `count()`: Counts the number of nodes.
- `concat()`: Concatenates strings.
- `string-length()`: Returns the length of a string.

Example to count the number of books:

.. code-block:: text

   let $bookCount := count(doc("library.xml")//book)
   return <result>Number of books: {$bookCount}</result>

This counts the number of `<book>` elements in the XML document and returns it.


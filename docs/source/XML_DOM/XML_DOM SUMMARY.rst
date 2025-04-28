XML DOM SUMMARY!
=================

DOM Introduction
-----------------
The XML DOM (Document Object Model) represents an XML document as a structured tree. Each element, attribute, and piece of text is a node. DOM provides a way to dynamically access and modify the content and structure of XML documents using programming languages like JavaScript, Java, and Python.

DOM Nodes
---------
In the DOM tree, every part of an XML document is a node:
- Document node
- Element node
- Attribute node
- Text node
- Comment node
Each type of node has properties and methods specific to its role.

DOM Accessing
-------------
Nodes are accessed through methods like:
- `getElementsByTagName()`
- `getElementById()`
- `getElementsByClassName()`
Accessing nodes is essential for reading and modifying XML documents.

Example:

.. code-block:: xml

   <library>
     <book id="b1">
       <title>Harry Potter</title>
     </book>
   </library>

Access title element:

.. code-block:: html

   <script>
   const title = xmlDoc.getElementsByTagName("title")[0];
   console.log(title.childNodes[0].nodeValue);  // Harry Potter
   </script>

DOM Node Info
-------------
Each node provides information through properties:
- `nodeName`: the name of the node
- `nodeValue`: the value of the node (if text/attribute)
- `nodeType`: the type (1 for Element, 2 for Attribute, 3 for Text)

Example:

.. code-block:: html

   <script>
   console.log(title.nodeName); // title
   console.log(title.nodeType); // 1 (Element Node)
   </script>

DOM Node List
-------------
A NodeList is a collection of nodes, usually returned by methods like `getElementsByTagName()`. It behaves like an array but not exactly — it can be live (auto-updating) or static.

Example:

.. code-block:: html

   <script>
   const books = xmlDoc.getElementsByTagName("book");
   for (let i = 0; i < books.length; i++) {
     console.log(books[i].getAttribute("id"));
   }
   </script>

DOM Traversing
--------------
Traversing refers to moving across the DOM tree:
- `parentNode`
- `childNodes`
- `firstChild`
- `lastChild`
- `nextSibling`
- `previousSibling`

Example:

.. code-block:: html

   <script>
   const book = xmlDoc.getElementsByTagName("book")[0];
   const title = book.firstChild;
   console.log(title.nodeName); // title
   </script>

DOM Navigating
--------------
DOM navigation properties allow movement between related nodes:
- Move to parent, child, or sibling nodes.
- Useful for dynamically working with any XML structure.

Example:

.. code-block:: html

   <script>
   const library = xmlDoc.documentElement;
   const firstBook = library.firstChild;
   const nextBook = firstBook.nextSibling;
   </script>

DOM Get Values
--------------
Retrieving values is a frequent operation:
- Element text: via `nodeValue`
- Attribute values: via `getAttribute()`

Example:

.. code-block:: html

   <script>
   const category = book.getAttribute("category");
   const titleText = title.childNodes[0].nodeValue;
   </script>

DOM Change Nodes
----------------
You can change node values:
- Update text content
- Update attributes

Example:

.. code-block:: html

   <script>
   title.childNodes[0].nodeValue = "Harry Potter and the Goblet of Fire";
   book.setAttribute("category", "fantasy");
   </script>

DOM Remove Nodes
----------------
Nodes can be removed using `removeChild()`.

Example:

.. code-block:: html

   <script>
   library.removeChild(book);
   </script>

DOM Replace Nodes
-----------------
Nodes can be replaced using `replaceChild(newNode, oldNode)`.

Example:

.. code-block:: html

   <script>
   const newBook = xmlDoc.createElement("book");
   library.replaceChild(newBook, book);
   </script>

DOM Create Nodes
----------------
New nodes are created using:
- `createElement()`
- `createTextNode()`

Example:

.. code-block:: html

   <script>
   const newTitle = xmlDoc.createElement("title");
   const text = xmlDoc.createTextNode("New Book Title");
   newTitle.appendChild(text);
   </script>

DOM Add Nodes
-------------
Adding new nodes involves creating a node and appending it to an existing parent.

Example:

.. code-block:: html

   <script>
   book.appendChild(newTitle);
   </script>

DOM Clone Nodes
---------------
Nodes can be duplicated using `cloneNode(true/false)`:
- `true` means deep clone (with all children)
- `false` means shallow clone (without children)

Example:

.. code-block:: html

   <script>
   const cloneBook = book.cloneNode(true);
   library.appendChild(cloneBook);
   </script>

DOM Examples
------------
Examples combine everything:
- Load an XML document
- Access and modify elements
- Create new nodes dynamically

Full Example:

.. code-block:: html

   <script>
   const parser = new DOMParser();
   const xmlString = `
   <library>
     <book category="fiction">
       <title>Harry Potter</title>
     </book>
   </library>`;
   const xmlDoc = parser.parseFromString(xmlString, "application/xml");
   const book = xmlDoc.getElementsByTagName("book")[0];
   const title = book.getElementsByTagName("title")[0];
   title.childNodes[0].nodeValue = "Harry Potter and the Chamber of Secrets";
   console.log(title.childNodes[0].nodeValue);
   </script>

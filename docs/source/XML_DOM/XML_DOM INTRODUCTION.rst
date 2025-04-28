XML DOM Tutorial
==================

What is XML DOM?
-------------------
- XML = eXtensible Markup Language (stores/transports data)
- DOM = Document Object Model (tree structure where everything is an object)
- The XML DOM allows programs to dynamically read, modify, delete, or add data.

XML DOM Tree Structure:
------------------
Example XML:

<library>
  <book category="fiction">
    <title>Harry Potter</title>
    <author>J.K. Rowling</author>
  </book>
</library>

Tree:
Document
└── library
    └── book (category="fiction")
        ├── title ("Harry Potter")
        └── author ("J.K. Rowling")

Common DOM Methods:
---------------------
- getElementsByTagName(): returns elements by tag name
- getElementById(): returns element by ID
- getAttribute(): gets an attribute's value
- setAttribute(): sets an attribute's value
- appendChild(): adds a child node
- removeChild(): removes a child node
- createElement(): creates a new element
- createTextNode(): creates a text node

Sample Access (JavaScript):
-----------------
<script>
const parser = new DOMParser();
const xmlString = `
<library>
  <book category="fiction">
    <title>Harry Potter</title>
    <author>J.K. Rowling</author>
  </book>
</library>`;
const xmlDoc = parser.parseFromString(xmlString, "application/xml");
const title = xmlDoc.getElementsByTagName("title")[0].childNodes[0].nodeValue;
console.log(title);  // Output: Harry Potter
</script>

Why Learn XML DOM?
-----------------
- Easy XML file manipulation
- Important for web services, SOAP APIs, configuration files
- Supported in Java, Python, JavaScript, C#, etc.

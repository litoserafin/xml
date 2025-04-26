 # XML DOM (Document Object Model)

---

## Introduction
The **DOM (Document Object Model)** is a platform- and language-independent interface that represents XML or HTML documents as a structured tree of nodes. It allows developers to programmatically access and manipulate a document’s structure, style, and content.

---

## Key Concepts

- **Document Tree**: Represents the entire XML/HTML document as a tree structure.
- **Nodes**:
  - **Document Node**: The root of the tree.
  - **Element Nodes**: Represent tags like `<book>` or `<title>`.
  - **Text Nodes**: Contain the text inside elements.
  - **Attribute Nodes**: Represent attributes of elements.
  - **Comment Nodes**: Represent comments in the XML/HTML.

---

## DOM Hierarchy


---

 What Can You Do with DOM?

- Traverse the XML tree.
- Read and modify element values.
- Add or delete nodes dynamically.
- Search elements by tag name or attributes.
- Use with languages like JavaScript, Python, Java, etc.

---

 Example (JavaScript)

```javascript
// Parse XML string
const parser = new DOMParser();
const xmlDoc = parser.parseFromString(xmlString, "application/xml");

// Access an element
const title = xmlDoc.getElementsByTagName("title")[0];

// Modify the text content
title.textContent = "Updated Title";

 Why DOM?
--------------

Enables dynamic document manipulation

Works with any programming language

Makes structured data easier to navigate and modify

📌 DOM is essential when working with XML data in web applications or enterprise systems!




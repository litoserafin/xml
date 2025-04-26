XML RDF (Resource Description Framework)
=========================================

**RDF** (Resource Description Framework) is a standard model for **data interchange on the web**.  
It allows structured and semi-structured data to be mixed, shared, and reused across different applications.

RDF is **XML-based** when serialized using RDF/XML syntax — meaning it follows XML rules to describe relationships between resources.

---

 What is RDF?
----------------

- 🔗 **Describes Resources**: RDF describes resources (like a book, person, or website) using **triples** (subject, predicate, object).
- 📖 **Triple Structure**:
  - **Subject**: The resource being described.
  - **Predicate**: The property or characteristic of the resource.
  - **Object**: The value of the property.
- 🌐 **Web-Friendly**: Designed for linking data across the web (Semantic Web).

---

 Basic Structure of RDF/XML
-----------------------------

An RDF/XML document typically looks like this:

```xml
<?xml version="1.0"?>
<rdf:RDF xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
         xmlns:ex="http://example.com/">

  <rdf:Description rdf:about="http://example.com/book1">
    <ex:title>Learning XML</ex:title>
    <ex:author>John Doe</ex:author>
    <ex:published>2024-05-01</ex:published>
  </rdf:Description>

</rdf:RDF>

The root element is <rdf:RDF>.

Namespaces are used (xmlns:rdf and xmlns:ex) to identify vocabularies.

Each resource is described with a <rdf:Description> element.

Explained with Example:
  ------------------
Subject: http://example.com/book1 (the book resource)

Predicate: ex:title, ex:author, ex:published (properties)

Object: "Learning XML", "John Doe", "2024-05-01" (property values)

Why Use RDF?
--------------
✅ Data Integration: Connects information from different sources.
✅ Machine-Readable: Easy for programs to understand and process.
✅ Extensible: New properties can be added without breaking the model.
✅ Semantic Web Foundation: Core technology behind the semantic web (Web 3.0).



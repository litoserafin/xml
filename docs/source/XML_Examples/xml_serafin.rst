XML EXAMPLE 
================
.. code-block:: xml

<?xml version="1.0" encoding="UTF-8"?>
<bookstore>
    <book category="fiction">
        <title lang="en">The Alchemist</title>
        <author>Paulo Coelho</author>
        <year>1988</year>
        <price>9.99</price>
    </book>
    <book category="science">
        <title lang="en">A Brief History of Time</title>
        <author>Stephen Hawking</author>
        <year>1988</year>
        <price>15.50</price>
    </book>
</bookstore>

What's going on here:
------------------------
<bookstore> is the root element.

Each <book> has child elements: <title>, <author>, <year>, and <price>.

Attributes are used in <book> (category="fiction") and <title> (lang="en").

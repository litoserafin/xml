XSD String Data Types
======================

1. **string**  
   - **Definition**: A sequence of characters. The most general string type.
   - **Example**: <name>John Doe</name>
   - **Usage**: Used for general textual data without restrictions.

2. **normalizedString**  
   - **Definition**: Similar to `string`, but whitespace is normalized (leading/trailing spaces removed, multiple spaces collapsed).
   - **Example**: <description>  This is a   description   text.  </description> 
   - **Result**: "This is a description text."
   - **Usage**: Ideal for text that should not have excessive spaces.

3. **token**  
   - **Definition**: A more restrictive form of `normalizedString` where multiple spaces are collapsed, and leading/trailing spaces are removed.
   - **Example**: <category>Sports  Cars  Motorcycles</category> 
   - **Result**: "Sports Cars Motorcycles"
   - **Usage**: Best for clean, single-space formatted strings like tags.

4. **language**  
   - **Definition**: Represents an ISO 639-1 language code (e.g., "en" for English).
   - **Example**: <language>en</language>
   - **Usage**: Used for specifying languages in multilingual systems.

5. **Name**  
   - **Definition**: A string that must follow XML Name rules. It must start with a letter or underscore and can contain letters, digits, hyphens, and periods.
   - **Example**: <elementName>item123</elementName>
   - **Usage**: Used for naming elements and attributes in XML.

6. **NCName**  
   - **Definition**: Similar to `Name` but without colons (`:`). Cannot contain namespace prefixes.
   - **Example**: <attributeName>itemId</attributeName>
   - **Usage**: Used for local names without namespaces.

7. **ID**  
   - **Definition**: A unique identifier within the XML document. Follows the `Name` rules.
   - **Example**: <product id="p123">Product Description</product>
   - **Usage**: Used for unique IDs in the document.

8. **IDREF**  
   - **Definition**: A reference to an `ID` within the document.
   - **Example**: <item ref="p123">Item Description</item>
   - **Usage**: Used to refer to elements identified by `ID`.

9. **ENTITY**  
   - **Definition**: A reference to an entity within the XML document. Can represent special characters or external resources.
   - **Example**: <symbol>&#x1F601;</symbol>
   - **Usage**: For embedding reusable content or external data.

Why Use XSD String Data Types?
--------------------------------
- **Data Validation**: Ensures adherence to text formatting rules.
- **Consistency**: Ensures clean and predictable data.
- **Interoperability**: Facilitates smooth sharing of XML data across platforms.

Tip: Use specific XSD string types to ensure better data quality, consistency, and cleaner XML data!

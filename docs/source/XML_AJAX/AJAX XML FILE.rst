AJAX XML Example Summary
============
  
What It Does
------------
AJAX can be used to interact with an XML file dynamically without reloading the page.
In this example, a webpage fetches CD information from an XML file and displays it in a table.

Process Overview
User Action: Click the "Get CD Info" button.

AJAX Request:

loadDoc() function creates an XMLHttpRequest object.

It prepares a GET request for the cd_catalog.xml file.

Sends the request asynchronously.

Server Response:

Once the response is ready (readyState == 4 and status == 200), it triggers myFunction().

Data Processing:

Parses the XML.

Extracts <TITLE> and <ARTIST> nodes from each <CD>.

Builds an HTML table dynamically.

Update the Webpage:

Displays the table inside an HTML element (like <div id="demo">).

JavaScript Code Example
----------------
javascript
Copy
Edit
function loadDoc() {
  var xhttp = new XMLHttpRequest();
  xhttp.onreadystatechange = function() {
    if (this.readyState == 4 && this.status == 200) {
      myFunction(this);
    }
  };
  xhttp.open("GET", "cd_catalog.xml", true);
  xhttp.send();
}

function myFunction(xml) {
  var i;
  var xmlDoc = xml.responseXML;
  var table = "<tr><th>Title</th><th>Artist</th></tr>";
  var x = xmlDoc.getElementsByTagName("CD");
  for (i = 0; i < x.length; i++) {
    table += "<tr><td>" +
      x[i].getElementsByTagName("TITLE")[0].childNodes[0].nodeValue +
      "</td><td>" +
      x[i].getElementsByTagName("ARTIST")[0].childNodes[0].nodeValue +
      "</td></tr>";
  }
  document.getElementById("demo").innerHTML = table;
}

XML File ("cd_catalog.xml")
----------------
Example
xml
Copy
Edit
<CATALOG>
  <CD>
    <TITLE>Empire Burlesque</TITLE>
    <ARTIST>Bob Dylan</ARTIST>
  </CD>
  <CD>
    <TITLE>Hide Your Heart</TITLE>
    <ARTIST>Bonnie Tyler</ARTIST>
  </CD>
  <!-- More CD entries -->
</CATALOG>

Key Points
--------------
AJAX enables real-time communication with an XML file.

XML data can be parsed and used to build dynamic HTML content.

Useful for catalogs, menus, product listings, etc.

✅ Conclusion:
AJAX + XML = Dynamic data-driven websites without refreshing the page!

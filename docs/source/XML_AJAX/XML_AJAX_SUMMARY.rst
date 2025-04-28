XML AJAX SUMMARY.rst
=================

AJAX Introduction
-----------------
**AJAX (Asynchronous JavaScript and XML)** is a technique used to create dynamic and interactive web applications. It allows web pages to update asynchronously by exchanging small amounts of data with the server behind the scenes. This makes web pages more responsive without requiring a full page reload.

AJAX XMLHttp
-------------
**XMLHttpRequest** is the key component of AJAX. It is an API used by JavaScript to send and receive HTTP requests asynchronously. It allows web pages to load data in the background without interfering with the current page.

Basic example of creating an XMLHttpRequest object:

.. code-block:: javascript

   var xhttp = new XMLHttpRequest();

AJAX Request
------------
An **AJAX request** is initiated by calling the `open()` and `send()` methods on the `XMLHttpRequest` object. These methods allow you to send a request to the server and process the response.

Example of making an AJAX request:

.. code-block:: javascript

   var xhttp = new XMLHttpRequest();
   xhttp.onreadystatechange = function() {
     if (this.readyState == 4 && this.status == 200) {
       console.log(this.responseText);
     }
   };
   xhttp.open("GET", "data.xml", true);
   xhttp.send();

AJAX Response
-------------
When the server responds to an AJAX request, the data is typically returned as a plain text, JSON, or XML. The response can be accessed through the `responseText` or `responseXML` properties of the `XMLHttpRequest` object.

Example of handling the AJAX response:

.. code-block:: javascript

   var response = xhttp.responseText;
   console.log(response);

AJAX XML File
-------------
AJAX can be used to load and display **XML data** from a file. Once the XML file is retrieved, you can parse and manipulate its content using JavaScript.

Example of using AJAX to load an XML file:

.. code-block:: javascript

   var xhttp = new XMLHttpRequest();
   xhttp.onreadystatechange = function() {
     if (this.readyState == 4 && this.status == 200) {
       var xmlDoc = this.responseXML;
       var title = xmlDoc.getElementsByTagName("title")[0].childNodes[0].nodeValue;
       console.log(title);
     }
   };
   xhttp.open("GET", "books.xml", true);
   xhttp.send();

AJAX PHP
--------
AJAX can be integrated with **PHP** to dynamically update content on the server. PHP can process the request and return the response in formats such as JSON or XML.

Example of using AJAX with PHP:

.. code-block:: javascript

   var xhttp = new XMLHttpRequest();
   xhttp.onreadystatechange = function() {
     if (this.readyState == 4 && this.status == 200) {
       document.getElementById("content").innerHTML = this.responseText;
     }
   };
   xhttp.open("GET", "server.php", true);
   xhttp.send();

PHP script (`server.php`):

.. code-block:: php

   <?php
     echo "Hello, world!";
   ?>

AJAX ASP
--------
In **ASP (Active Server Pages)**, AJAX can be used to send requests to a server-side ASP script. The server processes the request and returns a response.

Example of using AJAX with ASP:

.. code-block:: javascript

   var xhttp = new XMLHttpRequest();
   xhttp.onreadystatechange = function() {
     if (this.readyState == 4 && this.status == 200) {
       document.getElementById("content").innerHTML = this.responseText;
     }
   };
   xhttp.open("GET", "server.asp", true);
   xhttp.send();

ASP script (`server.asp`):

.. code-block:: asp

   <% Response.Write("Hello from ASP!"); %>

AJAX Database
-------------
**AJAX and databases** can be integrated by sending a request to the server to fetch or manipulate data stored in a database, and then returning the result to the client.

Example of using AJAX with a MySQL database (via PHP):

.. code-block:: javascript

   var xhttp = new XMLHttpRequest();
   xhttp.onreadystatechange = function() {
     if (this.readyState == 4 && this.status == 200) {
       document.getElementById("content").innerHTML = this.responseText;
     }
   };
   xhttp.open("GET", "fetch_data.php", true);
   xhttp.send();

PHP script (`fetch_data.php`):

.. code-block:: php

   <?php
     $conn = new mysqli("localhost", "username", "password", "database");
     $result = $conn->query("SELECT name FROM users");
     while($row = $result->fetch_assoc()) {
       echo $row["name"] . "<br>";
     }
   ?>

AJAX Applications
-----------------
AJAX is widely used in creating **dynamic web applications** such as:
- Real-time updates on social media platforms
- Autocomplete search boxes
- Form validation without page refresh
- Chat applications

Example of AJAX in a **real-time search application**:

.. code-block:: javascript

   var xhttp = new XMLHttpRequest();
   xhttp.onreadystatechange = function() {
     if (this.readyState == 4 && this.status == 200) {
       document.getElementById("searchResults").innerHTML = this.responseText;
     }
   };
   xhttp.open("GET", "search.php?query=" + query, true);
   xhttp.send();

AJAX Examples
-------------
Here are a few practical examples of AJAX:

1. **Simple content update**:

.. code-block:: javascript

   var xhttp = new XMLHttpRequest();
   xhttp.onreadystatechange = function() {
     if (this.readyState == 4 && this.status == 200) {
       document.getElementById("result").innerHTML = this.responseText;
     }
   };
   xhttp.open("GET", "data.txt", true);
   xhttp.send();

2. **Loading data from an XML file**:

.. code-block:: javascript

   var xhttp = new XMLHttpRequest();
   xhttp.onreadystatechange = function() {
     if (this.readyState == 4 && this.status == 200) {
       var xmlDoc = this.responseXML;
       var books = xmlDoc.getElementsByTagName("book");
       var content = "";
       for (var i = 0; i < books.length; i++) {
         content += books[i].getElementsByTagName("title")[0].childNodes[0].nodeValue + "<br>";
       }
       document.getElementById("bookList").innerHTML = content;
     }
   };
   xhttp.open("GET", "books.xml", true);
   xhttp.send();

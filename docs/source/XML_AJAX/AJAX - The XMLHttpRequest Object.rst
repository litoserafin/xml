The XMLHttpRequest Object
============
All modern browsers support the XMLHttpRequest object.
-----------------

The XMLHttpRequest object can be used to exchange data with a server behind the scenes. This means that it is possible to update parts of a web page, without reloading the whole page.

 What is the XMLHttpRequest Object?
-----------------------------
The core of AJAX.

Built-in to all modern browsers (Chrome, Firefox, Edge, Safari, Opera).

Allows sending/receiving data behind the scenes without reloading the whole web page.

Supports asynchronous communication with servers.

 How to Create an XMLHttpRequest Object
-----------------------
var xhttp = new XMLHttpRequest();

XMLHttpRequest Methods (Summary)
----------------------
Method | Description
new XMLHttpRequest() | Creates a new request object
abort() | Cancels the current request
getAllResponseHeaders() | Returns all response headers
getResponseHeader(header) | Returns a specific header
open(method, url, async, user, psw) | Configures the request
send() | Sends the request (GET)
send(string) | Sends the request with data (POST)
setRequestHeader(header, value) | Sets HTTP headers

XMLHttpRequest Properties (Summary)
-----------------------
Property | Description
onreadystatechange | Event handler triggered when readyState changes
readyState | Current state of the request:
 | - 0: Request not initialized
 | - 1: Server connection established
 | - 2: Request received
 | - 3: Processing request
 | - 4: Request finished and response ready
responseText | Response data as a string
responseXML | Response data as XML
status | HTTP status code (e.g., 200, 403, 404)
statusText | Status message text (e.g., "OK", "Not Found")

 Common HTTP Status Codes
--------------------
Code | Meaning
200 | OK (Success)
403 | Forbidden
404 | Not Found

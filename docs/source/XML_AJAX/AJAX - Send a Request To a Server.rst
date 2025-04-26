AJAX - Send a Request to a Server
===============
  
 How AJAX Sends a Request
------------
The XMLHttpRequest object is used to exchange data with a server.

Two key methods are used:

open(method, url, async): Prepares the request.

send(): Sends the request to the server.

 Method Details
--------------

Method	Description
open(method, url, async)	Sets the request type (GET or POST), target URL, and async mode
send()	Sends the request (used for GET)
send(string)	Sends the request with data (used for POST)
method: "GET" or "POST"

url: File or server location

async: true (asynchronous) or false (synchronous)

 GET or POST?
--------------
Use GET when:

Simpler and faster communication is needed.

The request does not modify data on the server.

Use POST when:

You are updating server resources (e.g., database).

Sending large amounts of data (no size limit).

Handling sensitive or unknown user input (POST is safer).

 Simple GET Request Example
-----------------
javascript
Copy
Edit
xhttp.open("GET", "demo_get.asp", true);
xhttp.send();
This may return a cached result.

Avoid Caching in GET Requests
---------------
Add a random query string to the URL:

javascript
Copy
Edit
xhttp.open("GET", "demo_get.asp?t=" + Math.random(), true);
xhttp.send();
Forces the server to return a fresh response.

 Sending Data with GET
---------------
Attach the data as URL parameters:

javascript
Copy
Edit
xhttp.open("GET", "demo_get2.asp?fname=Henry&lname=Ford", true);
xhttp.send();
Data is visible in the URL (not recommended for sensitive information).

Tip:
For sensitive or large data, always prefer using POST instead of GET!

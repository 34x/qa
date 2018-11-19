# HTTP

## Overview

> The **Hypertext Transfer Protocol** (HTTP) is an application protocol for distributed, collaborative, hypermedia information systems.[1] HTTP is the foundation of data communication for the World Wide Web, where hypertext documents include hyperlinks to other resources that the user can easily access, for example by a mouse click or by tapping the screen. HTTP was developed to facilitate hypertext and the World Wide Web.
>
> [Wikipedia](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol)
>
> In non technical words **http** is the way to get and to send information
>
> The **Hypertext** is text displayed on a computer display or other electronic devices with references (hyperlinks) to other text that the reader can immediately access.[1] Hypertext documents are interconnected by hyperlinks, which are typically activated by a mouse click, keypress set or by touching the screen. Apart from text, the term "hypertext" is also sometimes used to describe tables, images, and other presentational content formats with integrated hyperlinks.
>
> [Wikipedia](https://en.wikipedia.org/wiki/Hypertext)
>
> In non technical words **Hypertext** is the system of web-pages with hyperlinks
>
> [How it works](https://en.wikipedia.org/wiki/Hypertext#/media/File:Sistema_hipertextual.jpg)
>
## Request
>
> The **http request** is a way to apply to web resourse
>
> The **http request** defines methods to indicate the desired action to be performed on the identified resource.
>
> **The two most common HTTP methods are: GET and POST**
>
> [Wikipedia](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol#Request_methods)
>
> The **GET** method requests a representation of the specified resource. Requests using GET should only retrieve data and should have no other effect
>
> In non technical words **GET request** sends all information as a part of URL, so it can be seen (and stolen sometimes), when you ask server to show some particular page; when you click on a link
>
> ex. http://www.komtet.ru/script.php?login=admin&name=komtet
>
> The **POST** method requests that the server accept the entity enclosed in the request as a new subordinate of the web resource identified by the URI. The data POSTed might be, for example, an annotation for existing resources; a message for a bulletin board, newsgroup, mailing list, or comment thread; a block of data that is the result of submitting a web form to a data-handling process; or an item to add to a database.
>
> In non technical words **POST request** the web site client can't see the data, when you sent some data to server
>
> ex. http://www.komtet.ru/script.php
>
## Response
>
> **The response message consists of the following:**
>
> **a status line** which includes the status code and reason message (e.g., HTTP/1.1 200 OK, which indicates that the client's request succeeded.)
>
> **response header fields** (e.g., Content-Type: text/html)
>
> **an empty line**
>
> **an optional message body**
>
> [Wikipedia](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol#Response_message)
>

```
A Status-line

Zero or more header (General|Response|Entity) fields followed by CRLF

An empty line (i.e., a line with nothing preceding the CRLF) 
indicating the end of the header fields

Optionally a message-body
```

```
HTTP/1.1 200 OK
Date: Mon, 27 Jul 2009 12:28:53 GMT
Server: Apache/2.2.14 (Win32)
Last-Modified: Wed, 22 Jul 2009 19:15:56 GMT
Content-Length: 88
Content-Type: text/html
Connection: Closed
```




## Cookies
>
> The **http cookie** (also called web cookie, Internet cookie, browser cookie, or simply cookie) is a small piece of data sent from a website and stored on the user's computer by the user's web browser while the user is browsing. Cookies were designed to be a reliable mechanism for websites to remember stateful information (such as items added in the shopping cart in an online store) or to record the user's browsing activity (including clicking particular buttons, logging in, or recording which pages were visited in the past). They can also be used to remember arbitrary pieces of information that the user previously entered into form fields such as names, addresses, passwords, and credit card numbers.
>
> [Wikipedia](https://en.wikipedia.org/wiki/HTTP_cookie)
>
> In non technical words **cookie** is a small text files, that is sent by server to a client and kept on a user's computer by browser in order to remember user's password or login or both for ex
>
## Common status codes
>
> The **status codes** are issued by a server in response to a client's request made to the server. It includes codes from IETF Request for Comments (RFCs), other specifications, and some additional codes used in some common applications of the Hypertext Transfer Protocol (HTTP). The first digit of the status code specifies one of five standard classes of responses.
>
> [Wikipedia](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes)
>
> In non technical words **status code** is the first part of a server's answer to http request, also contains a phrase in English, that clears the problem
>
> All HTTP response status codes are separated into five classes (or categories). The first digit of the status code defines the class of response. The last two digits do not have any class or categorization role. There are five values for the first digit:
>
> **1xx (Informational):** The request was received, continuing process 
>
> **102** Processing 
>
> **2xx (Successful):** The request was successfully received, understood, and accepted
>
> **200 OK**
>
> **201 Created**
>
> **3xx (Redirection):** Further action needs to be taken in order to complete the request
>
> **301** Moved Permanently
>
> **302** Moved Temporarily
>
> **4xx (Client Error):** The request contains bad syntax or cannot be fulfilled
>
> **404** Not Found 
>
> **5xx (Server Error):** The server failed to fulfill an apparently valid request
>
> **500** Internal Server Error** 
>



Request:

```
METHOD URI PROTOCOL
HEADER1: header_value1
HEADER2: headr_value2

REQUEST BODY
```


GET request example

http://yandex.ru/some_document

```http
GET /some_document HTTP/1.1
User-Agent: Mozilla/4.0 (compatible; MSIE5.01; Windows NT)
Host: yandex.ru
```

---

Browser address bar: `http://example.com/hello.html`

```http
GET /hello.html HTTP/1.1
User-Agent: Mozilla/4.0 (compatible; MSIE5.01; Windows NT)
Host: example.com
Accept-Language: en-us
Accept-Encoding: gzip, deflate
Connection: Keep-Alive
```

---

Browser address bar: `http://google.com`
```http
GET / HTTP/1.1
User-Agent: Internet Explorer
Host: google.com
```
---

POST request example

```http
POST /login HTTP/1.1
User-Agent: Mozilla/4.0 (compatible; MSIE5.01; Windows NT)
Host: example.com
Content-Type: application/x-www-form-urlencoded
Content-Length: length
Accept-Language: en-us
Accept-Encoding: gzip, deflate
Connection: Keep-Alive

login=myname&password=mystrongestpassword
```


[What happens when you type google.com into your browser and press enter?](https://github.com/alex/what-happens-when) - detailed explanation

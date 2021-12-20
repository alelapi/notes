# REST API

 Representational state transfer (REST) is a software architectural style that defines a set of constraints to architecture of a Web distributed system. The REST architectural style focus on:
- scalability of interactions between components 
- uniform interfaces 
- independent deployment of components
- the creation of a layered architecture to facilitate caching components

A web API that obeys the REST constraints is informally described as RESTful.
RESTful web APIs are typically based on HTTP methods to access resources via URL-encoded parameters and the use of JSON or XML to transmit data.

In a RESTful Web service, requests made to a resource's URI elicit a response with a payload formatted in HTML, XML, JSON, or some other format.
The most common protocol for these requests and responses is HTTP. It provides stateless operations (HTTP methods) such as GET, POST, PUT, and DELETE.

## HTTP Methods
- GET: only retrieve data without other effect.
- HEAD: retrieve a resource like GET but without data, only with metadata.
- POST: used to send data enclosed in the body, without know the location.
- PUT: used to create or update a resource. It's idempotent and not cachable.
- DELETE: used to delete a resource.
- OPTIONS: request the http methods supported.
- CONNECT: used to request a TCP connection for HTTP tunneling
- TRACE: used to test receiver.
- PATCH: used to applies partial modifications to a resource.

## HTTP Status code

### 1xx Informational response
- 100 Continue: The server has received the request headers and the client should proceed to send the request body 
- 101 Switching Protocols
- 102 Processing
- 103 Early Hints

### 2xx Success
- 200 OK: Standard response for successful HTTP requests.
- 201 Created: The request has been fulfilled, resulting in the creation of a new resource.
- 202 Accepted: The request has been accepted for processing, but the processing has not been completed.
- 203 Non-Authoritative Information: The server is a transforming proxy (e.g. a Web accelerator) that received a 200 OK from its origin, but is returning a modified version of the origin's response.
- 204 No Content
- 205 Reset Content
- 206 Partial Content
- 207 Multi-Status
- 208 Already Reported
- 226 IM Used

### 3xx redirection
- 300 Multiple Choices
- 301 Moved Permanently
- 302 Found (Previously "Moved temporarily")
- 303 See Other
- 304 Not Modified: Indicates that the resource has not been modified since the version specified by the request headers If-Modified-Since or If-None-Match.
- 305 Use Proxy: The requested resource is available only through a proxy.
- 306 Switch Proxy: No longer used.
- 307 Temporary Redirect
- 308 Permanent Redirect

### 4xx client errors
- 400 Bad Request
- 401 Unauthorized
- 402 Payment Required
- 403 Forbidden
- 404 Not Found
- 405 Method Not Allowed
- 406 Not Acceptable
- 407 Proxy Authentication Required
- 408 Request Timeout
- 409 Conflict: Indicates that the request could not be processed because of conflict in the current state of the resource, such as an edit conflict between multiple simultaneous updates.
- 410 Gone: Indicates that the resource requested is no longer available and will not be available again.
- 411 Length Required
- 412 Precondition Failed
- 413 Payload Too Large
- 414 URI Too Long
- 415 Unsupported Media Type
- 416 Range Not Satisfiable
- 417 Expectation Failed
- 418 I'm a teapot
- 421 Misdirected Request
- 422 Unprocessable Entity
- 423 Locked
- 424 Failed Dependency
- 425 Too Early
- 426 Upgrade Required
- 428 Precondition Required
- 429 Too Many Requests
- 431 Request Header Fields Too Large
- 451 Unavailable For Legal Reasons

### server errors
- 500 Internal Server Error
- 501 Not Implemented: The server either does not recognize the request method.
- 502 Bad Gateway: The server was acting as a gateway or proxy and received an invalid response from the upstream server.
- 503 Service Unavailable: The server cannot handle the request. Generally, this is a temporary state.
- 504 Gateway Timeout: The server was acting as a gateway or proxy and did not receive a timely response from the upstream server.
- 505 HTTP Version Not Supported
- 506 Variant Also Negotiates
- 507 Insufficient Storage
- 508 Loop Detected
- 510 Not Extended
- 511 Network Authentication Required
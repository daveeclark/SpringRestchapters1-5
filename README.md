# SpringRestchapters1-5

Chapter 1 : Introduction to REST
(pg 7 online pdf, page 1 in book)

REST:
REpresentational
State Transfer

Architectural style for designing distributed network applications composed of six constraints or principles
  - Client-Server: concerns should be seperated between clients and servers enabling client and server components to evolve independently and allows system to scale
  - Stateless: the communication between client and server should be stateless, making client include all necessary info in request so server can understand and process it
  - Layered System: multiple hierarchial layers such as gateways, firewalls, and proxies can exist between client and server
  - Cache: responses from the server must be declared as cacheable or noncacheable allowing the client or intermediary components to cache responses and reuse them later
  - Uniform Interface: Simplified overall architecture between all interactions of client, server, and intermediary components
  - Code On Demand (optional constraint): Clients can extend functionality by downloading and executing code on demand i.e JavaScript
  
Before interacting with and using a resource, you have to properly identify it; WEB provides Uniform Resource Identifier (URI) for uniquely identifying resources

Syntax of a Uniform Resource Identifier is: scheme:scheme-specific-part or http://www.apress.com/9781484208427

The 'http' is the scheme, indicating that the scheme should be used for interpreting the rest of the URL

Curly braces {} indicate the part of the standarized URI template is a (path) variable, allowing clients to substitute the value for another value

REST components interact with a resource by transferring its representations back and forth, they never directly interact with the resource

The same resource can have several representations ranging from text-based HTML, XML, and JSON formats to other binary formats like PDFs, JPEGs, and MP4s

Content negotiation: when a client request a particular representation and the process

The HTTP standard provides eight HTTP methods that allow clients to interact and manipulate resources
  Most commonly used methods are: GET (Read), POST (Create), PUT (Update), DELETE (delete)
  
  Safety: used to retrieve resources and doesnt change the system state
  Idempotency: if operation produces the same server state no matter how many times its applied, it is considered idempotent (denoting an element of a set which is unchanged in value when multiplied or otherwise operated on by itself
  GET (safe/idempotency): used to retrieve a resource's representation, considered safe because they don't modify server state
  HEAD (safe/idempotency): used to check if a resource exists without showing actual representation
  DELETE (safe): requests a resource to be deleted
  PUT (idempotent: allows client to modify or create a new resource (only if client knows the URI) and sends the updated representation to the server using the method
  POST(neither safe or idempotent): used to create resources under subcollections without knowing the URI of resource, server is responsible for assigning an ID to the resource and and where it will reside
  PATCH(neither safe or idempotent: performs partial resoucre updates '{"name":"New Awesome Title"}'

HTTP Status Codes (important role in REST API design) - allows a server to communicate the results of processing a client's request
  -Informational Codes: server has received the request but hasn't completed processing it, 100 series
  -Success Codes: request has been successfully received and processed, 200 series
  -Redirection Codes: request has been processed but client must perform additional action to complete request, 300 series
  -Client Error Codes: indicates error with client's request, 400 series
  -Server Error Codes: indicates there was an error on server while processing client's request, 500 series

Richardson's Maturity Model (RMM) - classifies REST-based Web services on how well they adhere to REST principles in four classifications

  - Level 0
    - Most rudimentary, uses HTTP as transport mechanism and perform remote procedure calls on a single Uniform Resource Identifier (URI)

  - Level 1
    - Introduces multiple URI's, complex functionality with large service endpoint is broken down into multiple resources

  - Level 2
    - Makes right use of HTTP verbs and status codes avaiable in protocol

  - Level 3
    - Most mature level for a service built around notion of Hypermedia as the Engine of Application State (HATEOAS), that allows discoverability by providing responses that contain links to related resources
    
Steps in building a RESTful API: Identify Resources (app's domain or entities), Identify Endpoints, Identify Actions (HTTP methods that can be used to perform operations on resources), Identify Responses



CHAPTER 2: Spring Web MVC Primer























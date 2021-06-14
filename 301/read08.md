# Read08: APIs

## API Design Best Practices

- What does REST stand for?
  **REST** stands for Representational State Transfer, which is an architectural approach to designing web services.  
  <br/>

- REST APIs are designed around a <ins> resources</ins>.
  <br/>

- What is an identifer of a resource? Give an example.
  A resource has an _identifier_, which is a **URI** that uniquely identifies that resource.  
  ex) `https://adventure-works.com/orders/1`
  <br/>

- What are the most common HTTP verbs?
  The most common operations are GET, POST, PUT, PATCH, and DELETE.
  <br/>

- What should the URIs be based on?
  **URI**s should be based on _nouns_ (the resource) and not verbs (the operations on the resource).

<br/>

- Give an example of a good URI.
  `https://adventure-works.com/orders` // Good

  `https://adventure-works.com/create-order` // Avoid
  <br/>

- What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?
  **"chatty" web APIs** are those that expose a large number of small resources. Such an **API** may require a client application to send multiple requests to find all of the data that it requires. This procedure will cause a load on the server and it is not something you want.  
  <br/>

- What status code does a successful GET request return?
  A successful `GET` method typically returns `HTTP status code 200`(OK).

<br/>

- What status code does an unsuccessful GET request return?
  An unsuccessful `GET` method returns `404 (Not Found)`.

<br/>

- What status code does a successful POST request return?
  A successful `POST` method, that creates a new resource return `HTTP status code 201 `(Created).
  <br/>

- What status code does a successful DELETE request return?
  A successful `DELETE` method return `HTTP status code 204`.  
  <br/>
  <br/>

## References:

[API Design Best Practices](https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design)

# Read13: CRUD

## Status Codes Based On REST Methods

- In your own words, describe what each group of status code represents:

- 100’s = Informational status codes, the header part of the request has been received, but it won't success.
- 200’s = Success codes. meaning it will respond with what the user asked.
- 300’s = Redirection codes. They tell the client that the resource they are requesting isn’t available at the expected location anymore.
- 400’s = Error codes. They happen when the user send invalid request like timeouts, wrong URI, missing authentication, etc.
- 500’s = Server error codes. Most of the times the happen due to problems in the server, but they can happen also, from the user end, if the user trigger a special error during request. These errors can be temporary or permanent.

<br/>

- What is a status code 202?

This status code can occur during many HTTP methods or be used in many situations like:

- `POST()` : When trying to create an action, and it is accepted this code appears.

- `PUT()` or `PATCH()` : When trying to make an update, and If the update is done asynchronous, this code can be used. It should include an URL to access the updated resource or an URL to check if the update has been succeeded. It can also include an estimation of how long the update will take.

- `DELETE()` : When using delete action. If the deletion is asynchronous and takes some time, which is the case in distributed systems, it can be appropriate to return this code with some information or URL to tell the client when it will be deleted.

<br/>

- What is a status code 308?

This status code can occur during many HTTP methods or be used in many situations like:

- `GET()` : When trying to read data, it tells the client to use another URL to access the resource and not use the current URL anymore. It’s helpful when we have multiple endpoints for one resource, but don’t want to implement reading from all of them.

- API change : This is the right code if the resource will now be available at a new URL and the client should directly access it via the new URL in the future. The current endpoint can’t control the clients’ behavior after the request and a subsequent redirect if the resource URL changes again have to be issued from the new URL.

- Multiple Endpoints for One Resource : If we have nested resources `/user/kay/comments/456` and `/posts/123/comments/456`; and a root resource `/comments/456` it can make things easier to simply issue 308 redirects at the nested resources with the Location header field pointed to the root resource so not every endpoint needs a delivery implementation. This should only be done for `GET` requests.

- Wrong URL: If the URL the user used is wrong. This would be the right code if we know that a resource has moved to a different URL and we can tell the client about it.

<br/>

- What code would you use if an update didn’t return data to a client?
  204 No Content : For updates that don’t return data to the client, for example when just saving a currently edited document.
  <br/>

- What code would you use if a resource used to exist but no longer does?
  404 : This code is what is used mostly when a resource is not existing. It also can be used in different situations, like when a resource exist, but due too security measures we can't give access to the user.
  <br/>

- What is the ‘Forbidden’ status code?
  The Forbidden status code, which is **403** is given whenever the user can not get access to a resource. Wether the user is authorized or not  
  <br/><br/>

## Build A REST API With Node.js, Express, & MongoDB

- Why do we need to pull our MongoDB database string out of our server and put it into our .env?
  Because when we want to deploy our application we want to use other services than our local host.
  <br/>

- What is middleware?
  middleware is a code that runs once the servers get the request, but before it is passed to the routes.
  <br/>

- What does app.use(express.json()) do?
  It lets our server accept `JSON` ad a body inside `HTTP` methods.
  <br/>

- What does the /:id mean in a route?
  This mean that `id` is a parameter, that can be used in requests as `request.params.id`
  <br/>

- What is the difference between PUT and PATCH?
  `PUT` update the entirety of a resource, while `PUT` update only what the user give it.

- How do you make a defalut value in a schema?
  To make a default value in a Schema, we only pass in it a key called `default` and give it a value of the same type.
  <br/>

- What does a 500 error status code mean?
  It means that there is an error at our server, not related to the user or client.
  <br/>

- What is the difference between a status 200 and a status 201?
  status code 200 means everything was successful, while status code 201 mean a successful creation of a resource.

<br/><br/>

# References:

[Status Codes Based On REST Methods](https://www.moesif.com/blog/technical/api-design/Which-HTTP-Status-Code-To-Use-For-Every-CRUD-App/) <br/>
[Build A REST API With Node.js, Express, & MongoDB](https://www.youtube.com/channel/UCFbNIlppjAuEX4znoulh0Cw)

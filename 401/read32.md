# Read: 32 - Serverless and Amplify

## Serverless Architecture

> Focus on your application, not the infrastructure

- **Serverless** is a cloud computing execution model where the cloud provider dynamically manages the allocation and provisioning of servers.

- a lot of your daylight hours go into implementing, maintaining, debugging, and monitoring the infrastructure, *Serverless* will lift out of the way all of that infrastructure heavy, so we can focus on the business goals our applications serve.

- Pricing is based on the number of executions rather than pre-purchased compute capacity.


### Traditional vs. Serverless Architecture

In the traditional the server side have to handle the logic (back and front) and the security and the Database, but in the **serverless architecture** the front end logic is handled on the client side and the (security , database , backend logic) are 3rd party services.

- advantages and disadvantages of serverless arch:

![dis](https://s7280.pcdn.co/wp-content/uploads/2018/01/key.png)

### The Serverless App consist of:

- **Client Application**: The UI of your application is rendered client side in Modern Frontend Javascript App which allows us to use a simple, static web server.

- **Web Server**: Amazon S3 provides a robust and simple web server.

- **Lambda functions (FaaS)**: They are the key enablers in Serverless architecture. Some popular examples of FaaS are AWS Lambda, Google Cloud Functions and Microsoft Azure Functions.

- **Security Token Service (STS)**: generates temporary AWS credentials (API key and secret key) for users of the application.

- **User Authentication**: AWS Cognito is an identity service which is integrated with AWS Lambda. With Amazon Cognito, you can easily add user sign-up and sign-in to your mobile and web apps.

- **Database**: AWS DynamoDB provides a fully managed NoSQL database.


## AWS Amplify

> AWS Amplify is a set of tools and services that can be used together or on their own, to help front-end web and mobile developers build scalable full stack applications, powered by AWS. With Amplify, you can configure app backends and connect your app in minutes, deploy static web apps in a few clicks, and easily manage app content outside the AWS console.

- Amplify web frameworks including supported:

1. JavaScript.
2. React.
3. Angular.
4. Vue.
5. Next.js

- mobile platforms supported:

1. Android.
2. iOS.
3. React Native.
4. Ionic.
5. Flutter.

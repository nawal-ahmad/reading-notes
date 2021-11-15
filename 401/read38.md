# Read: 38 - Notifications


## SNS

> Amazon Simple Notification Service (Amazon SNS) is fully-managed event-driven pub/sub messaging service that can be used to decouple distributed systems and microservices.

**How it works:**
First of all you have to create a topic, which is an access point for subscribers interested in receiving notifications about a specific subject. When a message is published to a topic, Amazon SNS pushes the message to all appropriate subscribers, which could be HTTP endpoints, Amazon SQS queues, or AWS Lambda functions.

**Some common cases for private networking and messaging include:**

- Isolating development and testing environments
- Sharing personally identifiable information (PII) about your customers
- Hosting a PCI-compliant e-commerce website
- Developing healthcare applications subject to HIPAA
- Implementing a cryptographic algorithm subject to FIPS 140.

## VPC

> Amazon Virtual Private Cloud (VPC) is a virtual network that closely resembles a traditional network that you’d operate in your own data center.

> Amazon VPC lets you provision a logically isolated section of the AWS Cloud where you can launch AWS resources in a virtual network that you define. 
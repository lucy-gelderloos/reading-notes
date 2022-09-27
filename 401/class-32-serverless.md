# Serverless, Amplify, GraphQL

## [Intro to serverless architecture](https://hackernoon.com/what-is-serverless-architecture-what-are-its-pros-and-cons-cc4b804022e9)

### Describe “serverless” to a new 301 Code Fellows student

Serverless architecture is a system where the vendor allocates space for each of your app's processes as needed, eliminating the need to maintain your own servers.

**Pros:**

- pay per execution, rather than maintaining a server 24/7
- easy to set up new environments
- less time spent on administration

**Cons:**

- less control over your system
- potential security and disaster recovery risks
- unpredictable costs
- new technology, so tools and best practices are not as developed as more established systems

## [AWS Amplify documentation](https://aws.amazon.com/amplify/)

## [GraphQL data modeling](https://docs.amplify.aws/cli/graphql/data-modeling/)

GraphQL types annotated with `@model` will automatically have DynamoDB database tables generated (including auto-generated primary keys).

### Pros & Cons

Graph is quick and flexible, and allows nesting of queries to make them more efficient. However, as a new technology, it's hard to know how it will scale in the future and whether that efficiency will remain.

### REST vs. Graph

Rest is well-developed and reliable, but may be less flexible and have slower response times as requests become more frequent. Graph has strong typing, which means it can never send back a String in response to a request for an integer.

REST uses HTTP caching to reduce the load of its GET requests; since most (originally all) GraphQL requests are POST requests, they don't use caching.  

## Things I'd like to know more about

How to stay on top of which tools are the most efficient for a particular project.

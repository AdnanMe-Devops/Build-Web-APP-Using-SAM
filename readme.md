ln this project we build  a serverless web application using Python 3.6 and we use Lambda, API Gateway, S3, DynamoDB, and Cognito to create a multi-user to-do list application based on Vue.js.
this was current and ongoing learning process with SAM and pythan boto3 .The project is on vagrant .
Native serverless applications can be easier to develop because there's usually a lot less application code.

However, they also require a lot more test code because there's a lot of services that we're going to need mock out. The todo application services including Cognito, S3, APIGateway, Lambda and DynamoDB. By using APIGateway to kick off our Lambda functions, we ended up with a highly scalable app that's highly available within a single region.

Our application was built with Python 3.6 and we used the included unit test module for our testing. To mock out DynamoDB, we used the moto framework that is a mock version of boto. We used view Vue. js on the front end to facilitate kicking off a call to Cognito to authenticate. Then we passed the authtoken to APIGateway where it decoded and passed the claims over to our Lambda functions.

Once the functions ran, they used boto to make calls to DynamoDB and then sent the response back through APIGateway back to the Vue. js application. So, while it was a simple application, there are a lot of moving parts. 
steps 
 architecture of a serverless web application
Set up the AWS services required for the app
Create and deploy an API using Python 3.6
unit tests
Use a Cognito User Pool within your app

# Vue.js TodoMVC Example

> Vue.js is a library for building interactive web interfaces.
It provides data-driven, nestable view components with a simple and flexible API.

> _[Vue.js - vuejs.org](http://vuejs.org)_

## Learning Vue.js

The [Vue.js website](http://vuejs.org/) is a great resource to get started.

Here are some links you may find helpful:

* [Official Guide](http://vuejs.org/guide/)
* [API Reference](http://vuejs.org/api/)
* [Examples](http://vuejs.org/examples/)
* [Building Larger Apps with Vue.js](http://v1.vuejs.org/guide/application.html)

Get help from other Vue.js users:

* [Vue.js on Twitter](https://twitter.com/vuejs)
* [Vue.js on Gitter](https://gitter.im/vuejs/vue)
* [Vue.js Forum](http://forum.vuejs.org)

_If you have other helpful links to share, or find any of the links above no longer work, please [let us know](https://github.com/tastejs/todomvc/issues)._

## Credit

This TodoMVC application was created by [Evan You](http://evanyou.me).

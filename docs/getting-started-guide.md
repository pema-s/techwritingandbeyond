---
title: "How to create a Getting Started guide for API Docs"
keywords: "api documentation, api, documentation, dev docs, developer, documentation, technical, writers" 
tags: [getting_started]
sidebar: mydoc_sidebar
permalink: getting-started-guide.html
folder: techwritingandbeyond
---
## How to create a Getting Started guide for your API Documentation
**Reading time**: 5 mins <br>
**Writing for**: Developers new to your API or solution.

So you have auto generated your API documentation from the code source and everyone loves it! It’s easy to assume that auto generated API docs are enough to get your users to start using it but without explaining some basic how-tos about using the APIs, it will never serve the purpose.  

Think about a new user that is trying to integrate with your system so they can start making API calls at the earliest. While you might have designed your APIs in a straightforward way, there’s always something worth calling out that can make a huge difference to the user. For instance, when I was working on a freelancing project, it was absolutely critical to explain the synchronous and asynchronous way of receiving API responses because without that knowledge, the consumer of API would be lost.

As with all things, the devil “lies in the details” so having a well detailed out “Getting Started” guide for your APIs is very critical. I’ve seen API documentation jumping straight into the descriptions of an API without setting the ground around the nature in which the APIs work. How you expect the request to be sent or how you’ve implemented the authentication. There are a bunch of things that might seem very basic to you but without calling them out at the onset, your API documentation will fall short. 

This post attempts to list down the most common sections worth including in your “Getting Started” guide so that you can give a great head-start to your API consumers. Every Getting Started guide will be different. However, in essence what you should solve for are:

- Making API docs self-serving: Ensure your documentation allows the developer to start the API integration without having to consult anyone. 
- Building confidence in new developers: Setting the ground clearly with Getting Started guide makes a new developer want to try out without any second thoughts. Imagine you're the developer user and you're able to get a clear understanding of errors that you might run into if you do something wrong and how to resolve them. Wouldn't it really make you want to give it a shot?   

Some specific categories of information you can add to your Getting Started guide for your APIs are given below: 

### Define the Base URL
A really great approach to starting your API documentation is clearly calling out the API base URL. Defining this in the start of the document makes it super easy to refer as that’s practically the first thing a developer will need. 

Example:

The Twilio API docs begin by stating the Base URL first. Below is a screenshot of how they’ve shown that information: 


### Define the Production or Staging URLs
This is also a good place to also mention if you have any staging API endpoints that you want to expose for your users to send test requests. 

Additionally, you can add details such as: 
API versioning and supported features

### Authentication and Authorization
The users of your APIs will most likely need to know what authentication they should use in order to successfully send the API request. Having the Authentication section in the Getting Started guide makes it very handy. 

Some insights you might want to use to document this are: 

- What kind of authentication is used: There are many ways of authenticating API requests such as basic auth, HMAC, Hashing, etc. Make sure you understand this clearly so you can write a detailed explanation here. One of the most important thing here would be to highlight that the **API keys or credentials used for authentication are very confidential and should not be shared with anyone**.

Example:

The Stripe API docs begin by stating the Base URL first. Below is a screenshot of how they’ve shown that information: 


- How it works and what they need to do (Authentication header) 
If there is anything specific you need to call out, show with an example. In the Sendgrid docs, they want the users to add an `authorization` header to the API request and show a sample of how that is to be added:  

- Allow list of IPs
Some APIs allow requests from only particular IP addresses and this must be called out clearly. The best place to add this piece of information is under Authorization/Authentication. 

Take a look at the way Braintree API addresses page to get an idea about listing these out. 

### Registration
This is another very obvious candidate that needs to go into your Getting Started guide. Since your user is new, they need a proper understanding of how the registration process works if they were to start using your API. Since the goal here is to allow your developers to be self-sufficient, ensure you handle all parts of this process such as how to generate the secret key, how to handle errors or the entire lifecycle of key generation. 

You could add details such as: 
- Auto-provisioning options
- API Key- how to create, replace, delete, etc. This can be a separate section in itself. See example from SendGrid API Keys page. 

### API Evaluation 
It would obviously be great if it could allow the users to do a quick evaluation of the APIs itself. There are many tools to create this functionality within the docs and I’d be documenting that in a separate post, but the common ones you can use are integrating Swagger UI or Postman. The key idea is to allow a playground so the idea of what the API can do becomes relatable rather than an abstract concept. 

Example:

In Pipedrive developer’s documentation, one can try out APIs by entering the API token at the on-set and also add specific parameters to “Run endpoint”. 

### Error Codes
The most important information worth capturing in the Getting Started guide is how one can handle errors. In this section, you can capture the following:

 Sample of the error response encountered preferably in curl. 
HTTP Status codes and the reason for the same.

Example: 
A very comprehensive way of capturing error codes and resolutions is documented in the Dailymotion’s API Error Codes page. 


These are some of the most common sections you will find in most API documentation and this post tries to present some ideas (via examples and references) so you can start creating your own. But you will always be the best judge of what’s really required to make your API documentation complete, self-serving and super helpful!

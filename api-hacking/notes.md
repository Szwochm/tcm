# API Hacking Notes

## Intro

### Interacting with APIs

Interesting, I wasn't aware that a normal get request could be using an API. I always assumed it was something at a lower level unavailable to the user.
Given the courses example of an API of a waiter in a restaurant, I wonder if a php script where you pass parameters is considered an API.
That's kind of what this seems like.

I know from building webpages that API's generally require some sort of token, it appears that the api token here is called
XSRF token, which is the same name of an attack.. I wonder how they are related or if its simply a coincidental naming

Commands

`curl catfacts.ninja/facts` -- manually get request from webpage

`curl catfacts.nina /facts -v` -- verbose to get headers, etc like you might see in Burpsuite

### Types of API


#### Rest API

- Client and server must be seperate entities.

- Rest or Restful APIs must use Http Methods

- Requests must be stateless
  
- They use URI's to identify resources
  
#### Public API -- anyone can use (like google maps api)

#### Partner API -- e.g. Engineer company shares api with Architecture company so they can share data

#### Private API -- e.g. personal company with a website that only that company can use

##### Http Methods

GET -- retrieve resource

POST -- creates a resource

PUT -- update or create within existing resource

PATCH -- partially modify resource

DELETE -- delete resource

### API Security





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

APIs are often spun up quickly, and constantly updated... this opens doors for potential attacks.

Another potential attack vector is depreciated, or legacy API's that devs forgot about. How would we enumerate these? Would it be with a directory fuzzing tools like WFUZZ?

## Lab Setup

### Tool Installation

`git clone https://github.com/Dewalt-arch/pimpmykali`

`/pimpmykali.sh`

Tools used in course -- Burpsuite, Postman, FoxyProxy

#### Installing Postman

Go to website, download

`tar -xvzf Postman`


##### Creating a link so you can place a tool anywhere and run it 

`sudo mv Postman /opt` -- can be any folder but opt is traditional

`sudo ln -s /opt/Postman/Postman /usr/bin/postman`

now we can run postman by just using `postman`

#### Installing FoxyProxy

Its just an browser extension, presumably for firefox only -- I wonder if a chormium version exists for burpsuite browser.

I wonder why we are doing this when setting up a proxy manually for burpsuite is pretty easy, and the burpsuite browser comes with built in browser proxy

Do assessments using multiple browsers, firefox may react differently than chrome


### Burpsuite Introduction

Video just basically walked through some fundamentals but there are some things of note here for me to use
- Using Scope to focus in on what type of traffic
- adjusting filters to see more content
- Using Decoder for base64, and url encoding / decoding
- burpsuite has extensions, I seen a couple that may help with the OSCP... (Agartha)
- Comparer can be used for quickly seeing differences between requests

### Postman Introduction

Workspaces are like projects
Collections are groups of requests -- you may want to group them based on functionality or some other logical grouping

Many websites provide API endpoint collections that you can import into Postman







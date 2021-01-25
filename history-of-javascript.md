# History of Javascript

## Give an overview of what happens under the hood in 1999 when a user used a web site. What different technologies, software is involved? Which standards/protocols are relevant?
Server used to send rendered/static HTML documents. Clicking a link caused a request for a new url and the server to generate a new HTML document. The browser reloaded that.

### What did jQuery changed about 1999?
Candidate should mention that jQuery was a tools to make the fetching and appending stuff to an existing DOM easier.

Bunch of tools to make manipulating existing DOM easier.

Tools to make it easier to perform requests for just fetching the data.

Fetching data became more independent of fetching page. Likely the user triggers the fetch, using visible **HTML** elements in the DOM. These visible elements are hooked up to Javascript which instructs browser using browsers API, to perform a http(s) network call. Possibly defining the details of what is to be fetched.
When response comes, browser invokes the callback func in js that modifies the DOM.

### What did Modern Javascript frameworks changed 1999
Candidate should see that the frameworks were a tool to structure bigger client application. Also the rapid re-rendering due to shadow DOM should be mentioned.

Frameworks made it easier to structure bigger applications.

The whole client could be loaded at once. Visual part of the UI, could change rapidly as the whole client application lives in the memory of the browser. Usage of shadow DOM made UI updates very rapid. React made it easy to use shadow DOM.

## How did the advent of modern framework changed about frontend/backend responsibilities? Candidate should see that the work that was done in backend is now done in frontend.
Lots of business logic changed to the frontend.

Modern web applications are like desktop applications, they can be cached and saved to consumer's browsers and backends are purely functioning to feed the data.

## What are the more often used browser APIs?
URL, fetch, DOM manipulation, storing of data, cookies, local storage, indexed db

## What other browser APIs/functionality do you know?
This measures how curious the candidate is.

Service workers combined with indexed db, request intercepting and caching, web assembly

## What is css-in-js
Your expectations here

### What are the advantages of it?
Your expectations here

### What are the disadvantages of it?
Your expectations here
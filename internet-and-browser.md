# The Internet Questions

## Can you tell me what CORS are?
- HTTP header based mechanism
- allows a server to indicate any other origin (domain, scheme, port) than its own which a browser should permit loading of recourses
- browser can make a "preflight" request to a server hosting the cross-origin resource, in order to check that the server permit an actual request
- browser sends headers that indicate HTTP method and header will be used in the actual request

## Can you give me an example for a cross-origin request?
`https://domain-a.com` uses `XMLHttpRequest` to make a request for `https://domain-b.com/data.json`.
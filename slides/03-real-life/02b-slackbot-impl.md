## "http-ping" Slackbot

```javascript
// set up some helper functions
const get = promisify(http.get);
const normalise, formatSuccess, formatError...;

// AWS Lambda API starts here
exports.handler = (event, context) => get(normalise(event.url))
    .then(formatSuccess)
    .catch(formatError);
```

``` javascript
> { "url": "https://google.com" }
```

```javascript
< {
<   "statusCode": 301,
<   "headers": {
<     "location": "https://www.google.com/",
<     "content-type": "text/html; charset=UTF-8"
<     ...
<   }
< }
```

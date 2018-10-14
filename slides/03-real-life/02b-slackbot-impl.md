## "http-ping" Slackbot

```javascript
> { "url": "https://google.com" }
```

```javascript
// assume we've imported libs and set up helper functions...

exports.handler = (event, context) => get(event.url)
    .then(formatSuccess)
    .catch(formatError);
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

## "http-ping" Slackbot

```javascript
> { "url": "https://google.com" }
```

<pre class="fragment">
<code class="lang-javascript">
exports.handler =
  (event, context) => get(event.url)
    .then(formatSuccess)
    .catch(formatError);
</code>
</pre>

## "web-ping" Slackbot

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

<pre class="fragment">
<code>
$> sam package --template-file webping.yaml ...
$> sam deploy --stack-name webpingdemo ...
</code>
<pre>

Note:
- scales up/down
- https
- HA
- monitoring, logging
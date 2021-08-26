# Example using Atlas MongoDB Trigger to call webhook

![Flow Diagram](.images/mongodb-webhook.svg)

Example script for trigger:

```javascript
exports = function(changeEvent) {
  const response = context.http.post({
    url: "https://0191e309cfbd.ngrok.io",
    body: changeEvent,
    encodeBodyAsJSON: true
  });
};
```

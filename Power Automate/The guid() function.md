# The Power Automate guid() function

The Power Automate (or Logic Apps) guid function allows you to auto generate a unique guid string in your Flows. This means you don't have to cobble together something using string manipulation and REGEX.

This function comes especially in handy if your logging the output of your Flows to a datasource to track failures, retries etc.

The formula looks as follows:

```yaml
guid('D')
```

You pass a specific letter depending on how you want your guid to be formatted. D is the default but N, B, P or X are also available.

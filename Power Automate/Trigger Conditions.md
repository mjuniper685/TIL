# Power Automate Trigger Conditions

Power Automate trigger conditions can be use to provide greater specificity on how and when triggers fire.

For example if you have a Flow which triggers when an item in a list is 'Created' you can set a condition so the Flow only triggers when the Created Date = today:

```json
@equals(triggerBody()?['Created'], utcNow('yyyy-MM-dd'))
```
I've used this to block a Flow from firing after a failure in order to prevent it sending out multiple emails.

TODO: Expand with more examples
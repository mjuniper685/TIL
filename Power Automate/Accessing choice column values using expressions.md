# Accessing choice column values using expressions

When writing a Flow to send out a weekly email, I was attempting to build a HTML table from a SharePoint list.

One of the columns on the list was a Choice column with two values. For some reason I could only Dynamically get the ID of the Choice and not the value.

Choice columns are returned as objects with IDs and Values (and a few other parameters)

I tried multiple different ways of accessing it and eventually found the following worked:

```json
@item()?['Document_x0200_Type']['Value']
```
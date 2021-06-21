# Adding to 'Most Recent' dropdown menus

## TLDR: adding a document to a SharePoint library will make the site appear in the 'Most Recent' dropdowns in the Power Platform

## Fuller explanation

This counts for both Power Automate and Apps as far as I can tell. I randomly came across it on the Power Apps forums and thought to make a note of it.

Across the Power Platform there are dropdown menus when using connectors of 'most recently used' (I'm thinking SharePoint here).

I was trying to add the right site into an environment variable when moving it from DEV to TEST. However the SharePoint link wouldn't work and I couldn't find it in the dropdown menu.

I found a tip which said adding a document to the site would make it appear in the dropdown. I did this, the Site appeared in the dropdown and I could use it in the variable.

It's annoying how buggy this stuff is from the front end.
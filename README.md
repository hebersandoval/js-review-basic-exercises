# Exercise Questions

### What does the following link do and what problems can that cause?

```
<a href="javascript: open('tac.pdf')">Read our Terms and Conditions</a>
```

This code opens a  .pdf file named `tac.pdf` in a new tab. This file could contain some malicoious code.

### Providing parameters for scripts is a powerful way of making them reusable. It is very important to keep the option to provide compact and easy to use parameters. What are the downsides of the following solution (which provides parameters that are compact and easy to use)?

```
<script src="badge.js"> var color = 'blue'; var background = 'yellow'; var width = 400; </script>
```

First, when using a `<script>` that has the `src` attribute, no code can't be place inside the tags. Also, the code inside could be placed inside a stylesheets file for separation of concern.

### What is the issue with so called “global variables”, and how can they be avoided?

For one, they can override some other functionality of your code that uses the same name some where else.

### Where in the document would you put a large script that is nice to have but not vital to the functionality of the site? Why?

You can put it at the bottom of your main js file and use the `script` tag's `src` attribute to reference it from there.

### What is the problem with executing scripts like this:

```
<body onload="init()">
```
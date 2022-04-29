# Exercise Questions

### What does the following link do and what problems can that cause?

```
<a href="javascript: open('tac.pdf')">Read our Terms and Conditions</a>
```

This code opens a .pdf file named `tac.pdf` in a new tab. This file could contain some malicoious code.

### Providing parameters for scripts is a powerful way of making them reusable. It is very important to keep the option to provide compact and easy to use parameters. What are the downsides of the following solution (which provides parameters that are compact and easy to use)?

```
<script src="badge.js"> var color = 'blue'; var background = 'yellow'; var width = 400; </script>
```

First, when using a `<script>` that has the `src` attribute, no code can't be place inside the tags. This is because the code within the tags will not be executed. Also, the code inside could be placed inside a stylesheets file for separation of concern.

### What is the issue with so called “global variables”, and how can they be avoided?

For one, they can override some other functionality of your code that uses the same name some where else. Also, it is common for web pages to include code not written by you or other developers in your team. These can include, third-party libraries, tracking and analytics scipts, scripts from an advertising partner.

### Where in the document would you put a large script that is nice to have but not vital to the functionality of the site? Why?

You can put it at the bottom of your main js file and use the `script` tag's `src` attribute to reference it from there. Order matters, as JS will load the file being referenced in the `src` attribute. Another viable solution that will enhance performance and prevent the browser from pausing the rendering process to the document, is to use a backend script to create a single file from all the files you have for your app to use.

### What is the problem with executing scripts like this:

```
<body onload="init()">
```

This is a hack and is not bullet proof to work. The reason for this hack, is the placement of the `script` tags in the `<head>` of the HMTL, you will have a rendering pause frenzy if you reference alot of scripts here. This will delay the rendering or display of the document and the script may not have access to the HTML in the document to do its job. This can cause more work in the developer to delay the execution of any script that changes the HTML of the document until it has finished loading.

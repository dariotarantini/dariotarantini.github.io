---
title: "How to create a Chrome extension"
date: 2021-07-04T17:13:27+01:00
---
A **Chrome extension** is a *sandboxed* webapp that can interact with a website or can run alone. 

In this shot, we are going to make a simple "hello world" extension.
### How to make it
First, we need to create a **manifest.json file** that will store information about our extension. It should be placed in the root dir of our project. You can copy this simple example:
```
{
  "name": "Hello educative!",
  "description": "Our simple project",
  "version": "1.0",
  "manifest_version": 3,
  "action": {
    "default_popup": "main.html",
    "default_icon": "icon.png"
  }
}
```
Here, we specified the *name* of the extension, the *description*, and an object called *action*.
We also specify the default "page" that should be displayed when clicking on the icon and the icon itself. 
If we omit the *default_icon*, Chrome will use a default one (as shown below).

> These strings are basically relative paths to the files.


Now we can add content to  our *main.html*, as follows:
```<!doctype html>
<html>
  <head>
    <title>Hello world!</title>
  </head>
  <body>
    <h1>Hello world!</h1>
  </body>
</html>
```
### Let's try everything!
Now, you just need to open Chrome, navigate to `chrome://extensions`, set Developer Mode and Load unpacked extension, and select our project root dir. That's it.

Once we click, you will see the extension working!
> More information can be found in the official documentation [here](https://developer.chrome.com/docs/extensions/mv3/).

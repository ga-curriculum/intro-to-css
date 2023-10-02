# Intro to CSS - Multiple Stylesheets

![Hero image](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to use multiple stylesheets to organize and manage CSS code.

When creating larger projects- especially ones with multiple pages- our CSS can quickly get messy if we only use one stylesheet. 

Instead, we can create a separate stylesheet for each page or section of our website/app/game, allowing us to keep things tidy and easily accessible. 

Some of the biggest benefits of using multiple stylesheets are:

- **Organization**
  
- **Performance**: Loading multiple stylesheets can help improve the performance of our web pages. This is because browsers can load stylesheets in parallel, which means that they can start loading the CSS code for your page before the HTML code has finished loading.
  
- **Maintenance**: Using multiple stylesheets can make it easier to maintain your CSS code. This is because you can isolate changes to specific stylesheets, which makes it less likely that you will accidentally break something when you make a change.


To use multiple stylesheets, simply add a `<link>` element to the `<head>` section of your HTML code for each stylesheet that you want to use. 

An example of what that might look like:

```html
<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" href="global.css">
  <link rel="stylesheet" href="page.css">
</head>
<body>
  ...
</body>
</html>
```

### Order of precedence

When a browser loads multiple stylesheets for a web page, it will apply the styles in the order that the stylesheets are linked in the `<head>` section of the HTML code. This means that the styles in the later stylesheets will override the styles in the earlier stylesheets.

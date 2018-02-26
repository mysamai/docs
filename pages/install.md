# Installing mySam

## Try live

You can try a live version of mySam at [mysamai.com/try/](https://mysamai.com/try/). It runs like a normal website and stores all data locally in the browser. It only includes the basic plugins.

## NodeJS

The [mysam](https://www.npmjs.com/package/mysam) NodeJS module comes with a command line tool that starts a simple webserver and hosts a copy of mySam locally:

```
npm i mysam -g
mysam
```

Once running, you can use mySam at [localhost:5050](http://localhost:5050). The server will also host the current folder which allows to customize your version of mySam. See the [writing plugins](./plugins.md) chapter for more information.

## In browser

The `mysam` NodeJS module is just a convenience wrapper for starting a webserver and hosting mySam's code. Since it runs completely in the browser, you do not need NodeJS. mySam can be initialized as a normal HTML page like this:

```html
<!DOCTYPE html>
<html>
<head>
  <title>MySam</title>
  <link href="//fonts.googleapis.com/css?family=Muli:400,400italic" rel="stylesheet" type="text/css">
  <link rel="stylesheet" href="//maxcdn.bootstrapcdn.com/font-awesome/4.3.0/css/font-awesome.min.css">
  <script src="//use.fontawesome.com/2a69994fc7.js"></script>
  <link rel="stylesheet" href="//unpkg.com/mysam@^0.2.0/dist/styles/styles.css">
</head>
<body>
  <div id="content" class="full"></div>
  <script src="//unpkg.com/mysam@^0.2.0/dist/mysam.js"></script>
  <script>
    var sam = mysam(document.getElementById('content'));
  </script>
</body>
</html>
```

# History / Miva Engine / Miva Script

## History

Miva Merchant began in 1996 as the HTMLScript Corporation. In 1997, the company released its first catalogue-based ecommerce product, KoolKat. Shortly after KoolKat’s release, the name of the company was changed to Miva, Inc, and KoolKat was renamed Miva Merchant. Since that time, there have been several updates to Miva Merchant’s core software, leading up to the most recent version, Miva Merchant 5.5.

In 2003 the company was purchased by FindWhat.com which changed its name to Miva, Inc in 2005.

## Miva Engine: Miva Mia

Miva Merchant Mia is an engine and personal web server environment that runs compiled MivaScript applications, giving store designers and software developers the means to run and test their work on their Windows desktop. Mia enables users and developers to create the same environment on a local Windows machine as would be available on a Web server under Miva Merchant Empresa.

Miva Merchant Mia provides an excellent development environment for MivaScript developers to build, test, and run interactive web applications offline before deployment on a production, Miva Merchant Empresa-enabled web server.

## Miva Script

Miva Script tags have the same form as HTML tags; the element names indicate their function and the attributes specify values that the tags operate on. They can be freely mixed with HTML tags or even embedded JavaScript. Along with tags, Miva Script provides a rich set operators and built in functions for string manipulation, math, file system, array manipulation, encryption, graphics and more.

### Miva Script Example

```
<MIVA STANDARDOUTPUTLEVEL = "text, html, compresswhitespace">
<html>
<head>
  <title>Discounted Price</title>
</head>
<body>

<MvASSIGN NAME="g.price" VALUE="100.00">
<MvASSIGN NAME="g.discount" VALUE="0.20">
<p>
  <b>Discount Price: </b> $<MvEVAL EXPR = "{ (g.price - (g.price * g.discount)) ROUND 2 }">
</p>
</body>
</html>
```

### Empresa

Miva Merchant Empresa is the backbone of Miva Script. As a server-side engine, Empresa installs on both Unix-based and Windows web servers, and enables them to run MivaScript-based web applications. Applications running under Empresa, such as Miva Merchant, are execute in a sandboxed data and runtime environment. Special virtual domain and shared server features let busy site administrators create per user and per domain environments. For more information about Empresa, [Click Here](http://www.mivascript.com/topic/empresa.html)

#### Key Empresa benefits

* An integrated, SQL-based data system, with cross-platform database and index support.
* Multiple database scheme interfacing, with support for MivaSQL, MySQL and xBase3.
* Commerce library functions allowing direct communication with remote services.
* Site-specific and server-wide administration and configuration options.
* Cross-platform capabilities, allowing it to run across different server interfaces and operating systems.

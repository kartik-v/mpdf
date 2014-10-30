mpdf
====

This is a fork of the [mPDF library](http://mpdf1.com/) that adds composer and packagist support. It also modifies the library to offer
Bootstrap CSS styling by default.

Why this repo?
--------------

I needed this for building many of my dependent PHP based projects that use this wonderful PDF library. Managing package dependencies via a central repository was important for folks like me. I use composer to manage package dependencies via packages on packagist.org.
In addition, if you are a user who works with the Bootstrap CSS framework like me, the default styling needed to be changed. So the minor changes from the official mPDF library are:

- Added ability to update library and manage dependencies via composer 
- Uses the latest development version (v6.0beta) of the mPDF library. I needed the latest development version via composer, which was not found elsewhere.
- The default mPDF.css contains v3.2.0 of the bootstrap css. 

Installation
------------
The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
$ php composer.phar require kartik-v/mpdf "dev-master"
```

or add

```
"kartik-v/mpdf": "dev-master"
```

to the ```require``` section of your `composer.json` file.

Refer the [readme instructions](https://github.com/kartik-v/mpdf/blob/master/README.txt) for other details on setting up the extension.


Usage
-----

PHP 5.4 and later can use namespaces to access. Refer the [official documentation manual](http://mpdf1.com/manual/index.php) at the [mpdf1 site](http://mpdf1.com) for further details and understanding of the library.

```php
use \mPDF;

$pdf = new mPDF();
```
mpdf
====

This is a fork of the [mPDF library](http://mpdf1.com/). mPDF is a PHP class which generates PDF files from UTF-8 encoded HTML. It is based on [FPDF](http://www.fpdf.org/) and [HTML2FPDF](http://html2fpdf.sourceforge.net/), with a number of enhancements.
It is slower than the original scripts e.g. HTML2FPDF and produces larger files when using Unicode fonts, but support for CSS styles etc. has been much enhanced.

See the [features](http://mpdf.bpm1.com/index.php?page=Features) and/or [examples](http://www.mpdf1.com/mpdf/index.php?page=Examples).

This fork adds composer and packagist support.

Why this repo?
--------------

I needed this for building many of my dependent PHP based projects that use this wonderful PDF library. Managing package dependencies via a central repository was important for folks like me. I use composer to manage package dependencies via packages on packagist.org.

- Added ability to update library and manage dependencies via composer 
- Uses the latest development version (v6.0beta) of the mPDF library. I needed the latest development version via composer, which was not found elsewhere.

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
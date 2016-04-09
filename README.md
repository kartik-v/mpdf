mpdf
====

[![Latest Stable Version](https://poser.pugx.org/kartik-v/mpdf/v/stable)](https://packagist.org/packages/kartik-v/mpdf)
[![License](https://poser.pugx.org/kartik-v/mpdf/license)](https://packagist.org/packages/kartik-v/mpdf)
[![Total Downloads](https://poser.pugx.org/kartik-v/mpdf/downloads)](https://packagist.org/packages/kartik-v/mpdf)
[![Monthly Downloads](https://poser.pugx.org/kartik-v/mpdf/d/monthly)](https://packagist.org/packages/kartik-v/mpdf)
[![Daily Downloads](https://poser.pugx.org/kartik-v/mpdf/d/daily)](https://packagist.org/packages/kartik-v/mpdf)

---

### Use the [mpdf/mpdf](https://github.com/mpdf/mpdf) repo instead

> Effective 08-Apr-2016, I am redirecting and encouraging folks to use the above repo - to ensure a single codebase for mpdf management in future. This repo was initially created since there was no other package having the 6.x release that could be installed via composer. For folks coming over from Yii, note that the [yii2-mpdf extension](https://github.com/kartik-v/yii2-mpdf) has been modified to use the [mpdf/mpdf](https://github.com/mpdf/mpdf) repo

---

This is a fork of the [mPDF library](http://mpdf1.com/). mPDF is a PHP class which generates PDF files from UTF-8 encoded HTML. It is based on [FPDF](http://www.fpdf.org/) and [HTML2FPDF](http://html2fpdf.sourceforge.net/), with a number of enhancements.
It is slower than the original scripts e.g. HTML2FPDF and produces larger files when using Unicode fonts, but support for CSS styles etc. has been much enhanced.

This fork adds composer and packagist support.

Why this repo?
--------------

I needed this for building many of my dependent PHP based projects that use this wonderful PDF library. Managing package dependencies via a central repository was important for folks like me. I use composer to manage package dependencies via packages on packagist.org. This repository allows access to some specific features and needs:

1. Adds ability to update library and manage dependencies via composer in your PHP based applications
2. Uses the latest development version (v6.0beta) of the mPDF library. I needed the latest development version via composer, which was not found elsewhere. mPDF 6.0 can utilise OpenType layout tables to display complex scripts. It will be of most interest to those wishing to use Arabic or Indic scripts (as well as Khmer, Lao, Myanmar etc.). It will  also improve the display of Thai, Vietnamese and Hebrew.
3. This beta release (v6.0) contains fonts (open source) to cover almost every imaginable script / language. It also includes additional fonts for Chinese, Japanese, and Korean.

Installation
------------
The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
$ php composer.phar require mpdf/mpdf "@dev"
```

or add

```
"mpdf/mpdf": "@dev"
```

to the ```require``` section of your `composer.json` file.

Refer the [readme instructions](https://github.com/mpdf/mpdf/blob/master/README.txt) for other details on setting up the extension.


Usage
-----

PHP 5.4 and later can use namespaces to access. Refer the [documentation manual](https://mpdf.github.io) or the [upstream mpdf site](http://mpdf1.com) for further details and understanding of the library.

```php
use \mPDF;

$pdf = new mPDF();
```

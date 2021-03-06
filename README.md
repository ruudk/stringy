Stringy - Object Oriented Manipulation of Strings in PHP!
=========================================================

[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/mpclarkson/stringy/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/mpclarkson/stringy/?branch=master)
[![Build Status](https://travis-ci.org/mpclarkson/stringy.svg?branch=master)](https://travis-ci.org/mpclarkson/stringy)

Overview
--------

Are you stick to death of PHP's inconsistencies in terms on manipulating strings? Well, look no further!

Rather than constantly having to write obtuse code like this to check if a string contains a substring:

```  php
  strpos($mystring, $substring) !== false ? true : false;

```

You can now do this (and many other things), sensibly!

``` php
  $string = new String($myString);

  $bool = $string->contains($substring);

```

Yay! :)

Usage
------------

After applying any methods, the underlying text/string can be accessed as follows:

```php
$stringy = new Stringy("mystring");
stringy->append("is fun", " ");

echo $stringy->string();
//"mystring is fun";

```

Methods
------------

Method | Parameters | Returns
--- | --- | ---
string | nil | string
truncate | $chars = 50, $appendWith = "..." | $this
length | nil | int
contains | $substring | bool
startsWith | $substring | bool
endsWith | $substring | bool
append | $string | $this
reverse | nil | $this
uppercase | nil | $this
uppercaseFirst | nil | $this
lowercase | nil | $this
lowercaseFirst | nil | $this
titleCase | nil | $this
sentenceCase | nil | $this
toArray | $delimiter = null | array
apply | callback | $this

Checkout the tests for examples of each method.

Requirements
------------

  * PHP 5.4+


Composer
---------

Use [Composer](https://getcomposer.org) by adding the following lines in your `composer.json`:

```json

    "require": {
        "mpclarkson/stringy": "dev-master"
    },

```

Todos
-----

  * More methods
  * Contributions welcome


Credits
-----

This has been inspired by the beautify string manipulation in Apple's Swift language.

Thanks goes to [Hilenium](http://hilenium.com).

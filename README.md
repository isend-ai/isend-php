# iSend PHP Bindings
The iSend PHP library provides convenient access to the iSend API from applications written in the PHP language. It includes a pre-defined set of classes for API resources that initialize themselves dynamically from API responses which makes it compatible with a wide range of versions of the iSend API.

## Requirements

PHP 5.6.0 and later.

## Composer

You can install the bindings via [Composer](http://getcomposer.org/). Run the following command:

```bash
composer require isend-ai/isend-php
```

To use the bindings, use Composer's [autoload](https://getcomposer.org/doc/01-basic-usage.md#autoloading):

```php
require_once 'vendor/autoload.php';
```

## Manual Installation

If you do not wish to use Composer, you can download the [latest release](https://github.com/isend-ai/isend-php/releases). Then, to use the bindings, include the `init.php` file.

```php
require_once '/path/to/isend-php/init.php';
```

## Dependencies

The bindings require the following extensions in order to work properly:

-   [`curl`](https://secure.php.net/manual/en/book.curl.php), although you can use your own non-cURL client if you prefer
-   [`json`](https://secure.php.net/manual/en/book.json.php)
-   [`mbstring`](https://secure.php.net/manual/en/book.mbstring.php) (Multibyte String)

If you use Composer, these dependencies should be handled automatically. If you install manually, you'll want to make sure that these extensions are available.

## Getting Started

Simple usage looks like:

```php
$is = new iSend('is_test_BQokikJOvBiI2HlWgH4olfQ2');
$email = $is->emails->send([
    'to' => 'hi@isend.ai',
    'subject' => 'Welcome to iSend',
    'body' => 'Welcome Test Send Email',
]);
echo $email;
```

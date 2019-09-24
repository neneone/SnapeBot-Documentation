---
title: Installation
description: Requirements and installation for SnapeBot
---
# Requirements

To properly run SnapeBot you need `PHP >= 7.1` and the `pdo`, `pdo-mysql`, `mbstring`, `curl` and `json` extensions.

They are often preinstalled, but if they are not, you'll have to install them.

# Installation

There are two ways to install SnapeBot:

* [Using PHAR (highly recommended)](installation.md#simple)
* [Using composer](installation.md#composer)

## Simple

It's very easy to install, use and update SnapeBot using the PHAR archive.

**You don't even need Composer**, and this method can be applyed on webhosts.

To install SnapeBot via PHAR, simply download [this file](https://neneone.xyz/SnapeBot/loadSnapeBot.php) and require it in your `index.php` as the following.

```php
require_once __DIR__.'/loadSnapeBot.php';
```

## Composer

It's very easy to install, use and update SnapeBot using composer too.

You can install SnapeBot using the following command:

```
echo '{}' > composer.json && composer config minimum-stability dev && composer require neneone/snapebot
```

then `require 'vendor/autoload.php'` in your `index.php` file.

[Next section](update.md)

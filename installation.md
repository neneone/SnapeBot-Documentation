---
title: Installation
description: Requirements and installation for SnapeBot
---
# Requirements

To properly run SnapeBot you need `PHP >= 7.2` and the `pdo`, `pdo-mysql`, `mbstring` and `curl` extensions.

They are often preinstalled, but if they are not, you'll have to install them.

_Please note that SnapeBot **could** be compatible with other PHP versions, but I haven't tested it so I cannot ensure the compatibility_


# Installation

There are two ways to install SnapeBot:

* [Using composer (highly recommended)](installation.md#composer)
* [Using `semiAutoloader.php`](installation.md#semiautoloader)


## Composer

It's very easy to install, require and update SnapeBot using composer.

You can install SnapeBot using the following command:

```
echo '{}' > composer.json && composer config minimum-stability dev && composer require neneone/snapebot
```

then `require 'vendor/autoload.php'` in your `index.php` file.


## semiAutoloader

It's not recommended at all to use this method, because it's pretty unstable, difficult to update and maybe it will be deprecated in the future.

To install SnapeBot with this method, run the following command:

```
git clone https://github.com/neneone/SnapeBot BOT_DIRECTORY
```

where `BOT_DIRECTORY` is the **empty** directory where you want to install SnapeBot.

Then require `semiAutoloader.php` in your `index.php` file.

[Next section](update.md)

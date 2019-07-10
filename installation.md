---
title: Installation
description: Requirements and installation for SnapeBot
---
# Requirements

To properly run SnapeBot you need `PHP >= 7.3` and the `pdo`, `pdo-mysql`, `mbstring` and `curl` extensions.

They are often preinstalled, but if they are not, you'll have to install them.


# Installation

There are two ways to install SnapeBot:

* [Using composer (highly recommended)](https://snapebot.neneone.cf/installation.html#composer)
* [Using `semiAutoloader.php`](https://snapebot.neneone.cf/installation.html#semiautoloader)


## Composer

It's very easy to install, require and update SnapeBot using composer; you can do it automatically using the following command:

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

[Next section](https://snapebot.neneone.cf/update.html)

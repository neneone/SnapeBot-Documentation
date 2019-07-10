---
title: Updating SnapeBot
description: How to update SnapeBot
---
# Updating

You have to update SnapeBot using the method you used to install it, so here are the methods to update it using composer and semiAutoloader.

## Composer

It's really easy to update SnapeBot using composer; just run the following command:

```
composer update
```


## semiAutoloader

`semiAutoloader.php` installation uses git, so you'll have to run this command to update SnapeBot:

```
git reset --hard HEAD && git pull
```


[Next section](settings.md)

---
title: Using BotAPI Methods
description: How to use all Bot API methods with SnapeBot
---
# Methods support

SnapeBot supports all the current BotAPI methods, and whenever a BotAPI updates comes out, it gets updated in a few days.

To know the parameters that these methods require, refer to the official [Bot API Documentation](https://core.telegram.org/bots/api).

# How to

To use a BotAPI method just write `$SnapeBot->BotAPI->methodName($param1, $param2);`.

You can also use an array containing the parameters: `$SnapeBot->BotAPI->methodName([$param1, $param2]);`.

[Next section](variables.md)

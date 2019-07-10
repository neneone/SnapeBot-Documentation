---
title: Understanding variables
description: A simple guide to understand SnapeBot's variables.
---
# Understanding variables

To have a complete knowledge of SnapeBot's variables you should have a look at [`variablesMaker.php`](https://github.com/neneone/SnapeBot/blob/master/src/VariablesMaker.php) file of the source code.

It works in the following way:

* When the bot receives an update, the function `makeVariables` is called.
* That function checks the type of the update and calls the `setMainUPDATE_TYPEData`, where `UPDATE_TYPE` is the update type.
* That function calls the `parseUPDATE_TYPE` function that parses all the update and that returns its value.
* Then all of the `$updateType->data` becomes `$SnapeBot->data`.

I know it looks pretty difficult to understand, but maybe it'll be clearer with the following example.

e.g.:

The user `@Nen3one`, with user ID `304949284`, sends the message `/start` to the bot.

`$SnapeBot->username` becomes `@Nen3one`

`$SnapeBot->userID` becomes `304949284`

`$SnapeBot->msg` becomes `/start`

and so on.

The name of the variables are in the [`variablesMaker.php`](https://github.com/neneone/SnapeBot/blob/master/src/VariablesMaker.php) file of the source code.

[Next section](database.md)

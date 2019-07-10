---
title: keyboard
description: keyboard API method
---
# API keyboard method

This method sends an `answerCallbackQuery` and, if set, an `editMessageText` query. You can use this to edit the keyboard, too.

| Parameter | Description | Required |
|-----------|-------------|----------|
|alert|"Notifiaction" to show when the button is clicked. Can be `''`|false|
|new text|New text to set. Can also be `''` and `false`|false|
|new menu|New inline menu. Can be `false`|false|
|alert click|Should the user need to click "Ok" when receives the notification? Default is `false`|false|

You can have an example for this method [here](https://github.com/neneone/SnapeBot/blob/master/Examples/simpleBot/botCommands.php).

[Back to the methods list](methods.md)

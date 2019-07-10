---
title: sendMessage
description: sendMessage API methods
---
# API sendMessage method

This method sends a message, with an easy-to-use keyboard parameter to send normal keyboards, inline keyboards or hide an inline keyboard.

| Parameter | Description | Required |
|-----------|-------------|----------|
|chatID|The chatID to send the message.|true|
|text|The message to send|true|
|keyboard|An inline or normal keyboard to send or the `hide` string to hide a normal keyboard|false|
|keyboard type|Can be `inline`, `hide` or anything else for a normal keyboard. Default is `inline`.|false|
|disable notification|Disable notification for this message? Default is `false`|false|

You can have an example for this method [here](https://github.com/neneone/SnapeBot/blob/master/Examples/simpleBot/botCommands.php).

[Back to the methods list](methods.md)

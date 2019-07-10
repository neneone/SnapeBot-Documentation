---
title: How to use SnapeBot
description: An easy guide to learn how to use SnapeBot
---
# How to use SnapeBot

SnapeBot is really easy to use once you have understood how to do it. Here is a little guide to learn how to use SnapeBot.

## $SnapeBot structure

A SnapeBot, technically `\neneone\SnapeBot\SnapeBot` is structured in the following way:

* `$SnapeBot->settings` is an array that contains the settings.
* `$SnapeBot->BotAPI` is an instance of `\neneone\SnapeBot\BotAPI`, a class that contains all of the Bot API methods (I'll spend more words about it later).
* `$SnapeBot->API` is an instance of `\neneone\SnapeBot\API`, a class that contains some handy functions to interact with the Bot API ([read more](API/methods.md)).
* `$SnapeBot->botToken` contains the Bot Token.
* `$SnapeBot->botInformations` contains the result of `getMe`. It's set only if [getBotInformations](settings.md#getbotinformations) setting is `true`.
* `$SnapeBot->db` is the PDO database connection.

Additionally, you can find variables at `$SnapeBot->variableName` following [this explanation](variables.md).

When creating a bot, I suggest you to create different files for a better legibility, but in this example I'll put all in one single file. You can find multifiles examples in the [Examples](https://github.com/neneone/SnapeBot/tree/master/Examples) folder.

```php
require_once __DIR__.'/vendor/autoload.php';
# Use the following line if you've installed SnapeBot with semiAutoloader.php
# require_once __DIR__.'/semiAutoloader.php';

$settings = [
  'database' => [
    'host' => 'localhost',
    'dbName' => 'myAwesomeDatabase',
    'username' => 'root',
    'password' => 'MyAwesomePassword',
    'tableName' => 'MyAwesomeBot',
  ],
  'botUsername' => 'myAwesomeBot',
  'firstRun' => false,
];

$update = json_decode(file_get_contents('php://input'), true); #Get the update
$bot = new \neneone\SnapeBot\SnapeBot('Bot Token', $update, $settings); #Create an instance of SnapeBot

if (isset($bot->msg) && $bot->msg == '/start') { #Check if there is a message, and if it's "/start"
    $bot->API->sendMessage($bot->chatID, 'Hello World!'); #Send the "Hello Wolrd!" message
}
```

This examples creates a bot that, when the `/start` command is sent, says `Hello World!`.

[Next section](variables.md)

---
title: SnapeBot's Settings
description: How to manage settings
---
# Settings

SnapeBot's settings schema is stored in `$SnapeBot::$settingsSchema`. When you create an instance of `\neneone\SnapeBot\SnapeBot` passing the settings, it automatically builds them setting default values when there is a setting that you haven't passed and that has a default value.

A required setting is a setting that hasn't a default value, so **you must specify his value**. If you don't, an Exception will be thrown.

You can edit the settings during the script execution, just edit `$SnapeBot->settings` array.

Here are all the settings, based on the default settings schema.

### getBotInformations

| Name | Type | Description | Default | Required |
|------|------|-------------|---------|----------|
|getBotInformations|boolean|If enabled, SnapeBot will call the `getMe` method and store its result in `$SnapeBot->botInformations`|false|false|

_Note that if there is no [`botUsername`](#botusername) this setting will be automatically enabled._


### botUsername

| Name | Type | Description | Default | Required |
|------|------|-------------|---------|----------|
|botUsername|string|The bot's username. Set it here for better speed.|false|false|

_Note that if there is no [`botUsername`](#botusername) [`getBotInformations`](#getbotinformations) will be automatically enabled._


### firstRun

| Name | Type | Description | Default | Required |
|------|------|-------------|---------|----------|
|firstRun|boolean|This is needed to be true only the first time you run the script, then you can turn it off for better speed.|true|false|


### autoSaveUsers

| Name | Type | Description | Default | Required |
|------|------|-------------|---------|----------|
|autoSaveUsers|boolean|Should the bot automatically save users into the database?|true|false|


### cbDataEncryption

| Name | Type | Description | Default | Required |
|------|------|-------------|---------|----------|
|cbDataEncryption|boolean|Should the bot encrypt callbackdatas?|false|false|

_[Read more](advanced/callbackDataEncryption.md)_


### encryptionData

| Name | Type | Description | Default | Required |
|------|------|-------------|---------|----------|
|encryptionData|array|Data for `specialEncrypt` and `specialDecrypt`, used also to encrypt callbackdatas.|down here|false|

#### Default:

| Name | Value |
|------|-------|
|key|SnapeBotKey2019|
|iv|SnapeBotAwesomeIV2019|

#### Structure:

| Name | Type | Description | Default | Required |
|------|------|-------------|---------|----------|
|key|string|The key for encryption|SnapeBotKey2019|false|
|iv|string|The IV for encryption|SnapeBotAwesomeIV2019|false|

_Note that if you really want to encrypt your callbackdatas **you must change** these values, otherwise everyone who understands you're using SnapeBot will be able to decrypt your callbackdatas._


### database

| Name | Type | Description | Required |
|------|------|-------------|---------|
|database|array|Database data to connect to the database|true|

#### Structure:

| Name | Type | Description | Default | Required |
|------|------|-------------|---------|----------|
|host|string|The host for the database connection|localhost|false|
|dbName|string|The database name||true|
|username|string|The username for the database connection||true|
|password|string|The password for the database connection|''|false|
|tableName|string|The table's name to create and/or to use|snapeBot|false|

_Note: I recommend to pay attention when passing database settings to SnapeBot 'cause you probably want to change also settings that have a default value._

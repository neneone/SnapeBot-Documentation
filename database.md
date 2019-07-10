---
title: SnapeBot's database
description: How to use the database
---
# SnapeBot's database

Here is an overview of how to use SnapeBot's database an the built-in functions.

## Connecting to the database

SnapeBot automatically connects to the database using PDO with the informations provided in the [database settings](settings.md#database).

The connection is stored in `$SnapeBot->db` so, for a query, you have to write `$SnapeBot->db->query('YOUR SQL');`.

## Database table

SnapeBot will automatically create a table too, named with the `tableName` you provided in the settings. For convenience, you can find the table name in `$SnapeBot->tName` too.

### Table structure

SnapeBot's table has the following structure:

| Field | Description |
|-------|-------------|
|ID|It's an autoincremented value that can be useful for some queries|
|userID|User's telegram ID|
|name|User's name|
|username|User's username|
|page|You can change it to store some temporary data about the users (e.g. if the user's going to send a message that the bot has to forward).|
|lastUpdate|Human-redeable date. The last time the bot updated the user's data in the database.|

## Users in the database

If the `autoAddUsers` setting is set to `true` (default), the following users' your bot meets data is stored in the database: `username`, `userID`, `name`.

If the user's already present in the database and the last time the bot updated his data is <= yesterday, the bot will update it.

## Handy functions to manage users

These functions are in `$SnapeBot->functionName()`.

### checkUserInDatabase

Checks if a user is in the database. If not, it adds him. If yes, it checks the last update time and, if it's <= yesterday, it updates the user's data.

| Parameter | Type | Description | Required |
|-----------|------|-------------|----------|
|userID|int|User's ID|true|
|name|string|User's name|true|
|username|string|User's username. Can be empty|false|

Returns the users data in the database (e.g `['ID' => 1, 'userID' => 289392, 'name' => 'Enea Dolcini', 'username' => 'Nen3one', 'page' = >'']`).


### addUserToDatabase

Adds a user to database, without checking if it exists or not.

| Parameter | Type | Description | Required |
|-----------|------|-------------|----------|
|userID|int|User's ID|true|
|name|string|User's name|true|
|username|string|User's username|true|


### updateUserInDatabase

Updates an user in the database, without checking `lastUpdate`.

| Parameter | Type | Description | Required |
|-----------|------|-------------|----------|
|userID|int|User's ID|true|
|name|string|User's name|true|
|username|string|User's username|true|

[Next section](API/methods.md)

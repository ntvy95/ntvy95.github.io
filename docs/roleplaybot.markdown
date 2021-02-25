---
layout: page
title: Roleplay bot on Discord
permalink: /discord/roleplay
---

This Roleplay bot on Discord can help you to keep track the interaction messages between players' characters. It is possible that you might run into some bugs and the bot may get offline for a while to fix the bugs. Due to the fact that I'm a poor student, I'm not sure if it's possible for me to keep this bot online for a possible huge number of requests. But let's see if this bot is of any use first.

Invitation link: [Click here](https://discord.com/api/oauth2/authorize?client_id=813439995519041586&permissions=519232&scope=bot)

![Example]({{ site.baseurl }}/images/roleplaybot.png "An example of Roleplay bot's usage.")

## Usage

### Game master

Firstly, you need to [create a new role in Server Settings](https://www.techjunkie.com/add-delete-roles-discord/#How_to_Create_Roles_in_Discord) and then run the below command to set that role the game master role on your server:

`!arp set role GM <your role name>`

Then you can check which characters on the server are waiting for your approval by the command:

`!arp show character to approve`

You can approve the most recently created characters by:

`!arp approve character recent <a number>`

You can only approve 10 most recently created characters at maximum due to the possible computational constraints.

Or you can approve a specific character by:

`!arp approve character <a character name>`

You can show which characters needing your approval by:

`!arp show character to approve`

Of course, you can undo your approval by:

`!arp unapprove character <a character name>`

### Player

#### Character

You should first create a character by sending a message whose first line should be:

`!prp create character <your character name>`

The next lines of the message should be used to describe your character. These lines will not be stored in the system's database.

You can edit your character name in the system by simply editing the message and replace the old character name with the new character name at the position of `<your character name>`.

You can remove the character from the database by simply deleting the message.

Your characters must be approved by the game master before being used in an interaction.

#### Interaction

An interaction is a series of messages which involves some characters. It is usually a continuous conversation between characters.

You can start an interaction by sending this short message:

    !prp init interaction
    Character: <character 1>, <character 2>, ... , <character n>
    Role: <Role 1>, <Role 2>, ... , <Role n>
    Your brief descriptiion about the interaction, e.g. the interaction time.

Then you can reply to the above message, insert the command "!prp" at the beginning of your reply message and then start your first interaction message. Other people can continue the interaction by replying to one of your interaction messages.

An interaction can contain up to 10 characters due to the possible computational constraints.

## FAQ

1. What kind of data will you collect and store on your database?

Guild ID, message ID, channel ID, user ID, role ID, and character names (which are registered by the players).



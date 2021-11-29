---
tags: bot-version/5.1.0beta
---

# Modules
Chuckster consists of modules, which can be enabled/disabled per server. Using the `/help` command, you can see the names of all modules, and whether they are enabled, disabled, or premium only. Premium modules are a work in progress and may be locked behind a paywall in the future.

The help command should look similar to this:

![[helpCommandExample.png]]

## List of Modules
- [[Events]] - Create events other users can join. Comes with notifications, timezone support, and event organisation.
- [[Plan]] - Find common time ranges between people for event planning. Works with timezones and find the longest shared time range between all users.
- [[Poll]] - Create fully customisable polls which other people can vote on.
- [[Roles]] - Create interractive messages which allow users to select a list of roles.
- [[Twitter Game]] - Fun game where you and your friends try to guess who sent to displayed tweet.

### Module Command Formatting
Module command parameters will be formatted as the following:

```ad-param
title: Example of a required parameter
```

```ad-paramop
title: Example of an optional parameter
```

The icon determines what type of data should be entered:

```ad-param
title: Integer
icon: hashtag
```

```ad-param
title: String
icon: font
```

## Enabling Modules
To enable a module on your server, and administrator must use the `/enablemodule` command. When selected, you will see a list of modules you are allowed to enable. Select one and send the command to instantly enable the module in your server.

## Disabling Modules
This is the same as [enabling modules](Modules.md#Enabling%20Modules), just with the `/disablemodule` command.
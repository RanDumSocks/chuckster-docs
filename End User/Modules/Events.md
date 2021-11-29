---
tags: bot-version/5.1.0beta, WIP
---

%%
- [ ] example of an event listing and all the elements labeled
- [ ] Element descriptions and images
	- [ ] Button descriptions on events
%%

```toc
max_depth: 3
```

# Events module
This was the main module for the creation of Chuckster. This makes setting and joining events easy for people in all parts of the world, as it takes timezones into account.

## Quick Start
In order to use this module to the fullest, you first must set your timezone. use the `/events setzone` command to do this. Using this command on its own will prompt you to go to a specific website and copy/paste the timezone string into the command as the optional parameter.

Once that is correctly set, you can now create an event with `/events create` which will ask for time and title information for the event you want to create.

![[eventsCreateExample.png]]

Notifications will go off a day before the event begins, and again an hour before the event. You will also be notified with more information about the event when it occurs.

```ad-warning
Subscribers and event creators must have direct messages from server members from at least one server Chuckster is in to see notifications.
```

<hr>

## Commands

<hr>

### create
Creates and event and posts it to the channel the event was created in, allowing users to subscribe to it.

#### Parameters

```ad-param
title: `year`
icon: hashtag
collapse:

**Description**
Year of the event.

**Restrictions**
All 4 digits of the year
```

```ad-param
title: `month`
icon: hashtag
collapse:

**Description**
Month of the event.

**Restrictions**
1-12
```

```ad-param
title: `day`
icon: hashtag
collapse:

**Description**
Day of the event.

**Restrictions**
1-31
```

```ad-param
title: `hour`
icon: hashtag
collapse:

**Description**
Hour of the event.

**Restrictions**
0-23
Must be 24 hour time format
```

```ad-param
title: `minute`
icon: hashtag
collapse:

**Description**
Minute of the event.

**Restrictions**
0-59
```

```ad-param
title: `title`
icon: font
collapse:

**Description**
Name of the event
```

```ad-paramop
title: `description`
icon: font
collapse:

**Description**
Description of the event
```

```ad-paramop
title: `startmessage`
icon: font
collapse:

**Description**
Message that displays to everyone who enabled notifications for the event. They will not see this until the event starts.
This can be used for invite links that event subscribers can only click on when the event starts.
```

```ad-paramop
title: `imageurl`
icon: font
collapse:

**Description**
Image link displayed with the event.

**Restrictions**
Must be a valid URL.
~~~regex
/https?:\/\/(www\.)?[-a-zA-Z0-9@:%._\+~#=]{2,256}\.[a-z]{2,4}\b([-a-zA-Z0-9@:%_\+.~#?&//=]*)
~~~
```

<hr>

### list
Lists all events you are subscribed to and created.
From here you can select any of these events, view more info about them, and post them in the current channel.

#### Parameters

```ad-paramop
title: `page`
icon: hashtag
collapse:

**Description**
If there are more than 25 events in one category, select the page here.

**Restrictions**
Must be a number between the minimum and maximum page count, inclusive.
```

<hr>
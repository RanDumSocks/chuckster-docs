---
tags: version/5.1.0beta
---

# Permissions
Module permissions are set but admins using the `/whitelist` command. Whitelist command structure is as follows:

```
/whitelist [module] [operation] [role] [channel] [user]
```

Technically, all parameters are optional. Leaving out all parameters shows the whitelist settings for all modules in the current server. Leaving out all but the `module` parameter shows the whitelist settings for the specified module.

```ad-example
title: Showing whitelist settings
collapse:

To show all whitelist options for all modules in a server:
~~~
/whitelist
~~~

To show whitelist for events module:
~~~
/whitelist module:events
~~~

```

The last 3 parameters are only used when using the `add` and `remove` operations.

If *any* of the conditions for a whitelist are met, the command succeeds, else it sends an error message to the user.

```ad-example
title: Example usage
collapse:

Say I only want people with the `@Event Planner` role to create events on a server.
I also want user `@Example User` to be able to create events anywhere regardless if they have the `@Event Planner` role.

~~~
/whitelist module:events operation:add role:@Event Planner user:@Example User

/whitelist module:events operation:enable
~~~

Discord and Chuckster should help auto-fill most of these parameters.

```

One exception for setting permissions is the 'all' module, which you will see in the suggestions for the 'operation' parameter. Rules set on this will propegate through all module rules. This means, all other modules rules effectively inherit the rules of 'all'.

```ad-example
title: 'all' module explaination
collapse:

Say a rule was set on 'all', and it is role `@bot admin`.
This means that anyone with the `@bot admin` role will be able to use any command on any module regardless of individual module rules.

```

## Operations

### `add`
Adds a rule to the whitelist.
Must specify at least one of `role`, `channel`, or `user` parameters.

```ad-bug
You can add multiple of the same channel, role, or user to a whitelist. Doing so just means you have to run the `remove` command multiple times to remove a given rule.
```

### `remove`
Removes a rule from the whitelist.
Must specify at least one of `role`, `channel`, or `user` parameters.

### `disable`
Disables whitelist for given module.

### `enable`
Enables whitelist for given module.

### `clear`
Clears all whitelist rules.

```ad-warning
This also disables the whitelist, effectively opening permissions to all users if the module is enabled on the server.
```

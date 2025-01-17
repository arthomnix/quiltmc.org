---
permalink: /usage/troubleshooting
title: Troubleshooting
description: How to troubleshoot Quilt when there's an issue
redirect-from:
- /troubleshooting.html
---

{% admonition %}

## Why am I getting an "Incompatible mod set!" error?

There are a few versions of this error, but they all ultimately mean the same thing: You're missing something another mod
needs to work, or your mods are incompatible with each other.

**Note:** We understand that these error pop-ups are ugly, difficult to read and extremely confusing. While we haven't
had time to fix this in time for our first beta, we are planning on solving this problem and providing something that
everyone can understand.

### Missing dependency

The following errors mean you're missing the [Quilt Standard Libraries](https://modrinth.com/mod/qsl) -- please download
them and add them to your `mods` folder or launcher mod list.

* Dependency for mod 'mod-id' on fabric versions ...
* Dependency for mod 'mod-id' on quilt_ ...

Any other dependencies listed similarly are other mods, and you'll need to download them separately and add them to 
your `mods` folder or launcher mod list.

### Incompatible mod versions

If the error specifies that a mod exists but isn't valid for resolution, you have incompatible mod versions. You'll 
need to double-check that all your mods are up-to-date and, if they are, contact the developers behind the mods that
are causing problems.

### Jar-in-jar resolution error

![JiJ resolution error](/assets/img/misc/jij-resolution-error.png)

If the error you're getting looks something like this, then this is a problem with a mod you're using -- you should 
report it to that mod's developers. The mod you're looking for in this example has been circled in red above for 
clarity -- in this case, the mod would be QuickCarpet.

{% endadmonition %}
{% admonition %}

## My game is crashing. Why is this happening?

If your game is crashing, the most likely cause is a problem with a mod you have installed. It's always worth trying
to figure out if this is the case, and you can attempt to do so by following these steps:

1. First, take a look at your `latest.log` - you can find this in the `logs/` folder located within your Minecraft
   profile, which will likely be in your `.minecraft/` by default.
2. If you notice errors in your log referring to a specific mod, try removing it and see whether you can reproduce the
   error.
3. You could also try using a binary search to track down a misbehaving mod - move half of your mods to another folder,
   and test the other half. If there's no issue in that half, switch to the other one. Continue to split your mods in
   half and test each half until you've managed to isolate the problematic mod.

If this doesn't help, or you have trouble reading the logs on your own, please feel free to drop into the
`#quilt-support` channel on [The Quilt Community Discord server](https://discord.quiltmc.org), and we'll try to
help you out. **Please remember to provide your `latest.log` and any other relevant issue when requesting support!**

{% endadmonition %}

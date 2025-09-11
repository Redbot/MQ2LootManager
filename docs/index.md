---
tags:
  - plugin
---

# MQ2LootManager

<!--desc-start-->
This simple loot manager will use EQ's built in Advanced Loot Window to decide how to handle loot.
<!--desc-end-->

## Commands

<a href="cmd-lootmanager/">
{% 
  include-markdown "plugins/community-plugins/mq2lootmanager/cmd-lootmanager.md" 
  start="<!--cmd-syntax-start-->" 
  end="<!--cmd-syntax-end-->" 
%}
</a>
:    {% include-markdown "plugins/community-plugins/mq2lootmanager/cmd-lootmanager.md" 
        start="<!--cmd-desc-start-->" 
        end="<!--cmd-desc-end-->" 
        trailing-newlines=false 
     %} {{ readMore('plugins/community-plugins/mq2lootmanager/cmd-lootmanager.md') }}

## Settings

There's no configuration file and none needed.

## Overview

Here's how MQ2LootManager handles loot. It should be noted that anytime "do nothing" is listed, it will defer to an EverQuest setting if available.

**Loot handling when in a group**

| EverQuest Setting | Personal Loot (top) | Shared Loot (bottom) | Personal Loot (<span class="accent">Not master looter</span>) |
|-------------------|---------------------|----------------------|-----------------------------------------------------------|
| Default | Do nothing | Do nothing | Loot |
| Need | Do nothing | Give to you | Do nothing |
| Greed | Do nothing | Give to you | Do nothing |
| Roll | Do nothing | Roll | Do nothing |
| Never | Do nothing | Leave on corpse | Do nothing |

In all other situations, it will await for the user to make a decision or manually handle the item.

This is most definitely not as feature rich as MQ2AutoLoot, but there is already an interface for handling loot in everquest. So why not use it?
Sure, it won't automatically distribute items to group members based on a predefined number of quest items set by the user.
But it also won't automatically give yourself any No Drop items because the default action is keep. The default action is Do NOTHING
(unless you're in a group, not the master looter, and an item has gone to your personal loot list.)

Meaning you can set it to do nothing, which allows you to manually distribute nodrop items, or handle any number of quest items manually.
Is this ideal? Perhaps not for you, but it works great for me.

## Acknowledgement

I did poke Plure's logic with a stick to get me going in the right direction. Thanx to you sir.
To be clear, I'm not saying there is anything wrong with MQ2Autoloot I have just always handled my loot like this with a personal macro.
This plugin might not be for everyone. It's very simplistic but it's how I've been doing it for a while. I decided to stop using a macro to handle it and make it a plugin so I don't have to remember to start it.
Plus, this way you can use it too if you choose.
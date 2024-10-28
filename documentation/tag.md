---
icon: tags
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Tag

## Definition

Tag system (not to be confused with Unity Tags) is essential to PAT. <mark style="color:orange;">**Action State’s transition logic is defined by Tags, and that creates a dynamic state machine system.**</mark> Beyond that, some other components also use Tags for communication purposes. For example, you can make a character invincible by granting it invincible Tag and Hurtbox will react to it.

All tags are stored inside a script named **GamePlayTag**, you may edit it on your own need. It is a huge enum. Every Tag is represented by a name and a number.&#x20;

Tags are toggled on the Action State component.

***

## Inspector

TODO






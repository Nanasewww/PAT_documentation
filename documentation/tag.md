---
icon: tag
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

T[ag system](#user-content-fn-1)[^1] is essential to PAT. <mark style="color:orange;">**Action State’s transition logic is defined by Tags, which creates a dynamic state machine system.**</mark> Beyond that, some other components also use Tags for communication purposes. For example, you can make a character invincible by granting it invincible Tag and [Hurtbox ](#user-content-fn-2)[^2]will react to it.

{% content-ref url="../tutorial/tag/create-a-new-tag.md" %}
[create-a-new-tag.md](../tutorial/tag/create-a-new-tag.md)
{% endcontent-ref %}

## Tag Container

At run time, Character will automatically add a Tag Container Component to itself. This stores all the Tags that a character is currently holding and is updated each frame. It is a very helpful tool for debugging if Tags were successfully granted.

TODO: PIC



[^1]: Not to be confused with Unity Tags

[^2]: Receiver on characters that receives from hitbox

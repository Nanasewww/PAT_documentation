---
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

# Step 5: State Modifiers

## Goal

* Understand State Modifiers

***

## Review

We have talked about Action States and Tags and chained States together, but the game feels wrong. We want a more precise control over the States, so there comes State Modifiers.

***

## State Modifier

<mark style="color:orange;">**State Modifiers**</mark> works with Action States to modify the action behaviors. They are triggered during the State they are attached to and grants different functionality to the State. For example, <mark style="color:orange;">controlling animations, activating hitboxes, modifying movement speed</mark>, etc. Action States by themselves only form a logic chain of your character, they need State Modifiers for different functions.&#x20;

Most modifier scripts are named as _**XXXMod**_, where <mark style="color:orange;">**Mod**</mark> stands for <mark style="color:orange;">**MODifier**</mark>. Each Modifier has a Begin and an End Timing Attribute, which defines when will this mod get activated, as well as the duration of it.

***

## Component

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfJHgu82STMVeajloMlYkejVXe7lKRJ7aoo5KXf1YRVYpuCvVazGJH3OTYHSdUV6TRtVnZwd59ig-clyJNm-aldzQ2kxuFa--xHXBb2SaA-JCIqfT3J9tRgL1Ua8dT87dJrHLGfUqNARC-oVloIHAOEWbIV?key=wjgYipemgHjXa5pb_ZH-6A" alt=""><figcaption><p>View of a basic State Modifier</p></figcaption></figure>

* **Mod Name**\
  A name for you to track what this modifier is for.
* **Timing Attribute**\
  Controls when this modifier will be activated. \
  There are two different Modes to select. You can find more details in [#timing-attribute](../../../documentation/actions/state-modifier.md#timing-attribute "mention").

{% hint style="warning" %}
_Animation Event requires modifying the animations, so let's use By Time in State for now._
{% endhint %}

### Events

Apart from the functionality of modifiers themselves, you can <mark style="color:orange;">**add additional functionality by using the begin & end unity event**</mark> exposed in the inspector. And a vanilla state modifier is solely for that. But be aware that Unity events are not easy to maintain and debug, please don’t use that for your core logic.

This is only a basic template of a State Modifier. It only triggers Unity Events. Given that Unity Events can be hard to handle, we allow you to extend from State Modifier and create your own modifiers. We also provided template Mods that you can use and learn the implementation pattern.

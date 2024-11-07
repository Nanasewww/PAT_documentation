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

# Practice 1.1 & Ex: Grant Tag Mod

## Goal

* Solve weird transition between Attack1 & Attack2

***

## Using Timing Attribute

We don't want to have Chain 1 in Tag Container during the entire Attack1 state. It should make sense for the animation. If you don't want Attack2 to be triggered before the slashing part of Attack1's animation ends even if you pressed attack, <mark style="color:orange;">**the Chain 1 Tag should only exist for a specific time interval**</mark>. This is what State Modifiers are designed to handle.

## Remove Idle & Chain 1 From Main Tags

First, let's reset the Main Tag in Attack2 back to <mark style="color:orange;">**Attack**</mark>:

<figure><img src="../../.gitbook/assets/image (53).png" alt=""><figcaption><p>Idle &#x26; Chain 1 removed</p></figcaption></figure>

## Add Grant Tag Mod to Attack1

Grant Tag Mod extends from the base class of State Modifier. It can <mark style="color:orange;">**add a tag inside Grant Tags**</mark> at the Begin Time / Index, and remove it at End Time / Index.

<figure><img src="../../.gitbook/assets/image (38).png" alt=""><figcaption><p>Grant Tag Mod for Idle Tag</p></figcaption></figure>

Two Grant Tag Mods should be added to Attack1 for Idle and Chain1.

* <mark style="color:orange;">**Idle Tag**</mark>\
  The Idle tag should exist in the entire Attack1 state, so the time attribute should be set to <mark style="color:orange;">begin at 0 and end at -1</mark> to cover the entire Action State.
* <mark style="color:orange;">**Chain1 Tag**</mark>\
  The Chain1 tag should only exist for after the slashing animation ends. You can use either <mark style="color:orange;">By Time in State Mode</mark> or <mark style="color:orange;">By Animation Event Mode</mark> to achieve this. You can find more details about Timing Attribute in page [#timing-attribute](../../documentation/actions/state-modifier.md#timing-attribute "mention").\
  In the next Steps, we will talk about how animations are connected to Action States, and how they are used to trigger State Modifiers using By Animation Event Mode.


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

Solving weird transition of Attack1 & Attack2

***

## Using Timing Attribute

We don't want to have Chain 1 in Tag Container during the entire Attack1. It should make sense for the animation. If you don't want Attack2 be triggered before the slashing part of Attack1's animation ends even if you pressed attack, the Chain 1 Tag should only exist for a specific time interval. This is what State Modifiers are designed to handle.

## Remove Idle & Chain 1 From Main Tags

First, let's set the Action State component of Attack2 back to one Main Tag:

<figure><img src="../../.gitbook/assets/image (53).png" alt=""><figcaption><p>Idle &#x26; Chain 1 removed</p></figcaption></figure>

Here's one example of Mod. Grant Tag Mod extends from the base class of State Modifier, it grants tags inside Grant Tags. Tags are added at the Begin Time / Index, and removed at End Time / Index

You may add two Grant Tag Mods to Attack1 and set the Grant Tags to Idle & Chain1. You can set Idle to begin at 0 and end at -1, which means it will cover the entire Action State.

<figure><img src="../../.gitbook/assets/image (38).png" alt=""><figcaption><p>Grant Tag Mod for Idle Tag</p></figcaption></figure>

But for Chain 1, it should only exist for after the slashing animation ends. You can also use By Time in State Mode, but it requires you to figure out the exact time of your animation. Or you may also use By Animation Event Mode. When you select Animation Event, you will see the inspector asking for a Begin Index and End Index. What does that mean? In the next Steps, we will talk about how animations are connected to Action States, and how they are used to trigger State Modifiers.

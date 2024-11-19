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

# Step 7: Trigger Animation Event

## Goal

* Understand how Trigger Animation Event is used for controlling State Modifiers

***

## Find your Animation

* In Unity Editor, find _<mark style="color:orange;">Window/Animation/Animation</mark>_ and click to open the Animation panel.
* Click on the Penguin game object and you can see the following stuff:&#x20;

<figure><img src="../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
_If you don't <mark style="color:red;">select the game object with Animator</mark>, the animations shown in the panel would not be writable and you cannot click the play button to preview it._&#x20;
{% endhint %}

Clicking onto _1H\_Melee\_Attack\_Slice\_Diagonal_, which is the animation clip for Attack1, you should see the following animation:

<figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

## Animation Event

There are 4 labels on top of the properties. You can click on them, and the inspector will look like:

<figure><img src="../../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

As the name suggests, these are the Animation Events that are used in Timing Attributes of State Modifiers. The Int in the inspector is for the Begin Index and End Index. We <mark style="color:red;">**HIGHLY RECOMMEND**</mark> ordering the events in ascending order, so it will not cause any potential problem.

## Add New Animation Event

To add an event, click the circled button:

<figure><img src="../../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

In the inspector view of the animation event, you need to select <mark style="color:orange;">**TriggerAnimatinoEvent(int)**</mark>:

<figure><img src="../../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>

This method is provided by <mark style="color:orange;">**Model Handler**</mark> attached to the same object as Animator.

<figure><img src="../../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

If you added your own Animation Event, remember to set an Int and drag it to the correct order.


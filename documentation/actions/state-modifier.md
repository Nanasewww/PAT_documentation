---
icon: circle-chevron-right
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

# State Modifier

## Definition

<mark style="color:orange;">**State Modifiers**</mark> are attached to Action States. They are triggered during the state and grants different functionality to Action States. For example, controlling animations, activating hitboxes, modifying movement speed, etc.&#x20;

Most modifier scripts are named as _**XXXMod**_, where <mark style="color:orange;">**Mod**</mark> stands for <mark style="color:orange;">**MODifier**</mark>. Each Modifier has a Begin and an End Timing Attribute, that defines when will this mod get activated, as well as the duration of it.

***

## Inspector Details

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfJHgu82STMVeajloMlYkejVXe7lKRJ7aoo5KXf1YRVYpuCvVazGJH3OTYHSdUV6TRtVnZwd59ig-clyJNm-aldzQ2kxuFa--xHXBb2SaA-JCIqfT3J9tRgL1Ua8dT87dJrHLGfUqNARC-oVloIHAOEWbIV?key=wjgYipemgHjXa5pb_ZH-6A" alt=""><figcaption><p>State Modifier inspector</p></figcaption></figure>

### Mod Name

A name for you to track what this modifier is for.

### Timing Attribute

<mark style="color:orange;">**Controls when this modifier will be activated.**</mark>&#x20;

There are basically two different **Modes** can select:

<details>

<summary>By Time in State</summary>

An Action State will <mark style="color:orange;">**count the time**</mark> after it is entered.&#x20;

Modifiers in this mode will be **triggered on Begin Time and** **stop functioning after End Time**.

* _Begin Time of -1 means the modifier will be triggered as soon as the State is entered._&#x20;
* _End Time of -1 means the modifier will not be turned off until the State is exited._

</details>

<details>

<summary>By Animation Event</summary>

You may add Trigger Animation Events to any animation clip through Unity. You must input an index to it in the inspector.&#x20;

Modifiers in this mode will **be triggered when the animation attached to the current state has passed Begin Index and** will **end on End Index**.&#x20;

_<mark style="color:yellow;">Please align indexes in increasing order for proper functioning. Note that Action States must have an animation for modifiers using this mode.</mark>_

* _Begin Index of -1 means the modifier will be triggered as soon as the State is entered._&#x20;

<!---->

* _End Index of -1 means the modifier will not be turned off until the State is exited._

</details>

### Events

Apart from the functionality of modifiers themselves, you can <mark style="color:orange;">**add additional functionality by using the begin & end unity event**</mark> exposed in the inspector. And a vanilla state modifier is solely for that. But be aware that Unity events are not easy to maintain and debug, please don’t use that for your core logic.

## Some Common Modifiers

## Grant Tag Mod

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXc3Ye_P4ij_0BBCm18YbYsIqGRLKaW8lDMNgw582DmXSGT2G9-og16aaiRFEMWUKL4CbOmDeRKDPLuCfAr3n9T8ec2AlJ7OT2wqbawXccdxHX2fNJA6FMt8hwm5mmYz8hdOXBudldeScrEI7v0uu1MxV7hk?key=wjgYipemgHjXa5pb_ZH-6A" alt=""><figcaption><p>Grant Tag Mod inspector</p></figcaption></figure>

When the character is in an Action State, it will hold all tags listed in the State’s Main Tag. Using this mod, it allows an Action State to <mark style="color:orange;">**have extra Tags**</mark> for further State transition.

## Animation Montage Mod

This Mod <mark style="color:orange;">**plays an animation state**</mark> in the model's animator and uses crossfade to create transitions.&#x20;

{% hint style="info" %}
Please note that this <mark style="color:red;">**ONLY**</mark> works with animator that structures in PAT’s template. If you need your own way to implement the animator, you might want to have your own version of Animation Modifier.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

### **Reference Animation Controller** <a href="#state-name" id="state-name"></a>

Drag in the Animation Controller that contains the animations.

### Layer

Choose the layer that contains your desired Animation.

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

### **Animation State** <a href="#state-name" id="state-name"></a>

Name of the State that contains the desired Animation state inside the Animator.

### **Fade in Time**

The duration of crossfade when the animation starts.

### **Fade out Time**

Fade out duration, and the target is a state called “Empty” in the same layer. This is helpful because the new state might be playing animation in a different layer.

### Animation Clip

Clicking on it brings you to the location of selected clip

### **Keep Play on Exit**

The animator will not try to fade to “Empty” automatically when state end.

### **Exit On Montage End**

Action State will auto exit if the Unity Animation Play Time reaches 1, helpful for many actions like _attack_, _roll_.






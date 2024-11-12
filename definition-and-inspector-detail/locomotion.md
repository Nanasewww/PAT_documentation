---
icon: person-walking-arrow-right
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

# Locomotion

## Locomotion Base

Character Locomotion Base processes general locomotion data for current movement and rotation.&#x20;

<figure><img src="../.gitbook/assets/image (33).png" alt=""><figcaption><p>CharacterLocomotionBase inspector</p></figcaption></figure>

### Inspector

#### Character Reference

* <mark style="color:orange;">**Character**</mark>: Reference to the Character this locomotion is referred to. If it is none, the script will automatically find Character component in this game object and its parent.&#x20;
* <mark style="color:orange;">**Character Transform**</mark>: Reference to the transform which the locomotion will be applied to. If it is none, the script will automatically set the Character transform.

#### Attributes

* <mark style="color:orange;">**Gravity**</mark>: The direction and magnitude of gravity. If you want to disable gravity, check **Base Data > Ignore Gravity** below.&#x20;
* <mark style="color:orange;">**Base Data**</mark>: Basic locomotion data including move speed, rotation speed, animation speed, root motion multiplier and ignore gravity.&#x20;
* <mark style="color:orange;">**Base Extra Data**</mark>: Extra locomotion data related to acceleration and damp for ground and air.&#x20;

#### Runtime Inspector

This includes some useful locomotion runtime parameters which would be very helpful for debugging.&#x20;

* <mark style="color:orange;">**On Ground**</mark>: Whether the character is on the ground.&#x20;
* <mark style="color:orange;">**Current Move Direction**</mark>: Current pending character move direction from player input.&#x20;
* <mark style="color:orange;">**Current Rotate Direction**</mark>: Current pending character rotate direction controlled by player input and aimer.&#x20;
* <mark style="color:orange;">**Current Movement**</mark>: Current movement mostly based on player input and calculated with speed and acceleration. This movement is gradually slowing down influenced by **Base Extra Data > Damp** instead of resetting to zero every Fixed Update.&#x20;
* <mark style="color:orange;">**Extra Movement**</mark>: Extra instant movement mostly added by root motion and modifiers. This movement is reset to zero every Fixed Update.&#x20;

## Locomotion Motor

Locomotion Motor applies the processed locomotion data in Locomotion Base to the character. In other words, it is the motor that decides how the character moves in a scene.&#x20;

Depending on different game types or special game design, different motors can be added to change character's locomotion.&#x20;

## Locomotion Anim Controller






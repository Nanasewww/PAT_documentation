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

# Step 10.1: Hitbox & Hurtbox

## Goal

* Understand Hitbox & Hurtbox.
* Understand how effects are transmitted through them.

***

## Hitbox

<figure><img src="../../../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

There is a <mark style="color:orange;">**Hitbox Component**</mark> on the sword move set. Typically, it is controlled by a State Modifier.

<figure><img src="../../../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

The Attack with <mark style="color:orange;">**Hitbox Mod**</mark> is responsible for the hitbox's activation and effects to send on collision.

## Hurtbox

<figure><img src="../../../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>

You must have hurtbox component for P Entities to get hurt. It is responsible for receiving effects and allowing the receiver to have invincible frame.


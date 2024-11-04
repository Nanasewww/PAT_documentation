# Step 10.1: Hitbox & Hurtbox

## Goal

Understanding Hitbox & Hurtbox and how effects are transmitted through them.

***

## Hitbox

<figure><img src="../../.gitbook/assets/image (66).png" alt=""><figcaption><p>Hitbox Component on Sword Moveset</p></figcaption></figure>

There is a Hitbox Component on the sword move set. Typically, it is controlled by a State Modifier.

<figure><img src="../../.gitbook/assets/image (67).png" alt=""><figcaption><p>Attack with Hitbox Mod</p></figcaption></figure>

The Attack with Hitbox Mod is responsible for the hitbox's activation and effects to send on collision.

## Hurtbox

<figure><img src="../../.gitbook/assets/image (68).png" alt=""><figcaption><p>Hurtbox</p></figcaption></figure>

You must have hurbox components for PAT\_Components to get hurt. It is responsible for receiving effects and allowing the receiver to have invincible frame.

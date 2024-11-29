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

# Apply Effects

There's several way to apply Effects a Character:

### Hitbox & Hurtbox

<figure><img src="../../.gitbook/assets/image (2) (1) (1).png" alt=""><figcaption><p>Hitbox</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1).png" alt=""><figcaption><p>Hurtbox</p></figcaption></figure>

When hitbox is activated, if collided with hurtbox, it will send all effect it holds to the hurtbox's character if that's a successful hit. Hurtbox can be invincible if the character holds it's I-Frame tag. Also, a Hitbox will only hit a Hurtbox once before reactivating.

Although we used raycst, this hit detection still relies on box collision a lot, we recommend you give all Hurtbox a rigid body to enable the collision.



We generally recommend you to control hitbox with _Attack with Hitbox Mod_

### Add Effect Mod

<figure><img src="../../.gitbook/assets/image (3) (1) (1).png" alt=""><figcaption><p>The Add Effect Mod</p></figcaption></figure>

This add the effects it holds to character

### Write Your Own Code

Code with, there's two ways to apply an effect to a character:

**Add Effect:**&#x20;

<figure><img src="../../.gitbook/assets/image (76).png" alt=""><figcaption></figcaption></figure>

This simply add the effect to a character. Good for single character cases.



**Send Effect Package:**&#x20;

<figure><img src="../../.gitbook/assets/image (77).png" alt=""><figcaption></figcaption></figure>

This call will let one character send effects to another character, and this action will be broadcasted to action events. Hitbox and Hurtbox are actually using this to deal damages. <mark style="color:orange;">**This call will also send a duplicate of the effect instead of the originally one to prevent reference issue.**</mark> You shall use this method to achieve the between character interaction.


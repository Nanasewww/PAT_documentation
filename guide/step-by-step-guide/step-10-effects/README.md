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

# Step 10: Effects

## Goal

* Understand how to modify Attributes on a different PAT\_Component[^1] through effects.

***

## Attributes on Other Characters

In [Step 9](../step-9-attributes.md), we talked how a character can modify its own Attribute by State Modifiers. That is within one character. How can we do the same thing to other characters? For example, how do I deal damage?

You might have already noticed there is a dummy capsule in the scene, and the health bar does respond to both your attacks.&#x20;

<figure><img src="../../../.gitbook/assets/image (62).png" alt=""><figcaption><p>Training Dummy</p></figcaption></figure>

## Effect

In PAT, we are <mark style="color:orange;">**using Effect to modify attributes on other PAT\_Components**</mark>.&#x20;

Effects are scriptable objects. You may find an example through Attack1. The Attack with <mark style="color:orange;">**Hitbox Mod**</mark> is a State Modifier that sends a list of Effects through colliders.

<figure><img src="../../../.gitbook/assets/image (63).png" alt=""><figcaption><p>Attack with Hitbox Mod</p></figcaption></figure>

If you click on to the Scriptable Object, you should see this:

<figure><img src="../../../.gitbook/assets/image (64).png" alt=""><figcaption><p>Effect: Damage Attack 1</p></figcaption></figure>

To put this in a simple way, what matters here is the EffectModValue part.&#x20;

<figure><img src="../../../.gitbook/assets/image (65).png" alt=""><figcaption><p>Effect Mod Value</p></figcaption></figure>

You will find it working just like the Use Attribute Mod, also with a Resource Tag and a value. But there is a lot more about Effects. You can find details in the link below:

{% content-ref url="../../../documentation/effect.md" %}
[effect.md](../../../documentation/effect.md)
{% endcontent-ref %}

[^1]: Character is extended from PAT\_Component

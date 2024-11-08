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

# Create an Effect

## Effect Creation

&#x20;To create an Effect, you can either <mark style="color:orange;">**create a ScriptableObject asset in your project**</mark> or <mark style="color:orange;">**implement your own custom Effect**</mark> by inheriting from the appropriate class. Just like action state, effect themselves don't do anything, <mark style="color:orange;">**you need to add Effect Component to make them impact gameplay.**</mark>&#x20;

### Create an Effect via ScriptableObject

Using ScriptableObjects is preferred for prototyping and designing game logic. You can find many mods, such as _Add Effect_ or _Add Effect On Hit_, created this way. _Attack with hitbox_ also can use effect directly from scrtipable object.

<figure><img src="../../.gitbook/assets/image (71).png" alt=""><figcaption></figcaption></figure>

Once created an effect, you will see this

<figure><img src="../../.gitbook/assets/image (72).png" alt=""><figcaption></figcaption></figure>

**MainTags:** character owning this effect will have those tag as long as this effect stays

**InfoTags:** for Effect Components to communicate

Applied Time, Source, Target: will automaically been set in the process

To add an Effect Component, <mark style="color:orange;">**you select the type in dropdown first, then click the add button**</mark>

<figure><img src="../../.gitbook/assets/image (73).png" alt=""><figcaption><p>Current Effect Component we provided</p></figcaption></figure>

EffectModValue: modify the value of an Attribute in different ways. This can be used for damage, but also used for something like speed control.

**EffectLifeControl:** how long will the effect stay on a character

**EffectKnockBack:** the target of this effect will be knocked backed, if that's a character

**EffectHitboxInfo:** Hitbox will add this to damage effect inorder to pass some extra information

**EffectHoldLaw:** this effect will contains extra attributelaw, we will talked about attribute law latter.

### Create Effect via Factory

Some scripts, like Attack with Hitbox, can get effect from factory:

<figure><img src="../../.gitbook/assets/image (74).png" alt=""><figcaption><p>All subclass of EffectFactory will be in the list</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (75).png" alt=""><figcaption><p>As you selected the Factory, some property of Effect generation will be exposed to you</p></figcaption></figure>

By this, you don't need to create tons of scriptable object for different attacks. You simply record the data here and an Effect with all thos setting will be created in run time.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>How Effect Factory Looks like in code</p></figcaption></figure>

We encourgae you to use Factory for some script that want to apply effects dynamically. You can also write your own Factory by overriding the orignal abstract class.


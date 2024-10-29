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

Currently, there are two types of Effect components implemented in PAT: Effect Life Control and Effect Mod Value. To create an Effect, you can either <mark style="color:orange;">**create a ScriptableObject asset in your project**</mark> or <mark style="color:orange;">**implement your own custom Effect**</mark> by inheriting from the appropriate class.

### Create a ScriptableObject

Using ScriptableObjects is preferred for prototyping and designing game logic. You can find many mods, such as _Add Effect_ or _Add Effect On Hit_, created this way.

<figure><img src="../../.gitbook/assets/image (8) (1) (1).png" alt=""><figcaption><p>reating new Effect in Unity editor</p></figcaption></figure>

### Implement custom Effect

Script generation is preferred for dynamic hit processing. Modifiers like _Block Mod_ and _Attack Mod_ are typically implemented using this method.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1).png" alt=""><figcaption><p>ample code for implementing new Effect</p></figcaption></figure>


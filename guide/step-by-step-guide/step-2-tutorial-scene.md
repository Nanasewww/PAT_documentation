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

# Step 2: Tutorial Scene

## Goal

* Locate and open the tutorial scene
* Learn the scene hierarchy

***

## Locate the Tutorial Scene

Go to _<mark style="color:blue;">**Assets/PenguinActionToolkit/Demos/Scenes/Tutorial**</mark>_, open it, you should see a scene like this:

<figure><img src="../../.gitbook/assets/image (12) (1).png" alt=""><figcaption></figcaption></figure>

If you start the game, you will find yourself playing as a penguin-look character. You can move around with WASD or Controller Stick, roll dodge with Space Bar or B button on XBOX controller (or other east buttons if you are using other controllers).&#x20;

***

## Scene Hierarchy

### Character

From the hierarchy panel, you can find the <mark style="color:orange;">**MyFirstCharacter**</mark> contains the following game objects:

<figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

<mark style="color:orange;">**Locomotion**</mark>\
It holds components which control how the character is moving around, including walking and roll dodging.

* <mark style="color:orange;">**Model Container**</mark>\
  It contains the model of the character with some components to handle weapon models and animations.
* <mark style="color:orange;">**Attributes**</mark>\
  It stores the health and stamina attributes. These attributes are reflected on the Inspector. \
  Your roll dodging will consume <mark style="color:orange;">Stamina</mark>.

### Player

Under the <mark style="color:orange;">**GameFlow**</mark> object, you can see a <mark style="color:orange;">**Player**</mark> prefab.&#x20;

<figure><img src="../../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

The <mark style="color:orange;">**Player**</mark> prefab decides which character the player is currently controlling and handles the <mark style="color:orange;">player input</mark> and <mark style="color:orange;">camera</mark> for it.&#x20;

* <mark style="color:orange;">**Player Cam**</mark>
* <mark style="color:orange;">**Input Units**</mark>: it handles several input Elements.&#x20;
  * Element: it includes an Input Tag (We will talk about its meaning very soon!) and an Input Action Reference.  It bounds the Input Action to the selected Input Tag.&#x20;

## Play Mode

In the inspector, you can see that we actually set up the Attack input in Player, which is mapped to Left Click on your mouse (or west button on controllers). If you click your mouse in the game, you will find the character doing a simple attack.&#x20;

The following steps will try to walk through you how to correctly bound an input with an Action.&#x20;


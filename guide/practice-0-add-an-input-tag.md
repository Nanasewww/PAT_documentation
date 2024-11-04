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

# Practice 0: Add an Input Tag

## Goal

* Use Input Tag to allow the knight performing other attacks.

***

## Task

You might have noticed this: there exists <mark style="color:orange;">**two attack objects**</mark> in the move set prefab.

<figure><img src="../.gitbook/assets/image (29).png" alt=""><figcaption><p>Attack 2</p></figcaption></figure>

Attack 2 and Attack 1 are almost identical, but only Attack 1 is triggered when you left click your mouse.&#x20;

The reason is simple: <mark style="color:orange;">**Attack 2 does not have an Input Tag**</mark>. No matter what button you clicked, it will never be triggered.

So now let's try to add an Input Tag to this State.

<figure><img src="../.gitbook/assets/image (30).png" alt=""><figcaption><p>Input - lightAttack</p></figcaption></figure>

Select _light attack_ Input Tag from inspector.

Now run the game. You should find the knight attacking with a new animation when you left click / press west button.

***

## Question

Now <mark style="color:orange;">**one action state is overriding another**</mark>. We don't really want that. We want the two action states form a combo that are triggered with a fixed order. When you left click twice, you should always see the knight performing Attack1 first, then Attack2.&#x20;

<details>

<summary>Why do they override each other like this? </summary>

In MoveSet, the actions are checked in a fixed order, <mark style="color:orange;">from top to down</mark>.&#x20;

In this case, Attack 2 compares its Input Tag with tags in Tag Container first, and successfully grabs the Light Attack tag from it. When checking Attack 1, there is no Light Attack tag anymore and it will not be triggered.&#x20;

In short, they have different priority so Attack 2 will always be triggered before Attack 1. By dragging Attack 1 above Attack 2, you can find now it is Attack 1 which is triggered every time.&#x20;

</details>

In the next steps, we will explain how to accomplish that.


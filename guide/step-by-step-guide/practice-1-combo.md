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

# Practice 1: Combo

## Goal

* Make a combo with Attack1 and Attack2
* Understand how to use Tags to change Action States

***

## Review

We've covered the very basic terminologies and structure of PAT, and now it's time to check if you can use what you have learned to create your own stuff. Go ahead and try this assignment: <mark style="color:orange;">**add a new action state that forms a combo of Attack1 and Attack2**</mark>.&#x20;

{% hint style="info" %}
_This practice will not be finished in this article, we will keep introducing features of PAT while helping you complete this task._
{% endhint %}

***

## Find Attack2

Find [SwordMoveset](step-3-character-action-states.md#find-swordmoveset) again. Click onto Attack2.&#x20;

In practice 0, we've implemented that if you left click your mouse, the penguin will always perform Attack2. It is not what we expected. We want to build a combo, which means the first click to trigger Attack 1, and the second click to trigger Attack 2.

<figure><img src="../../.gitbook/assets/image (9) (1).png" alt=""><figcaption></figcaption></figure>

## Add Requirement Tag to Attack2

Now Attack2 has only one requirement apart from the input: the Idle Tag. As long as there is an Idle Tag in the Tag Container, Attack 2 is valid for triggering.&#x20;

<details>

<summary>Why does Attack2 override Attack1?</summary>

In MoveSet, the actions are checked in a fixed order, <mark style="color:orange;">from top to down in Hierarchy</mark>.&#x20;

In this case, Attack 2 compares its Input Tag with tags in Tag Container first, and successfully grabs the Light Attack tag from it. When checking Attack 1, there is no Light Attack tag anymore and it will not be triggered.&#x20;

In short, they have different priority so Attack 2 will always be triggered before Attack 1. By dragging Attack 1 above Attack 2, you can find now it is Attack 1 which is triggered every time.&#x20;

</details>

To fix this, we want to <mark style="color:orange;">**add an additional Require Tag to Attack2**</mark> which is only granted while the character is performing Attack1.&#x20;

Add an inner element to the <mark style="color:orange;">**Require Tags**</mark> of Attack2, select it to be <mark style="color:orange;">**Chain1**</mark>.&#x20;

For the difference of inner elements and outer elements within Require Tags, you can find more details in Action State [#inspector-details](../../documentation/actions/action-state.md#inspector-details "mention").

<figure><img src="../../.gitbook/assets/image (35).png" alt=""><figcaption><p>Add Chain 1 to Attack2</p></figcaption></figure>

## Add Main Tag to Attack1

Now Attack2 requires another Chain1 Tag. If you play the game now, the character will do Attack1 again and Attack2 cannot be triggered, because <mark style="color:orange;">**nothing is granting Chain 1 Tag to the character**</mark>. We want to make Attack1 grants this tag so Attack2 can form a combo with it.

As all Tags in Main Tags will be added to the Tag Container when that Action State is triggered, we can <mark style="color:orange;">**add Idle & Chain 1 to Attack1's Main Tag**</mark>. Now it allows Attack2 get triggered.&#x20;

<figure><img src="../../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>

But there is another problem: <mark style="color:orange;">**you can trigger Attack2 at any time during Attack1**</mark>.&#x20;

This makes the game feels weird. The animation of slash in Attack1 might not even started before moving on to Attack2. As a game developer, you want something more fluent. It requires a more precise control over the Action States. That leads us to the next Step: State Modifiers.&#x20;


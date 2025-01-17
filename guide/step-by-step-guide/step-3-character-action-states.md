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

# Step 3: Character - Action States

## Goal

* Undertand what Action State is
* Find Tag Container
* Understand how Action State are connected to Input Tags

***

## Find SwordMoveset

Under <mark style="color:orange;">**MyFirstCharacter**</mark>, you can find <mark style="color:orange;">**SwordMoveset**</mark> Object.

<figure><img src="../../.gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>

Click onto Attack1.

What matters in this step is the Action State Script.&#x20;

<figure><img src="../../.gitbook/assets/image (27) (1).png" alt=""><figcaption></figcaption></figure>

An <mark style="color:orange;">**Action State**</mark> is the minimal state that describes a character’s action.&#x20;

Action States include locomotion actions like moving, jumping, dashing, or combat actions like swinging a sword or firing a gun. It is the basic unit that adds up to the entirety of our action system in PAT. Action State by itself has very limited functionality, it serves as a [logic system](#user-content-fn-1)[^1] that shows which state a character is in (what it is doing), and what it can do from the current state.&#x20;

For more details, you can find in [action-state.md](../../documentation/actions/action-state.md "mention").

{% hint style="info" %}
_Most real functionalities are fulfilled by State Modifiers that are add on to Action States, and we will cover those later._
{% endhint %}

So how does an Action State know when it should be triggered? What allows the penguin to attack after a left click?

***

## Input Unit

If you recall what we mentioned at the end of [step-2-tutorial-scene.md](step-2-tutorial-scene.md "mention"), the Player Component handles your inputs. Each input unit bounds an action reference from the Input Action System to an Input Tag.

<figure><img src="../../.gitbook/assets/image (5) (1) (1).png" alt=""><figcaption><p>Player Component from last step</p></figcaption></figure>

For example, if you input the Attack button (left clicking your mouse / west button on controller), the Player will send a Light Attack Tag to the Character, and Character will find if it matches the Action State's Input Tag.

***

## Tag Container

For you to check what tags were sent to a character, we have a component called <mark style="color:orange;">**Tag Container**</mark> generated by Character component. In this tutorial, it is on <mark style="color:orange;">**MyFirstCharacter**</mark>.&#x20;

{% hint style="info" %}
_Note that it is only added to the object <mark style="color:orange;">**at runtime**</mark>, so you have to start the game first to find it in the inspector._
{% endhint %}

Tag Container is a very useful tool for debugging your character, especially when the character doesn't behave as you expected. You can check whether the player input is correctly handled, or which State Tags are added to the character at this moment.

<figure><img src="../../.gitbook/assets/image (7) (1) (1).png" alt=""><figcaption><p>How the Tag Container looks like if you left click your mouse</p></figcaption></figure>

***

## Input Tag

On each Update, all Action States <mark style="color:orange;">**compare their Input Tags with current tags in Tag Container**</mark>. If they found the matching Input Tag, the Action State will <mark style="color:orange;">**try to be triggered**</mark>. This is how the penguin attacks -- It receives an Input Tag from the Player.&#x20;

{% hint style="warning" %}
_However, this doesn't mean they can always be triggered with the Input Tag. There are more restrictions that will be explained in the next Step._
{% endhint %}

<figure><img src="../../.gitbook/assets/image (28) (1).png" alt=""><figcaption><p>Input Tag - Light Attack</p></figcaption></figure>

Now let's try do the same thing for another Action State.

[^1]: or State Machine, if you prefer

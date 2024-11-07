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

# Practice 1.2: Back to Grant Tag Mod

## Goal

* Solve the chain 1 Tag problem

***

Now we have everything we need to solve it. If you look into the animation clip of Attack1, you should find <mark style="color:orange;">**Event\[2]**</mark> is around the time where the slash animation is completed.

{% hint style="warning" %}
_If you added your own animation event in the last Step, please check if the index here should still be <mark style="color:orange;">**2**</mark>._
{% endhint %}

<figure><img src="../.gitbook/assets/image (51).png" alt=""><figcaption><p>Event[2]</p></figcaption></figure>

When we go back to the move set prefab and <mark style="color:orange;">**select Attack1**</mark>, we can now set the <mark style="color:orange;">**Grant Tag Mod**</mark> which grants Chain 1 to begin at animation index 2, and ends at -1.&#x20;

This means the <mark style="color:orange;">**Chain 1 Tag will not be granted before the Animation Event 2**</mark>, and it will <mark style="color:orange;">**not be removed until the end of the State**</mark>.

<figure><img src="../.gitbook/assets/image (52).png" alt=""><figcaption></figcaption></figure>

Now try playing the game, you should find the animation looks better than before.

***

## Recap

From Practice 1, we discussed:

* Action States
* Tags
* State Modifiers
* Animation Montage
* Trigger Animation Event

These contents above are the fundamental elements of our Toolkit. If you find anything confusing, please reread those parts and also check on other documentations of these parts.


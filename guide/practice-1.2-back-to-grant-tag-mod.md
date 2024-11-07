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

Now we have everything we need to solve it. If you look into the animation clip of Attack1, you should find Event\[2] is around the time where the slash animation is completed (If you added your own animation event in the last Step, please check if the index here should still be 2).

<figure><img src="../.gitbook/assets/image (51).png" alt=""><figcaption><p>Event[2]</p></figcaption></figure>

When we go back to the move set prefab, select Attack1, we can now set the Grant Tag Mod which grants Chain 1 to begin at animation index 2, and ends at -1. This means the Chain 1 Tag will not be granted before the Animation Event 2, and it will not be removed until the end of the State.

<figure><img src="../.gitbook/assets/image (52).png" alt=""><figcaption></figcaption></figure>

Now try playing the game, you should find the animation looks better than before.

***

## Recap

From Practice 1, we discussed Action States, Tags, State Modifiers, Animation Montage, and Trigger Animation Event. These contents are the fundamental elements of our Toolkit. If you find anything confusing, please reread those parts and also check on other documentations of these parts.

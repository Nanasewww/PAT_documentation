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

Goal

The final goal of Practice 1 would be making a combo starting from the two attacks we have. It involves understanding of using Tags to change Action States.

## Review

Now we covered the very basic terminologies and structure of PAT, and you might want to see if you can use what you have read to create your own stuff. So now go ahead and try this assignment: add a new action state that forms a combo of Attack1 and Attack2.

Please note this practice will not be finished in this article, we will keep introducing features of PAT while helping you complete this task.

***

## Step 1: Go to Attack2

Again, find the move set, open it.

Click onto Attack2. Remember if you left click your mouse, the knight will always perform Attack2. It is not what we desired. We want the first click to trigger Attack 1, and the second click to trigger Attack 2.

<figure><img src="../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>

## Step 2: Add Requirement

Now Attack2 has only one requirement apart from the input: the Idle Tag. As long as there exists an Idle Tag in the Tag Container, Attack 2 is valid for triggering. Given that it is above Attack1 in the prefab hierarchy, Unity will always trigger the upper Action State, i.e., Attack2 rather than Attack1. This is why it overrides Attack1.

To fix this, we want to add an additional requirement to Attack2. A Tag that is only granted while the character is performing Attack1.&#x20;

Add an inner element to the Require Tags of Attack2, select it to be Chain1.&#x20;

(If you wonder the difference of inner elements and outer elements within Require Tags, please refer to the Inspector Detail Page of [Action State](../documentation/actions/action-state.md#tags))

<figure><img src="../.gitbook/assets/image (35).png" alt=""><figcaption><p>Add Chain 1 to Attack2</p></figcaption></figure>

## Step 3: Add Main Tag to Attack1

Now Attack2 requires another Tag. If you play the game now, you will find the character doing Attack1 again, but Attack2 cannot be triggered, because nothing is granting Chain 1 Tag to the character. We want to make Attack1 grants this tag so Attack2 can form a combo with it.

We mentioned that all Tags in Main Tags will be added to the Tag Container when that Action State is triggered. We can add Idle & Chain 1 to Attack1's Main Tag, so now it will allow Attack2 get triggered.&#x20;

<figure><img src="../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>

But now you may find another problem: you can trigger Attack2 at any time during Attack1. It makes the game feels weird. The animation of slash in Attack1 might not even started before moving on to Attack2. As a game developer, you want something more fluent. It requires a more precise control over the Action States. That leads us to the next Step: State Modifiers.

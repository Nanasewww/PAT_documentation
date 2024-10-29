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

## Find Action State Melee 1

TODOFind MoveSet

TODOOpen Moveset Prefab

TODOFind Melee 1

What matters in this Step is the Action State Script.&#x20;

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

An <mark style="color:orange;">**Action State**</mark> is the minimal state that describes a character’s action. It includes locomotion actions like moving, jumping, dashing, or any combat action like swinging a sword or firing a gun. It is the basic unit that adds up to the entirety of our action system in PAT. <mark style="color:orange;">Action State by itself has very limited functionality</mark>, it serves as a logic system that shows which state a character is in (what it is doing), and what it can do from the current state. Most _real_ functionalities are fulfilled by <mark style="color:orange;">State Modifiers</mark> that are add on to Action States, and we will cover that later.

***

## Input Tag

So how do inputs from players get transmitted to the characters? If you recall what we mentioned in the last article _Step 2: A Basic Scene_, the Player Script handles your inputs. Each input unit bounds an action reference from the Input Action System to an Input Tag (which is the Tag field shown below)

<figure><img src="../.gitbook/assets/image (2) (1) (1).png" alt=""><figcaption><p>This is from Player in the last article</p></figcaption></figure>

For example, if you input the Attack button, the Player will try to send a Light Attack Tag to the Character, and Character will find if it matches the Action State's Input Tag.

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption><p>Melee 1 has an Input Tag of Light Attack</p></figcaption></figure>

You can find what State the Character is in by going to the Character Object. It is on the Character Script.

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

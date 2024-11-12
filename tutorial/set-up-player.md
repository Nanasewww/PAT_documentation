---
icon: hammer
---

# Set Up

## Using Prefab

The easiest way is to drag a prefab from our folder

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1).png" alt=""><figcaption><p>location of the prefab</p></figcaption></figure>

This prefab has input finding settled down and have one real camera and two virtual cameras for 3D third person game.

<figure><img src="../../.gitbook/assets/image (4) (1) (1) (1).png" alt=""><figcaption><p>How player looks like when you drag from prefab</p></figcaption></figure>

You might find the Character slot empty. Drag your in-scene character (not prefab) in it and you will now be controlling the character. You can also set player character through code by calling the Change Character method in Player

<figure><img src="../../.gitbook/assets/image (5) (1) (1).png" alt=""><figcaption></figcaption></figure>

For the Player Index, keep it to -1 for single player game. We will cover how to set up multiplayer in the multiplayer session.&#x20;

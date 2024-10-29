---
hidden: true
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

# Step 2: A Basic Scene

Create a simple scene, add a large enough plane into it.

<figure><img src="../.gitbook/assets/image (2) (1).png" alt=""><figcaption><p>Start from here</p></figcaption></figure>

After creating the scene, let's bringing some prefabs from our toolkit so you can skip the difficult part.&#x20;

***

First, go to _Assets/PenguinActionToolkit/Core/Prefab/Player_, and find the <mark style="color:blue;">Player</mark> prefab, drag it into the scene. This prefab contains 3 cameras and the Player script that finds the character you are controlling. But he most important thing to remember about this prefab right now is that it keeps track of your input.

<figure><img src="../.gitbook/assets/image (7) (1).png" alt=""><figcaption><p>Input Units are matching action references to real actions</p></figcaption></figure>

You might wonder what the Tags are referencing to. They are essential to our toolkit, and we will cover that part very soon. If you are interested in what else does <mark style="color:blue;">Player</mark> do, please refer to the link below, but that part might be confusing at this moment. We recommend moving on and check on that later.

<figure><img src="../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

{% content-ref url="../tutorial/player/" %}
[player](../tutorial/player/)
{% endcontent-ref %}

***

Go and find a sample character prefab in _Assets/PenguinActionToolkit/Core/Prefab/Character_, select the <mark style="color:blue;">TODO</mark> prefab, **DUPLICATE** it, bring the duplicated prefab to your own folder, and then drag it into the scene.

<figure><img src="../.gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>

***

On the Player object, drag the character into the Character field. Now start the game, you should find yourself controlling the character.

<figure><img src="../.gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure>

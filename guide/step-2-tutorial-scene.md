# Step 2: Tutorial Scene

## Goal

Open the tutorial scene we provided you, have a look at the hierarchy panel.

***

Go to _Assets/PenguinActionToolkit/Demos/Scenes/Tutorial_, open it, you should see a scene like this:

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

If you start the game, you will find yourself playing as a knight-look character. You are able to move around with WASD or Controller Stick, roll dodge with Space Bar or B button on XBOX controller (or other east buttons if you are using other controllers).&#x20;

From the hierarchy panel, you can see the MyFirstCharacter contains the following game objects:

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption><p>The knight character</p></figcaption></figure>

### Game Objects

The parent object includes the following children:

* **Locomotion**\
  Controls how the character is moving around, this includes walking and roll dodging.
* **Model Container**\
  Contains the model of the character.
* **Attributes**\
  Stores the health and stamina attributes. It is reflected on the UI. Your roll dodging will consume Stamina.

***

## Player

Under the GameFlow object, you can see a Player prefab.&#x20;

<figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

The <mark style="color:blue;">Player</mark> prefab handles Cameras, which character you are controlling. The most important thing to remember at this moment is that it handles <mark style="color:orange;">inputs</mark>.

## Play Mode

In the inspector, the Input Units contains several Elements. Each elements include an Input Tag (We will talk about its meaning very soon!) and an Input Action Reference. It bounds the Input Action to the selected Input Tag. You can see that we actually set up the Attack input, which is mapped to Left Click on your mouse (or west button on controllers). If you click your mouse in the game, you will find the character doing a simple attack. The following steps will try to walk through you how to correctly bound an input with an Action.&#x20;

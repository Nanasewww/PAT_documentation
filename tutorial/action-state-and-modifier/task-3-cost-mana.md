---
icon: circle-chevron-right
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

# Task 3: Cost mana

By right-clicking, PlayerRabbit can perform a ranged attack. This powerful, long-distance attack doesn’t require the player to approach enemies. To balance its strength, we can add mana consumption to limit its usage.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfYilOFFi_qKnDfzX4ixVrSrJkTuJwRoww-AG2HMMb2plyVI9dqMKLjQ1qjYGUFsq9krQ1BB6inHH3Ivlf5v9S99X7gTR6Lol3uGrwh54klB5e4ucaVVIX54cBQK0fEk2h_eYsCP8uLLa4ZsBi6aMc07E4?key=p_nH-JdSTTyX01UFeuszxg" alt=""><figcaption></figcaption></figure>

UseAttributeMod is a Modifier that can send a value change Effect to a character's Attribute. The Resource Tag specifies the target of the modification, while the Amount determines the value used.&#x20;

An Attribute is a MonoBehaviour that holds a value. Health, Posture, Mana, and Stamina are all examples of Attributes. Since Attributes can be influenced by Effects in an easy and stable way without tightly coupling your code, we encourage you to use Attributes for many other values you want to change dynamically during gameplay. For more details on Attributes and Effects, please refer to our documentation.






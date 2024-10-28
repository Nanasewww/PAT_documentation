---
icon: circle-chevron-right
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

# Create a Character

There are many ways you can create a Character in PAT. Here we’ll cover the 3 recommended ones.&#x20;

{% hint style="info" %}
_For PAT beginners, we <mark style="color:red;">**HIGHLY**</mark> recommend using the first way - Copy from templates._
{% endhint %}

## Copy from templates

PAT provides a range of templates to simplify the character initialization process. These templates include <mark style="color:orange;">**different functional characters and enemies**</mark> commonly seen in 2D/3D action games, equipped with various weapons and abilities. With just a few steps, you can have a playable Character and start exploring PAT's unique Action State system to create your own signature combat abilities.

{% stepper %}
{% step %}
### Find a Character you like from the demos


{% endstep %}

{% step %}
### Locate its prefab


{% endstep %}

{% step %}
### Duplicate the prefab


{% endstep %}

{% step %}
### Rename it to whatever you want your Character to be called


{% endstep %}

{% step %}
### Make skeleton automatically
{% endstep %}
{% endstepper %}

***

## Create skeleton automatically

TODO <mark style="color:blue;">@Minghao</mark>

## Create from scratches

You can also create a Character from scratches. This is not the preferred way since there are many tedious steps before you can have a playable character. Unless you are very confident about your understanding of PAT’s system, we do not recommend using this approach to create characters.

<details>

<summary><strong>[PAT Character structure reference]</strong></summary>



**\[NewCharacter]**\
Add a Character component\
Add a Character Locomotion Base component\
Add a Locomotion Motor component corresponding to your game type\
Add a capsule collider or any other components required by your Motor

* **MoveSets**
  * **LocomotionSet**\
    Use LocomotionSet Prefab here
  * **NewMoveSet**\
    Add a Move Set component
    *   **New Action 1**\
        Add an Action State component

        Add multiple Modifier components you want to define your action behavior
    * **New Action 2**
    * ...
* **ModelContainer**
  * **Character Model**
*   **Hurt Box**\
    Add a Effect Receive Box component

    Add a Box Collider component

    Add a Rigidbody component

</details>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfEl2bY5ibu3dQ1i7_DmAh9Y1guq6aDkOgPrH4kTO2MzLBYQT21QsUuec5srI9-lRkUOuUIKRWvBwL12vLmtbgOTsHPFlj2tIuHuXf6LjD0jitMidsG6Ar_LMrC5P49ksQCj2xs1OMyRMepqtFkE43xJdTS?key=p_nH-JdSTTyX01UFeuszxg" alt=""><figcaption><p>Example: one available character hierarchy</p></figcaption></figure>






# Step 5: State Modifiers

## Review

We have talked about Action States and Tags and added your own State. However, it is

***

## State Modifier

<mark style="color:orange;">**State Modifiers**</mark> are attached to Action States. They are triggered during the state and grants different functionality to Action States. For example, <mark style="color:orange;">controlling animations, activating hitboxes, modifying movement speed</mark>, etc. Action States by themselves only form a logic chain of your character, they need State Modifiers for different functions.

Most modifier scripts are named as _**XXXMod**_, where <mark style="color:orange;">**Mod**</mark> stands for <mark style="color:orange;">**MODifier**</mark>. Each Modifier has a Begin and an End Timing Attribute, which defines when will this mod get activated, as well as the duration of it.

***

## Component

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfJHgu82STMVeajloMlYkejVXe7lKRJ7aoo5KXf1YRVYpuCvVazGJH3OTYHSdUV6TRtVnZwd59ig-clyJNm-aldzQ2kxuFa--xHXBb2SaA-JCIqfT3J9tRgL1Ua8dT87dJrHLGfUqNARC-oVloIHAOEWbIV?key=wjgYipemgHjXa5pb_ZH-6A" alt=""><figcaption><p>View of a basic State Modifier</p></figcaption></figure>

### Mod Name

A name for you to track what this modifier is for.

### Timing Attribute

<mark style="color:orange;">**Controls when this modifier will be activated.**</mark>&#x20;

There are two different **Modes** to select:

<details>

<summary>By Time in State</summary>

An Action State will <mark style="color:orange;">**count the time**</mark> after it is entered.&#x20;

Modifiers in this mode will be **triggered on Begin Time and** **stop functioning after End Time**.

* _Begin Time of -1 means the modifier will be triggered as soon as the State is entered._&#x20;
* _End Time of -1 means the modifier will not be turned off until the State is exited._

</details>

<details>

<summary>By Animation Event</summary>

You may add Trigger Animation Events to any animation clip through Unity. You must input an index to it in the inspector.&#x20;

Modifiers in this mode will **be triggered when the animation attached to the current state has passed Begin Index and** will **end on End Index**.&#x20;

_<mark style="color:yellow;">Please align indexes in increasing order for proper functioning. Note that Action States must have an animation for modifiers using this mode.</mark>_

* _Begin Index of -1 means the modifier will be triggered as soon as the State is entered._&#x20;

<!---->

* _End Index of -1 means the modifier will not be turned off until the State is exited._

</details>

<mark style="color:red;">Animation Event requires modifying the animations, so let's use By Time in State for now.</mark>

### Events

Apart from the functionality of modifiers themselves, you can <mark style="color:orange;">**add additional functionality by using the begin & end unity event**</mark> exposed in the inspector. And a vanilla state modifier is solely for that. But be aware that Unity events are not easy to maintain and debug, please don’t use that for your core logic.



This is only a basic template of a State Modifier. It only triggers Unity Events. Given that Unity Events can be hard to handle, we allow you to extend from State Modifier and create your own modifiers. We also provided template Mods that you can use and learn the implementation pattern.

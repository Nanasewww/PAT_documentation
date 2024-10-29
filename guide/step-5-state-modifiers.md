# Step 5: State Modifiers

## Review

We have talked about Action States and Tags and added your own State. However, we used a component called Animation Montage Mod for the animation clip to be correctly played. So, what is Animation Montage Mod? It is in fact a State Modifier.

***

## State Modifier

<mark style="color:orange;">**State Modifiers**</mark> are attached to Action States. They are triggered during the state and grants different functionality to Action States. For example, <mark style="color:orange;">controlling animations, activating hitboxes, modifying movement speed</mark>, etc. Action States by themselves only form a logic chain of your character, they need State Modifiers for different functions.

Most modifier scripts are named as _**XXXMod**_, where <mark style="color:orange;">**Mod**</mark> stands for <mark style="color:orange;">**MODifier**</mark>. Each Modifier has a Begin and an End Timing Attribute, which defines when will this mod get activated, as well as the duration of it.

***


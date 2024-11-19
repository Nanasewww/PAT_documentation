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

# Step 6: Animation Montage

## Goal

* Understand Animation Montage Mod
* Get familiar with the Animation Controller

***

## Animation Montage Mod

<mark style="color:orange;">**Animations are attached to Action States by Modifiers**</mark>. We provide this <mark style="color:orange;">**Animation Montage Mod**</mark> for you to bind an Animation State from your Animator to an Action State.

<figure><img src="../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

A blank Animation Montage Mod will look like this:

<figure><img src="../../.gitbook/assets/image (42).png" alt=""><figcaption><p>Blank Animation Montage Mod</p></figcaption></figure>

Dragging in the <mark style="color:orange;">**Reference Animation Controller**</mark> of your character saves a lot of time for enabling the dropdown menu. We recommend doing that for your future projects.

## Animator

If you go to the current animation controller, which is the <mark style="color:orange;">**HumanoidCharacter**</mark>, you can find the following view in Animator Panel. Different animation states are categorized on different layers. To find the animation state for your Action State, you should select the corresponding layer, then select the desired animation state.&#x20;

<figure><img src="../../.gitbook/assets/image (43).png" alt=""><figcaption><p>Animator</p></figcaption></figure>

When you can see the Animation Clip field tied with a specific clip, it means now the Action State will automatically play that clip when entered.&#x20;

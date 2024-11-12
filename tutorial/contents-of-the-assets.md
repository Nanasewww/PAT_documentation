---
icon: folder
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

# Contents of the Assets

<details>

<summary><mark style="color:orange;">Table of Contents</mark></summary>

* Core
  * Prefab
    * AI
    * Camera
    * Character
      * Attributes
      * MoveSets
    * GUI
    * Player
  * Resources
    * AttributeLaw
    * EffectObj
  * Scripts
    * AI
    * Character
    * CombatCore
    * Editor
    * Feedback
    * GamePlayTags
    * GeneralTools
    * GUI
    * Node
    * Player

<!---->

* Demos

<!---->

* ThirdParty

</details>

## Core

**Core** folder contains all scripts which are necessary for an action system. When using PAT, you'll make sure this folder is in your game. The main structure is made of the following folders:

### Prefab

* <mark style="color:orange;">**AI**</mark>:&#x20;
* <mark style="color:orange;">**Camera**</mark>: different cameras which are ready to use in your game
* <mark style="color:orange;">**Character**</mark>
  * <mark style="color:orange;">Attributes</mark>
  * <mark style="color:orange;">MoveSets</mark>
  * <mark style="color:orange;">Models</mark>
* <mark style="color:orange;">**GUI**</mark>: general GUI for health bar and damage number
* <mark style="color:orange;">**Player**</mark>: single player and multiplayer set up

### Resources

* <mark style="color:orange;">**AttributeLaw**</mark>
* <mark style="color:orange;">**EffectObj**</mark>

### Scripts

* <mark style="color:orange;">**AI**</mark>: a simple example for AI control logic
* <mark style="color:orange;">**Character**</mark>
  * <mark style="color:orange;">Abilities</mark>
  * <mark style="color:orange;">CustomActionStates</mark>: some frequently used special Action States (e.g. jump, dash)
  * <mark style="color:orange;">Locomotion:</mark> scripts related to character movement
    * <mark style="color:orange;">LocomotionMotor</mark>: locomotion motors used for different game mode (e.g. 2D, 3D)
  * <mark style="color:orange;">MoveSetTools</mark>
  * <mark style="color:orange;">StateModifier</mark>: pre-made modifiers with common usages
* <mark style="color:orange;">**CombatCore**</mark>: scripts for combat-related functions
  * AttributeLaw
  * CustomAttributes
  * EffectComponents
  * EffectFactory
  * EffectTransitionTools
* <mark style="color:orange;">**Editor**</mark>: scripts enhancing inspector's readability and usability
* <mark style="color:orange;">**Feedback:**</mark>
* <mark style="color:orange;">**GamePlayTags**</mark>:&#x20;
* <mark style="color:orange;">**GeneralTools**</mark>
* <mark style="color:orange;">**GUI**</mark>: implementation for some general UI functions
* <mark style="color:orange;">**Node:**</mark>&#x20;
* <mark style="color:orange;">**Player**</mark>: core player functions with input and camera
  * <mark style="color:orange;">Camera</mark>: scripts implementing different cameras
  * <mark style="color:orange;">Input</mark>: different controls for player locomotion input

***

## Demos


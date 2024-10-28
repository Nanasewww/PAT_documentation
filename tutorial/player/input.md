---
icon: gamepad-modern
---

# Input

Input Unit defines how Player Input is sent to character. For our native solution, we use Unity's Input System package as dependency since it has good controller supports and local muti-player solution. If you want to use old input system, you might need to override the player class and implement how tag is sent to character.

Expand the Input Unit's fold out, you will see this:

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

Tag: the input tag that shall send to character

Action Ref: what input action is bind to this unit

Hold Input: should this input be a press once trigger once event, or shall this be continuously triggered when holding the button

Input Buffer Time: if this input is currently not used to trigger any action, how long will it stay in the input tag list? This will make your game's input windows more graceful.&#x20;



Be aware that you shall only set one input tag to one input unit for the same player. If you want some more advance inputs like special commands/weapon input override, we will add documentation of the input addon class later.

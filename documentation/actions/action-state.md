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

# Action State

## Definition

An <mark style="color:orange;">**Action State**</mark> is the minimal state that describes a character’s action. It includes locomotion actions like moving, jumping, dashing, or any combat action like swinging a sword or firing a gun. It is the basic unit that adds up to the entirety of an action system in PAT. Action State by itself has very limited functionality, it is mostly a logic system that shows which state a character is in (what it is doing), and what it can do from the current state.

***

## Inspector Details

<mark style="color:yellow;">(All following description assumes the described Action State named as State A)</mark>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXe-p9tvInwbfoQp8LMyLjCDoIEDHaDRcylXHZL9gSJ2Ng6TdXtSXx0zXwBXnCYjkIvQaz5lsWVpso6T5qtv_RMOiS54QdOo5rrX8Ca2ua9ppGgoV2MWFda3aErm6aYY4dNn3pcszf02LAjjCRJc7zU_22U?key=wjgYipemgHjXa5pb_ZH-6A" alt="" width="563"><figcaption><p>Action State Inspector</p></figcaption></figure>

### Input Tag

<mark style="color:orange;">**Signals to trigger the State A**</mark>**.** For player controlled characters, it is decided by the Input Units on Player Component. \[PICTURE HERE] You can assign tags to player input, and everytime the character receives an input, it will try to trigger states using that specific tag.

### Can Repeat

If checked, State A <mark style="color:orange;">**can re-enter itself**</mark> if other conditions are satisfied (details below). Otherwise, re-entering the same state is prohibited by default.

### Auto Exit Time

State A will <mark style="color:orange;">**auto exit after this given amount of time**</mark>. By default it will enter Idle state. Or you may assign a specific Next State. If set to 0, it will not try to auto exit.

### Tags

<details>

<summary>Main Tags</summary>

The Tags a character will hold if it is in State A

</details>

<details>

<summary>Require Tags</summary>

After receiving the corresponding Input Tag, State A will check if the character is currently holding the Required Tags before entering. If not, nothing will happen.&#x20;

*   The relationship among outer Elements is logical **disjunction (or)**.&#x20;

    _As long as one element has all of its requirements fulfilled, this is considered to be true and the State can be entered._&#x20;
*   The relationship among inner Elements is logical **conjunction (and)**.&#x20;

    _All requirement tags must be present for it to be considered true, or the no requirement is checked._

</details>

<details>

<summary>Prohibit Tags</summary>

If another State tries to enter when character is in State A, but at least one of its Main Tags is listed in State A’s Prohibit Tags, it cannot be entered.

</details>

<details>

<summary>Self-Prohibit Tags</summary>

If the character is in another State and is currently holding any Tag listed in State A’s Self-Prohibit Tags, State A cannot be entered.

</details>

### Special

<details>

<summary>Permit State</summary>

Regardless of the prohibit / require relationship of tags, any State listed here is allowed to enter during State A.

</details>

<details>

<summary>Next State</summary>

Force character to enter the Next State after the exit of State A instead of idle. Notice that this only applies when State A is exiting by itself, not interrupted by the other state.

</details>






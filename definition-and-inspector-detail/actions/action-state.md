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

An <mark style="color:orange;">**Action State**</mark> is the minimal state that describes a character’s action. It includes locomotion actions like moving, jumping, dashing, or any combat action like swinging a sword or firing a gun. It is the basic unit that adds up to the entirety of an action system in PAT. <mark style="color:orange;">Action State by itself has very limited functionality</mark>, it is mostly a logic system that shows which state a character is in (what it is doing), and what it can do from the current state. Most functionalities are fulfilled by State Modifiers.

***

## Inspector Details

<mark style="color:yellow;">(All following description assumes the described Action State named as State A)</mark>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXe-p9tvInwbfoQp8LMyLjCDoIEDHaDRcylXHZL9gSJ2Ng6TdXtSXx0zXwBXnCYjkIvQaz5lsWVpso6T5qtv_RMOiS54QdOo5rrX8Ca2ua9ppGgoV2MWFda3aErm6aYY4dNn3pcszf02LAjjCRJc7zU_22U?key=wjgYipemgHjXa5pb_ZH-6A" alt=""><figcaption><p>Action State Inspector</p></figcaption></figure>

### Input Tag

<mark style="color:orange;">**Signals to trigger the State A**</mark>**.** For player-controlled characters, it is decided by the Input Units on Player Component.

<figure><img src="../../.gitbook/assets/image (2) (1) (1).png" alt=""><figcaption><p>Tag within each element is the Input Tag</p></figcaption></figure>

You can assign tags to player input, and every time the character receives an input, it will try to trigger states using that specific tag.

{% content-ref url="../../tutorial/player/input.md" %}
[input.md](../../tutorial/player/input.md)
{% endcontent-ref %}

### Can Repeat

If checked, State A <mark style="color:orange;">**can re-enter itself**</mark> if other conditions are satisfied (details below). Otherwise, re-entering the same state is prohibited by default.

### Auto Exit Time

State A will <mark style="color:orange;">**auto exit after this given amount of time**</mark>. By default, it will enter Idle state. Or you may assign a specific Next State. If set to 0, it will not try to auto exit.

### Tags

* **Main Tags**\
  Tags a character will hold if it is in State A
*   **Require Tags**

    After receiving the corresponding Input Tag, State A will check if the character is currently holding the Required Tags before entering. If not, nothing will happen.&#x20;

    *   The relationship among outer Elements is logical **disjunction (or)**.&#x20;

        _As long as one element has all of its requirements fulfilled, this is considered to be true, and the State can be entered._&#x20;
    *   The relationship among inner Elements is logical **conjunction (and)**.&#x20;

        _All requirement tags must be present for it to be considered true, or the no requirement is checked._
* **Prohibit Tags**\
  If another State tries to enter when character is in State A, and at least one of its Main Tags is listed in State A’s Prohibit Tags, it cannot be entered.
* **Self-Prohibit Tags**\
  If the character is in another State and is currently holding any Tag listed in State A’s Self-Prohibit Tags, State A cannot be entered.

{% content-ref url="../tag.md" %}
[tag.md](../tag.md)
{% endcontent-ref %}

### Special

* **Permit State**\
  Regardless of the prohibit / require relationship of tags, any State listed here is allowed to enter during State A.
* **Next State**\
  Force character to enter the Next State after the exit of State A instead of idle. Notice that this only applies when State A is exiting by itself, not interrupted by the other state.






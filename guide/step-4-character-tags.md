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

# Step 4: Character - Tags

## Goal

* Understand Tag System and how it forms a State Machine

## Review

So far, you've learned how Input Tags are used to trigger Action States and allowed the knight to attack. However, you may wonder <mark style="color:orange;">**how different Action States could be triggered by the same Player Input**</mark> (i.e. A light attack combo all triggered by left clicking). They are using the same input but should be different Action States. How do I control which State to trigger?

In this Step, we will discuss the <mark style="color:orange;">**Tag System**</mark> and the <mark style="color:orange;">**Dynamic State Machine**</mark> in Penguin Action Toolkit.

***

## Tag System

In PAT, Tags serve as tickets for the character to enter different Action States. Action States are triggered by corresponding <mark style="color:orange;">**Input Tags**</mark>, but they also request a list of <mark style="color:orange;">**Require Tags**</mark> in order to be entered. If they cannot find the required tags in [#tag-container](step-3-character-action-states.md#tag-container "mention"), the Action State cannot be entered.

<figure><img src="../.gitbook/assets/image (21).png" alt=""><figcaption><p>Attack1 requires character to have Idle Tag</p></figcaption></figure>

***

## Inspector

*   **Require Tags**

    After receiving the corresponding Input Tag, State A will check if the character is currently holding the Required Tags before entering. If not, nothing will happen.&#x20;

    *   The relationship among outer Elements is logical **disjunction (or)**.&#x20;

        _As long as one element has all of its requirements fulfilled, this is considered to be true, and the State can be entered._&#x20;
    *   The relationship among inner Elements is logical **conjunction (and)**.&#x20;

        _All requirement tags must be present, or the "no requirement" box is checked for this element to be considered true._

{% hint style="info" %}
_You can add new Tags into the Require Tags of Attack1, and you will find the knight unable to attack again._
{% endhint %}

After entering the Action State, the State will also grant tags to the character. All tags in the Main Tags field will be added to the Tag Container.

<figure><img src="../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

* **Main Tags**\
  Tags a character will hold if it is in this State

Apart from the things we mentioned, there are other usage of Tags to control state transitions. You can find the following fields in the inspector of Action State components.

* **Prohibit Tags**\
  If another State tries to enter when character is in State A, and at least one of its Main Tags is listed in State A’s Prohibit Tags, it cannot be entered.
* **Self-Prohibit Tags**\
  If the character is in another State and is currently holding any Tag listed in State A’s Self-Prohibit Tags, State A cannot be entered.

***

## Further Reading

You may find full documentation on Action State's inspector details by the following link. It is quite useful when creating your own Action State.

{% content-ref url="../documentation/actions/action-state.md" %}
[action-state.md](../documentation/actions/action-state.md)
{% endcontent-ref %}


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

# Use Attributes

## Attribute Usage

### Related Modifier

To use [Attribute](../../documentation/attribute.md) for one action, you may attach <mark style="color:orange;">**UseAttributeMod**</mark> to an Action State and choose the attribute through Resource Tag.&#x20;

{% hint style="info" %}
_Typically, the current attribute amount needs to be <mark style="color:orange;">equal or greater</mark> than the required Amount for this action state to be triggered._
{% endhint %}

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdjSOhcEbCz24BktSGry0h0TY48pv3zY-ASBryxki_D79F2hu6VlkxLRW5NF8Nde-6Bx9Pyt4jVS1HYNkI2GUamX4Uw8jQ2G1p0kA6NTiZmW0Ax0ZSJXVTun1OSsSseDp-BlZ4jNn3kz56F2_5lB1ivtVD9?key=Rv96SXV0rCMH8N9lwXnGWw" alt=""><figcaption><p>Use Attribute Mod inspector</p></figcaption></figure>

<details>

<summary>Resource Tag</summary>

Choose the resource tag that is bound to the attribute.

</details>

<details>

<summary>Amount</summary>

How much a character needs to cost for entering this state. This amount will be subtracted from the current amount.

</details>

<details>

<summary>Can Over Use</summary>

Even if the current attribute amount is less than the required amount, as long as it is greater than 0, it can still be triggered, and will set the current amount to 0.

</details>

<details>

<summary>Be Recovery</summary>

If checked, the specified attribute will not start its recovery while the Agent is still in this Action State.

</details>

### Learn by Doing

{% content-ref url="../action-state-and-modifier/task-3-cost-mana.md" %}
[task-3-cost-mana.md](../action-state-and-modifier/task-3-cost-mana.md)
{% endcontent-ref %}

***

## Attribute Recovery

1. You may set auto recovery through the attribute component.
2. For other ways of recovery, you probably need to write an Effect for it.

TODO








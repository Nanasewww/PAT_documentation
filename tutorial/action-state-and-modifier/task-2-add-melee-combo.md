---
icon: circle-chevron-right
hidden: true
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

# Task 2: Add melee combo

PlayerRabbit can now perform a melee attack, but having only one attack feels a bit limited. In Hierarchy, under MoveSets/\[==RabbitGun==]/MeleeAttack, you can find three different melee attacks. Let's try using them to create your first melee combo!

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXegSYFc66zk3CXKOqsOQjPbNvGPZbfAfBqk1tyCy7BwNPcC25Dk2-tbDYzJVMdmuHSw1dEnV1th8ew150Q5omGC4-ADNVJIcDkJnMnbHwn3nXznFaas7xZfZ1i9gDn728bsxZpxLlyT1zx8pkr_gcZZ8SY?key=p_nH-JdSTTyX01UFeuszxg" alt=""><figcaption></figcaption></figure>

To ensure these melee attacks are triggered in the correct sequence, we need to add entry conditions for each attack. On the GameObject for MeleeAttack1, there is a Modifier called GrantTagMod. This Modifier ensures that, during a specific period of the Action State, the character's tag container possesses a certain tag. By using GrantTagMod, we can add Chain1 tag just before MeleeAttack1 exits, preparing for MeleeAttack2 to trigger.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcJBuphojXWE2p-e0UsMbiLqkJm-oLaWWWmqFSfGqdMl_thlGWIynz8CJltAe-YDp24ag7Nr0jroB39B19B7Ay00WhQmb7DPonsNQYQMZc_1LeFaihHGLqpCT55WUetc9fydsU6CPppehDHZCw5TXll3zNl?key=p_nH-JdSTTyX01UFeuszxg" alt=""><figcaption></figcaption></figure>

An Action State's trigger conditions can be thought of in two parts: detecting the corresponding input and verifying that the character currently holds the required tags to trigger the action.&#x20;

The Input Tag represents the input needed to activate the action, and once met, it checks the validity of the current state. It will check if the character is currently holding the Required Tags before entering. If not, the entry will be canceled. While the character is in this action, they will hold all the tags listed in the Main Tag.

* The relationship among outer Elements is logical <mark style="color:orange;">**disjunction (or)**</mark>. \
  As long as one element has all of its requirements fulfilled, this is considered to be true and the State can be entered.&#x20;
* The relationship among inner Elements is logical <mark style="color:orange;">**conjunction (and)**</mark>. \
  All requirement tags must be present for it to be considered true, or the no requirement is checked.

We add Chain1 to the Required Tag for MeleeAttack2. This means MeleeAttack2 can only be triggered after receiving the LightAttack input and when the character holds the Chain1 tag, ensuring it follows MeleeAttack1. With this setup, we've created a simple attack combo.






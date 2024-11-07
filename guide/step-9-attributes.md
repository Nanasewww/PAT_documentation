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

# Step 9: Attributes

## Goal

* Understand what Attributes are.
* Understand how Attributes  are consumed / recovered in PAT.

***

## Attributes

<mark style="color:orange;">**Attributes are the stats a character can have**</mark>, such as health, resistance, attack and stamina.&#x20;

Each of them is stored in an Attribute Component under the Character object or under its children.

<figure><img src="../.gitbook/assets/image (55).png" alt=""><figcaption><p>Health Attribute of knight</p></figcaption></figure>

At runtime, Character component will <mark style="color:orange;">**automatically collect all the Attribute Component under it**</mark>.&#x20;

Obviously, we don't want the attribute to stay at the initial amount forever. We want to modify the value during gameplay. How can we make that happen?

## Resource Tag

In the previous articles we talked about how Tags[^1] are used to trigger and validate Action States. Apart from that, there is another usage of Tags.&#x20;

We use <mark style="color:orange;">**Resource Tags**</mark> to label attributes. For example, the Stamina Attribute on the knight has a resource tag of Stamina.

<figure><img src="../.gitbook/assets/image (56).png" alt=""><figcaption><p>Resource Tag: Stamina</p></figcaption></figure>

<mark style="color:orange;">**With a resource tag set, an Action State can use the tag to find its attribute.**</mark>

Let's look at the locomotion move set of the knight.

<figure><img src="../.gitbook/assets/image (57).png" alt=""><figcaption><p>Go to the Main Move Set</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (58).png" alt=""><figcaption><p>Go to Roll</p></figcaption></figure>

In the inspector of Roll, we can see another modifier: <mark style="color:orange;">**Use Attribute Mod**</mark>.

<figure><img src="../.gitbook/assets/image (59).png" alt=""><figcaption><p>Roll - Use Attribute Mod</p></figcaption></figure>

You can see it also has a Resource Tag field, and it is pointing to Stamina. This makes Roll Dodge costing Stamina every time it gets triggered. You can control the amount being cost in the mod as well. If you set the number to be negative, you will find it recovering attributes instead of consuming it.



[^1]: Hopefully you haven't forgotten about Tags.&#x20;

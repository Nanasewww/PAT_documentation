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

# Practice 2: Cost HP

## Goal

* Make Attack 2 costs HP or a new attribute you add.

***

{% hint style="info" %}
_This is not a hard challenge._ \
_You may try to do it on your own first and then come back for the answer._
{% endhint %}

## Solve

* Add Use Attribute Mod to Attack2.
* Select the Resource Tag to Health.
* Set an amount.

<figure><img src="../../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>

Now every Attack2 will take out 20 HP of the knight.

***

## Attribute in Inspector

If you are adding a new Attribute, and it is not on the UI, you might wonder how to check if it is correctly consumed.

You may go to the Character Component. It will display all the attributes it collects at runtime. You may even modify the value from there directly. If can be a helpful tool for debugging.

<figure><img src="../../.gitbook/assets/image (61).png" alt=""><figcaption><p>Character component on the right</p></figcaption></figure>


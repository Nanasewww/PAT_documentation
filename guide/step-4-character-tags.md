# Step 4: Character - Tags

In the last article, we covered how Input Tags are used to trigger Action States. You may ask: What if I want different Action States triggered by the same Input (i.e. A light attack combo triggered by button X on your controller), how do I control what is the right State to trigger?

In this article, we will discuss the Tag System and the Dynamic State Machine in Penguin Action Toolkit.

***

## Tags

When you start the game, you can find a Tag Container Component Attached to the character object. Note the Tag Container is only added to character at run time. It shows what Tags the character is holding. If you don't move at all, you will find the character holding an Idle Tag.

TODO: PIC

You may think of Tags as tickets for the character to enter different Action States. Action States are triggered by corresponding Input Tags, but they also request a list of Require Tags in order to be entered. If they cannot find the required tags in Tag Container, the Action State cannot be entered.

TODO: PIC

*   **Require Tags**

    After receiving the corresponding Input Tag, State A will check if the character is currently holding the Required Tags before entering. If not, nothing will happen.&#x20;

    *   The relationship among outer Elements is logical **disjunction (or)**.&#x20;

        _As long as one element has all of its requirements fulfilled, this is considered to be true, and the State can be entered._&#x20;
    *   The relationship among inner Elements is logical **conjunction (and)**.&#x20;

        _All requirement tags must be present, or the "no requirement" box is checked for this element to be considered true._

{% hint style="info" %}
You can add new Tags into the Require Tags of TODOMELEE, and you will find the character unable to attack.
{% endhint %}

After entering the Action State, the State will also grant tags to the character. All tags in the Main Tags field will be added to the Tag Container.

TODO: PIC

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


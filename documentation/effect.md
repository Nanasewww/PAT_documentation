---
icon: reflect-horizontal
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

# Effect

## Definition

<mark style="color:orange;">**An Effect is a ScriptableObject that can be applied to a Character.**</mark> In PAT, Effects control various logic such as damage, knockback, and more.

By default, an Effect has main tags. Once applied, it grants the tags it holds to the character, and these tags are removed when the Effect is removed.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfZOeNVaKSpec6KTW7GqSrjCktqIGfpOLes_8SpRn8WnKcv-8OsKVvLAqJzZSzSJUKQxyyNicUOdm2GqrweEDxZAYHcCh6g4WJ3H6yLA7T97C3OIbwE6zw1FTXQsnGUA2zmNpSdjxq42T-O1ZqJxOJU_d8V?key=wjgYipemgHjXa5pb_ZH-6A" alt=""><figcaption><p>Example: Chain1 Effect</p></figcaption></figure>

Effects also have components that modify their behavior in different ways. You can add an Effect Component by selecting a class from the dropdown and then clicking the 'Add Component' button.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfWcpzZW0_JJvZAJ1E-yzASSmQkHgLp2mOKJU5rMS0oDrtUYmqPXo-sTZ_IEvsWnONCl6Vi54jTvtmcdmN0NsTqhI2NZXURHp5-5qwV-ik24yMnkGTREoxAwfhalQrvxWMWD8XRHk0EDECSj1mhoXtCQm4?key=wjgYipemgHjXa5pb_ZH-6A" alt=""><figcaption><p>Select a component to add</p></figcaption></figure>

***

## Inspector

Currently, there are two types of Effect components implemented in PAT: Effect Life Control and Effect Mod Value.

## Effect Life Control

This component controls <mark style="color:orange;">**how long the Effect will remain on the character**</mark> on its own. It's a useful tool when you don't want to manage the Effect's lifespan manually.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeC7AM4ZvSlxxBtqh_tlTtSoETxOadl4pBefrGRRUjgkf_K9tTuUTpzKDSoLvLflpLwIzJx7doSpK560mS9Nv9J_ObpNg-yDJ24kk5sBHhiaFCK82fR2BaLPkx0cD2w0Fb0cgjvwxp3cGPCLQeox7GAkXU?key=wjgYipemgHjXa5pb_ZH-6A" alt=""><figcaption><p>Effect Life Control inspector</p></figcaption></figure>

## Effect Mod Value

This component <mark style="color:orange;">**influences the values of Attributes in various ways**</mark>. We will cover the details of Attributes later, but for now, it’s important to know that HP, Mana, Posture, Defense, and similar stats are all Attributes in PAT. Controlling Attributes generally means managing every non-action aspect of the game.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXevO7zc68Hcp0_rTMHf1Z9HISORp0_tG4LzD7BUsHlovDHO5wiCso0WDmK5_pJOu42UZRlAwUZtVFvTOfteXcpV0EFHCHR4PVzzprwSfSjlduhVQc3DZp52FYMF1TYCn9DuNc0GIRPAhq3IIi5_JjNgkbQ?key=wjgYipemgHjXa5pb_ZH-6A" alt=""><figcaption><p>Effect Mod Value inspector</p></figcaption></figure>

### **Resource Tag**

The Effect Mod Value will search for <mark style="color:orange;">**an Attribute with the same tag**</mark> and influence it.

### **Mod Target**

Specifies <mark style="color:orange;">**whether it modifies the Attribute's value or the auto-recovery rate**</mark> of the Attribute.

### **Mod Pattern**

* **To Base Value** \
  Adds or subtracts from the actual base value, commonly used for damage, mana, or stamina.&#x20;
* **Add** \
  Increases or decreases the final value but will no longer influence it once the Effect is removed. This is useful for buffs like a speed boost.
* **Add Multi**\
  Multiplies the value. Multiple Add Multis will stack together before the calculation. Similar to Add, it will no longer influence the final value once removed.
* **Final Multi**\
  Unlike Add Multi, this does not stack. It multiplies the value directly.
* **Override** \
  The value is directly replaced by the override value and will no longer influence the final value once the Effect is removed. Useful for effects like reducing movement speed to zero.
* **Level** \
  Not used by default, but you can implement special logic by overriding the Attribute class.
* **Order** \
  Determines the priority between multiple Effect Mod Values. If both have the same order, the most recently added Effect will take precedence.&#x20;

\



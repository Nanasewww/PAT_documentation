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

# Practice 1.1 & Ex: Grant Tag Mod

Here's one example of Mods. We have already discussed how Tags are granted to the Character through Main Tags of Action States. But sometimes we don't want certain Tags to carry through the entire State. For example, in our practice, if you add "Chain 1" into Main Tags of Melee1, Melee2 can override Melee1 immediately. If you want a start-up phase that cannot be cancelled, you can add this Grant Tag Mod under your Action State, set the Tags and Begin Time. Now the character will only have "Chain 1" in its Tag Container after 1.5s.

<figure><img src="../../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

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

# Task 1: Change action speed

PlayerRabbit can perform a cool slashing move by pressing the left mouse button. However, if it feels too slow, how can you speed it up?&#x20;

Take a look at the Modifiers attached to Melee1—there’s one called Montage Speed Mod that can help you modify the slash speed.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXchhrPUkM-jDTxAgAk04TcxqKKjyaIUUWaesdXZce6TIjj1Tt7ruEVEnJ75UzCpUFsdUZtHFW0tLOlwKKt0lmwj-CIWGToAG-oXkmG1ZND9Y_1pTYk_J1xQ8LNzo1xtjxBm3vIJmcnbQlojvdZqeMYSVxk?key=p_nH-JdSTTyX01UFeuszxg" alt=""><figcaption><p>Montage Speed Mod inspector</p></figcaption></figure>

Montage Speed Mod is a Modifier used to adjust the animation speed by modifying the MontageSpeed parameter in the Animator. Changing the value from 1.5 to 3, the slash speed can be significantly increased.&#x20;

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeFxHj47OjhEuRVrM8ajpPsWwWLuAK4-dJGeOlO3X2tokwEOQ0yBYF3EWGLi_XYY49hRDAx51NEVr7XXHAian9VWFapt4ncF6g9292nUGzC68n0zNg0XYk58ozF5vXfhVoINimBy0FGJhv9YejiOsj2tcgG?key=p_nH-JdSTTyX01UFeuszxg" alt=""><figcaption><p>Auto Exit Time in Actin State</p></figcaption></figure>

After speeding up the animation, you may notice that the character will pause in place after performing a quick slash. This happens because Melee1 is an auto-exit Action State, and during this Action, the player cannot control the character’s movement. By reducing the Auto Exit Time (0.9 -> 0.5) in Action State, we can make the character exit the Action earlier to avoid this pause.






---
description: 'Written by: Yuanheng Qu'
---

# Victim or the Crime

When the character you control does a brutal attack to a penguin, your character has its stats of attack damage, posture damage, knockback attribute, perhaps also critical damage and other special addons that modifies the amount of damage. When the penguin gets hit, it also reduces the damage based on its defense, hit point, thickness of leather and other reasons. If you are fighting a real penguin in Antarctica, laws of nature will handle that for you. All you need to consider is how to punch the penguin (please don't). But if it is a game, unfortunately, some one must deal with all the numbers for the body beneath the feather can be correctly damaged.

In the early stage of the project, we believed the receiver of damage (or other effects) should be responsible for calculating everything. If we do it the opposite way, the sender needs to send the signal first, get all the attributes it needs from the target, calculate the math, and send everything to the target once more. Does not sound efficient at all. So, we let the receiver handle that. In an attempt of attack, the attacker sends all the information to the receiver, and the receiver applies everything to itself. There's no need of sending information repetitively.

If the game does not involve complicate effect exchange, maybe that is the end of our problem. In our first demo, we had knockback and posture damage, which is all performed by a simple minus calculation. The simplicity makes it easy to handle. But, if the designers want something more complicated, e.g., The attacker will restore HP based on the final damage (after defensing), a single-time information exchange is not enough, because the attacker only knows how much damage it should deal, not how much damage is actually dealt. Should we exchange the information once more in that case? In another example, we want a different damage calculation formula for certain cases, how can we expand a logic that was written in the receiver's code? The former solution matched our intuition, but it is not flexible enough. Thus, how can we exchange the information in a simpler and more straightforward way?

The fact is, in the scenario we set, one important participant was ignored. When a ruthless character hurts a penguin, damage is not sent directly from character to the penguin. There exists a transmitter called Effect Package.

In PAT, characters (more precisely, PAT Components) record all its stats (health, defense, attack, etc.) as Attributes. PAT Components send Effects to modify Attributes on other PAT Components. Effect knows which Attributes to modify by what value. Receivers will then apply the Effects on themselves. In other words, when we talk about the damage dealt on the penguin, we are not only discussing you and the penguin, but also the Effect or Effect Package (multiple Effects) between you. Their job is to carry the information from one end to the other. What is the information for? They don't care.

The key towards the solution, is these carriers. We force them to take more responsibility than just sending the information. They know who the sender is, as well as who is the receiver. So, they have the right to calculate attributes collected from both sides. Next step is, how do they know what to calculate?

With such demand, a scriptable object named Attribute Law was born. Attribute Law contains: Resource Tag pointing to a specific Attribute, some Tags for recording, and the calculation formula towards the Attribute. When the sender sends out an Effect Package, all the Effects inside that Package will search for the Attribute Laws that should influence this transmit. The data is processed within the Package, and the outcome will be sent to both sender and receiver. There, they all know what actually happened after the calculation.

With the birth of Attribute Law, we no longer need to change code on receivers when we want a different logic. We just apply a different Law. "Should the victim or the crime be responsible for damage calculation?" We were fooled by this false question for a long time. But now, someone will actually be responsible for the penguins that are hurt.



11/3/2024

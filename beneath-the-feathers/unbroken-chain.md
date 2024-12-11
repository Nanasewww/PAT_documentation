---
description: 'Written by: Yuanheng Qu'
---

# Unbroken Chain

Our semester ends with a Game Jam. We were expecting that.

Certainly, we have additional work for its preparation, which includes the reconstruction of the AI system. But our work should end there. There was a consensus before the game jam among the team. But when you put enough time into something, you might always encounter some unexpected situations. But allow me to start with what we did with the AI.

In the past, we had an AI system, and both the enemies and friendly minions were driven by it. In different iterations of demos, people find it working properly. But, for Wuji, who is the designer of that AI system, it was not a beautiful structure. Those AIs were done before PAT had its final structure, which left them utilizing limited PAT functionalities. They were lacking extensibility and reusability. We were then considering the Game Jam as a fair opportunity to both fix the AI and end the semester.

There was a long conversation arguing how to design good AI. Two diverging thoughts emerged. First is we design the AI based on spontaneous nodes, with each node trying to trigger itself once permitted. That's how Action States were processed. It also fits into our intuition. Wuji, however, had something else in his mind. He claimed that we should separate AI from a PAT character. The AI nodes should be completely decoupled from Action States. It allows the AI to obtain more modularity, and it avoids the scenario where an AI system can only serve one character. In his idea, AI should only try to reach a node that is connected to the node taking effect. Transitions are handled by a centralized brain, not by each separate node.

With this new design, it improves the flexibility and decreases the cost of computation ("Although it really saves nothing comparing with the cost of rendering", Wuji said). This framework was finished in two days. Not too long cause it wasn't that complicated. We started with the Interfaces and Abstract Classes which were later extended. The extension took a bit longer, but gave us a brain, a template of nodes, conditions for nodes to be entered and exited, and behaviors for nodes to execute. Later, they were applied to the robots fighting a rabbit on the moon for bug fixing. Finally, the Unity Robot Kyle (who was also the boss character in our game jam) learned how to fight like a master.

Now it seemed like we should just hold the game jam and prepare ourselves for the winter in Pittsburgh. But there are always coincidences when you prepare yourself for the possibilities. Sometimes they aren't very appealing. But we were lucky this time.

When Wuji was editing the animations of the boss, he wondered about the real industry pipeline. We heard rumors of large companies using Timeline for editing attacks. But we had used Timeline before, and we all knew it wasn't a friendly tool. You cannot even preview the VFX or animation. We assumed the companies made modifications to it so the Timeline can be somewhat more usable. It is natural that you cannot easily find anything like that online. Still, with some time devoted to internet surfing, Wuji find a handwritten Timeline. Although it had zero documentation with no examples, the sample picture caught his attention. We had no idea of how long it would take to build up the entire thing, so he gave it an evening, which leads to the birth of Action State Timeline.

On the exact morning of Game Jam, a rough but usable Timeline was added to the package. Now an Action State with different State Modifiers can be presented in the timeline window. The users may help themselves with dragging the blocks to adjust the effect timing of different Modifiers and preview the State without starting the game. It was almost sufficient to replace the Animation Events. The design of State Modifiers naturally allows us to present them in the form of a timeline. Because, we decided to add a timing attribute to all State Modifiers when we were doing the 2D prototype Pen-stleVania.

We recognize the Action State Timeline as a game changer of PAT. It lowers the learning curve of the entire system significantly, and allows users to adjust Action States without much explanation. It was born from so many choices that we never expected them to lead us here: If we weren't using the animations from a partner, if we weren't holding the Game Jam, if we didn't add time to all State Modifiers. All the stories sown along the way guided us to push PAT further and even further at the very end of the project. How far can we get to in the future? Only the future can tell.

This is the very last story of Beneath the Feathers. Special thanks to everyone who has used PAT.

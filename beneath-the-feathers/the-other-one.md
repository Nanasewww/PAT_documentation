---
description: 'Written By: Yuanheng Qu, Edited by: Yanchen Hu, Wuji Cao'
---

# The Other One

The power of Penguin Action Toolkit (PAT) can be brought into play on action game development, sometimes even beyond people's imagination. This is what we claimed during advertising. In fact, it keeps surprising us, the developers, throughout the process of coding and testing. A few changes inside Unity Inspector allows a Soul-Like game turn into a resource management game where character loses HP when moving. The players are running and dying at the same time, how exciting is that? The more exciting fact is: we did not design PAT for such a detailed use case, yet it grants the ability for playtesters and game designers to bring their whim and inspiration into reality. Because of that, we believe: these illuminating moments must be recorded, and they shall not be forgotten just because this project will eventually come to an end. Therefore, a series of blogs, Beneath the Feathers, a tribute to Dota2's Between the Lanes, is now born.

In these blog posts, we will review certain cases from our development, try to bring all those decisions, aspirations, and technical details of PAT to the public. Tell the problems that were solved, share the moment that sparked. We hope these stories that are as amusing as video games themselves can be a part of PAT. It doesn't matter if you will be using PAT to make your own action game, you may always find some joy from these posts.

"Does our framework support multiplayer?" That's a very interesting question. During past internal tests, we tacitly assumed the toolkit is built for classic single-player games. From there, we had rabbit running over the moon and a robot diving into Castlevania. A single player controls a single character.

When the question was asked, we could not just provide an answer. PAT uses a special input system. An input from the player is presented to the Player Component that controls the character, and it will turn the signal into a special Input Tag in order to trigger different Action States. How do we distinguish different inputs and bring them to the correct character? That's the problem we needed to figure out. We don't want to neglect the possibility, where two penguins -- or even more penguins -- can hold their hands (or flippers) and march forward together on the same screen. We should try it. Perhaps someday, someone will use it for some fun ideas. So we spent some spare time verifying whether PAT allows the existence of two controllers.

We started by the attempt of finding usable API that sets a corresponding player for each Input Action. It is the instinction of us. If Unity provides that, we can use it, and the problem is solved. We had no find even after we dived into the source code of Unity itself. But we did manage to find some very interesting messages:

It is a good notice for us: even Unity has in-developing stuff. The engine developers of Unity are confused and tortured by all kinds of problems just like us. All human are treated equal, in that perspective.

Giving up on searching for APIs, we turned to a more formal pipeline. Unity actually has this pipeline for multiplayer game controlling schemes. Two Components, Player Input Manager and Player Input, allow us to distinguish different inputs and bind them with different characters. We did not use the pipeline until now. What we used is a Script called Input Manager that exists on some Game Object. It decides everything for us. This was a habit from the past experience of making indie-games and game-jam games. After all, if there is only one player, Input Manager seems sufficient enough.

So, how difficult it is to adapt our system to this formal pipeline? It wasn't hard to do the moving part. Soon we have two robots running left and right in the Castlevania world. But it was not so easy to make the second character jump and attack.

Here we need to bring up how Unity's Player Input Component actually works. The component has four behavior options. Send Message, Broadcast Message, Unity Event, and C# Event. The first two Message behaviors require us to provide functions named after required names. Any modification on the names will cause the system fail to operate without any warning or error from Unity. Unity Event is what we have been evading, because it makes Unity Inspector do the work that should be done in the code, and it leads to chaotic logic chains that are hard to tackle. So, the only option left was C# Event.

C# Event has its own disadvantage: we will have to do String comparison for the inputs. Every time we detects an input, we need to compare the Action name to the Actions that exist on its Action Map. We were not excited to see a lot of String comparisons, but at least the Strings that were used are from the Action Asset -- it makes it a lot more stable than using Messages. Perhaps there exists a solution that is better than this, but none of the four behaviors is perfect, so we have to settle for less. With some extra code, inputs other than moving were passed to the correct character with String comparison. Finally, two robots were taking their adventures together.

Or they might be killing each other.

This change of Input System pushed PAT forward from two sides. First, it's capable of even more things. We had never considered if it should support multiplayer, and now it already does. Second, the structure of our Sample Scene is more formal (or at least from Unity's own perspective). For developers that will use PAT, they can now see the standardized structure from our sample. In the end, after series of attempts, we proved PAT allows multiplayer. It went beyond our expectation, once more. Will someone use it to build a multiplayer game? Who knows. Maybe we should do it ourselves.

Hopefully these paragraphs and pictures brought you some joy. It is an exploration over PAT. What can it do? What should it do? We keep asking ourselves those two questions. The former one proves its capability, the latter one guides us to design it better. In the next blog post, we will probably discuss the latter question: What is PAT designed for?



9/30/2024

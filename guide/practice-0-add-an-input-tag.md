# Practice 0: Add an Input Tag

## Goal

Use Input Tag to allow the knight performing other attacks.

***

## Task

You might have noticed this: there exists two attack objects in the move set prefab.

<figure><img src="../.gitbook/assets/image (29).png" alt=""><figcaption><p>Attack 2</p></figcaption></figure>

Attack 2 and Attack 1 are almost identical, but only Attack 1 is triggered when you left click your mouse.

The reason is simple: Attack 2 does not have an Input Tag. No matter what button you clicked, it will never be triggered.

So now let's try to add an Input Tag to this State.

<figure><img src="../.gitbook/assets/image (30).png" alt=""><figcaption><p>Input - lightAttack</p></figcaption></figure>

Select _light attack_ Input Tag from inspector.

Now run the game. You should find the knight attacking with a new animation when you left click / press west button.

***

## Question




# Step 7: Trigger Animation Event

## Goal

Understanding how Trigger Animation Event is used for controlling State Modifiers

***

## Trigger Animation Event

If you go to the knight object in the scene, open the animation panel, click on the dropdown menu, you should see the following stuff:

<figure><img src="../.gitbook/assets/image (45).png" alt=""><figcaption><p>Animation Clip</p></figcaption></figure>

If you click onto 1H\_Melee\_Attack\_Slice\_Diagonal, which is the animation clip for Attack1, you should see the following:

<figure><img src="../.gitbook/assets/image (46).png" alt=""><figcaption><p>Attack1 animation clip</p></figcaption></figure>

You might have noticed the 4 labels on top of the properties. You can click onto them, and the inspector will look like:

<figure><img src="../.gitbook/assets/image (47).png" alt=""><figcaption><p>Animation Event</p></figcaption></figure>

As the name suggests, these are the Animation Events that are used in Timing Attributes of State Modifiers. The Int in the inspector is for the Begin Index and End Index. We _**HIGHLY RECOMMEND**_ ordering the events in ascending order, so it will not cause any potential problem.

If you want to add an event, click the circled button:

<figure><img src="../.gitbook/assets/image (48).png" alt=""><figcaption></figcaption></figure>

In the inspector view of the animation event, you need to select the following method:

<figure><img src="../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>

This method is provided by Model Handler attached to the same object as Animator

<figure><img src="../.gitbook/assets/image (50).png" alt=""><figcaption><p>Model Handler</p></figcaption></figure>

If you added your own Animation Event, remember to set an Int and drag it to the correct order

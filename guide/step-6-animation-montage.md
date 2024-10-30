# Step 6: Animation Montage

## Goal

Understanding Animation Montage Mod, getting familiar with the Animation Controller

***

## Animation Montage Mod

Animations are attached to Action States by Modifiers. We provide you this Animation Montage Mod for you to bind an Animation State from your Animator to an Action State.

<figure><img src="../.gitbook/assets/image (41).png" alt=""><figcaption><p>Animation Montage Mod on Attack1</p></figcaption></figure>

A blank Animation Montage Mod will look like this:

<figure><img src="../.gitbook/assets/image (42).png" alt=""><figcaption><p>Blank Animation Montage Mod</p></figcaption></figure>

Dragging in the Reference Animation Controller of your character saves a lot of time for enabling the dropdown menu. We recommend doing that for your future projects.

## Animator

If you go to the current animation controller, which is the HumanoidCharacter, you can find the following view in Animator Panel. Different animation states are categorized on different layers. To find the animation state for your Action State, you should select the corresponding layer, then select the desired animation state.&#x20;

<figure><img src="../.gitbook/assets/image (43).png" alt=""><figcaption><p>Animator</p></figcaption></figure>

When you can see the Animation Clip field tied with a specific clip, it means now the Action State will automatically play that clip when entered.&#x20;

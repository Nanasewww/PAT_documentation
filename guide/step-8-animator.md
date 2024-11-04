# Step 8: Animator

## Goal

Understand how PAT controls animation.

***

## Dynamic State Machine

As we mentioned earlier, PAT uses a dynamic state machine to control the character. You do not need to connect all your animation states in the animator to make transitions. It keeps the animator simple and clear. You only need to put them on the correct layer, then call it from the Animation Montage Mod.&#x20;

## Weight

This is more of a Unity problem instead of a PAT problem. However, we have seen questions about this so it might be better if we mention it here.

<figure><img src="../.gitbook/assets/image (54).png" alt=""><figcaption><p>Weight</p></figcaption></figure>

Each layer in the animation has a weight. You can see that by clicking the gear icon. When a new layer is created, Unity sets its weight to 0. This means other layers will override it. Don't forget to change that.


# Change to Your Own Model

## Q: How do I swap the character model in the given template

{% hint style="info" %}
The given template uses animation clips for humanoid character. If your model is not humanoid, you need to change the animator as well.
{% endhint %}

## Answer:

{% stepper %}
{% step %}
### Import the asset


{% endstep %}

{% step %}
### Find the Model Container, drag in your model, disable the old one

<img src="../.gitbook/assets/image (2).png" alt="" data-size="original">
{% endstep %}

{% step %}
### Select the Controller to the corresponding animator

<img src="../.gitbook/assets/image (3).png" alt="" data-size="original">
{% endstep %}

{% step %}
### Add a model handler

<img src="../.gitbook/assets/image (4).png" alt="" data-size="original">
{% endstep %}

{% step %}
### Under the character script, change the character model reference

<img src="../.gitbook/assets/image (5).png" alt="" data-size="original">
{% endstep %}

{% step %}
### Create a socket for weapon (if needed)

<img src="../.gitbook/assets/image (6).png" alt="" data-size="original">
{% endstep %}

{% step %}
### Set the socket to weapon move set

<img src="../.gitbook/assets/image (7).png" alt="" data-size="original">
{% endstep %}

{% step %}
### Adjust the Hurtbox collider if doesn't fit


{% endstep %}
{% endstepper %}

Now your new model should have the exact same functionality as the old one.

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

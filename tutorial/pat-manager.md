---
description: An editor we provide to help visualize the PAT character structure
icon: merge
---

# PAT Manager

The PAT Manager will display a PAT character as a node graph, displaying all the MoveSets, Action States, Tags related to the states, and State Modifiers that compose this character. This editor will be extremely useful when creating a complex character or understanding the logic of an existing character.\


We also provide some convenient functions like selecting corresponding GameObject, drag-and-drop to attach scripts, synchronizing node deletion and creation, and etc. The paragraph will show all the usages of this editor.&#x20;

***

## How to display a PAT character

{% stepper %}
{% step %}
### Create an empty Node Graph

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXciibUwzFKH8bio_sOP89XqA7tyJZBSxTAc1-YFZHqUQSAu9YXCYWZvkwoXseb2p1-HDVPKUROYjQhqI8RBa967HovqMIoAm8xK0ODTYVu_L8Zbw6KfdansxFIFr8yad132uJxW?key=FgW71u4vKTVODEVBYPADR_E6)![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe6d806mTQYqSDo2Cm7kW6Hb4gjEaPkaM0SyWpzeJXs8mDfaprMx0hAKgqoaJkezHggK0YQYUlz5fqSdWLhx9bHPepERFocFuLwIoKlKp7VO9VToOgiIZOB7w9gWs61paD9aeIfOQ?key=FgW71u4vKTVODEVBYPADR_E6)

Go to the folder you want to save the node graph and right click, you can find the PAT\_Node Graph in the create panel. After clicking, you will see a PAT\_Node Graph successfully created. You may rename it whatever you like and it will then be saved.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXch5Bgo7L_iEtv7LPY95bbakzqfKGKiYd40R-TP3aH5tR6fjjP_op-tEJXOVib2B11WzqKIBXybkNoKrRj0OSGNGGy5Fc4sQmjO31Lej9ZDxRYBbfAEZy_UPdnNJkk7I3p1ps7YRw?key=FgW71u4vKTVODEVBYPADR_E6)
{% endstep %}

{% step %}
### Find the character and attach the required script

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf07_H9xbXnafzHryx0p4bmXgVwz_UF5XAkHMIeEtztou9BkaysfmT1vtoji7wqm6RotzUwQjIx7OTa-ohic9g2FO2c3BT9CY1J7g8ssiMxrs3gTyBfyH6dRaHPU2OyKbZeP-n1Rw?key=FgW71u4vKTVODEVBYPADR_E6)

The PAT\_GraphRunner is required to use the editor. Simply drag and drop it on the desired character.&#x20;

<mark style="color:red;">IMPORTANT: It should be dragged on to the GameObject that has PATCharacter Script attached, so that it can be recognized as a PAT character.</mark>

<img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeQxqN80lE3EO7uYR0jNoraDORV-r-gCf4iZIkWTL7xx0IokWiVO87vkltCRtUS0VUN8sBStQx6q4XNq-oiaeTm0kcd-8e08WvBwrKV8i_EHo1xQjrLrm4Yi650qQpAo5UmYHHXlA?key=FgW71u4vKTVODEVBYPADR_E6" alt="" data-size="original">

You should be able to see this after the script has been attached. Now drag the PAT\_Node Graph you just created into the slot.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXddq_aWcqoFn0toPIMFlOaSp9ADgzaKPC1pCSxfNdZQ7vsXvb7KHdDus3xzizAs4ejzJxWdKAgye4xo5Zjcox8X3fnT2MTL6ugFQNECDs7cVg3iC22Lu5vB6KnW5dsag1DCUOTObQ?key=FgW71u4vKTVODEVBYPADR_E6)\

{% endstep %}

{% step %}
### Click on the button

Now Click the “Initialize/Update PAT Graph from Character” and your character should now be successfully mapped to the graph. Double click on the PAT\_Node Graph to open it up, you will see the character structure now:

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcNIFlxMPjG4dFx--dvDIiKJm4eWfQFflJaU2imUvFhIm6YDQouD1_-NUwQToC3bAtHpMI5Ncye8QxBsTM3IXTsN3I4rIKDpJVL3i42onkFH4eU4TYSq8FPMfmz3oQSVETnPK6EBQ?key=FgW71u4vKTVODEVBYPADR_E6)
{% endstep %}
{% endstepper %}

***

## Convenient functions of PAT\_Manager:

### Selecting corresponding GameObject

Right click on the node and you will see the option “select corresponded GameObject”, simply click on it and now the GameObject will be selected.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeP00Id2_9zqS_B2AUU7TA27icDzU4jbOdmnM4PAHo4MajL0rSEypOvO3Gc7m7JCWzbR1XxJdbI9Dyoeko2JwdkUazByT4hfUawlQGSrQ3Bk8eub4cnusGYx40lsMuIsW4CySllbw?key=FgW71u4vKTVODEVBYPADR_E6" alt=""><figcaption></figcaption></figure>

### Edit Title

Select the “Edit Title” and you may rename the nodes.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeqUckRiWMn15PRjSVDJ1PV1m2oTkUxF3isMe8eSTPwXT4sqGLngo61ImGq1dH0ZPK9sICnjxrbZJAtLfwE6xc5_9eWY09JB2iP0sJsK3ujH4vqoaL6V1ZpQQK0zDW8T4WYAaWX?key=FgW71u4vKTVODEVBYPADR_E6" alt=""><figcaption></figcaption></figure>

### Drag and drop to attach / remove scripts

You can drag a script and drop it onto a node, it will be attached to the node then. All the scripts attached to a node are displayed in the left inspector panel.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXexFlVb9JAHAIB4I8Ef745_BgkY3tEJ2w3xzC6b0bQrtDn5DeEc7wZSpstdP6KyTK0KY1jmkH4XCezpUB9QuFZzmsIbr8SEvSy_8OIPcRa8YOnqhEKyy_7clCwwWfXVE-BztF9j?key=FgW71u4vKTVODEVBYPADR_E6)

Right click on the script name and you will see the option to remove.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeGCldQYeij_eS0gne5ZFoyVr62gHwlGed6A-CDpbkdzTrgkaA02RYKtGkTFzPqKSVmQVxZdUitlq6yD47-ZOB7bbyuV_jF7ZKCcjz6J9CTVhj09VGz_dwidX5CZ4gxBtQDxF5gMg?key=FgW71u4vKTVODEVBYPADR_E6)

### Initialize a character from Node Graph

You might notice there is another option in the Graph Runner Script, “Initialize PAT Character From Graph”

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeCPyN3_x2ra_8vLf-SV5c2P7wy-8RjIt2UDT8saN3s2OBUsU-scUuLEG0Z8XSeoZjGtjJvypDGjQw7gLJ0MxHO50Ur2A7uIBpxDXK8toCHxEgc-2vn3p5M-T_A378PorZt4AKq?key=FgW71u4vKTVODEVBYPADR_E6" alt=""><figcaption></figcaption></figure>

To use the function, you need to attach the graph runner script to another empty GameObject. And drag a valid node graph into the slot.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXerig5_S-pxGzcZpHESi-gyn16jkuWBdl0tFSRxIDwiPWkbw5pQ_ok5V5FzEliiqHtD8R6Q92N2iu5KmzUV1LufaLInIIupxAL4fCuOstZIFAImiGM08_wxTzor8k-47pZqQkQYPQ?key=FgW71u4vKTVODEVBYPADR_E6" alt=""><figcaption></figcaption></figure>

Now simply click the first button and there should be components generated under the GameObject. The name of the GameObject will also be changed based on the Character Node title.

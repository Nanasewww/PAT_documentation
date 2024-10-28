---
icon: circle-chevron-right
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

# Animation Event

#### Trigger Animation Event:

If you are trying to control your state modifiers by animation events, you will need to add Model Handler to where your animator is at. We recommend you open the animation by clicking on the animator you attached to your character. If you directly click on the animation clip, the inspector view will be more confusing due to Unity’s own issue.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXc5S_MoPICW6SIcruJ78NV1pU66mMZRO2DqGMXUFI9On_bc-7YqicIxM3OxhwtyIyNXSm4DqPOWpw07Ml_MaCHzW1AyrDAaj322VcQYDhHSqBbSDjs5KmC-wgtJBDJx9L_4nBM_tjhMkOWk1Rl5vBapQQt6?key=Rv96SXV0rCMH8N9lwXnGWw" alt=""><figcaption></figcaption></figure>

After selecting an Animation Clip, you may use the circled button to add a trigger animation event to an animation clip. This is used for modifiers to track their begin and end timing.

If you click onto the events, you may find this in the inspector. You should choose TriggerAnimationEvent from Model Handler. You need to have a Model Handler on the same object as the Animator. After that, you can set Int which is the index we use for the modifier's timing. It should be in ascending order on the timeline

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdw7YaWlWClwiENAaaEOkQYcrPU6bjgLsXWi0Fy9II1aaIbmTbKJ77FD_fjdDUhVE1UTrZuZZzx3bmn7vuDjw5MokQgXX2wFiepM7Q76XcUItZ8Ou0BObGiXSG9YNo4fe3wW-hFgayj0u5qLDp14XWbbls?key=Rv96SXV0rCMH8N9lwXnGWw" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXd7OIi0L0jhnXviAcGfQUdJSJX-NWrHwd30kr2RaQ9AI11HWlSpg8iUAUL5050vSB-QJHjhBOJC9v98k3ZIa2u6kuw6iEQnQQsUIL6k2aSnKyPN5QWtES41PjfZC3oK59I582NGDYdlz87h0jUsR2uRQ-7I?key=Rv96SXV0rCMH8N9lwXnGWw" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcQbpd8lOYmSEIKHINE9QXO7TmBXxBY_3cASuQTSloaxxuafHJUUZVsdGPD4sWcRIhq0gfs2cakUn4XEjhMfZf4YsVX1V144v4imqegXOn3avh--ABA0qo1YHNJJsaaWrv-Zpj5ex0jzkYOrzP5rh-C5oMq?key=Rv96SXV0rCMH8N9lwXnGWw" alt=""><figcaption></figcaption></figure>

\



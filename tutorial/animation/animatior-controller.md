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

# Animatior Controller

{% hint style="info" %}
Please note that this <mark style="color:red;">**ONLY**</mark> works with animator that structures in PAT’s template. If you need your own way to implement the animator, you might want to have your own version of Animation Modifier.
{% endhint %}

In PAT, the transitions among different animation states is controlled by Animation Montage Modifiers attached to each Action State. It keeps the animator clean and understandable. Your animator should look like the pictures below:

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXchEVZ_GZekhV_m2N62-CLUDzlJeDHsJUrFfG6LcgqhXt23VItTep-z5C_1qlFCUdTt1oLtwre3iGP_N1rixcauaGpLg8vrxcLWY1-3oBKR3uaRpePDdvd7BxRFmZ_ROTe3CdlQNGU83P-iqdihmPfK03w?key=Rv96SXV0rCMH8N9lwXnGWw" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeYEiC9fPdqy6EZRkqB0AoPcTat_tCRKetE4ofGiy05txAl00CZm8UWoEXD5vZRXwGC7J7IGs7uHQ2AiUWWwPl13YEpuYFhNP85f8bWgvBo3PHFQpFAhc2u2TVy9Ys8oRvVbq3R6So3nSEHp13HlkiADnn4?key=Rv96SXV0rCMH8N9lwXnGWw" alt=""><figcaption></figcaption></figure>

We recommend you categorize animation clips under different layers. Each layer has an index, starting from 0.

On the parameter page, you may want to introduce parameters like MontageSpeed, which allows you to use MontageSpeedMod to control the speed of your animation.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXe-Joa-F1QMp2CE9U44iN8-pDzlvpTfm1ZXbCUtK6HCRYK-8PGKWYAgHX8bBHwvgAjKhDybcscRGVoM2_PfpskqqI2D55_f0fiMzXDQF7OfW3SIuxs91moH0wMRO7pa3k29p2b5YnROx-I8_mkyJjS4SP4?key=Rv96SXV0rCMH8N9lwXnGWw" alt=""><figcaption></figcaption></figure>

You may choose the animation state and put in your speed multiplier.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcB5uWOth_Y9SHSAWbaSW4wsidVOzi7moIGu9ZmCx3j_CIgjWzjpLxOW9kNH5wn_bL0IOmkKuX9qSuEYGWSkNZLoe__x7yb_bYP4l4taJcQdL95qeaj9z6QqJKeqHGVO7wRbswhui0IEFnBC7yXd4C7VdCk?key=Rv96SXV0rCMH8N9lwXnGWw" alt=""><figcaption></figcaption></figure>

\



---
icon: tag
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

# Tag

## Definition

T[ag system](#user-content-fn-1)[^1] is essential to PAT. <mark style="color:orange;">**Action State’s transition logic is defined by Tags, which creates a dynamic state machine system.**</mark> Beyond that, some other components also use Tags for communication purposes. For example, you can make a character invincible by granting it invincible Tag and Hurtbox will react to it.

All tags are stored inside a script named **GamePlayTag**, you may edit it on your own need. It is a huge Enum. Every Tag is represented by a name and a number.&#x20;

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeI3LyalgJMG2ts7pQQx8U8rrg6RoGb_HmmpV9ysGZ-Wg4rTPf4qdT6s1TsLkf3rJa4-S1LF6g8zsmIae4dapNB5SiesRsVkw2QhsTBOu7fVf6DGM_ybx3eZZ20usIGGURDrK6fd-hA2Ss8dxeEPuVVQdCu?key=Rv96SXV0rCMH8N9lwXnGWw" alt=""><figcaption><p>Script View</p></figcaption></figure>

Tags are toggled on the Action State component.

You may also find the scriptable object named GamePlayTagHelper for non-script view.&#x20;

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdiQ8S429MtoXe9fSheGOHrfaDtfG1LRYrgU7QZUp7ohNfK28VFNN_ZZ2VMA5ImXyl9AMDm2D_LN3D_mvJctMqNii1V1bdlUohVwCkVmgfj4U5h0kVWf29PxGRY6EC7SzuCWu4ae6t_zd4aesCaJeSjBtxw?key=Rv96SXV0rCMH8N9lwXnGWw" alt=""><figcaption><p>Where the Helper is located</p></figcaption></figure>

You have to right click in the inspector and choose “refresh” for your changes to be reflected. Any new tags added in the script will be put into “Other”. You need to manually copy & paste it into the folder you like.

\


<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfJtywG1fZPzeoip5tPovfYnE-qUEFyL2NJFLIbRUnCOrsczy_ePj5HYb3Ko_kncirZ0ftN_Pu3is0o2h-hv_Rz2zwHIK0w2xAvt9KDJipYN75gXKNSIkvMrAYEVX6V332KnFZe8nSENVbR8PSNBHokL4CK?key=Rv96SXV0rCMH8N9lwXnGWw" alt=""><figcaption></figcaption></figure>

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdt3qG7ulS9Der5mOxqcJOfyXme32M1eUb9jEFreMu6-OQW9YYdVlEGmud0uMF2Zbor2GD7qTrTeJzoz2AVfhE_Q8A4MH-dxEyr3GIpEPHRR5uHyrDwsUQ8ElScCLJWmbGCwTMT_0qgkMuJGxiodeIFpm4K?key=Rv96SXV0rCMH8N9lwXnGWw" alt=""><figcaption><p>Copy, paste it to the folder you like, delete the original one</p></figcaption></figure>

\




[^1]: Not to be confused with Unity Tags

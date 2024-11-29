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

# Create a new Tag

## Introduction

All tags are stored inside a script named [<mark style="color:orange;">**GamePlayTag**</mark>](#user-content-fn-1)[^1], you may edit it on your own need. It is a huge Enum. Every Tag is represented by a name and a unique number.&#x20;

{% hint style="warning" %}
_The number of each tag should be unique to avoid unexpected behaviors._
{% endhint %}

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeI3LyalgJMG2ts7pQQx8U8rrg6RoGb_HmmpV9ysGZ-Wg4rTPf4qdT6s1TsLkf3rJa4-S1LF6g8zsmIae4dapNB5SiesRsVkw2QhsTBOu7fVf6DGM_ybx3eZZ20usIGGURDrK6fd-hA2Ss8dxeEPuVVQdCu?key=Rv96SXV0rCMH8N9lwXnGWw" alt=""><figcaption><p>Script view of Tag Helper</p></figcaption></figure>

Tags are toggled on the Action State component.

For a non-script view, you can find a scriptable object named [<mark style="color:orange;">**GamePlayTagHelper**</mark>](#user-content-fn-2)[^2] in the same folder. Click on the helper and you can find all the tags listed in the Inspector.&#x20;

<figure><img src="../.gitbook/assets/image (8) (1) (1).png" alt=""><figcaption><p>Inspector view of Tag Helper</p></figcaption></figure>

## Instructions

### Step1: Add a new tag in GamePlayTag

* Open [<mark style="color:orange;">**GamePlayTag**</mark>](#user-content-fn-3)[^3] in script view.&#x20;
* Add a new tag with a unique number to the GamePlayTag enum.&#x20;

<figure><img src="../.gitbook/assets/image (9) (1) (1).png" alt="" width="563"><figcaption><p>Example: add <em><strong>chain5</strong></em> as a new tag</p></figcaption></figure>

{% hint style="warning" %}
_There is no special constrain to the number except uniqueness._

_However, in order to better manage the folder hierarchy, we suggest that <mark style="color:red;">numbers of the same group of tags should be close to each other</mark>._&#x20;
{% endhint %}

### Step2: Refresh GamePlayTagHelper

* Back to Unity Project, click on [<mark style="color:orange;">**GamePlayTagHelper**</mark>](#user-content-fn-4)[^4] .
* In Inspector, right click on the helper and choose <mark style="color:orange;">**Refresh**</mark> to update it.&#x20;

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfJtywG1fZPzeoip5tPovfYnE-qUEFyL2NJFLIbRUnCOrsczy_ePj5HYb3Ko_kncirZ0ftN_Pu3is0o2h-hv_Rz2zwHIK0w2xAvt9KDJipYN75gXKNSIkvMrAYEVX6V332KnFZe8nSENVbR8PSNBHokL4CK?key=Rv96SXV0rCMH8N9lwXnGWw" alt="" width="563"><figcaption><p>Right click to Refresh</p></figcaption></figure>

* After refreshing, the new tag should be listed in _<mark style="color:orange;">**Folders/Other**</mark>_.&#x20;

<figure><img src="../.gitbook/assets/image (10) (1).png" alt="" width="427"><figcaption><p>Tag Helper after refreshing</p></figcaption></figure>

### Step3: Fix Helper hierarchy

* Right click on your new tag in _**Other**_ and choose <mark style="color:orange;">**Copy**</mark>.
* Go to your target folder and <mark style="color:orange;">**click +**</mark> to add a new enum here.
* Right click this tag and choose <mark style="color:orange;">**Paste**</mark> to move your tag to the correct hierarchy.
* <mark style="color:orange;">**Click -**</mark> to remove your tag from _**Other**_.

<figure><img src="../.gitbook/assets/image (11) (1).png" alt="" width="420"><figcaption><p>Tag Helper after fixing the hierarchy</p></figcaption></figure>



[^1]: Path: _<mark style="color:blue;">/Core/Scripts/GamePlayTags/ GamePlayTag</mark>_

[^2]: Path: _<mark style="color:blue;">/Core/Scripts/GamePlayTags/ GamePlayerTagHelper</mark>_

[^3]: Path: _<mark style="color:blue;">/Core/Scripts/GamePlayTags/ GamePlayTag</mark>_

[^4]: Path: _<mark style="color:blue;">/Core/Scripts/GamePlayTags/ GamePlayerTagHelper</mark>_

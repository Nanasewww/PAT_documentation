---
icon: arrow-down-to-arc
---

# Installation

{% stepper %}
{% step %}
### Create a 3D URP project

Please use Unity Version **2022.3.32f1**
{% endstep %}

{% step %}
### Import PAT

There might be compile errors in your console due to some Unity packages missing. These packages are Input System, Cinemachine, Animation Rigging, AI Navigation.
{% endstep %}

{% step %}
### Install the missing packages

1. Open _manifest.json_ in path _YourUnityProjectFolder/Packages/manifest.json_
2. Copy the following content into "dependencies"

```
"com.unity.inputsystem": "1.7.0",
"com.unity.cinemachine": "2.10.1",
"com.unity.animation.rigging": "1.2.1",
"com.unity.ai.navigation": "1.1.5"
```

It should be like this:

![](https://lh7-rt.googleusercontent.com/docsz/AD\_4nXcDthLI6BUvOoBRQgV2s\_Mk\_c4SjsnoT\_4bai1jErYdhz\_zRTevaIKpG\_FUwgYsEVgZT1lUCEZBaRKtSAxyF3x8BWLhL41DEo0WpBL\_1f8lQEJby-dGx7iaWLdl8GDF\_ULhRT5ObYvLJLgQQoVKpkmTUAE?key=htNSsP1Z5pxNb19QhZc4Mg)


{% endstep %}

{% step %}
### Save and reload Unity

1. Save the file and then return to Unity.
2. Unity will automatically download and install the missing packages listed in manifest.json.&#x20;
{% endstep %}
{% endstepper %}

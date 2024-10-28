---
icon: calculator-simple
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

# Attribute

## Definition

An Attribute is a Mono Behavior that holds a value.&#x20;

Health, Posture, Mana, and Stamina are all examples of Attributes. Since Attributes can be influenced by Effects in an easy and stable way without tightly coupling your code, we encourage you to use Attributes for any values you want to change dynamically during gameplay.

## Inspector

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdzH0lWMXRFekXlnYJLnE6aSp3BuYEL3pCnC4vF-3j2jA6vYu2E9ZNVjF-GVsSuELzg3jdu9L1UEpSoEYtowopJg0KJ2tGNJar7Kaq5mQJ-k-SoAlFjIXIQVAcL2S-6trp8_2hV194AEHu2ywtVpRb2T-87?key=wjgYipemgHjXa5pb_ZH-6A" alt=""><figcaption><p>Attribute inspector</p></figcaption></figure>

### **Resource Tag**

The identifier for the Attribute. <mark style="color:orange;">Effects</mark> and <mark style="color:orange;">Use Attribute Mod</mark> use this to find their target Attribute.

### **Max Amount**

The maximum value the Attribute can hold.

### **Min Amount**

The minimum value the Attribute can hold.

### **Start Amount**

The starting value of the Attribute.

### **Start Recovery Speed**

The rate at which the base value recovers or decreases. This can also be modified by an Effect.

### **Recover Mode**

The method of recovery for the Attribute.

### **Can Recover**

This should ideally be removed. The recommended way to disable recovery is by using an override Effect Mod Value to set the Recover Speed to 0.

## Usage

To get the current value of an Effect, right-click on the component and select 'Log Value.' The value will be printed in the console. We plan to make this more visible in the future.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfXSzFuC_aabfdXxVYauQ4AYg0LOTPOY8J4c4hAqkQPIDuTbr7YO6PO89B73cG1ctSK_OVXIKUn4wr_hGMWHRTvSvXnPM5kP5naU0ukmu6moXmt7u0WsQKI2uQoKz4Hr3EE_Xp0EQn8CZPSSHn0a7ZsunFC?key=wjgYipemgHjXa5pb_ZH-6A" alt=""><figcaption><p>Manually fresh Attribute value</p></figcaption></figure>

Attributes can be dynamically added to a character. Some special Attribute classes, like Health and Knockback, have different behaviors. However, we may change how Knockback is handled in the future.






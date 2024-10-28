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

# Create a new Modifier

To write your own State Modifiers, you need to extend the State Modifier in your new script.

```csharp
public class AnimationMontageMod: StateModifier
```

Typically, there are two functions you need to override: BeginEvent & EndEvent. BeginEvent is what happens when the State Modifier is triggered, while EndEvent is when the State Modifier is exited.

```csharp
public override void BeginEvent()
{
    base.BeginEvent();
}


public override void EndEvent()
{
    base.EndEvent();
}
```

If you want to use a State Modifier to decide whether the character should enter the action state (ex. We did that in UseAttributeMod), you might also override Validate().




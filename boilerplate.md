# Session 2
## Boilerplate

We're ready to write our first of two components! Add a new component called `AlwaysLookAt`, and Unity will generate the following code:

```cs
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class AlwaysLookAt : MonoBehaviour {

	// Use this for initialization
	void Start () {

	}

	// Update is called once per frame
	void Update () {

	}
}
```

### Syntax
There's a lot of stuff here, and to avoid the sense that anything is magic, walk your students through the syntax.

#### `using`
The [`using` directive](https://msdn.microsoft.com/en-us/library/sf0df423.aspx) makes types available to this file with shorter names. C# types live inside of [namespaces](https://msdn.microsoft.com/en-us/library/z2kcy19k.aspx) to avoid overlapping names. Almost everything in Unity is in the `UnityEngine` namespace, which means that the full names of Unity types are actually `UnityEngine.Vector3` and `UnityEngine.Collider`. This is repetitive, so the `using` directive says "in this file, use names from `UnityEngine` without repeating `UnityEngine.` every time". Unity also adds `using` directives for `System.Collections` and `System.Collections.Generic`, which are namespaces built in to C# that Unity thinks are useful.

#### `public class AlwaysLookAt : MonoBehaviour`
`public class` tells C# that we're about to start writing a *class* and that it is going to be [*public*](https://msdn.microsoft.com/en-us/library/yzh058ae.aspx), meaning other code can see and use it. Recall that Unity components are implemented as C# classes, and we're going to have to create a class everytime we want to make a new component. You will always want your components to be public, otherwise Unity cannot see or use it. There are other keywords you can put here, called the [*accessibility levels*](https://msdn.microsoft.com/en-us/library/ba0a1yw2.aspx), and they are useful for C# classes in general to organize your code, but for a Unity component this will always be `public`.

Following that, finally something familiar: `AlwaysLookAt` is the name of our component!

The `:` in this context means that our class will *inherit* from another class, in this case from Unity's [`MonoBehaviour`](https://docs.unity3d.com/ScriptReference/MonoBehaviour.html). [C# inheritance](https://msdn.microsoft.com/en-us/library/ms173149.aspx) is a big topic, and does not come up very often in Unity, so its up to you how deep to get into that. But recall that Components are either built in to Unity or scripts written by developers. inheriting from `MonoBehaviour` tells Unity that this isn't a "normal" C# class, but instead a class intended to be used as a user-defined component.

#### `//`
C# comments are either `//` to the end of the line anything between `/*` and `*/`. The computer ignores this text and its a good place for notes.

#### `void Start ()`, `void Update ()`,
Unity calls the events that GameObjects can react to *Messages* (scroll down half way on the [MonoBehaviour page](https://docs.unity3d.com/ScriptReference/MonoBehaviour.html)). They are implemented as C# methods on component classes.

Basically, by writing methods with the right name, Unity will trigger that code when appropriate. It provides components with Start (triggered once when the game starts) and Update (triggered once per frame) methods by default, to be useful. We only need `Update`, so you can remove `Start` if you wish or leave it in, it makes no difference.

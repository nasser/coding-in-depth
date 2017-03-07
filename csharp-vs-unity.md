# Session 2
## C# vs Unity

Before Unity is the game engine we are working in, but C# is the *programming language* we are writing code in. Their relationship is important to explain.

### C# the language
C# is a language designed by Microsoft in 1999. It is *object oriented*, meaning it wants you to organize your code into [*classes*](https://en.wikipedia.org/wiki/Object-oriented_programming#Objects_and_classes). Classes are collections of data called *fields* and code called *methods*. C# doesn't tell you exactly *how* you organize your code, but classes, fields, and methods are the tools it gives you.

Another important aspect of C# is that it is *statically typed*, meaning that every value has to be annotated with the *type* of data it represents. A type can be something built in to C#, like numbers (e.g. `int`, `float`) or a class written in C#. In practice, these classes either come from Microsoft (like [`DateTime`](https://msdn.microsoft.com/en-us/library/system.datetime.aspx)), Unity (like [`AudioClip`](https://docs.unity3d.com/ScriptReference/AudioClip.html)), a library you imported, or you.

#### Classes vs Instances
The difference between classes and instances is a consistent source of confusion, and unfortunately unavoidable in Unity. A class is a *blueprint* from which *instances* (or "objects") can be made. You can then access the *instance fields and methods* on that instance.

```cs
Vector3 v = new Vector3(3, 4, 5); // v is now an instance of the class Vector3
v.x;                              // you can access the x instance field
v.Set(300, 400, 500);             // you can access the Set instance method
```

But classes are more than just blueprints. They can contain their own fields and methods that can be accessed from anywhere in the program!

```case
Vector3 w = new Vector3(7, 3, 1);
Vector3 v = new Vector3(3, 4, 5);
Vector3.Distance(w, v); // Vector3.Distance is a method that lives in the Vector3 class itself
Input.GetKey("space");  // Input.GetKey is a method that lives in the Input class
```

This appears to invalidate the "everything is a GameObject or Component" rule, but that rule is only true of Unity. C# has its own rules, and to use Unity effectively you need work towards understanding both systems.

### C# In Unity
Unity *uses* C#'s object oriented features to implement very different ideas, namely the [*entity-component-system*](history.md). These two approaches can seem in tension at times, and can result in a bit of repetitive code.

When you write your own components, you do that by writing a C# class. When you expose parameters to the Unity inspector, you do that by writing public C# fields. When you react to Unity events, you do that by writing C# methods.

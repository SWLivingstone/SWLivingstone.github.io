---
layout: post
title: .flatten Explained (Ruby)
---

## .flatten explained (for ruby)

While an array may contain strings and integers it can also contain other arrays (known as nested arrays).  If we imagine a standard array, say `["this", "is", "an", "array"]`, we can call it flat.  That is to say that it extends along only one axis, the x axis, like a line.  If we add a nested array to this array, like this `["this", "is", ["nested", "array"], "an", "array"]`, it will now have another dimension, the y axis.  In this case the y axis has a value of 1 because the nested array is nested 1 deep.  

Consider the following examples

```
# two nested arrays each nested 1 deep
["this", "is", ["nested", "array"], "an",["hello"], "array"]

# two nested arrays. One is nested 1 deep and the other is nested 2 deep.
["this", "is", ["nested", ["hello"], "array"], "an", "array"]
```

As you can see from the examples that nesting arrays with in arrays creates additional levels of depth (levels on the y axis).
The `.flatten` method, when used on an array, returns a new array that has been "flatted". Hence the nested arrays are no longer nested and their contents now exist with in one flat array.

```
# Before .flatten is called
["this", "is", ["nested", ["hello"], "array"], "an", "array"]

# After .flatten is called
["this", "is", "nested", "hello", "array", "an", "array"]
```

`.flatten` can also be passed an optional argument that determines how many levels to flatten.

```
# Before .flatten(1) is called
["this", "is", ["nested", ["hello"], "array"], "an", "array"]

# After .flatten(1) is called
["this", "is", "nested", ["hello"], "array", "an", "array"]
```

It is also possible to call `.flatten` with an optional `!` like this `some_array.flatten!` which, instead of returning a new array, modifies the called upon array.

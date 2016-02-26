# CURLY

Curly is a general recommendation on how to annotate things with metadata using plain text enclosed in curly brackets. The resulting metadata is referred to as a curlytag and appears as follows:

```
{key: value}

```

So you might be thinking, umm... isn't this just [CSON]()? The answer: pretty much!

You can think of it as a CSON Object that only supports *one* key-value pairing. That means, the following expression is illegal:

> Curly really only supports one key-value pairing? That's stupid! {todo: "elaborate on its stupidity", tag: "curly"}

Using curly, we can annotate the following text snippet outlining that it is not yet complete.

> Curly takes much of it's inspiration from the JSON data-interchange standard defined in {todo: find standard}.

Another use case could be to tag nodes in mindmaps.

> Principle Agent Problem {aka: theory of agency} {field: Business} {tag: ["Brand-Image", "coombs"]}

[Node with curlytags]()

This text could then be intepreted by the application whichever way it sees fit. In the context of a mindmapping program it could convert the curlytags into node attributes

[Node with attributes]()

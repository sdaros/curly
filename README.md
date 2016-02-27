# CURLY

Curly is a general recommendation on how to annotate things with metadata using plain text enclosed in curly brackets. The resulting metadata is called "curlytag" and looks like this:

```
{key: value}

```

You can think of it as a [JSON](http://json.org/) Object that has *only one* key-value pairing. Insert your curlytags wherever its appropriate to quickly tag things.

## Use Cases

Sometimes I want to be able to dad a comment in a text-document that I am proofreading for someone.

Original:

> In this report we will discuss about the importance of Open-Source Software.

Annotated with a comment:

> In this report we will discuss about the importance of Open-Source Software {comment: since Richard Stallman will be reading this, you might want to change "Open-Source Software" to "Libre Software"}.

With proper application support, this curlytag could be turned into a comment.

![Doc with comment](https://cip.li/res/curly_oss_comment.png)

Usually, when i'm trying to avoid doing real work, I feel the spontaneous need to tag all the things I should be doing.

Original (an output of my todo.txt file):

> - clean the kitchen
> - do the laundry
> - winter tires for the car
> - donate to the EFF

Annotated:

> - clean the kitchen {context: Home}
> - do the laundry {context: Home} {delegate}
> - winter tires for the car {context: City}
> - donate to the EFF {context: Computer}

Notice the curlytag `{delegate}`. This is just shortform for the following JSON equivalent `{"delegate": true}`

## Design Goals

The following design goals guide the development and usage of curlytag (in order of preference):

1. Legibility
2. Simplicity
3. YAGNI (You Aint Going to Need It)

## Seriously, that can't be it...

Fine, here are the technical details.

### TODO

## Illegal Use Cases

- Anything that's complex. The user won't use it anyway
Inserting
> Curly really only supports one key-value pairing within curly brackets? That's stupid! {todo: "elaborate on its stupidity", tag: "curly"}

Another use case could be to tag nodes in mindmaps.

> Principle Agent Problem {aka: theory of agency} {field: Business} {tag: "Brand-Image", "coombs"}

![Node with curlytags]()

This text could then be intepreted by the application whichever way it sees fit. In the context of a mindmapping program it could convert the curlytags into node attributes

![Node with attributes]()

## FAQ

#### Umm... I don't get it

{todo: Solve the user's confusion}

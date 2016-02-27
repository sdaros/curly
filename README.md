# CURLY

Curly is a general recommendation on how to annotate things with metadata using plain text enclosed in curly brackets. The resulting metadata is called "curlytag" and looks like this:

```cson
{key: value}

```

You can think of it as a [JSON](http://json.org/) Object with *only one* key-value pairing. Insert your curlytags wherever its appropriate to quickly annotate things.

## Use Cases

##### Sometimes I want to add a comment in a text-document that I am proofreading.

Original:

> In this report we will discuss about the importance of Open-Source Software.

Annotated with a comment:

> In this report we will discuss about the importance of Open-Source Software {comment: since Richard Stallman will be reading this, you might want to change "Open-Source Software" to "Libre Software"}.

With proper application support, this curlytag could be turned into a comment.

![Doc with comment](https://cip.li/res/curly_oss_comment.png)

##### While avoiding work, I like to tag all the things I should be doing.

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

##### I want to simply tag nodes in my mindmaps.

Original: 
> Principle Agent Problem
![Node without curlytags]()

Annotated:
> Principle Agent Problem {aka: theory of agency} {field: Business} {tag: "Brand-Image", "coombs"}
![Node with curlytags]()

The mindmapping software could then simply display the curlytags as node attributes

![Node with attributes]()

## Design Goals

No guarantees can be made for machine parseability, since curlytags are designed to be as simple as possible for humans to write and read. The following design goals guide the development and usage of curlytag:

1. Legibility
2. Simplicity
3. YAGNI (You Aint Going to Need It)

## Seriously, that can't be it...

Fine, here are the technical details.

{todo: fill out the technical details}

## Illegal Usage

##### Anything that's too complicated.

Example:

> {todo: insert overly complex example here}

##### Curly tags that have *more than one* key-value pairing.

Example:

> Curly really only supports one key-value pairing within curly brackets? That's stupid! {todo: "elaborate on its stupidity", tag: "curly"}

## FAQ

#### Umm... I don't get it

{todo: Solve the user's confusion}

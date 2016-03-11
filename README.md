# CURLY

Curly is a general recommendation on how to annotate things with metadata using plain text enclosed in curly brackets _or_ paranthesis. The resulting metadata is called "curlytag" and looks like this:

```cson
{key: value}
```
or like this:
```cson
(key: value)
```


You can think of it as a [JSON](http://json.org/) Object with *only one* key-value pairing. Insert your curlytags wherever its appropriate to quickly annotate things.

## Use Cases

##### Sometimes I want to add a comment in a text-document that I am proofreading.

Original:

> In this report we will discuss about the importance of Open-Source Software.

Annotated with a comment:

> In this report we will discuss about the importance of Open-Source Software (comment: since Richard Stallman will be reading this, you might want to change "Open-Source Software" to "Libre Software").

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

Notice the curlytag `{delegate}`. This is just shortform for the following JSON equivalent `{"delegate": true}`.

##### Annotating nodes in my mindmaps can be useful.

Original: 
![Node without curlytags](https://cip.li/res/curly_mindmap_no_tags.png)

Annotated:
![Node with curlytags](https://cip.li/res/curly_mindmap_with_tags.png)

The mindmapping software could then simply display the curlytags as node attributes.

![Node with attributes](https://cip.li/res/curly_mindmap_with_attributes.png)

## Design Goals

No guarantees can be made for machine parseability, since curlytags are designed to be as simple as possible for humans to write and read. The following design goals guide the development and usage of curlytag:

1. Legibility
2. Simplicity
3. YAGNI (You Aint Going to Need It)

## Seriously, that can't be it...

Relax, we're still at version 0.1.0. The technical details for those that want to parse curlytags will come. 

## Illegal Usage

##### Curly tags that have *more than one* key-value pairing.

Example:

> Curly really only supports one key-value pairing within curly brackets? That's really stupid! The authors clearly did not think this through... {todo: "elaborate on its stupidity", tag: "curly"}

## FAQ

#### Umm... I don't get it

(todo: Solve the user's confusion)

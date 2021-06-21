# Getting Started

Let's get started, get the module via [toobolx](https://www.roblox.com/library/6978094397/Bases) or copy the code into a module from [github](https://github.com/remideas/Bases).

## Configuring the module

Set the parent of the module, I prefer ReplicatedStorage, open the module, and scroll down until you reach **Settings** now the only two things you need to focus on right now are:
```lua
local debug_enabled = true -- Print the recognized classes after loading them.
local silence_module = "__" -- Keyword to silence modules.
```
I think the comments are self-explanatory, but I will explain you anyways; **debug_enabled** is a variable that will determine whether or not to print the recognized classes
after loading them.
<div class="mermaid">
graph LR;
  A[Script] -->|require| B[Module];
  B --> C[Load Classes];
  C --> |Silenced|D[Ignore];
  C --> |Not Silenced| E[Load];
  E --> F[Error?];
  F --> |yes| D;
  F --> |no| G[Print];
</div>

It will look like this

![debug_photo](https://github.com/remideas/Bases/blob/main/images/DebugPhoto.png?raw=true)

If the value is set to false, the message will stop printing in the output, if a class was not loaded, means that its either silenced or it raises an error. The **silence_module**
variable it's the prename you will need to set to a module's name to silence it.

## Adding classes

To add a class to Bases module, all you need to do is create a [ModuleScript](https://developer.roblox.com/en-us/api-reference/class/ModuleScript) inside it; the name of it must be
the name you want to assign to your class. Example:

![example_gif](https://github.com/remideas/Bases/blob/main/images/CreateClassGif.gif)

## Silencing modules

Silencing a module means ignore it when loading the classes in the master module, you may noticed that Bases module includes a children  
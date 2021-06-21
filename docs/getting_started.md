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
  C --> D[Silenced?];
  D --> |true| E[Ignore];
  D --> |false| F[Accept];
  F --> G[Error?];
  G --> |yes| E;
  G --> |no| H[Print];
</div>

It will look like this

![alt text](https://github.com/remideas/Bases/blob/main/assets/DebugPhoto.png?raw=true)

If the value is set to false, the message will stop printing in the output, if a class was not loaded, means that its either silenced or it raises an error.
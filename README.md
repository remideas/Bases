# ![icon](https://github.com/remideas/Bases/blob/main/images/Icon.png?raw=true) Bases
Bases it's a Roblox Studio module made by remi that allows you to sandbox with custom instance classes to do any crazy ideas you can imagine, no metatables needed, just a table in a module script.

I'm trying to improve sandboxing and performance the best I can, if you have any suggestion / idea feel free to tell me about it. If you find any bug I would be very happy that you report it to me.

## It's simple!
Start working with Bases it's very simple, no need for being a scientific to know what to do, you have documents, examples and everything setted up so you can start using it!

It's simple as just creating a new empty module and writing one line no need for any extra steps.
```lua
local bases = require(script.Parent)
local my_class = bases("setup", script)
```

## Extras
Bases brings two friends into the party, even if you dont know their names you will like to use them! Bases has two additional modules added into its source code which you can access from any script if wanted.

Those modules were originally only going to be available for the master module, but why not let users use them? So you are free to check them out.

Theres no need for adding those separately, they come together!

### SignalConnection Class
A module that will imitate the behaviour of the RBXScriptSignal and RBXScriptConnection in order to make custom events for your objects, this is already implemented on bases and you don't need to worry about it, but if you want to use it, its there!
```lua
local Signal = require(6976644438)

local MySignal = Signal("SignalName")
local MyConnection
MyConnection = MySignal:Connect(function()
  print("My signal got fired!")
  MyConnection:Disconnect()
end
```

### Useful Functions
A module that will modify and add Roblox built in functions and libraries, this includes very useful functions that will help you in your code!
```lua
local Functions = require(6976698809)
local table = Functions.table

local template = {1, 2, 3, 4, 5, 6}

local clone = table.clone(template)
```

## More
For more information check out the documents.

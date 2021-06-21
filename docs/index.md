# Introduction

Bases it's a Roblox Studio module made by remi that allows you to sandbox with custom instance classes to do any crazy ideas you can imagine, no metatables needed, just a table in a module script.

I'm trying to improve sandboxing and performance the best I can, if you have any suggestions/ideas feel free to tell me about them. If you find any bug I would be very happy that you report it to me.

Here's the GitHub [repository](https://github.com/remideas/Bases).

## It's very simple!

Bases allow you to create custom instance classes without any effort, even a banana can do it! It's just a few lines of code to start working on amazing projects. We will guide you
through in this documents to solve any question you have!

## Why Bases?

You may be asking why you should use Bases over the conventional [OOP](https://en.wikipedia.org/wiki/Object-oriented_programming) method? Well, Bases it's created around the idea of creating custom instance classes. This means that you can simulate the
behavior of a normal Roblox's instance and create your own instance type, for example, a Roblox's instance of the class BasePart looks like this:

![alt text](https://github.com/remideas/Bases/blob/main/images/BasePartClass.png?raw=true)

And an instance created from the next Bases' class looks like this:

```lua
local bases = require(script.Parent)
local bouncy_part = bases("setup", script)

local methods = bouncy_part.methods

bouncy_part.instance_name = "BouncyPart"

bouncy_part.add_attribute("public", "BounceForce", 25)

function methods:Bounce()
	self:ApplyImpulse(Vector3.new(0, self.BounceForce, 0) * self:GetMass() * 3)
end

return bouncy_part
```

![alt text](https://github.com/remideas/Bases/blob/main/assets/BouncyPartClass.png?raw=true)

So basically, Bases allows you to wrap instance classes to create your own instance class with custom attributes and methods, being able to interact with your object within the real instance.
To achieve this with the conventional OOP method, you just need to modify your metamethods and class but it will not look like a Roblox's instance class to the user; so I made it for you!

!!! warning
	You shouldn't use Bases to create non-instance classes since you will be wasting memory.
	
## Extras

Bases bring two friends to the party, even if you don't know their names you will like to use them! Bases include two additional modules added into its source code which you can access from any script if wanted.

Those modules were originally only going to be available for the master module, but why not let users use them? So you are free to check them out.

There's no need for adding those separately, they come together!
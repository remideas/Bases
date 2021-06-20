# Bases module

Bases it's a Roblox Studio module made by remi that allows you to sandbox with custom instance classes to do any crazy ideas you can imagine, no metatables needed, just a table in a module script.

I'm trying to improve sandboxing and performance the best I can, if you have any suggestion / idea feel free to tell me about it. If you find any bug I would be very happy that you report it to me.

Heres the github [repository](https://github.com/remideas/Bases).

## It's very simple!

Bases allows you to create custom instance classes without any effort, even a banana can do it! It's just a few lines of code to start working in amazing projects. We will guide you
through in this documents to solve any question you have!

## Why Bases?

You may be asking why you should use Bases over the conventional OOP method? Well Bases it's created around the idea of creating custom instance classes. This means that you can simulate the
behaviour of a normal Roblox's instance and create your own instance type, for example a Roblox's instance of the class BasePart looks like this:

![alt text](https://github.com/remideas/Bases/blob/main/BasePartClass.png?raw=true)

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

![alt text](https://github.com/remideas/Bases/blob/main/BouncyPartClass.png?raw=true)

So basically, Bases allows you to wrap instance classes to create your own instance class with custom attributes and methods, being able to interact with your object within the real instance.
To achieve this with the convetional OOP method, you must need to modify your metamethod and class and it will not look as a Roblox's instance class.

!!! warning
	You shouldn't use Bases to create non instance classes since you will be wasting memory.


	
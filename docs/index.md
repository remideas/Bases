# Welcome to my documentation!

Heres the github repository [remi-reyes/Documentations](https://github.com/remi-reyes/Documentations).

## About

This is just an example of documentation with Material for MKDocs

I'm just going to show off an idiotic thing everyone knows. (if you don't learn it omegalul)

```lua linenums="1"
-- This is a lua codeblock.
local class = {}
class.__index = class

function class:SayMessage()
	print(self.message)
end

function class:SetMessage(message)
	self.message = message
end

function class.new(message)
	local object = setmetatable({}, class)
	
	object.message = message
	
	return object
end
```

??? example "Example of creating an object."
	To create an object, simply use the constructor method in class.
	```lua linenums="1"
	local object = class.new("Hi!") -- Creates our new object.
	
	object:SayMessage() -- This will print "Hi!"
	object:SetMessage("Bye!") -- This will set the object's attribute to "Bye!"
	object:SayMessage() -- This will print "Bye!"
	```
	
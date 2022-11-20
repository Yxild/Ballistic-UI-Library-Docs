# Offcialdwaedkl docs for balls-istic libriby UI

This documentation is for the UI Library that Ballistic uses.


# Main Stuff

## Adding Library

Let's first add the library using the feature named Loadstring 

```lua
loadstring(game:HttpGet("https://github.com/BallisticDevelopment/Roblox/blob/main/library.lua"), true)()
```

## Creating a Window
The **Window** is the main part of the UI Library.


### Example :
```lua
local Window = Library:Window({
		Text = "Baseplate"
})
```

## Creating a Tab
**Tabs** are great at preventing *sections* items together.


### Example :
```lua
local Tab = Window:Tab({
		Text = "Aiming"
})
```

## Creating a Section
**Sections** are useful for **grouping** items together, many UI Libraries rely on **Sections** for the Style / Theme.

### Example :
```lua
local Section = Tab:Section({
		Text = "Chams"
})
```

# Default Stuff

## Creating a Toggle
Basic ol' toggle!

### Example :
```lua
Section:Toggle({
		Text = "Enabled"
})
```

## Creating a Radio Button
For settings and stuff like dat :)

### Example :
```lua
Section:RadioButton({
		Text = "Radio Button",
		Options = {
			"Legit",
			"Blatant"
		},
		Callback = function(v)
				warn(v)
		end
})
```

## Creating a Button
Basic ol' toggle!

### Example :
```lua
Section:Button({
		Text = "Reset FOV"
})
```

## Creating a Label
A **Label** for listing items and stuff!

### Example :
```lua
local label = Section3:Label({
		Text = "This is a label example.",
		Color = Color3.fromRGB( 255, 255, 255 )
})
```

## Creating a Dropdown
A **Dropdown** for picking stuff!

### Example :
```lua
local dropdown = Section:Dropdown({
		Text = "Dropdown Example",
		List = {
			"Head",
			"Torso",
			"Random"
		},
		Flag = "DropdownFlag",
		Callback = function(v)
				warn(v)
		end
})
```

## Creating a Input
**Input** for stuff ( just a generic textbox :) )

### Example :
```lua
Section:Input({
		Placeholder = "Input ur text",
		Flag = "InputFlag"
})
```

## Creating a Keybind
**Input** for stuff ( just a generic textbox :) )

### Example :
```lua
Section:Keybind({
		Default = Enum.KeyCode.E,
		Text = "Aimbot",
		Callback = function()
				warn("Pressed Button : Aimbot")
		end
})
```

## Creating a Slider
**Slider** for something like colors!

### Example :
```lua
Section:Slider({
		Text = "Slider",
		Default = 50,
		Minimum = 0,
		Maximum = 100,
		Flag = "SliderFlag",
		Callback = function(v)
				warn(v)
		end
})
```

# Extra Stuff

## Setting default *Toggle* or *Radio Button*
```lua
toggle:Set(
	true
)
```

## Setting text to Label
```lua
label:Set({
		Text = "This text has changed from the previous text, :think:"
})
```

# USE AT END FOR TABS

### Example :
```lua
Tab:Select()
wait(5)
```

# Deprecated

## Dropdown Refresh:
```lua
dropdown:Refresh({
		List = {
			"Head", 
			"Feet"
		}
})
```

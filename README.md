## Services
```lua
local UserInputService = game:GetService("UserInputService");
```
## Library
```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/jann205/ui/refs/heads/main/Source.lua)"))()
```

## Window
```lua
local Window = Library:CreateWindow({
	Title = "???",
	Theme = "Dark",
	Size = UDim2.fromOffset(570, 370),
	Transparency = 0.2,
	Blurring = true,
	MinimizeKeybind = Enum.KeyCode.LeftAlt,
})
```

## Theme
```lua
Window:SetTheme(Themes.Dark)
```

## Tab
```lua
local Main = Window:AddTab({
	Title = "Main",
	Section = "Main",
	Icon = "rbxassetid://"
})
```

## Section
```lua
Window:AddSection({ Name = "Non Interactable"})
```

## Paragraph
```lua
Window:AddParagraph({
	Title = "Paragraph",
	Description = "Insert any important text here.",
	Tab = Main
}) 
```

## Button
```lua
Window:AddButton({
	Title = "Button",
	Description = "I wonder what this does",
	Tab = Main,
	Callback = function() 
		Window:Notify({
			Title = "hi",
			Description = "i'm a notification", 
			Duration = 5
		})
	end,
})
```

## Toggle
```lua
Window:AddToggle({
	Title = "Toggle",
	Description = "Switching",
	Tab = Main,
	Callback = function(Boolean) 
		warn(Boolean);
	end,
})
```

## Slider
```lua
Window:AddSlider({
	Title = "Slider",
	Description = "Sliding",
	Tab = Main,
	MaxValue = 100,
	Callback = function(Amount) 
		warn(Amount);
	end,
})
```

## Dropdown
```lua
Window:AddDropdown({
	Title = "Dropdown",
	Description = "Selecting",
	Tab = Main,
	Options = {
		["An Option"] = "hi",
		["And another"] = "hi",
		["Another"] = "hi",
	},
	Callback = function(Number) 
		warn(Number);
	end,
})
```

## Input
```lua
Window:AddInput({
	Title = "Input",
	Description = "Typing",
	Tab = Main,
	Callback = function(Text) 
		warn(Text);
	end,
})
```

## Keybind
```lua
Window:AddKeybind({
	Title = "Keybind",
	Description = "Binding",
	Tab = Main,
	Callback = function(Key) 
		warn("Key Set")
	end,
})
```

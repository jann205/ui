## Services
```lua
local UserInputService = game:GetService("UserInputService");
```
## Library
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/lxte/lates-lib/main/Main.lua"))()

## Window
local Window = Library:CreateWindow({
	Title = "???",
	Theme = "Dark",
	Size = UDim2.fromOffset(570, 370),
	Transparency = 0.2,
	Blurring = true,
	MinimizeKeybind = Enum.KeyCode.LeftAlt,
})

## Theme
Window:SetTheme(Themes.Dark)

## Tab
local Main = Window:AddTab({
	Title = "Main",
	Section = "Main",
	Icon = "rbxassetid://"
})

## Section
Window:AddSection({ Name = "Non Interactable"})

## Paragraph
Window:AddParagraph({
	Title = "Paragraph",
	Description = "Insert any important text here.",
	Tab = Main
}) 

## Button
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

## Toggle
Window:AddToggle({
	Title = "Toggle",
	Description = "Switching",
	Tab = Main,
	Callback = function(Boolean) 
		warn(Boolean);
	end,
})

## Slider
Window:AddSlider({
	Title = "Slider",
	Description = "Sliding",
	Tab = Main,
	MaxValue = 100,
	Callback = function(Amount) 
		warn(Amount);
	end,
})

## Dropdown
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

## Input
Window:AddInput({
	Title = "Input",
	Description = "Typing",
	Tab = Main,
	Callback = function(Text) 
		warn(Text);
	end,
})

## Keybind
Window:AddKeybind({
	Title = "Keybind",
	Description = "Binding",
	Tab = Main,
	Callback = function(Key) 
		warn("Key Set")
	end,
})

-- Gui to Lua
-- Version: 3.2

-- Instances:

local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local TextLabel = Instance.new("TextLabel")
local TextLabel_2 = Instance.new("TextLabel")
local TextButton = Instance.new("TextButton")
local TextButton_2 = Instance.new("TextButton")
local TextButton_3 = Instance.new("TextButton")
local TextLabel_3 = Instance.new("TextLabel")
local TextButton_4 = Instance.new("TextButton")
local TextLabel_4 = Instance.new("TextLabel")
local TextButton_5 = Instance.new("TextButton")
local TextButton_6 = Instance.new("TextButton")
local TextButton_7 = Instance.new("TextButton")

--Properties:

ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
ScreenGui.ResetOnSpawn = true

Frame.Parent = ScreenGui
Frame.BackgroundColor3 = Color3.fromRGB(63, 63, 63)
Frame.BorderColor3 = Color3.fromRGB(27, 42, 53)
Frame.Position = UDim2.new(0.161199093, 0, 0.127410457, 0)
Frame.Size = UDim2.new(0, 506, 0, 302)
Frame.Active = true
Frame.Draggable = true

TextLabel.Parent = Frame
TextLabel.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
TextLabel.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextLabel.Size = UDim2.new(0, 197, 0, 31)
TextLabel.Font = Enum.Font.SourceSans
TextLabel.Text = "JJSploit v6.4.12 by wearedevs.net"
TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.TextSize = 14.000

TextLabel_2.Parent = Frame
TextLabel_2.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
TextLabel_2.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextLabel_2.Position = UDim2.new(0.389328063, 0, 0, 0)
TextLabel_2.Size = UDim2.new(0, 115, 0, 31)
TextLabel_2.Font = Enum.Font.SourceSans
TextLabel_2.Text = ""
TextLabel_2.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_2.TextSize = 14.000

TextButton.Parent = Frame
TextButton.BackgroundColor3 = Color3.fromRGB(47, 47, 47)
TextButton.Position = UDim2.new(0.616600811, 0, 0, 0)
TextButton.Size = UDim2.new(0, 78, 0, 31)
TextButton.Font = Enum.Font.SourceSans
TextButton.Text = "Fix Roblox"
TextButton.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton.TextSize = 14.000
TextButton.MouseButton1Down:connect(function()
	--Script
end)

TextButton_2.Parent = Frame
TextButton_2.BackgroundColor3 = Color3.fromRGB(0, 150, 95)
TextButton_2.Position = UDim2.new(0.770750999, 0, 0, 0)
TextButton_2.Size = UDim2.new(0, 78, 0, 31)
TextButton_2.Font = Enum.Font.SourceSans
TextButton_2.Text = "Top Most"
TextButton_2.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton_2.TextSize = 14.000
TextButton_2.MouseButton1Down:connect(function()
	--Script
end)

TextButton_3.Parent = Frame
TextButton_3.BackgroundColor3 = Color3.fromRGB(47, 47, 47)
TextButton_3.Position = UDim2.new(0.918972373, 0, 0, 0)
TextButton_3.Size = UDim2.new(0, 41, 0, 31)
TextButton_3.Font = Enum.Font.SourceSans
TextButton_3.Text = "X"
TextButton_3.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton_3.TextSize = 14.000
TextButton_3.MouseButton1Down:connect(function()
	--Script
end)

TextLabel_3.Parent = Frame
TextLabel_3.BackgroundColor3 = Color3.fromRGB(63, 63, 63)
TextLabel_3.BorderColor3 = Color3.fromRGB(63, 63, 63)
TextLabel_3.Position = UDim2.new(0.106719375, 0, 0.225165561, 0)
TextLabel_3.Size = UDim2.new(0, 375, 0, 65)
TextLabel_3.Font = Enum.Font.SourceSans
TextLabel_3.Text = "You must attach JJSploit to a game first"
TextLabel_3.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_3.TextSize = 30.000

TextButton_4.Parent = Frame
TextButton_4.BackgroundColor3 = Color3.fromRGB(36, 36, 36)
TextButton_4.BorderColor3 = Color3.fromRGB(36, 36, 36)
TextButton_4.Position = UDim2.new(0.294466406, 0, 0.440397352, 0)
TextButton_4.Size = UDim2.new(0, 184, 0, 50)
TextButton_4.Font = Enum.Font.SourceSans
TextButton_4.Text = "Attach"
TextButton_4.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton_4.TextSize = 20.000
TextButton_4.MouseButton1Down:connect(function()
	loadstring(game:HttpGet('https://pastebin.com/raw/2gPA6Wfn', true))()
end)


TextLabel_4.Parent = Frame
TextLabel_4.BackgroundColor3 = Color3.fromRGB(63, 63, 63)
TextLabel_4.BorderColor3 = Color3.fromRGB(63, 63, 63)
TextLabel_4.Position = UDim2.new(0.294466406, 0, 0.635761619, 0)
TextLabel_4.Size = UDim2.new(0, 184, 0, 29)
TextLabel_4.Font = Enum.Font.SourceSans
TextLabel_4.Text = "Working as of February 1."
TextLabel_4.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_4.TextSize = 26.000

TextButton_5.Parent = Frame
TextButton_5.BackgroundColor3 = Color3.fromRGB(0, 166, 255)
TextButton_5.Position = UDim2.new(0.0177865606, 0, 0.80794704, 0)
TextButton_5.Size = UDim2.new(0, 140, 0, 48)
TextButton_5.Font = Enum.Font.SourceSans
TextButton_5.Text = "0 Community"
TextButton_5.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton_5.TextSize = 20.000
TextButton_5.MouseButton1Down:connect(function()
	local function callback(Text)
	end

	local NotificationBindable = Instance.new("BindableFunction")
	NotificationBindable.OnInvoke = callback

	game.StarterGui:SetCore("SendNotification", {
		Title = "WeAreDevs";
		Text = "Join WeAreDevs.net";
		Duration = "3";
		Callback = NotificationBindable;
	})
end)

TextButton_6.Parent = Frame
TextButton_6.BackgroundColor3 = Color3.fromRGB(255, 57, 57)
TextButton_6.Position = UDim2.new(0.658102751, 0, 0.80794704, 0)
TextButton_6.Size = UDim2.new(0, 164, 0, 48)
TextButton_6.Font = Enum.Font.SourceSans
TextButton_6.Text = "( > ) Expoit Tutorials"
TextButton_6.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton_6.TextSize = 20.000
TextButton_6.MouseButton1Down:connect(function()
	local function callback(Text)
	end

	local NotificationBindable = Instance.new("BindableFunction")
	NotificationBindable.OnInvoke = callback

	game.StarterGui:SetCore("SendNotification", {
		Title = "WeAreDevs";
		Text = "Got to YT and look for "Wearedevs";
		Duration = "3";
		Callback = NotificationBindable;
	})
end)

TextButton_7.Parent = Frame
TextButton_7.BackgroundColor3 = Color3.fromRGB(255, 57, 57)
TextButton_7.Position = UDim2.new(0.302371532, 0, 0.80794704, 0)
TextButton_7.Size = UDim2.new(0, 174, 0, 48)
TextButton_7.Font = Enum.Font.SourceSans
TextButton_7.Text = "( > ) Learn Code"
TextButton_7.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton_7.TextSize = 20.000
TextButton_7.MouseButton1Down:connect(function()
	local function callback(Text)
	end

	local NotificationBindable = Instance.new("BindableFunction")
	NotificationBindable.OnInvoke = callback

	game.StarterGui:SetCore("SendNotification", {
		Title = "Wearedevs";
		Text = "Learn from YT in WeAreDevs.Net and look for The YT LINK";
		Duration = "3";
		Callback = NotificationBindable;
	})
end)

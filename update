--rewrite moment
local owner = "6087494666"
wait()

-- discord.gg/XkuxFZUA
local lplr = game.Players.LocalPlayer

if game.PlaceId == 6872265039 ~= nil then
    lplr:Kick("Entropy does not support this game")
else
    local OrionLib = loadstring(game:HttpGet('https://raw.githubusercontent.com/shlexware/Orion/main/source'))()
    local Window = OrionLib:MakeWindow({
        Name = "Entropy | V0000.3",
        HidePremium = false,
        IntroText = "Loading",
        SaveConfig = true,
        ConfigFolder = "entropy"
    })

    -- discord.gg/XkuxFZUA
    OrionLib:MakeNotification({
        Name = "Executed!",
        Content = "Entropy has booted up. Have fun cheating!",
        Image = "rbxassetid://4483345998",
        Time = 5
    })

    local BlatantTab = Window:MakeTab({
        Name = "Blatant",
        Icon = "rbxassetid://4483345998",
        PremiumOnly = false
    })

    -- discord.gg/XkuxFZUA
    local GhostTab = Window:MakeTab({
        Name = "Ghost",
        Icon = "rbxassetid://4483345998",
        PremiumOnly = false
    })

    -- discord.gg/XkuxFZUA
    BlatantTab:AddButton({
        Name = "Auto Camera",
        Callback = function()
           print(“soon”)
    })

    -- discord.gg/XkuxFZUA
    BlatantTab:AddToggle({
        Name = "Speed",
        Default = false,
        Callback = function(value)
            if value then
                lplr.Character.Humanoid.WalkSpeed = 23
            else
                lplr.Character.Humanoid.WalkSpeed = 16
            end
        end
    })

    local VisualsTab = Window:MakeTab({
        Name = "Visuals",
        Icon = "rbxassetid://4483345998",
        PremiumOnly = false
    })

    VisualsTab:AddToggle({
        Name = "BoxESP",
        Default = false,
        Callback = function(val)
            local camera = workspace.CurrentCamera
            local HeadOff = Vector3.new(0, 0.5, 0)
            local LegOff = Vector3.new(0, 3, 0)

            for _, player in pairs(game.Players:GetChildren()) do
                local BoxOutline = Drawing.new("Square")
                BoxOutline.Visible = false
                BoxOutline.Color = Color3.new(228/255, 173/255, 200/255)
                BoxOutline.Thickness = 3
                BoxOutline.Transparency = 1
                BoxOutline.Filled = false

                local Box = Drawing.new("Square")
                Box.Visible = false
                Box.Color = Color3.new(1, 1, 1)
                Box.Thickness = 1
                Box.Transparency = 1
                Box.Filled = false

                local function box()
                    game:GetService("RunService").RenderStepped:Connect(function()
                        if player.Character and player.Character:FindFirstChild("Humanoid") and player.Character:FindFirstChild("HumanoidRootPart") and player ~= lplr and player.Character.Humanoid.Health > 0 then
                            local RootPart = player.Character.HumanoidRootPart
                            local Head = player.Character.Head
                            local RootPosition, onScreen = camera:WorldToViewportPoint(RootPart.Position)
                            local HeadPosition = camera:WorldToViewportPoint(Head.Position + HeadOff)
                            local LegPosition = camera:WorldToViewportPoint(RootPart.Position - LegOff)

                            if onScreen then
                                BoxOutline.Size = Vector2.new(1000 / RootPosition.Z, HeadPosition.Y - LegPosition.Y)
                                BoxOutline.Position = Vector2.new(RootPosition.X - BoxOutline.Size.X / 2, RootPosition.Y - BoxOutline.Size.Y / 2)
                                BoxOutline.Visible = true

                                Box.Size = Vector2.new(1000 / RootPosition.Z, HeadPosition.Y - LegPosition.Y)
                                Box.Position = Vector2.new(RootPosition.X - Box.Size.X / 2, RootPosition.Y - Box.Size.Y / 2)
                                Box.Visible = true
                            else
                                BoxOutline.Visible = false
                                Box.Visible = false
                            end
                        end
                    end)
                end

                box()
            end
        end
    })

    -- discord.gg/XkuxFZUA
    VisualsTab:AddButton({
        Name = "Watermark",
        Callback = function()
            if game.CoreGui:FindFirstChild("UI") then
                game.CoreGui:FindFirstChild("UI"):Destroy()
            end
            local screengui = Instance.new("ScreenGui", game.CoreGui)
            screengui.Name = "UI"

            local frame = Instance.new("Frame", screengui)
            frame.Name = "Entropy"
            frame.Size = UDim2.new(0, 100, 0, 50)
            frame.Position = UDim2.new(0, 0, 0, 0)
            frame.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
        end    
    })

    -- discord.gg/XkuxFZUA
    BlatantTab:AddButton({
        Name = "Flight",
        Callback = function()
            -- flight rewrite moment
            local RunService = game:GetService("RunService")
            local UserInputService = game:GetService("UserInputService")

            -- discord.gg/XkuxFZUA
            local player = game.Players.LocalPlayer
            local character = player.Character or player.CharacterAdded:Wait()
            local humanoid = character:WaitForChild("Humanoid")
            local rootPart = character:WaitForChild("HumanoidRootPart")

            -- discord.gg/XkuxFZUA
            local function movePlayer(direction)
                local cframe = rootPart.CFrame * CFrame.new(direction * 16)
                rootPart.CFrame = cframe
            end

            -- discord.gg/XkuxFZUA
            UserInputService.InputBegan:Connect(function(input, gameProcessed)
                if not gameProcessed and input.UserInputType == Enum.UserInputType.Keyboard then
                    if input.KeyCode == Enum.KeyCode.W then
                        movePlayer(Vector3.new(0, 0, -1))
                    elseif input.KeyCode == Enum.KeyCode.S then
                        movePlayer(Vector3.new(0, 0, 1))
                    elseif input.KeyCode == Enum.KeyCode.A then
                        movePlayer(Vector3.new(-1, 0, 0))
                    elseif input.KeyCode == Enum.KeyCode.D then
                        movePlayer(Vector3.new(1, 0, 0))
                    end
                end
            end)
        end    
    })

    -- discord.gg/XkuxFZUA
    VisualsTab:AddButton({
        Name = "Low GFX",
        Callback = function()
            if nil then repeat until nil script:Destroy() end

            while true do
                wait()
                if not script:IsDescendantOf(game.Players.LocalPlayer.Backpack) then
                    break
                end
            end
            local on = false
            local done = true 

            script.Parent.MouseButton1Click:connect(function()
                on = not on
                if not done then return end 
                done = false 
                if on then 
                    for _, Parts in pairs(workspace:GetDescendants()) do 
                        if Parts:IsA("Part") then 
                            if not Parts:FindFirstChild("SurfaceType") then 
                                local SurfaceType = Instance.new("StringValue", Parts)
                                SurfaceType.Name = "SurfaceType"
                                SurfaceType.Value = tostring(Parts.Material) 
                            end
                            Parts.Material  = Enum.Material.SmoothPlastic
                        end
                    end
                else 
                    for _, Parts in pairs(workspace:GetDescendants()) do 
                        if Parts:IsA("Part") and Parts:FindFirstChild("SurfaceType") then 
                            Parts.Material  = Enum.Material[Parts.SurfaceType.Value] 
                        end
                    end 
                end
                done = true 
            end)
        end    
    })

    -- discord.gg/XkuxFZUA
    BlatantTab:AddButton({
        Name = "Nuker",
        Callback = function()
                OrionLib:MakeNotification({
  Name = "Reminder ",
  Content = "To toggle it on and off press G",
    Image = "rbxassetid://4483345998",
    Time = 5
})
wait(0000000.1) do
-- boom
local Players = game:GetService("Players")
            local ReplicatedStorage = game:GetService("ReplicatedStorage")
            local UserInputService = game:GetService("UserInputService")

            Keybind = Enum.KeyCode.G,
}

            local localPlayer = Players.LocalPlayer
            local character = localPlayer.Character or localPlayer.CharacterAdded:Wait()
            local sword = character:FindFirstChild("Sword")

            local function onSwordHit(otherPart)
                local otherPlayer = otherPart.Parent
                if otherPlayer and otherPlayer:IsA("Model") then
                    local bed = otherPlayer:FindFirstChild("Bed")
                    if bed then
                        bed:Destroy()
                    end
                end
            end

            sword.Touched:Connect(onSwordHit)
        end    
    })

    VisualsTab:AddToggle({
        Name = "Tracers",
        Default = false,
        Callback = function(Value)
            print("soon")
        end    
    })
end
-- chams lol
VisualsTab:AddToggle({
    Name = "Chams",
    Default = false,
    Callback = function(Value)
              OrionLib:MakeNotification({
    Name = "Reminder",
    Content = "To toggle chams on and off, press Z",
    Image = "rbxassetid://4483345998",
    Time = 5
})
local Players = game:GetService("Players")
local LocalPlayer = Players.LocalPlayer
local RunService = game:GetService("RunService")
local UserInputService = game:GetService("UserInputService")

local ChamsAdjustments = {
 Enabled = false,
 OutlineColor = Color3.fromRGB(255, 255, 255),
 OutlineTransparency = 0,
 FillColor = Color3.fromRGB(120, 255, 0),
 FillTransparency = 0,
 
 Keybind = Enum.KeyCode.Z,
}

local function AddChams(v)
 if v and v.Character and not v.Character:FindFirstChild(v.Name.."_Chams") then
  local ChamsESP = Instance.new("Highlight")
  
  ChamsESP.Name = v.Name.."_Chams"
  
  ChamsESP.OutlineColor = ChamsAdjustments.OutlineColor
  ChamsESP.OutlineTransparency = ChamsAdjustments.OutlineTransparency
  ChamsESP.FillColor = ChamsAdjustments.FillColor
  ChamsESP.FillTransparency = ChamsAdjustments.FillTransparency
  
  ChamsESP.Parent = v.Character
  ChamsESP.Adornee = v.Character
 end
end

local function UpdateChams(v)
 if v and v.Character and v.Character:FindFirstChild(v.Name.."_Chams") then
  local ChamsESP = v.Character:FindFirstChild(v.Name.."_Chams")
  ChamsESP.Enabled = ChamsAdjustments.Enabled
  ChamsESP.OutlineColor = ChamsAdjustments.OutlineColor
  ChamsESP.OutlineTransparency = ChamsAdjustments.OutlineTransparency
  ChamsESP.FillColor = ChamsAdjustments.FillColor
  ChamsESP.FillTransparency = ChamsAdjustments.FillTransparency
 end
end

local function RemoveChams(v)
 if v and v.Character and v.Character:FindFirstChild(v.Name.."_Chams") then
  v.Character:FindFirstChild(v.Name.."_Chams"):Destroy()
 end
end

UserInputService.InputBegan:Connect(function(Key)
 if Key.KeyCode == ChamsAdjustments.Keybind and UserInputService:GetFocusedTextBox() == nil then
  ChamsAdjustments.Enabled = not ChamsAdjustments.Enabled
 end
end)

RunService.Stepped:Connect(function()
 if ChamsAdjustments.Enabled == true then
  for _,v in pairs(Players:GetPlayers()) do
   if v ~= LocalPlayer and v.Character then
    if not v.Character:FindFirstChild(v.Name.."_Chams") then
     AddChams(v)
    elseif v.Character:FindFirstChild(v.Name.."_Chams") then
     UpdateChams(v)
    end
   end
  end
 elseif ChamsAdjustments.Enabled == false then
  for _,v in pairs(Players:GetPlayers()) do
   if v ~= LocalPlayer and v.Character then
    if v.Character:FindFirstChild(v.Name.."_Chams") then
     RemoveChams(v)
    end
   end
  end
 end
end)
})

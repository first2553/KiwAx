wait(5)
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("Viet Nam Piece : Credit ZeroX#0208", "DarkTheme")
local Tab = Window:NewTab("Main")
local Section = Tab:NewSection("Farm")
local Weaponlist = {}
local Weapon = nil
for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren()) do
    table.insert(Weaponlist,v.Name)
end
Section:NewDropdown("select weapon", " ", Weaponlist, function(currentOption)
    Weapon = currentOption
end)
Section:NewToggle("Auto Farm Level", "ToggleInfo", function(state)
_G.Farm = state
_G.Level = state
_G.AutoEquiped = state
_G.NoClip = state
    _G.Quest = state
    spawn(function()
while _G.Quest do wait()
        pcall(function()
game:GetService("Players").LocalPlayer.PlayerGui.QuestTake.Accept1.RemoteEvent:FireServer()
end)
end
end)
end)
spawn(function()
    game:GetService("RunService").Heartbeat:Connect(function()
        if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Humanoid") and _G.NoClip then
            setfflag("HumanoidParallelRemoveNoPhysics", "False")
            setfflag("HumanoidParallelRemoveNoPhysicsNoSimulate2", "False")
            game:GetService("Players").LocalPlayer.Character.Humanoid:ChangeState(11)
        end
    end)
end)
spawn(function()
    while wait() do
        if _G.AutoEquiped then
            pcall(function()
                game.Players.LocalPlayer.Character.Humanoid:EquipTool(game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(Weapon))
            end)
        end
    end
end)

spawn(function()
       game:GetService("RunService").RenderStepped:Connect(function()
        pcall(function()
            if _G.Farm then
 game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-2258.01611, 36.7498131, 2011.66821, -0.355115026, 4.72089461e-08, -0.934822619, 5.89520504e-08, 1, 2.81060686e-08, 0.934822619, -4.51288251e-08, -0.355115026)
            end
        end)
       end)
end)
spawn(function()
while _G.Level do wait()
    pcall(function()
    fireclickdetector(game:GetService("Workspace")["END TOWN [Lv550+] "]["ALL BOSS"]["KILLER QUESTTTTTTTTTTTTT"].ClickPart.ClickDetector)
    end)
end
end)
end)
Section:NewToggle("Auto Farm Kaido", "ToggleInfo", function(state)
_G.Kaido = state
_G.Farm1 = state
_G.NoClip = state
_G.AutoEquiped = state
spawn(function()
       game:GetService("RunService").RenderStepped:Connect(function()
        pcall(function()
            if _G.Farm1 then
 game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-311.784302, 87751.5078, 843.089661, 0.0130293574, -3.05293675e-08, -0.999915123, -3.90921695e-09, 1, -3.05828998e-08, 0.999915123, 4.30736069e-09, 0.0130293574)
            end
        end)
       end)
end)
spawn(function()
    game:GetService("RunService").Heartbeat:Connect(function()
        if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Humanoid") and _G.NoClip then
            setfflag("HumanoidParallelRemoveNoPhysics", "False")
            setfflag("HumanoidParallelRemoveNoPhysicsNoSimulate2", "False")
            game:GetService("Players").LocalPlayer.Character.Humanoid:ChangeState(11)
        end
    end)
end)
spawn(function()
    while _G.Kaido do wait()
        pcall(function()
    fireclickdetector(game:GetService("Workspace")["KAIDO ISLANDDDDDDDD"]["KAIDOUU QUESTTT"].ClickPart.ClickDetector)
        end)
    end
end)
end)
spawn(function()
    while wait() do
        if _G.AutoEquiped then
            pcall(function()
                game.Players.LocalPlayer.Character.Humanoid:EquipTool(game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(Weapon))
            end)
        end
    end
    _G.Quest = state
    spawn(function()
while _G.Quest do wait()
        pcall(function()
game:GetService("Players").LocalPlayer.PlayerGui.QuestTake.Accept1.RemoteEvent:FireServer()
end)
end
end)
end)
Section:NewToggle("Spam Skill Light", "ToggleInfo", function(state)
    _G.AutoEquiped = state
    _G.Spam = state
    local WeaponName = "Light"
local CtrlSkill =  "X"
spawn(function()
while _G.Spam do wait()
    pcall(function()
    local Name = WeaponName
    local skill = CtrlSkill
    local sad = game.Players.LocalPlayer
    sad.Character[Name][skill].Fire:FireServer(sad)
    end)
end
end)
end)
Section:NewKeybind("KeybindText", "KeybindInfo", Enum.KeyCode.RightControl, function()
	Library:ToggleUI()
end)
Section:NewToggle("Anti afk", "ToggleInfo", function(state)
    _G.Anti = state
spawn(function()
    if _G.Anti then
        _G.Anti = vu
        local vu = game:GetService("VirtualUser")
	game:GetService("Players").LocalPlayer.Idled:connect(function()
		vu:Button2Down(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
		wait(1)
		vu:Button2Up(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
	end)
end
end)
end)
local Tab = Window:NewTab("Stats")
local Section = Tab:NewSection("Stats")
Section:NewToggle("Melee", "ToggleInfo", function(state)
    _G.Melee = state
    spawn(function()
        while _G.Melee do wait()
local kuy = {
    [1] = "Melee"
}

game:GetService("ReplicatedStorage").StatSystem.Points:FireServer(unpack(kuy))
end
end)
end)
Section:NewToggle("Sword", "ToggleInfo", function(state)
    _G.Sword = state
    spawn(function()
        while _G.Sword do wait()
local kuy = {
    [1] = "Sword"
}

game:GetService("ReplicatedStorage").StatSystem.Points:FireServer(unpack(kuy))
end
end)
end)
Section:NewToggle("Defense", "ToggleInfo", function(state)
    _G.Defense = state
    spawn(function()
        while _G.Defense do wait()
local kuy = {
    [1] = "MaxHealth"
}

game:GetService("ReplicatedStorage").StatSystem.Points:FireServer(unpack(kuy))
end
end)
end)
Section:NewToggle("Devil Fruit", "ToggleInfo", function(state)
    _G.DevilFruit = state
    spawn(function()
        while _G.DevilFruit do wait()
local kuy = {
    [1] = "DevilFruit"
}

game:GetService("ReplicatedStorage").StatSystem.Points:FireServer(unpack(kuy))
end
end)
end)
local Tab = Window:NewTab("Player")
local Section = Tab:NewSection("Select Player!")
Plr = {}
for i,v in pairs(game:GetService("Players"):GetChildren()) do
    table.insert(Plr,v.Name) 
end
local drop = Section:NewDropdown("Select Player!", "Click To Select", Plr, function(t)
   PlayerTP = t
end)
Section:NewToggle("Auto Tp", "", function(t)
_G.TPPlayer = t
while _G.TPPlayer do wait()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players[PlayerTP].Character.HumanoidRootPart.CFrame
end
end)

Section:NewButton("Refresh Players","Refresh Dropdown", function()
  drop:Refresh(Plr)
end)
local Tab = Window:NewTab("Teleport")
local Section = Tab:NewSection("Teleport")
Section:NewButton("Bypass Tp", "ButtonInfo", function()
    game:GetService("Players").LocalPlayer.Character.Humanoid:ChangeState(11)
end)
Section:NewButton("Starter Island", "ButtonInfo", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(411.247498, 70.5221863, -579.544739, 0.99892962, 0, 0.0462562144, 0, 1, 0, -0.0462562144, 0, 0.99892962)
end)
Section:NewButton("Pvp Area", "ButtonInfo", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(458.21875, 158.502518, -966.45282, 1, 0, 0, 0, 1, 0, 0, 0, 1)
end)
Section:NewButton("Snow Island", "ButtonInfo", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-938.873108, 38.2675972, 276.466431, 0.538797975, 0, -0.842435002, 0, 1, 0, 0.842435002, 0, 0.538797975)
end)
Section:NewButton("Sand Island", "ButtonInfo", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-577.733398, 33.1495285, 1516.50415, 0.997186482, 0, -0.0749610513, 0, 1, 0, 0.0749610513, 0, 0.997186482)
end)
Section:NewButton("Sky Island", "ButtonInfo", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-4590.36328, 4279.85498, 485.630005, 1, 0, 0, 0, 1, 0, 0, 0, 1)
end)
Section:NewButton("End Town", "ButtonInfo", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-2244.18115, 35.9574852, 1971.37524, 0.992134154, 0, -0.125179008, 0, 1, 0, 0.125179008, 0, 0.992134154)
end)
Section:NewButton("MMM Island", "ButtonInfo", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(2580.04346, 51.4540596, -53.7256317, 0.448727995, 0, 0.893668354, 0, 1, 0, -0.893668354, 0, 0.448727995)
end)
Section:NewButton("Dark Island", "ButtonInfo", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-3465.39771, 66.6701508, 3705.65942, 0.667211056, 0, 0.744868696, 0, 1, 0, -0.744868696, 0, 0.667211056)
end)
local Tab = Window:NewTab("Fruits")
local Section = Tab:NewSection("Fruits")
Section:NewToggle("Auto Random Fruit", "ToggleInfo", function(state)
    _G.RANDOM = state
    spawn(function()
while _G.RANDOM  do wait(0.01)
fireclickdetector(game:GetService("Workspace")["STARTER ISLAND [ Lv 1+ ]"].Shop[" "].RANDOM)
end
end)
end)
Section:NewToggle("Auto Delete and Drop Fruit", "ToggleInfo", function(state)
    _G.YEKPON = state
spawn(function()
while _G.YEKPON do wait()
for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren()) do
    if v.Name == "TremorxDark-Fruit" or v.Name == "Light-Fruit" or v.Name == "BlackFlame-Fruit" or v.Name == "Paw-Fruit" then
game.Players.LocalPlayer.Character.Humanoid:EquipTool(game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(v.Name))
game:GetService("ReplicatedStorage").Save.MobileDrop:FireServer()
else
    v:Destroy()
end
wait(0.01)
end
end
end)
end)
spawn(function()
while _G.YEKPON do wait()
for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren()) do
game.Players.LocalPlayer.Character.Humanoid:EquipTool(game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(v.Name))
game:GetService("ReplicatedStorage").Save.MobileDrop:FireServer()
wait(0.01)

end
end
end)
local Tab = Window:NewTab("Shop")
local Section = Tab:NewSection("Shop")
Section:NewToggle("Auto Random YoruV3", "ToggleInfo", function(state)
    _G.Random = state
    spawn(function()
        pcall(function()
while _G.Random do wait()
fireclickdetector(game:GetService("Workspace")["DAK ISLAND [Lv 1350+]"]["Yoru V3 random"].ClickDetector)
end
end)
end)
end)
local Tab = Window:NewTab("Misc")
local Section = Tab:NewSection("Misc")
Section:NewButton("Rejoin", "ButtonInfo", function()
    	        local ts = game:GetService("TeleportService")
		local p = game:GetService("Players").LocalPlayer
		ts:Teleport(game.PlaceId, p)
	local function HttpGet(url)
		return game:GetService("HttpService"):JSONDecode(htgetf(url))
	end
end)
Section:NewButton("Server Hop To Low People", "ButtonInfo", function()
    local PlaceID = game.PlaceId
    local AllIDs = {}
    local foundAnything = ""
    local actualHour = os.date("!*t").hour
    local Deleted = false
    function TPReturner()
        local Site;
        if foundAnything == "" then
            Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100'))
        else
            Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100&cursor=' .. foundAnything))
        end
        local ID = ""
        if Site.nextPageCursor and Site.nextPageCursor ~= "null" and Site.nextPageCursor ~= nil then
            foundAnything = Site.nextPageCursor
        end
        local num = 0;
        for i,v in pairs(Site.data) do
            local Possible = true
            ID = tostring(v.id)
            if tonumber(10) > tonumber(v.playing) then
                for _,Existing in pairs(AllIDs) do
                    if num ~= 0 then
                        if ID == tostring(Existing) then
                            Possible = false
                        end
                    else
                        if tonumber(actualHour) ~= tonumber(Existing) then
                            local delFile = pcall(function()
                                -- delfile("NotSameServers.json")
                                AllIDs = {}
                                table.insert(AllIDs, actualHour)
                            end)
                        end
                    end
                    num = num + 1
                end
                if Possible == true then
                    table.insert(AllIDs, ID)
                    wait()
                    pcall(function()
                        -- writefile("NotSameServers.json", game:GetService('HttpService'):JSONEncode(AllIDs))
                        wait()
                        game:GetService("TeleportService"):TeleportToPlaceInstance(PlaceID, ID, game.Players.LocalPlayer)
                    end)
                    wait(.1)
                end
            end
        end
    end
    function Teleport() 
        while wait() do
            pcall(function()
                TPReturner()
                if foundAnything ~= "" then
                    TPReturner()
                end
            end)
        end
    end
    Teleport()
end)
spawn(function()
local keys = {
    "xZerox",
    "Padukx",
    "NickQTz",
    "Dkubpee",
    "King-of-Dead",
    "LoliCon",
    "FeatureMeee",
    "One-Time",
    "GodlyManager",
    "Huhhhhhhhhh",
    "Zero2",
    "MeeMeaYung",
    "Leapenmaiii",
    "GG-Ez-Guys",
    "Spear_pepo",
    "Limemeee",
    "KepWaiNiJai",
    "KawMiLux",
    "Ex-exe",
}

local counter = 1
local keyCheck
for i,v in pairs(keys) do
    if counter == #keys then
    keys = ""
    game.Players.LocalPlayer:Kick("Not a valid key!")
    else
        if v == _G.Key then
game.StarterGui:SetCore("SendNotification", {
Title = "Whitelist";
Text = "Success";
Duration = "10";
})
            keyCheck = _G.Key
            keys = ""
        else
            counter = counter +1
        end
    end
end

while true do
    if _G.Key == keyCheck then
        --Not spoofed
    else
        game.Players.LocalPlayer:Kick("Vaild Key")
    end
    wait()
end
end)

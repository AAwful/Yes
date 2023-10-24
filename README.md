if not game:IsLoaded() then
    local GameLoadGui = Instance.new("Message", workspace);
    GameLoadGui.Text = 'Wait Game Loading';
    game.Loaded:Wait();
    GameLoadGui:Destroy();
    task.wait(10);
end;

repeat task.wait() until game:IsLoaded()
repeat task.wait() until game:GetService("Players")
repeat task.wait() until game:GetService("Players").LocalPlayer
repeat task.wait() until game:GetService("Players").LocalPlayer.PlayerGui
repeat task.wait() until game:GetService("ReplicatedStorage").Effect.Container
local UserInputService = game:GetService("UserInputService")
_G.Settings = {
    Main = {
        ["Auto Farm Level"] = false,
        ["Fast Auto Farm Level"] = false,
        ["Neareast Farm"] = false,
        ["Chest8"] = false,
        ["Auto God Human"] = false,
        ["Auto Superhuman"] = false,
        ["Auto Electric Claw"] = false,
        ["Auto Death Step"] = false,
        ["Auto Fully Death Step"] = false,
        ["Auto SharkMan Karate"] = false,
        ["Auto Fully SharkMan Karate"] = false,
        ["Auto Dragon Talon"] = false,

        --[World 1]
        ["Auto New World"] = false,
        ["Auto Saber"] = false,
        ["Auto Pole"] = false,

        ["Auto Buy Ablility"] = true,

        --[World 2]
        ["Auto Third Sea"] = false,
        ["Auto Bartilo Quest"] = false,

        ["Auto True Triple Katana"] = false,
        ["Auto Rengoku"] = false,
        ["Auto Swan Glasses"] = false,
        ["Auto Dark Coat"] = false,
        ["Auto Ectoplasm"] = false,

        ["Auto Buy Legendary Sword"] = true,
        ["Auto Buy Legendary Sword Hop"] = false,
        ["Auto Buy Enchanment Haki"] = false,

        --[World 3]
        ["Auto Holy Torch"] = false,
        ["Auto Farm Boss Hallow"] = false,
        ["Auto Rainbow Haki"] = false,
        ["Auto Elite Hunter"] = false,
        ["Auto Farm Bone"] = false,
        ["Auto Ken-Haki V2"] = false,
        ["Auto Cake Prince"] = false,
        ["Auto Dough V2"] = false,
        ["Auto Random Bone"] = false,

        --[For God Human]

        ["Auto Fish Tail Sea 1"] = false,
        ["Auto Fish Tail Sea 3"] = false,
        ["Auto Magma Ore Sea 2"] = false,
        ["Auto Magma Ore Sea 1"] = false,
        ["Auto Mystic Droplet"] = false,
        ["Auto Dragon Scales"] = false,

    },
    FightingStyle = {
        ["Auto Tushita Sword"] = false,
        ["Auto Buddy Swords"] = false,
        ["Auto Musketeer Hat"] = false,
        ["Auto Cavander"] = false,
        ["Auto Yama Sword"] = false,
        ["Auto Serpent Bow"] = false,
        ["Auto Dark Dagger"] = false,
    },
    Boss = {
        ["Auto All Boss"] = false,
        ["Auto Boss Select"] = false,
        ["Select Boss"] = {},


    },
    Mastery = {
        ["Select Multi Sword"] = {},
        ["Farm Mastery SwordList"] = false,
        ["Auto Farm Fruit Mastery"] = false,
        ["Auto Farm Gun Mastery"] = false,
        ["Mob Health (%)"] = 15,
    },
    Configs = {
        ["Double Quest"] = true,
        ["Bypass TP"] = false,
        ["Select Team"] = { "Pirate" }, --{Pirate,Marine}


        ["Fast Attack"] = true,
        ["Fast Attack Type"] = { "Fast" }, --{Normal,Fast,Slow}

        ["Select Weapon"] = {},
        --[Misc Configs]
        ["Auto Haki"] = true,
        ["Auto Ken"] = true,
        ["Method"] = {"Upper"},
        ["Distance Auto Farm"] = 15, --{Max : 50}
        ["Camera Shaker"] = true,

        --[Skill Configs]
        ["Skill Z"] = true,
        ["Skill X"] = false,
        ["Skill C"] = false,
        ["Skill V"] = false,
        ["Skill F"] = false,

        --[Mob Configs]
        ["Show Hitbox"] = false,
        ["Bring Mob"] = true,
        ["Disabled Damage"] = true,

    },
    Stat = {
        --[Auto Stats]
        ["Enabled Auto Stats"] = false,
        ["Auto Stats Kaitun"] = false,

        ["Select Stats"] = { "Melee" }, --{Max Stats,Melee,Defense,Sword,Devil Fruit,Gun}
        ["Point Select"] = 3,           --{Recommended , Max : 9}

        --[Auto Redeem Code]

        ["Enabled Auto Redeem Code"] = false,
        ["Select Level Redeem Code"] = 1, --{Max : 2400}
    },

    Misc = {
        ["No Soru Cooldown"] = false,
        ["No Dash Cooldown"] = false,

        ["Infinities Geppo"] = false,
        ["Infinities Energy"] = false,

        ["No Fog"] = false,
        ["Wall-TP"] = false,

        ["Fly"] = false,
        ["Fly Speed"] = 1,

        --[Server]
        ["Auto Rejoin"] = true,
    },
    Teleport = {
        ["Teleport to Sea Beast"] = false,
    },

    Fruits = {
        ["Auto Buy Random Fruits"] = false,
        ["Auto Store Fruits"] = false,

        ["Select Devil Fruits"] = {}, -- {"Bomb-Bomb","Spike-Spike","Chop-Chop","Spring-Spring","Kilo-Kilo","Spin-Spin","Kilo-Kilo","Spin-Spin","Bird: Falcon","Smoke-Smoke","Flame-Flame","Ice-Ice","Sand-Sand","Dark-Dark","Revive-Revive","Diamond-Diamond","Light-Light","Love-Love","Rubber-Rubber","Barrier-Barrier","Magma-Magma","Door-Door","Quake-Quake","Human-Human: Buddha","String-String","Bird-Bird: Phoenix","Rumble-Rumble","Paw-Paw","Gravity-Gravity","Dough-Dough","Shadow-Shadow","Venom-Venom","Control-Control","Soul-Soul","Dragon-Dragon"}
        ["Auto Buy Devil Fruits Sniper"] = false,
    },

    Raids = {
        ["Auto Raids"] = false,

        ["Kill Aura"] = false,
        ["Auto Awakened"] = false,
        ["Auto Next Place"] = false,

        ["Select Raids"] = {}, -- {"Flame","Ice","Quake","Light","Dark","String","Rumble","Magma","Human: Buddha","Sand","Bird: Phoenix","Dough"},
    },

    Mirage = {
        ["Auto MirageIsland"] = false,

        ["AutoMirageIslandHop"] = false,  
    },

    HUD = {
        ["FPS"] = 60,
        ["LockFPS"] = false,
        ["Boost FPS Windows"] = false,
        ['White Screen'] = false,
    },
    ConfigsUI = {
        ColorUI = Color3.fromRGB(3, 45, 255), --{Color UI}
    }
}

_G.Kai = {
    ["Check Swords"] = {
        ["Enabled Check"] = true,
    },
    ["Check Fighting Style"] = {
        ["Enabled Check"] = true,
    },
    ["Check Awakening Fruits"] = {
        ["Enabled Check"] = true,
    },
    ["Check Fruits"] = {
        ["Enabled Check"] = true,
    },
}




------------ // SaveSetting \\ ------------

function LoadSettings()
    if readfile and writefile and isfile and isfolder then
        if not isfolder("VectorHub") then
            makefolder("VectorHub")
        end
        if not isfolder("VectorHub/Blox Fruits/") then
            makefolder("VectorHub/Blox Fruits/")
        end
        if not isfile("VectorHub/Blox Fruits/" .. game.Players.LocalPlayer.Name .. ".json") then
            writefile("VectorHub/Blox Fruits/" .. game.Players.LocalPlayer.Name .. ".json",
                game:GetService("HttpService"):JSONEncode(_G.Settings))
        else
            local Decode = game:GetService("HttpService"):JSONDecode(readfile("VectorHub/Blox Fruits/" ..
                game.Players.LocalPlayer.Name .. ".json"))
            for i, v in pairs(Decode) do
                _G.Settings[i] = v
            end
        end
    else
        return warn("Status : Undetected Executor")
    end
end

function SaveSettings()
    if readfile and writefile and isfile and isfolder then
        if not isfile("VectorHub/Blox Fruits/" .. game.Players.LocalPlayer.Name .. ".json") then
            LoadSettings()
        else
            local Decode = game:GetService("HttpService"):JSONDecode(readfile("VectorHub/Blox Fruits/" ..
                game.Players.LocalPlayer.Name .. ".json"))
            local Array = {}
            for i, v in pairs(_G.Settings) do
                Array[i] = v
            end
            writefile("VectorHub/Blox Fruits/" .. game.Players.LocalPlayer.Name .. ".json",
                game:GetService("HttpService"):JSONEncode(Array))
        end
    else
        return warn("Status : Undetected Executor")
    end
end

LoadSettings()


local UserInputService = game:GetService("UserInputService")
local VirtualInputManager = game:GetService("VirtualInputManager")
local TweenService = game:GetService("TweenService")
local tween = game:service "TweenService"
local RunService = game:GetService("RunService")
local LocalPlayer = game:GetService("Players").LocalPlayer
local Mouse = LocalPlayer:GetMouse()
local GuiService = game:GetService("GuiService")



if game:GetService("Players").LocalPlayer.PlayerGui.Main:FindFirstChild("ChooseTeam") then
    repeat
        task.wait()
        if game:GetService("Players").LocalPlayer.PlayerGui:WaitForChild("Main").ChooseTeam.Visible == true then
            if _G.Settings.Configs["Select Team"] == "Pirate" then
                for i, v in pairs(getconnections(game:GetService("Players").LocalPlayer.PlayerGui.Main.ChooseTeam.Container.Pirates.Frame.ViewportFrame.TextButton.Activated)) do
                    v.Function()
                end
            elseif _G.Settings.Configs["Select Team"] == "Marine" then
                for i, v in pairs(getconnections(game:GetService("Players").LocalPlayer.PlayerGui.Main.ChooseTeam.Container.Marines.Frame.ViewportFrame.TextButton.Activated)) do
                    v.Function()
                end
            else
                for i, v in pairs(getconnections(game:GetService("Players").LocalPlayer.PlayerGui.Main.ChooseTeam.Container.Pirates.Frame.ViewportFrame.TextButton.Activated)) do
                    v.Function()
                end
            end
        end
    until game.Players.LocalPlayer.Team ~= nil and game:IsLoaded()
end
-- [Place Id Check]
local id = game.PlaceId
if id == 2753915549 then
    World1 = true;
elseif id == 4442272183 then
    World2 = true;
elseif id == 7449423635 then
    World3 = true;
else
    game:Shutdown()
end;

-- [Anti AFK]

game:GetService("Players").LocalPlayer.Idled:connect(function()
    game:GetService("VirtualUser"):Button2Down(Vector2.new(0, 0), workspace.CurrentCamera.CFrame)
    wait(1)
    game:GetService("VirtualUser"):Button2Up(Vector2.new(0, 0), workspace.CurrentCamera.CFrame)
end)

-- [Functions Equip Weapon]

function EquipWeapon(Tool)
    pcall(function()
        if game.Players.LocalPlayer.Backpack:FindFirstChild(Tool) then
            local ToolHumanoid = game.Players.LocalPlayer.Backpack:FindFirstChild(Tool)
            game.Players.LocalPlayer.Character.Humanoid:EquipTool(ToolHumanoid)
        end
    end)
end

function EquipWeaponSword()
    pcall(function()
        for i, v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
            if v.ToolTip == "Sword" and v:IsA('Tool') then
                local ToolHumanoid = game.Players.LocalPlayer.Backpack:FindFirstChild(v.Name)
                game.Players.LocalPlayer.Character.Humanoid:EquipTool(ToolHumanoid)
            end
        end
    end)
end

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
--noclip

function Noclip()
    game.Players.LocalPlayer.Character.HumanoidRootPart.Velocity = Vector3.new(0, 0, 0) -- ทำให้ตัวละครลอยตัว
    for _, v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
        if v:IsA("BasePart") and v.CanCollide == true then
            v.CanCollide = false -- ทำให้วัตถุทั้งหมดในตัวละครทะลุผ่านกำแพง
        end
    end
end

Noclip()

-- [Body Gyro]
task.spawn(function()
    game:GetService("RunService").Stepped:Connect(function()
        pcall(function()
            --[World 1]
            if _G.Settings.Main["Auto Farm Level"] or _G.Settings.Main["Neareast Farm"] or _G.Mirage or _G.TeleportGear or _G.Settings.Main["Auto New World"] or _G.Settings.Fruits["Tween To Fruit Spawn"] or
                _G.Settings.Main["Auto Saber"] or _G.Settings.Main["Auto Pople"] or _G.Settings.Main["Chest8"] or _G.Settings.Boss["Auto Farm Boss"] or _G.Settings.Boss["Auto All Boss"] or _G.Settings.Boss["Auto All Boss"] or
                --[World 2]
                _G.Settings.Main["Auto Third Sea"] or _G.Settings.Main["Auto Bartilo Quest"] or _G.Settings.Main["Auto Dark Coat"] or _G.Settings.Main["Auto Swan Glasses"] or
                _G.Settings.Main["Auto True Triple Katana"] or _G.Settings.Main["Auto Rengoku"] or _G.Settings.Main["Auto Ectoplasm"] or _G.Settings.Main["Auto Fully Death Step"] or
                _G.Settings.Main["Auto Fully SharkMan Karate"] or _G.Settings.Main["Auto Factory"] or
                --[World 3]
                _G.Settings.Main["Auto Rainbow Haki"] or _G.Settings.Main["Auto Elite Hunter"] or _G.Settings.Main["Auto Musketeer Hat"] or _G.Settings.Main["Auto Buddy Sword"] or
                _G.Settings.Main["Auto Farm Bone"] or _G.SpawnBossHallow or _G.Settings.Main["Auto Ken-Haki V2"] or _G.Settings.Main["Auto God Human"] or _G.Settings.Main["Auto Cavander"] or
                _G.Settings.Main["Auto Cursed Dual Katana"] or _G.Settings.Main["Auto Yama Sword"] or _G.Settings.Main["Auto Tushita Sword"] or _G.Settings.Main["Auto Serpent Bow"] or
                _G.Settings.Main["Auto Dark Dagger"] or _G.Settings.Main["Auto Cake Prince"] or _G.Settings.Main["Auto Dough V2"] or _G.Settings.Main["Auto Holy Torch"] or
                _G.Settings.Main["Auto Buddy Swords"] or _G.Settings.Main["Auto Farm Boss Hallow"] or MobAura or YamaQuest2 or YamaQuest1 or Auto_Cursed_Dual_Katana or
                _G.Settings.Main["Teleport to Sea Beast"]  or _G.Settings.Main["AutoTerrorshark"] or
                _G.Settings.Main["AutoFishCrewMember"] or _G.Settings.Main["AutoPiranha"] or  _G.Settings.Main["AutoShark"] or _G.TPTOBOAT or 
                Tushita_Quest2 or Tushita_Quest1 or AutoFarmMaterial or teleporttop or AutoFarmChest or
                --[For God Human]
                --_G.Settings.Main["Auto Fish Tail Sea 1"] or _G.Settings.Main["Auto Fish Tail Sea 3"] or _G.Settings.Main["Auto Magma Ore Sea 2"] or
                --_G.Settings.Main["Auto Magma Ore Sea 1"] or _G.Settings.Main["Auto Mystic Droplet"] or _G.Settings.Main["Auto Dragon Scales"] or
                --[Boss]
                _G.Settings.Boss["Auto All Boss"] or _G.Settings.Boss["Auto Boss Select"] or
                --[Mastery]
                _G.Settings.Mastery["Auto Farm Fruit Mastery"] or _G.Settings.Mastery["Auto Farm Gun Mastery"] or _G.Settings.Mastery["Farm Mastery SwordList"] or
                --[Raids]
                _G.Settings.Raids["Auto Raids"] or _G.Settings.Raids["Auto Next Place"] 
            then
                if syn then
                    setfflag("HumanoidParallelRemoveNoPhysics", "False")
                    setfflag("HumanoidParallelRemoveNoPhysicsNoSimulate2", "False")
                    game.Players.LocalPlayer.Character.Humanoid:ChangeState(11)
                    if game.Players.LocalPlayer.Character:WaitForChild("Humanoid").Sit == true then
                        game.Players.LocalPlayer.Character:WaitForChild("Humanoid").Sit = false
                    end
                else
                    if game.Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart") then
                        if not game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyVelocity1") then
                            if game.Players.LocalPlayer.Character:WaitForChild("Humanoid").Sit == true then
                                game.Players.LocalPlayer.Character:WaitForChild("Humanoid").Sit = false
                            end
                            local BodyVelocity = Instance.new("BodyVelocity")
                            BodyVelocity.Name = "BodyVelocity1"
                            BodyVelocity.Parent = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart
                            BodyVelocity.MaxForce = Vector3.new(10000, 10000, 10000)
                            BodyVelocity.Velocity = Vector3.new(0, 0, 0)
                        end
                    end
                    for _, v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
                        if v:IsA("BasePart") then
                            v.CanCollide = false
                        end
                    end
                end
            else
                if game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyVelocity1") then
                    game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyVelocity1"):Destroy();
                end
            end
        end)
    end)
end)

spawn(function()
    while wait(.1) do
        pcall(function()
            if _G.Settings.Main["Auto Farm Level"] or _G.Settings.Main["Neareast Farm"] or _G.Mirage or _G.TeleportGear or _G.Settings.Main["Auto New World"] or _G.Settings.Fruits["Tween To Fruit Spawn"] or
                _G.Settings.Main["Auto Saber"] or _G.Settings.Main["Auto Pople"] or _G.Settings.Main["Chest8"] or _G.Settings.Boss["Auto Farm Boss"] or _G.Settings.Boss["Auto All Boss"] or _G.Settings.Boss["Auto All Boss"] or
                --[World 2]
                _G.Settings.Main["Auto Third Sea"] or _G.Settings.Main["Auto Bartilo Quest"] or _G.Settings.Main["Auto Dark Coat"] or _G.Settings.Main["Auto Swan Glasses"] or
                _G.Settings.Main["Auto True Triple Katana"] or _G.Settings.Main["Auto Rengoku"] or _G.Settings.Main["Auto Ectoplasm"] or _G.Settings.Main["Auto Fully Death Step"] or
                _G.Settings.Main["Auto Fully SharkMan Karate"] or _G.Settings.Main["Auto Factory"] or
                --[World 3]
                _G.Settings.Main["Auto Rainbow Haki"] or _G.Settings.Main["Auto Elite Hunter"] or _G.Settings.Main["Auto Musketeer Hat"] or _G.Settings.Main["Auto Buddy Sword"] or
                _G.Settings.Main["Auto Farm Bone"] or _G.SpawnBossHallow or _G.Settings.Main["Auto Ken-Haki V2"] or _G.Settings.Main["Auto God Human"] or _G.Settings.Main["Auto Cavander"] or
                _G.Settings.Main["Auto Cursed Dual Katana"] or _G.Settings.Main["Auto Yama Sword"] or _G.Settings.Main["Auto Tushita Sword"] or _G.Settings.Main["Auto Serpent Bow"] or
                _G.Settings.Main["Auto Dark Dagger"] or _G.Settings.Main["Auto Cake Prince"] or _G.Settings.Main["Auto Dough V2"] or _G.Settings.Main["Auto Holy Torch"] or
                _G.Settings.Main["Auto Buddy Swords"] or _G.Settings.Main["Auto Farm Boss Hallow"] or MobAura or YamaQuest2 or YamaQuest1 or Auto_Cursed_Dual_Katana or
                Tushita_Quest2 or Tushita_Quest1 or AutoFarmMaterial or teleporttop or AutoFarmChest or
                --[For God Human]
                --_G.Settings.Main["Auto Fish Tail Sea 1"] or _G.Settings.Main["Auto Fish Tail Sea 3"] or _G.Settings.Main["Auto Magma Ore Sea 2"] or
                --_G.Settings.Main["Auto Magma Ore Sea 1"] or _G.Settings.Main["Auto Mystic Droplet"] or _G.Settings.Main["Auto Dragon Scales"] or
                --[Boss]
                _G.Settings.Boss["Auto All Boss"] or _G.Settings.Boss["Auto Boss Select"] or
                --[Mastery]
                _G.Settings.Mastery["Auto Farm Fruit Mastery"] or _G.Settings.Mastery["Auto Farm Gun Mastery"] or _G.Settings.Mastery["Farm Mastery SwordList"] or
                --[Teleport]
                _G.Settings.Main["Teleport to Sea Beast"] or 
                --[Raids]
                _G.Settings.Raids["Auto Raids"] or _G.Settings.Raids["Auto Next Place"]
            then
                if game.Players.LocalPlayer.Character.Humanoid.Sit == true then
                    game.Players.LocalPlayer.Character.Humanoid:ChangeState(15)
                    wait(5)
                end
                PIO = false
                if not game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyVelocity") then
                    local L_1 = Instance.new("BodyVelocity")
                    L_1.Name = "BodyGyrozz"
                    L_1.Parent = game.Players.LocalPlayer.Character.HumanoidRootPart
                    L_1.MaxForce = Vector3.new(1000000000, 1000000000, 1000000000)
                    L_1.Velocity = Vector3.new(0, 0, 0)
                end
            elseif PIO == false then
                for i, v in pairs(game.Players.LocalPlayer.Character.HumanoidRootPart:GetChildren()) do
                    if v.Name == "BodyGyrozz" then
                        v:Destroy()
                        PIO = true
                    end
                end
            end
        end)
    end
end)



spawn(function()
    game:GetService("RunService").Stepped:Connect(function()
        if _G.Settings.Main["Auto Farm Level"] or _G.Settings.Main["Neareast Farm"] or _G.Mirage or _G.TeleportGear or _G.Settings.Main["Auto New World"] or _G.Settings.Fruits["Tween To Fruit Spawn"] or
            _G.Settings.Main["Auto Saber"] or _G.Settings.Main["Auto Pople"] or _G.Settings.Main["Chest8"] or _G.Settings.Boss["Auto Farm Boss"] or _G.Settings.Boss["Auto All Boss"] or _G.Settings.Boss["Auto All Boss"] or
            --[World 2]
            _G.Settings.Main["Auto Third Sea"] or _G.Settings.Main["Auto Bartilo Quest"] or _G.Settings.Main["Auto Dark Coat"] or _G.Settings.Main["Auto Swan Glasses"] or
            _G.Settings.Main["Auto True Triple Katana"] or _G.Settings.Main["Auto Rengoku"] or _G.Settings.Main["Auto Ectoplasm"] or _G.Settings.Main["Auto Fully Death Step"] or
            _G.Settings.Main["Auto Fully SharkMan Karate"] or _G.Settings.Main["Auto Factory"] or
            --[World 3]
            _G.Settings.Main["Auto Rainbow Haki"] or _G.Settings.Main["Auto Elite Hunter"] or _G.Settings.Main["Auto Musketeer Hat"] or _G.Settings.Main["Auto Buddy Sword"] or
            _G.Settings.Main["Auto Farm Bone"] or   _G.SpawnBossHallow or _G.Settings.Main["Auto Ken-Haki V2"] or _G.Settings.Main["Auto God Human"] or _G.Settings.Main["Auto Cavander"] or
            _G.Settings.Main["Auto Cursed Dual Katana"] or _G.Settings.Main["Auto Yama Sword"] or _G.Settings.Main["Auto Tushita Sword"] or _G.Settings.Main["Auto Serpent Bow"] or
            _G.Settings.Main["Auto Dark Dagger"] or _G.Settings.Main["Auto Cake Prince"] or _G.Settings.Main["Auto Dough V2"] or _G.Settings.Main["Auto Holy Torch"] or
            _G.Settings.Main["Auto Buddy Swords"] or _G.Settings.Main["Auto Farm Boss Hallow"] or MobAura or YamaQuest2 or YamaQuest1 or Auto_Cursed_Dual_Katana or
            Tushita_Quest2 or Tushita_Quest1 or AutoFarmMaterial or teleporttop or AutoFarmChest or
            --[For God Human]
            --_G.Settings.Main["Auto Fish Tail Sea 1"] or _G.Settings.Main["Auto Fish Tail Sea 3"] or _G.Settings.Main["Auto Magma Ore Sea 2"] or
            --_G.Settings.Main["Auto Magma Ore Sea 1"] or _G.Settings.Main["Auto Mystic Droplet"] or _G.Settings.Main["Auto Dragon Scales"] or
            --[Boss]
            _G.Settings.Boss["Auto All Boss"] or _G.Settings.Boss["Auto Boss Select"] or
            --[Mastery]
            _G.Settings.Mastery["Auto Farm Fruit Mastery"] or _G.Settings.Mastery["Auto Farm Gun Mastery"] or _G.Settings.Mastery["Farm Mastery SwordList"] or
            --[Teleport]
            _G.Settings.Main["Teleport to Sea Beast"] or 
            --[Raids]
            _G.Settings.Raids["Auto Raids"] or _G.Settings.Raids["Auto Next Place"]
        then
            for _, v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
                if v:IsA("BasePart") then
                    v.CanCollide = false
                end
            end
        end
    end)
end)

function changestate()
    game.Workspace["Part"].CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.X,
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Y - 3.92,
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Z)
end

spawn(function()
    while task.wait() do
        pcall(function()
            if _G.Settings.Main["Auto Farm Level"] or _G.Settings.Main["Neareast Farm"] or _G.Mirage or _G.TeleportGear or _G.Settings.Main["Auto New World"] or _G.Settings.Fruits["Tween To Fruit Spawn"] or
                _G.Settings.Main["Auto Saber"] or _G.Settings.Main["Auto Pople"] or _G.Settings.Main["Chest8"] or _G.Settings.Boss["Auto Farm Boss"] or _G.Settings.Boss["Auto All Boss"] or _G.Settings.Boss["Auto All Boss"] or
                --[World 2]
                _G.Settings.Main["Auto Third Sea"] or _G.Settings.Main["Auto Bartilo Quest"] or _G.Settings.Main["Auto Dark Coat"] or _G.Settings.Main["Auto Swan Glasses"] or
                _G.Settings.Main["Auto True Triple Katana"] or _G.Settings.Main["Auto Rengoku"] or _G.Settings.Main["Auto Ectoplasm"] or _G.Settings.Main["Auto Fully Death Step"] or
                _G.Settings.Main["Auto Fully SharkMan Karate"] or _G.Settings.Main["Auto Factory"] or
                --[World 3]
                _G.Settings.Main["Auto Rainbow Haki"] or _G.Settings.Main["Auto Elite Hunter"] or _G.Settings.Main["Auto Musketeer Hat"] or _G.Settings.Main["Auto Buddy Sword"] or
                _G.Settings.Main["Auto Farm Bone"] or   _G.SpawnBossHallow or _G.Settings.Main["Auto Ken-Haki V2"] or _G.Settings.Main["Auto God Human"] or _G.Settings.Main["Auto Cavander"] or
                _G.Settings.Main["Auto Cursed Dual Katana"] or _G.Settings.Main["Auto Yama Sword"] or _G.Settings.Main["Auto Tushita Sword"] or _G.Settings.Main["Auto Serpent Bow"] or
                _G.Settings.Main["Auto Dark Dagger"] or _G.Settings.Main["Auto Cake Prince"] or _G.Settings.Main["Auto Dough V2"] or _G.Settings.Main["Auto Holy Torch"] or
                _G.Settings.Main["Auto Buddy Swords"] or _G.Settings.Main["Auto Farm Boss Hallow"] or MobAura or YamaQuest2 or YamaQuest1 or Auto_Cursed_Dual_Katana or
                Tushita_Quest2 or Tushita_Quest1 or AutoFarmMaterial or teleporttop or AutoFarmChest or
                --[For God Human]
                --_G.Settings.Main["Auto Fish Tail Sea 1"] or _G.Settings.Main["Auto Fish Tail Sea 3"] or _G.Settings.Main["Auto Magma Ore Sea 2"] or
                --_G.Settings.Main["Auto Magma Ore Sea 1"] or _G.Settings.Main["Auto Mystic Droplet"] or _G.Settings.Main["Auto Dragon Scales"] or
                --[Boss]
                _G.Settings.Boss["Auto All Boss"] or _G.Settings.Boss["Auto Boss Select"] or
                --[Mastery]
                _G.Settings.Mastery["Auto Farm Fruit Mastery"] or _G.Settings.Mastery["Auto Farm Gun Mastery"] or _G.Settings.Mastery["Farm Mastery SwordList"] or
                --[Teleport]
                _G.Settings.Main["Teleport to Sea Beast"] or    
                --[Raids]
                _G.Settings.Raids["Auto Raids"] or _G.Settings.Raids["Auto Next Place"] then
                if not game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip") then
                    local Noclip = Instance.new("BodyVelocity")
                    Noclip.Name = "BodyClip"
                    Noclip.Parent = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart
                    Noclip.MaxForce = Vector3.new(100000, 100000, 100000)
                    Noclip.Velocity = Vector3.new(0, 0, 0)
                end
            else
                game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip"):Destroy()
            end
        end)
    end
end)

spawn(function() ------body velocity
    game:GetService("RunService").Stepped:Connect(function()
        if _G.Settings.Main["Auto Farm Level"] or _G.Settings.Main["Neareast Farm"] or _G.Mirage or _G.TeleportGear or _G.Settings.Main["Auto New World"] or _G.Settings.Fruits["Tween To Fruit Spawn"] or
            _G.Settings.Main["Auto Saber"] or _G.Settings.Main["Auto Pople"] or _G.Settings.Main["Chest8"] or _G.Settings.Boss["Auto Farm Boss"] or _G.Settings.Boss["Auto All Boss"] or _G.Settings.Boss["Auto All Boss"] or
            --[World 2]
            _G.Settings.Main["Auto Third Sea"] or _G.Settings.Main["Auto Bartilo Quest"] or _G.Settings.Main["Auto Dark Coat"] or _G.Settings.Main["Auto Swan Glasses"] or
            _G.Settings.Main["Auto True Triple Katana"] or _G.Settings.Main["Auto Rengoku"] or _G.Settings.Main["Auto Ectoplasm"] or _G.Settings.Main["Auto Fully Death Step"] or
            _G.Settings.Main["Auto Fully SharkMan Karate"] or _G.Settings.Main["Auto Factory"] or
            --[World 3]
            _G.Settings.Main["Auto Rainbow Haki"] or _G.Settings.Main["Auto Elite Hunter"] or _G.Settings.Main["Auto Musketeer Hat"] or _G.Settings.Main["Auto Buddy Sword"] or
            _G.Settings.Main["Auto Farm Bone"] or   _G.SpawnBossHallow or _G.Settings.Main["Auto Ken-Haki V2"] or _G.Settings.Main["Auto God Human"] or _G.Settings.Main["Auto Cavander"] or
            _G.Settings.Main["Auto Cursed Dual Katana"] or _G.Settings.Main["Auto Yama Sword"] or _G.Settings.Main["Auto Tushita Sword"] or _G.Settings.Main["Auto Serpent Bow"] or
            _G.Settings.Main["Auto Dark Dagger"] or _G.Settings.Main["Auto Cake Prince"] or _G.Settings.Main["Auto Dough V2"] or _G.Settings.Main["Auto Holy Torch"] or
            _G.Settings.Main["Auto Buddy Swords"] or _G.Settings.Main["Auto Farm Boss Hallow"] or MobAura or YamaQuest2 or YamaQuest1 or Auto_Cursed_Dual_Katana or
            Tushita_Quest2 or Tushita_Quest1 or AutoFarmMaterial or teleporttop or AutoFarmChest or
            --[For God Human]
            --_G.Settings.Main["Auto Fish Tail Sea 1"] or _G.Settings.Main["Auto Fish Tail Sea 3"] or _G.Settings.Main["Auto Magma Ore Sea 2"] or
            --_G.Settings.Main["Auto Magma Ore Sea 1"] or _G.Settings.Main["Auto Mystic Droplet"] or _G.Settings.Main["Auto Dragon Scales"] or
            --[Boss]
            _G.Settings.Boss["Auto All Boss"] or _G.Settings.Boss["Auto Boss Select"] or
            --[Mastery]
            _G.Settings.Mastery["Auto Farm Fruit Mastery"] or _G.Settings.Mastery["Auto Farm Gun Mastery"] or _G.Settings.Mastery["Farm Mastery SwordList"] or
            --[Teleport]
            _G.Settings.Main["Teleport to Sea Beast"] or 
            --[Raids]
            _G.Settings.Raids["Auto Raids"] or _G.Settings.Raids["Auto Next Place"]
        then
            if not game.Players.localPlayer.Character.HumanoidRootPart:FindFirstChild('bv') then
                local bv = Instance.new("BodyVelocity", game.Players.LocalPlayer.Character.HumanoidRootPart)
                bv.Name = 'bv'
                bv.MaxForce = Vector3.new(100000, 100000, 100000)
                bv.Velocity = Vector3.new(0, 0, 0)
            end
        else
            if game.Players.localPlayer.Character.HumanoidRootPart:FindFirstChild('bv') then
                game.Players.localPlayer.Character.HumanoidRootPart:FindFirstChild('bv'):Destroy()
            end
        end
    end)
end)

function changestate()
    game.Workspace["Part"].CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.X,
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Y - 3.92,
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Z)
end
spawn(function()
    while task.wait() do
        pcall(function()
            if _G.TeleportIsland
            then
                if not game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip") then
                    local Noclip = Instance.new("BodyVelocity")
                    Noclip.Name = "BodyClip"
                    Noclip.Parent = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart
                    Noclip.MaxForce = Vector3.new(100000, 100000, 100000)
                    Noclip.Velocity = Vector3.new(0, 0, 0)
                end
            else
                game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip"):Destroy()
            end
        end)
    end
end)
task.spawn(function()
    game:GetService("RunService").Stepped:Connect(function()
        pcall(function()
            --[World 1]
            if  _G.TeleportIsland
            then
                if syn then
                    setfflag("HumanoidParallelRemoveNoPhysics", "False")
                    setfflag("HumanoidParallelRemoveNoPhysicsNoSimulate2", "False")
                    game.Players.LocalPlayer.Character.Humanoid:ChangeState(11)
                    if game.Players.LocalPlayer.Character:WaitForChild("Humanoid").Sit == true then
                        game.Players.LocalPlayer.Character:WaitForChild("Humanoid").Sit = false
                    end
                else
                    if game.Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart") then
                        if not game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyVelocity1") then
                            if game.Players.LocalPlayer.Character:WaitForChild("Humanoid").Sit == true then
                                game.Players.LocalPlayer.Character:WaitForChild("Humanoid").Sit = false
                            end
                            local BodyVelocity = Instance.new("BodyVelocity")
                            BodyVelocity.Name = "BodyVelocity1"
                            BodyVelocity.Parent = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart
                            BodyVelocity.MaxForce = Vector3.new(10000, 10000, 10000)
                            BodyVelocity.Velocity = Vector3.new(0, 0, 0)
                        end
                    end
                    for _, v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
                        if v:IsA("BasePart") then
                            v.CanCollide = false
                        end
                    end
                end
            else
                if game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyVelocity1") then
                    game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyVelocity1"):Destroy();
                end
            end
        end)
    end)
end)
spawn(function()
    while wait(.1) do
        pcall(function()
            if  _G.TeleportIsland
            then
                if game.Players.LocalPlayer.Character.Humanoid.Sit == true then
                    game.Players.LocalPlayer.Character.Humanoid:ChangeState(15)
                    wait(5)
                end
                PIO = false
                if not game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyVelocity") then
                    local L_1 = Instance.new("BodyVelocity")
                    L_1.Name = "BodyGyrozz"
                    L_1.Parent = game.Players.LocalPlayer.Character.HumanoidRootPart
                    L_1.MaxForce = Vector3.new(1000000000, 1000000000, 1000000000)
                    L_1.Velocity = Vector3.new(0, 0, 0)
                end
            elseif PIO == false then
                for i, v in pairs(game.Players.LocalPlayer.Character.HumanoidRootPart:GetChildren()) do
                    if v.Name == "BodyGyrozz" then
                        v:Destroy()
                        PIO = true
                    end
                end
            end
        end)
    end
end)
---noclip
task.spawn(function()
    while true do
        task.wait()
        if setscriptable then
            setscriptable(game.Players.LocalPlayer, "SimulationRadius", true)
        end
        if sethiddenproperty then
            sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
        end
    end
end)

task.spawn(function()
    while task.wait() do
        pcall(function()
            if StartMagnet then
                for i, v in pairs(game.Workspace.Enemies:GetChildren()) do
                    if not string.find(v.Name, "Boss") and (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 500 then
                        if InMyNetWork(v.HumanoidRootPart) then
                            v.HumanoidRootPart.CFrame = PosMon
                            v.Humanoid.JumpPower = 0
                            v.Humanoid.WalkSpeed = 0
                            v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                            v.HumanoidRootPart.Transparency = 1
                            v.HumanoidRootPart.CanCollide = false
                            v.Head.CanCollide = false
                            if v.Humanoid:FindFirstChild("Animator") then
                                v.Humanoid.Animator:Destroy()
                            end
                            v.Humanoid:ChangeState(11)
                            v.Humanoid:ChangeState(14)
                        end
                    end
                end
            end
        end)
    end
end)

if game.Players.LocalPlayer.Character:FindFirstChild("Stun") then
    game.Players.LocalPlayer.Character.Stun.Changed:connect(function()
        pcall(function()
            if game.Players.LocalPlayer.Character:FindFirstChild("Stun") then
                game.Players.LocalPlayer.Character.Stun.Value = 0
            end
        end)
    end)
end

spawn(function()
    while task.wait() do
        for i, v in pairs(game:GetService("Workspace")["_WorldOrigin"]:GetChildren()) do
            pcall(function()
                if v.Name == "CurvedRing" or v.Name == "SlashHit" or v.Name == "SwordSlash" then -- v.Name == ("SlashTail") then --or v.Name == ("Sounds")
                    v:Destroy()
                end
            end)
        end
    end
end)

getgenv().NoDieEffect = true
if getgenv().NoDieEffect then
    if game:GetService("ReplicatedStorage").Effect.Container:FindFirstChild("Death") then
        game:GetService("ReplicatedStorage").Effect.Container.Death:Destroy()
    end
    if game:GetService("ReplicatedStorage").Effect.Container:FindFirstChild("Respawn") then
        game:GetService("ReplicatedStorage").Effect.Container.Respawn:Destroy()
    end
end
local CombatFramework = require(game:GetService("Players").LocalPlayer.PlayerScripts:WaitForChild("CombatFramework"))
local CombatFrameworkR = getupvalues(CombatFramework)[2]
local RigController = require(game:GetService("Players")["LocalPlayer"].PlayerScripts.CombatFramework.RigController)
local RigControllerR = getupvalues(RigController)[2]
local realbhit = require(game.ReplicatedStorage.CombatFramework.RigLib)
local cooldownfastattack = tick()

-- [Disabled Damage Interface]
function DisabledDamage()
    task.spawn(function()
        while task.wait() do
            pcall(function()
                if _G.Settings.Configs["Disabled Damage"] then
                    game:GetService("ReplicatedStorage").Assets.GUI.DamageCounter.Enabled = false
                else
                    game:GetService("ReplicatedStorage").Assets.GUI.DamageCounter.Enabled = true
                end
            end)
        end
    end)
end
function CameraShaker()
    local Camera = require(game.ReplicatedStorage.Util.CameraShaker)
    Camera:Stop()
end
function CurrentWeapon()
    local ac = CombatFrameworkR.activeController
    local ret = ac.blades[1]
    if not ret then return game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Name end
    pcall(function()
        while ret.Parent ~= game.Players.LocalPlayer.Character do ret = ret.Parent end
    end)
    if not ret then return game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Name end
    return ret
end

function getAllBladeHitsPlayers(Sizes)
    local Hits = {}
    local Client = game.Players.LocalPlayer
    local Characters = game:GetService("Workspace").Characters:GetChildren()
    for i = 1, #Characters do
        local v = Characters[i]
        local Human = v:FindFirstChildOfClass("Humanoid")
        if v.Name ~= game.Players.LocalPlayer.Name and Human and Human.RootPart and Human.Health > 0 and Client:DistanceFromCharacter(Human.RootPart.Position) < Sizes + 5 then
            table.insert(Hits, Human.RootPart)
        end
    end
    return Hits
end

function getAllBladeHits(Sizes)
    local Hits = {}
    local Client = game.Players.LocalPlayer
    local Enemies = game:GetService("Workspace").Enemies:GetChildren()
    for i = 1, #Enemies do
        local v = Enemies[i]
        local Human = v:FindFirstChildOfClass("Humanoid")
        if Human and Human.RootPart and Human.Health > 0 and Client:DistanceFromCharacter(Human.RootPart.Position) < Sizes + 5 then
            table.insert(Hits, Human.RootPart)
        end
    end
    return Hits
end

function AttackFunction()
    local ac = CombatFrameworkR.activeController
    if ac and ac.equipped then
        for indexincrement = 1, 1 do
            local bladehit = getAllBladeHits(60)
            if #bladehit > 0 then
                local AcAttack8 = debug.getupvalue(ac.attack, 5)
                local AcAttack9 = debug.getupvalue(ac.attack, 6)
                local AcAttack7 = debug.getupvalue(ac.attack, 4)
                local AcAttack10 = debug.getupvalue(ac.attack, 7)
                local NumberAc12 = (AcAttack8 * 798405 + AcAttack7 * 727595) % AcAttack9
                local NumberAc13 = AcAttack7 * 798405
                (function()
                    NumberAc12 = (NumberAc12 * AcAttack9 + NumberAc13) % 1099511627776
                    AcAttack8 = math.floor(NumberAc12 / AcAttack9)
                    AcAttack7 = NumberAc12 - AcAttack8 * AcAttack9
                end)()
                AcAttack10 = AcAttack10 + 1
                debug.setupvalue(ac.attack, 5, AcAttack8)
                debug.setupvalue(ac.attack, 6, AcAttack9)
                debug.setupvalue(ac.attack, 4, AcAttack7)
                debug.setupvalue(ac.attack, 7, AcAttack10)
                for k, v in pairs(ac.animator.anims.basic) do
                    v:Play(0.01, 0.01, 0.01)
                end
                if game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool") and ac.blades and ac.blades[1] then
                    game:GetService("ReplicatedStorage").RigControllerEvent:FireServer("weaponChange",
                        tostring(CurrentWeapon()))
                    game.ReplicatedStorage.Remotes.Validator:FireServer(
                        math.floor(NumberAc12 / 1099511627776 * 16777215), AcAttack10)
                    game:GetService("ReplicatedStorage").RigControllerEvent:FireServer("hit", bladehit, 2, "")
                end
            end
        end
    end
end

function AttackPlayers()
    local ac = CombatFrameworkR.activeController
    if ac and ac.equipped then
        for indexincrement = 1, 1 do
            local bladehit = getAllBladeHitsPlayers(60)
            if #bladehit > 0 then
                local AcAttack8 = debug.getupvalue(ac.attack, 5)
                local AcAttack9 = debug.getupvalue(ac.attack, 6)
                local AcAttack7 = debug.getupvalue(ac.attack, 4)
                local AcAttack10 = debug.getupvalue(ac.attack, 7)
                local NumberAc12 = (AcAttack8 * 798405 + AcAttack7 * 727595) % AcAttack9
                local NumberAc13 = AcAttack7 * 798405
                (function()
                    NumberAc12 = (NumberAc12 * AcAttack9 + NumberAc13) % 1099511627776
                    AcAttack8 = math.floor(NumberAc12 / AcAttack9)
                    AcAttack7 = NumberAc12 - AcAttack8 * AcAttack9
                end)()
                AcAttack10 = AcAttack10 + 1
                debug.setupvalue(ac.attack, 5, AcAttack8)
                debug.setupvalue(ac.attack, 6, AcAttack9)
                debug.setupvalue(ac.attack, 4, AcAttack7)
                debug.setupvalue(ac.attack, 7, AcAttack10)
                for k, v in pairs(ac.animator.anims.basic) do
                    v:Play(0.01, 0.01, 0.01)
                end
                if game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool") and ac.blades and ac.blades[1] then
                    game:GetService("ReplicatedStorage").RigControllerEvent:FireServer("weaponChange",
                        tostring(CurrentWeapon()))
                    game.ReplicatedStorage.Remotes.Validator:FireServer(
                        math.floor(NumberAc12 / 1099511627776 * 16777215), AcAttack10)
                    game:GetService("ReplicatedStorage").RigControllerEvent:FireServer("hit", bladehit, 2, "")
                end
            end
        end
    end
end


function InMyNetWork(object)
    if isnetworkowner then
        return isnetworkowner(object)
    else
        if (object.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 200 then
            return true
        end
        return false
    end
end

-- [Function (Abandoned Quest , Others)]

function Com(com, ...)
    local Remote = game:GetService('ReplicatedStorage').Remotes:FindFirstChild("Comm" .. com)
    if Remote:IsA("RemoteEvent") then
        Remote:FireServer(...)
    elseif Remote:IsA("RemoteFunction") then
        Remote:InvokeServer(...)
    end
end

-- [Tween Functions]

local function GetIsLand(...)
    local RealtargetPos = { ... }
    local targetPos = RealtargetPos[1]
    local RealTarget
    if type(targetPos) == "vector" then
        RealTarget = targetPos
    elseif type(targetPos) == "userdata" then
        RealTarget = targetPos.Position
    elseif type(targetPos) == "number" then
        RealTarget = CFrame.new(unpack(RealtargetPos))
        RealTarget = RealTarget.p
    end

    local ReturnValue
    local CheckInOut = math.huge;
    if game.Players.LocalPlayer.Team then
        for i, v in pairs(game.Workspace._WorldOrigin.PlayerSpawns:FindFirstChild(tostring(game.Players.LocalPlayer.Team)):GetChildren()) do
            local ReMagnitude = (RealTarget - v:GetModelCFrame().p).Magnitude;
            if ReMagnitude < CheckInOut then
                CheckInOut = ReMagnitude;
                ReturnValue = v.Name
            end
        end
        if ReturnValue then
            return ReturnValue
        end
    end
end

--BTP
function ByPass(Position)
    game.Players.LocalPlayer.Character.Head:Destroy()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Position
    wait(.5)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Position
    wait(.5)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(5555, 5555, 5555)
end

function BTP(Position)
    game.Players.LocalPlayer.Character.Head:Destroy()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Position
    wait(1)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Position
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetSpawnPoint")
end

-- [Tween Functions (toTarget)]

local function toTarget(...)
    local RealtargetPos = { ... }
    local targetPos = RealtargetPos[1]
    local RealTarget
    if type(targetPos) == "vector" then
        RealTarget = CFrame.new(targetPos)
    elseif type(targetPos) == "userdata" then
        RealTarget = targetPos
    elseif type(targetPos) == "number" then
        RealTarget = CFrame.new(unpack(RealtargetPos))
    end

    if game.Players.LocalPlayer.Character:WaitForChild("Humanoid").Health == 0 then
        if tween then tween:Cancel() end
        repeat wait() until game.Players.LocalPlayer.Character:WaitForChild("Humanoid").Health > 0; wait(0.2)
    end

    local tweenfunc = {}
    local Distance = (RealTarget.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position)
        .Magnitude
    if Distance < 1000 then
        Speed = 315
    elseif Distance >= 1000 then
        Speed = 300
    end

    if _G.Settings.Configs["Bypass TP"] then
        if Distance > 3000 and not AutoFarmMaterial and not _G.Settings.FightingStyle["Auto God Human"] and not _G.Settings.Raids["Auto Raids"] and not (game.Players.LocalPlayer.Backpack:FindFirstChild("Special Microchip") or game.Players.LocalPlayer.Character:FindFirstChild("Special Microchip") or game.Players.LocalPlayer.Backpack:FindFirstChild("God's Chalice") or game.Players.LocalPlayer.Character:FindFirstChild("God's Chalice") or game.Players.LocalPlayer.Backpack:FindFirstChild("Hallow Essence") or game.Players.LocalPlayer.Character:FindFirstChild("Hallow Essence") or game.Players.LocalPlayer.Character:FindFirstChild("Sweet Chalice") or game.Players.LocalPlayer.Backpack:FindFirstChild("Sweet Chalice")) and not (Name == "Fishman Commando" or Name == "Fishman Warrior") then
            pcall(function()
                tween:Cancel()
                fkwarp = false

                if game:GetService("Players")["LocalPlayer"].Data:FindFirstChild("SpawnPoint").Value == tostring(GetIsLand(RealTarget)) then
                    wait(.1)
                    Com("F_", "TeleportToSpawn")
                elseif game:GetService("Players")["LocalPlayer"].Data:FindFirstChild("LastSpawnPoint").Value == tostring(GetIsLand(RealTarget)) then
                    game:GetService("Players").LocalPlayer.Character:WaitForChild("Humanoid"):ChangeState(15)
                    wait(0.1)
                    repeat wait() until game:GetService("Players").LocalPlayer.Character:WaitForChild("Humanoid").Health > 0
                else
                    if game:GetService("Players").LocalPlayer.Character:WaitForChild("Humanoid").Health > 0 then
                        if fkwarp == false then
                            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = RealTarget
                        end
                        fkwarp = true
                    end
                    wait(.08)
                    game:GetService("Players").LocalPlayer.Character:WaitForChild("Humanoid"):ChangeState(15)
                    repeat wait() until game:GetService("Players").LocalPlayer.Character:WaitForChild("Humanoid").Health > 0
                    wait(.1)
                    Com("F_", "SetSpawnPoint")
                end
                wait(0.2)

                return
            end)
        end
    end


    local tween_s = game:service "TweenService"
    local info = TweenInfo.new(
        (RealTarget.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position)
        .Magnitude / Speed, Enum.EasingStyle.Linear)
    local tweenw, err = pcall(function()
        tween = tween_s:Create(game.Players.LocalPlayer.Character["HumanoidRootPart"], info, { CFrame = RealTarget })
        tween:Play()
    end)

    function tweenfunc:Stop()
        tween:Cancel()
    end

    function tweenfunc:Wait()
        tween.Completed:Wait()
    end

    return tweenfunc
end


function TP(Pos)
    Distance = (Pos.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if game.Players.LocalPlayer.Character.Humanoid.Sit == true then game.Players.LocalPlayer.Character.Humanoid.Sit = false end
    pcall(function()
        tween = game:GetService("TweenService"):Create(game.Players.LocalPlayer.Character.HumanoidRootPart,
            TweenInfo.new(Distance / 210, Enum.EasingStyle.Linear), { CFrame = Pos })
    end)
    tween:Play()
    if Distance <= 250 then
        tween:Cancel()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Pos
    end
    if _G.StopTween == true then
        tween:Cancel()
        _G.Clip = false
    end
end

function GetDistance(target)
    return math.floor((target.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude)
end

function two(gotoCFrame) --- Tween
    pcall(function()
        game.Players.LocalPlayer.Character.Humanoid.Sit = false
        game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = false
    end)
    if (game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart.Position - gotoCFrame.Position).Magnitude <= 200 then
        pcall(function()
            tweenz:Cancel()
        end)
        game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart.CFrame = gotoCFrame
    else
        local tween_s = game:service "TweenService"
        local info = TweenInfo.new(
            (game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart.Position - gotoCFrame.Position)
            .Magnitude /
            325, Enum.EasingStyle.Linear)
        tween, err = pcall(function()
            tweenz = tween_s:Create(game.Players.LocalPlayer.Character["HumanoidRootPart"], info, { CFrame = gotoCFrame })
            tweenz:Play()
        end)
        if not tween then return err end
    end
    function _TweenCanCle()
        tweenz:Cancel()
    end
end

function InfinitiesEnergy()
    game:GetService('Players').LocalPlayer.Character.Energy.Changed:connect(function()
        if _G.Settings.Misc["Infinities Energy"] then
            game:GetService('Players').LocalPlayer.Character.Energy.Value = game:GetService('Players').LocalPlayer
                .Character.Energy.MaxValue
        end
    end)
end

-- [No Cooldown , Infinities Geppo]

-- [Xray Function]

function xray(v)
    if v then
        for _, i in pairs(workspace:GetDescendants()) do
            if i:IsA("BasePart") and not i.Parent:FindFirstChildOfClass('Humanoid') and not i.Parent.Parent:FindFirstChildOfClass('Humanoid') then
                i.LocalTransparencyModifier = 0.5
            end
        end
    else
        for _, i in pairs(workspace:GetDescendants()) do
            if i:IsA("BasePart") and not i.Parent:FindFirstChildOfClass('Humanoid') and not i.Parent.Parent:FindFirstChildOfClass('Humanoid') then
                i.LocalTransparencyModifier = 0
            end
        end
    end
end

-- [Get Players Character]

function getRoot(char)
    local rootPart = char:FindFirstChild('HumanoidRootPart') or char:FindFirstChild('Torso') or
        char:FindFirstChild('UpperTorso')
    return rootPart
end

function r15(plr)
    if plr.Character:FindFirstChildOfClass('Humanoid').RigType == Enum.HumanoidRigType.R15 then
        return true
    end
end

-- [Functions Click]

function ClickCamera()
    game:GetService("VirtualUser"):CaptureController()
    game:GetService("VirtualUser"):ClickButton1(Vector2.new(851, 158), game:GetService("Workspace").Camera.CFrame)
end

function Click()
    game:GetService("VirtualUser"):CaptureController()
    game:GetService("VirtualUser"):Button1Down(Vector2.new(1280, 672))
end

-- [Server Hop Api]



-- [Remove Text Fruits]

function RemoveFruit(str)
    return str:gsub(" Fruit", "")
end



-- [Comma Value]

function comma_value(p1)
    local v1 = p1;
    while true do
        local v2, v3 = string.gsub(v1, "^(-?%d+)(%d%d%d)", "%1,%2");
        v1 = v2;
        if v3 ~= 0 then else
            break;
        end;
    end;
    return v1;
end;

-- [Check Fruit 1M]


_G.CheckFruitLocal1M = false
function CheckFruit1M()
    for i, v in pairs(game.ReplicatedStorage:WaitForChild("Remotes").CommF_:InvokeServer("getInventoryFruits")) do
        if v.Price >= 1000000 then
            _G.CheckFruitLocal1M = true
        end
    end
end

-- [Get FightingStyle]

function GetFightingStyle(Style)
    ReturnText = ""
    for i, v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
        if v:IsA("Tool") then
            if v.ToolTip == Style then
                ReturnText = v.Name
            end
        end
    end
    for i, v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do
        if v:IsA("Tool") then
            if v.ToolTip == Style then
                ReturnText = v.Name
            end
        end
    end
    if ReturnText ~= "" then
        return ReturnText
    else
        return "Not Have"
    end
end

local placeId = game.PlaceId
if placeId == 2753915549 then
    OldWorld = true
elseif placeId == 4442272183 then
    NewWorld = true
elseif placeId == 7449423635 then
    ThreeWorld = true
else
    game.Players.LocalPlayer:Kick("BLOXFRUIT!!!!!")
end

-- [CheckMasteryWeapon]

function CheckMasteryWeapon(NameWe, MasNum)
    if game.Players.LocalPlayer.Backpack:FindFirstChild(NameWe) then
        if tonumber(game.Players.LocalPlayer.Backpack:FindFirstChild(NameWe).Level.Value) < tonumber(MasNum) then
            return "true DownTo"
        elseif tonumber(game.Players.LocalPlayer.Backpack:FindFirstChild(NameWe).Level.Value) >= tonumber(MasNum) then
            return "true UpTo"
        end
    end
    if game.Players.LocalPlayer.Character:FindFirstChild(NameWe) then
        if tonumber(game.Players.LocalPlayer.Character:FindFirstChild(NameWe).Level.Value) < tonumber(MasNum) then
            return "true DownTo"
        elseif tonumber(game.Players.LocalPlayer.Character:FindFirstChild(NameWe).Level.Value) >= tonumber(MasNum) then
            return "true UpTo"
        end
    end
    return "else"
end

--[GetWeaponInventory]

function GetWeaponInventory(Weaponname)
    for i, v in pairs(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("getInventory")) do
        if type(v) == "table" then
            if v.Type == "Sword" then
                if v.Name == Weaponname then
                    return true
                end
            end
        end
    end
    return false
end

-- [GetMaterial]

function GetMaterial(matname)
    for i, v in pairs(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("getInventory")) do
        if type(v) == "table" then
            if v.Type == "Material" then
                if v.Name == matname then
                    return v.Count
                end
            end
        end
    end
    return 0
end

local AllMaterial
if World1 then
    AllMaterial = {
        "Magma Ore",
        "Leather",
        "Scrap Metal",
        "Angel Wings",
        "Fish Tail"
    }
elseif World2 then
    AllMaterial = {
        "Magma Ore",
        "Scrap Metal",
        "Radioactive Material",
        "Vampire Fang",
        "Mystic Droplet",
    }
elseif World3 then
    AllMaterial = {
        "Mini Tusk",
        "Fish Tail",
        "Scrap Metal",
        "Dragon Scale",
        "Conjured Cocoa",
        "Demonic Wisp",
        "Gunpowder",
    }
end

table.sort(AllMaterial)

-- [CustomFindFirstChild]

local function CustomFindFirstChild(tablename)
    for i, v in pairs(tablename) do
        if game:GetService("Workspace").Enemies:FindFirstChild(v) then
            return true
        end
    end
    return false
end

-- [IsNumber]

function isNumber(str)
    if tonumber(str) ~= nil or str == 'inf' then
        return true
    end
end

-- [Invisible]

local Player = game:GetService('Players').LocalPlayer

local function CheckRig()
    if Player.Character then
        local Humanoid = Player.Character:WaitForChild('Humanoid')
        if Humanoid.RigType == Enum.HumanoidRigType.R15 then
            return 'R15'
        else
            return 'R6'
        end
    end
end

local function InitiateInvis()
    local Character = Player.Character
    local StoredCF = Character.PrimaryPart.CFrame

    if CheckRig() == 'R6' then
        local Clone = Character.HumanoidRootPart:Clone()
        Character.HumanoidRootPart:Destroy()
        Clone.Parent = Character
    else
        local Clone = Character.LowerTorso.Root:Clone()
        Character.LowerTorso.Root:Destroy()
        Clone.Parent = Character.LowerTorso
    end
end

-- [CheckMaterial]

local function CheckMaterial(v1)
    if World1 then
        if (v1 == "Magma Ore") then
            MaterialMob = { "Military Soldier", "Military Spy" };
            CFrameMon = CFrame.new(-5815, 84, 8820);
        elseif ((v1 == "Leather") or (v1 == "Scrap Metal")) then
            MaterialMob = { "Brute"};
            CFrameMon = CFrame.new(-1145, 15, 4350);
        elseif (v1 == "Angel Wings") then
            MaterialMob = { "God's Guard"};
            CFrameMon = CFrame.new(-4698, 845, -1912);
        elseif (v1 == "Fish Tail") then
            MaterialMob = { "Fishman Warrior", "Fishman Commando" };
            CFrameMon = CFrame.new(61123, 19, 1569);
        end
    end
    if World2 then
        if (v1 == "Magma Ore") then
            MaterialMob = { "Magma Ninja" };
            CFrameMon = CFrame.new(-5428, 78, -5959);
        elseif (v1 == "Scrap Metal") then
            MaterialMob = { "Swan Pirate" };
            CFrameMon = CFrame.new(878, 122, 1235);
        elseif (v1 == "Radioactive Material") then
            MaterialMob = { "Factory Staff" };
            CFrameMon = CFrame.new(295, 73, -56);
        elseif (v1 == "Vampire Fang") then
            MaterialMob = { "Vampire" };
            CFrameMon = CFrame.new(-6033, 7, -1317);
        elseif (v1 == "Mystic Droplet") then
            MaterialMob = { "Water Fighter", "Sea Soldier" };
            CFrameMon = CFrame.new(-3385, 239, -10542);
        end
    end
    if World3 then
        if (v1 == "Mini Tusk") then
            MaterialMob = { "Mythological Pirate" };
            CFrameMon = CFrame.new(-13545, 470, -6917);
        elseif (v1 == "Fish Tail") then
            MaterialMob = { "Fishman Raider", "Fishman Captain" };
            CFrameMon = CFrame.new(-10993, 332, -8940);
        elseif (v1 == "Scrap Metal") then
            MaterialMob = { "Jungle Pirate" };
            CFrameMon = CFrame.new(-12107, 332, -10549);
        elseif (v1 == "Dragon Scale") then
            MaterialMob = { "Dragon Crew Archer", "Dragon Crew Warrior" };
            CFrameMon = CFrame.new(6594, 383, 139);
        elseif (v1 == "Conjured Cocoa") then
            MaterialMob = { "Cocoa Warrior", "Chocolate Bar Battler", "Sweet Thief",
                "Candy Rebel" };
            CFrameMon = CFrame.new(620.6344604492188, 78.93644714355469, -12581.369140625);
        elseif (v1 == "Demonic Wisp") then
            MaterialMob = { "Demonic Soul" };
            CFrameMon = CFrame.new(-9507, 172, 6158);
        elseif (v1 == "Gunpowder") then
            MaterialMob = { "Pistol Billionaire" };
            CFrameMon = CFrame.new(-469, 74, 5904);
        end
    end
end



-- [Check Quest]

function CheckQuest()
    local MyLevel = game.Players.LocalPlayer.Data.Level.Value
    if World1 then
        if MyLevel == 1 or MyLevel <= 9 then -- Bandit
            LevelFarm = 1

            Name = "Bandit"
            QuestName = "BanditQuest1"

            LevelQuest = 1
            NameMon = "Bandit"

            CFrameMon = CFrame.new(1145, 17, 1634)
            VectorMon = Vector3.new(1145, 17, 1634)

            CFrameQuest = CFrame.new(1060, 17, 1547)
            VectorQuest = Vector3.new(1060, 17, 1547)
        elseif MyLevel == 10 or MyLevel <= 14 then -- Monkey
            LevelFarm = 3

            Name = "Monkey"
            QuestName = "JungleQuest"

            LevelQuest = 1
            NameMon = "Monkey"

            CFrameMon = CFrame.new(-1496, 39, 35)
            VectorMon = Vector3.new(-1496, 39, 35)

            CFrameQuest = CFrame.new(-1602, 37, 152)
            VectorQuest = Vector3.new(-1602, 37, 152)
        elseif MyLevel == 15 or MyLevel <= 29 then -- Gorilla
            LevelFarm = 4

            Name = "Gorilla"
            QuestName = "JungleQuest"

            LevelQuest = 2
            NameMon = "Gorilla"

            CFrameMon = CFrame.new(-1237, 6, -486)
            VectorMon = Vector3.new(-1237, 7, -486)

            CFrameQuest = CFrame.new(-1602, 37, 152)
            VectorQuest = Vector3.new(-1602, 37, 152)
        elseif MyLevel == 30 or MyLevel <= 59 then -- Pirate
            LevelFarm = 6

            Name = "Pirate"
            QuestName = "BuggyQuest1"

            LevelQuest = 1
            NameMon = "Pirate"

            CFrameMon = CFrame.new(-1115, 14, 3938)
            VectorMon = Vector3.new(-1115, 14, 3938)

            CFrameQuest = CFrame.new(-1140, 5, 3828)
            VectorQuest = Vector3.new(-1140, 5, 3828)
        elseif MyLevel == 60 or MyLevel <= 74 then -- Desert Bandit
            LevelFarm = 9

            Name = "Desert Bandit"
            QuestName = "DesertQuest"

            LevelQuest = 1
            NameMon = "Desert Bandit"

            CFrameMon = CFrame.new(932, 7, 4484)
            VectorMon = Vector3.new(932, 7, 4484)

            CFrameQuest = CFrame.new(897, 7, 4388)
            VectorQuest = Vector3.new(897, 7, 4388)
        elseif MyLevel == 75 or MyLevel <= 89 then -- Desert Officre
            LevelFarm = 10

            Name = "Desert Officer"
            QuestName = "DesertQuest"

            LevelQuest = 2
            NameMon = "Desert Officer"

            CFrameMon = CFrame.new(1572, 10, 4373)
            VectorMon = Vector3.new(1572, 10, 4373)

            CFrameQuest = CFrame.new(897, 7, 4388)
            VectorQuest = Vector3.new(897, 7, 4388)
        elseif MyLevel == 90 or MyLevel <= 99 then -- Snow Bandits
            LevelFarm = 12

            Name = "Snow Bandit"
            QuestName = "SnowQuest"

            LevelQuest = 1
            NameMon = "Snow Bandits"

            CFrameMon = CFrame.new(1289, 150, -1442)
            VectorMon = Vector3.new(1289, 106, -1442)

            CFrameQuest = CFrame.new(1386, 87, -1297)
            VectorQuest = Vector3.new(1386, 87, -1297)
        elseif MyLevel == 100 or MyLevel <= 119 then -- Snowman
            LevelFarm = 13

            Name = "Snowman"
            QuestName = "SnowQuest"

            LevelQuest = 2
            NameMon = "Snowman"

            CFrameMon = CFrame.new(1289, 150, -1442)
            VectorMon = Vector3.new(1289, 106, -1442)

            CFrameQuest = CFrame.new(1386, 87, -1297)
            VectorQuest = Vector3.new(1386, 87, -1297)
        elseif MyLevel == 120 or MyLevel <= 149 then -- Chief Petty Officer
            LevelFarm = 15

            Name = "Chief Petty Officer"
            QuestName = "MarineQuest2"

            LevelQuest = 1
            NameMon = "Chief Petty Officer"

            CFrameMon = CFrame.new(-4855, 23, 4308)
            VectorMon = Vector3.new(-4855, 23, 4308)

            CFrameQuest = CFrame.new(-5036, 29, 4325)
            VectorQuest = Vector3.new(-5036, 29, 4325)
        elseif MyLevel == 150 or MyLevel <= 174 then -- Sky Bandit
            LevelFarm = 17

            Name = "Sky Bandit"
            QuestName = "SkyQuest"

            LevelQuest = 1
            NameMon = "Sky Bandit"

            CFrameMon = CFrame.new(-4981, 278, -2830)
            VectorMon = Vector3.new(-4981, 278, -2830)

            CFrameQuest = CFrame.new(-4842, 718, -2623)
            VectorQuest = Vector3.new(-4842, 718, -2623)
        elseif MyLevel == 175 or MyLevel <= 189 then -- Dark Master
            LevelFarm = 18

            Name = "Dark Master"
            QuestName = "SkyQuest"

            LevelQuest = 2
            NameMon = "Dark Master"

            CFrameMon = CFrame.new(-5250, 389, -2272)
            VectorMon = Vector3.new(-5250, 389, -2272)

            CFrameQuest = CFrame.new(-4842, 718, -2623)
            VectorQuest = Vector3.new(-4842, 718, -2623)
        elseif MyLevel == 190 or MyLevel <= 209 then -- Dark Master
            LevelFarm = 20

            Name = "Prisoner"
            QuestName = "PrisonerQuest"

            LevelQuest = 1
            NameMon = "Prisoner"

            CFrameMon = CFrame.new(5411, 96, 690)
            VectorMon = Vector3.new(5411, 96, 690)

            CFrameQuest = CFrame.new(5308, 2, 474)
            VectorQuest = Vector3.new(5308, 2, 474)
        elseif MyLevel == 210 or MyLevel <= 249 then -- Dark Master
            LevelFarm = 21

            Name = "Dangerous Prisoner"
            QuestName = "PrisonerQuest"

            LevelQuest = 2
            NameMon = "Dangerous Prisoner"

            CFrameMon = CFrame.new(5411, 96, 690)
            VectorMon = Vector3.new(5411, 96, 690)

            CFrameQuest = CFrame.new(5308, 2, 474)
            VectorQuest = Vector3.new(5308, 2, 474)
        elseif MyLevel == 250 or MyLevel <= 299 then -- Toga Warrior
            LevelFarm = 23

            Name = "Toga Warrior"
            QuestName = "ColosseumQuest"

            LevelQuest = 1
            NameMon = "Toga Warrior"

            CFrameMon = CFrame.new(-1824, 50, -2743)
            VectorMon = Vector3.new(-1824, 50, -2743)

            CFrameQuest = CFrame.new(-1576, 8, -2985)
            VectorQuest = Vector3.new(-1576, 8, -2985)
        elseif MyLevel == 300 or MyLevel <= 329 then -- Military Soldier
            LevelFarm = 25

            Name = "Military Soldier"
            QuestName = "MagmaQuest"

            LevelQuest = 1
            NameMon = "Military Soldier"

            CFrameMon = CFrame.new(-5555.064453125, 16.73392105102539, 8377.623046875)
            VectorMon = Vector3.new(-5555.064453125, 16.73392105102539, 8377.623046875)

            CFrameQuest = CFrame.new(-5316, 12, 8517)
            VectorQuest = Vector3.new(-5316, 12, 8517)
        elseif MyLevel == 330 or MyLevel <= 374 then -- Military Spy
            LevelFarm = 26

            Name = "Military Spy"
            QuestName = "MagmaQuest"

            LevelQuest = 2
            NameMon = "Military Spy"

            CFrameMon = CFrame.new(-5806.056640625, 99.96672058105469, 8777.8447265625)
            VectorMon = Vector3.new(-5806.056640625, 99.96672058105469, 8777.8447265625)

            CFrameQuest = CFrame.new(-5316, 12, 8517)
            VectorQuest = Vector3.new(-5316, 12, 8517)
        elseif MyLevel == 375 or MyLevel <= 399 then -- Fishman Warrior
            LevelFarm = 28

            Name = "Fishman Warrior"
            QuestName = "FishmanQuest"

            LevelQuest = 1
            NameMon = "Fishman Warrior"

            CFrameMon = CFrame.new(60859, 19, 1501)
            VectorMon = Vector3.new(60859, 19, 1501)

            CFrameQuest = CFrame.new(61123, 19, 1569)
            VectorQuest = Vector3.new(61123, 19, 1569)
        elseif MyLevel == 400 or MyLevel <= 449 then -- Fishman Commando
            LevelFarm = 29

            Name = "Fishman Commando"
            QuestName = "FishmanQuest"

            LevelQuest = 2
            NameMon = "Fishman Commando"

            CFrameMon = CFrame.new(61891, 19, 1470)
            VectorMon = Vector3.new(61891, 19, 1470)

            CFrameQuest = CFrame.new(61123, 19, 1569)
            VectorQuest = Vector3.new(61123, 19, 1569)
        elseif MyLevel == 450 or MyLevel <= 474 then -- God's Guards
            LevelFarm = 31

            Name = "God's Guard"
            QuestName = "SkyExp1Quest"

            LevelQuest = 1
            NameMon = "God's Guards"

            CFrameMon = CFrame.new(-4698, 845, -1912)
            VectorMon = Vector3.new(-4698, 845, -1912)

            CFrameQuest = CFrame.new(-4722, 845, -1954)
            VectorQuest = Vector3.new(-4722, 846, -1954)
        elseif MyLevel == 475 or MyLevel <= 524 then -- Shandas
            LevelFarm = 33

            Name = "Shanda"
            QuestName = "SkyExp1Quest"

            LevelQuest = 2
            NameMon = "Shandas"

            CFrameMon = CFrame.new(-7685, 5567, -502)
            VectorMon = Vector3.new(-7685, 5567, -502)

            CFrameQuest = CFrame.new(-7862, 5546, -380)
            VectorQuest = Vector3.new(-7862, 5546, -380)
        elseif MyLevel == 525 or MyLevel <= 549 then -- Royal Squad
            LevelFarm = 34

            Name = "Royal Squad"
            QuestName = "SkyExp2Quest"

            LevelQuest = 1
            NameMon = "Royal Squad"

            CFrameMon = CFrame.new(-7670, 5607, -1460)
            VectorMon = Vector3.new(-7670, 5607, -1460)

            CFrameQuest = CFrame.new(-7904, 5636, -1412)
            VectorQuest = Vector3.new(-7904, 5636, -1412)
        elseif MyLevel == 550 or MyLevel <= 624 then -- Royal Soldier
            LevelFarm = 35

            Name = "Royal Soldier"
            QuestName = "SkyExp2Quest"

            LevelQuest = 2
            NameMon = "Royal Soldier"

            CFrameMon = CFrame.new(-7828, 5607, -1744)
            VectorMon = Vector3.new(-7828, 5607, -1744)

            CFrameQuest = CFrame.new(-7904, 5636, -1412)
            VectorQuest = Vector3.new(-7904, 5636, -1412)
        elseif MyLevel == 625 or MyLevel <= 649 then -- Galley Pirate
            LevelFarm = 37

            Name = "Galley Pirate"
            QuestName = "FountainQuest"

            LevelQuest = 1
            NameMon = "Galley Pirate"

            CFrameMon = CFrame.new(5589, 45, 3996)
            VectorMon = Vector3.new(5589, 45, 3996)

            CFrameQuest = CFrame.new(5256, 39, 4050)
            VectorQuest = Vector3.new(5256, 39, 4050)
        elseif MyLevel >= 650 then -- Galley Captain
            LevelFarm = 38

            Name = "Galley Captain"
            QuestName = "FountainQuest"

            LevelQuest = 2
            NameMon = "Galley Captain"

            CFrameMon = CFrame.new(5649, 39, 4936)
            VectorMon = Vector3.new(5649, 39, 4936)

            CFrameQuest = CFrame.new(5256, 39, 4050)
            VectorQuest = Vector3.new(5256, 39, 4050)
        end
    end
    if World2 then
        if MyLevel == 700 or MyLevel <= 724 then -- Raider [Lv. 700]
            LevelFarm = 1

            Name = "Raider"
            QuestName = "Area1Quest"

            LevelQuest = 1
            NameMon = "Raider"

            CFrameQuest = CFrame.new(-425, 73, 1837)
            VectorQuest = Vector3.new(-425, 73, 1837)

            CFrameMon = CFrame.new(-746, 39, 2390)
            VectorMon = Vector3.new(-746, 39, 2389)
        elseif MyLevel == 725 or MyLevel <= 774 then -- Mercenary [Lv. 725]
            LevelFarm = 2

            Name = "Mercenary"
            QuestName = "Area1Quest"

            LevelQuest = 2
            NameMon = "Mercenary"

            CFrameQuest = CFrame.new(-425, 73, 1837)
            VectorQuest = Vector3.new(-425, 73, 1837)

            CFrameMon = CFrame.new(-856.213134765625, 135.4429473876953, 1407.4842529296875)
            VectorMon = Vector3.new(-856.213134765625, 135.4429473876953, 1407.4842529296875)
        elseif MyLevel == 775 or MyLevel <= 799 then -- Swan Pirate [Lv. 775]
            LevelFarm = 3

            Name = "Swan Pirate"
            QuestName = "Area2Quest"

            LevelQuest = 1
            NameMon = "Swan Pirate"

            CFrameQuest = CFrame.new(634, 73, 918)
            VectorQuest = Vector3.new(634, 73, 918)

            CFrameMon = CFrame.new(878, 122, 1235)
            VectorMon = Vector3.new(878, 122, 1235)
        elseif MyLevel == 800 or MyLevel <= 874 then -- Factory Staff [Lv. 800]
            LevelFarm = 4

            Name = "Factory Staff"
            QuestName = "Area2Quest"

            LevelQuest = 2
            NameMon = "Factory Staff"

            CFrameQuest = CFrame.new(634, 73, 918)
            VectorQuest = Vector3.new(634, 73, 918)

            CFrameMon = CFrame.new(295, 73, -56)
            VectorMon = Vector3.new(295, 73, -56)
        elseif MyLevel == 875 or MyLevel <= 899 then -- Marine Lieutenant [Lv. 875]
            LevelFarm = 6

            Name = "Marine Lieutenant"
            QuestName = "MarineQuest3"

            LevelQuest = 1
            NameMon = "Marine Lieutenant"

            CFrameMon = CFrame.new(-2806, 73, -3038)
            VectorMon = Vector3.new(-2806, 73, -3038)

            CFrameQuest = CFrame.new(-2443, 73, -3219)
            VectorQuest = Vector3.new(-2443, 73, -3219)
        elseif MyLevel == 900 or MyLevel <= 949 then -- Marine Captain [Lv. 900]
            LevelFarm = 7

            Name = "Marine Captain"
            QuestName = "MarineQuest3"

            LevelQuest = 2
            NameMon = "Marine Captain"

            CFrameMon = CFrame.new(-1869, 73, -3320)
            VectorMon = Vector3.new(-1869, 73, -3320)

            CFrameQuest = CFrame.new(-2443, 73, -3219)
            VectorQuest = Vector3.new(-2443, 73, -3219)
        elseif MyLevel == 950 or MyLevel <= 974 then -- Zombie [Lv. 950]
            LevelFarm = 9

            Name = "Zombie"
            QuestName = "ZombieQuest"

            LevelQuest = 1
            NameMon = "Zombie"

            CFrameMon = CFrame.new(-5736, 126, -728)
            VectorMon = Vector3.new(-5736, 126, -728)

            CFrameQuest = CFrame.new(-5494, 49, -795)
            VectorQuest = Vector3.new(-5494, 49, -794)
        elseif MyLevel == 975 or MyLevel <= 999 then -- Vampire [Lv. 975]
            LevelFarm = 10

            Name = "Vampire"
            QuestName = "ZombieQuest"

            LevelQuest = 2
            NameMon = "Vampire"

            CFrameMon = CFrame.new(-6033, 7, -1317)
            VectorMon = Vector3.new(-6033, 7, -1317)

            CFrameQuest = CFrame.new(-5494, 49, -795)
            VectorQuest = Vector3.new(-5494, 49, -795)
        elseif MyLevel == 1000 or MyLevel <= 1049 then -- Snow Trooper [Lv. 1000] **
            LevelFarm = 12

            Name = "Snow Trooper"
            QuestName = "SnowMountainQuest"

            LevelQuest = 1
            NameMon = "Snow Trooper"

            CFrameMon = CFrame.new(478, 402, -5362)
            VectorMon = Vector3.new(478, 402, -5362)

            CFrameQuest = CFrame.new(605, 402, -5371)
            VectorQuest = Vector3.new(605, 402, -5371)
        elseif MyLevel == 1050 or MyLevel <= 1099 then -- Winter Warrior [Lv. 1050]
            LevelFarm = 13

            Name = "Winter Warrior"
            QuestName = "SnowMountainQuest"

            LevelQuest = 2
            NameMon = "Winter Warrior"

            CFrameMon = CFrame.new(1157, 430, -5188)
            VectorMon = Vector3.new(1157, 430, -5188)

            CFrameQuest = CFrame.new(605, 402, -5371)
            VectorQuest = Vector3.new(605, 402, -5371)
        elseif MyLevel == 1100 or MyLevel <= 1124 then -- Lab Subordinate [Lv. 1100]
            LevelFarm = 15

            Name = "Lab Subordinate"
            QuestName = "IceSideQuest"

            LevelQuest = 1
            NameMon = "Lab Subordinate"

            CFrameMon = CFrame.new(-5782, 42, -4484)
            VectorMon = Vector3.new(-5782, 42, -4484)

            CFrameQuest = CFrame.new(-6060, 16, -4905)
            VectorQuest = Vector3.new(-6060, 16, -4905)
        elseif MyLevel == 1125 or MyLevel <= 1174 then -- Horned Warrior [Lv. 1125]
            LevelFarm = 16

            Name = "Horned Warrior"
            QuestName = "IceSideQuest"

            LevelQuest = 2
            NameMon = "Horned Warrior"

            CFrameMon = CFrame.new(-6406, 24, -5805)
            VectorMon = Vector3.new(-6406, 24, -5805)

            CFrameQuest = CFrame.new(-6060, 16, -4905)
            VectorQuest = Vector3.new(-6060, 16, -4905)
        elseif MyLevel == 1175 or MyLevel <= 1199 then -- Magma Ninja [Lv. 1175]
            LevelFarm = 18

            Name = "Magma Ninja"
            QuestName = "FireSideQuest"
            LevelQuest = 1
            NameMon = "Magma Ninja"

            CFrameMon = CFrame.new(-5428, 78, -5959)
            VectorMon = Vector3.new(-5428, 78, -5959)

            CFrameQuest = CFrame.new(-5430, 16, -5295)
            VectorQuest = Vector3.new(-5430, 16, -5296)
        elseif MyLevel == 1200 or MyLevel <= 1249 then -- Lava Pirate [Lv. 1200]
            LevelFarm = 19

            Name = "Lava Pirate"
            QuestName = "FireSideQuest"

            LevelQuest = 2
            NameMon = "Lava Pirate"

            CFrameMon = CFrame.new(-5270, 42, -4800)
            VectorMon = Vector3.new(-5270, 42, -4800)

            CFrameQuest = CFrame.new(-5430, 16, -5295)
            VectorQuest = Vector3.new(-5430, 16, -5296)
        elseif MyLevel == 1250 or MyLevel <= 1274 then -- Ship Deckhand [Lv. 1250]
            LevelFarm = 21

            Name = "Ship Deckhand"
            QuestName = "ShipQuest1"

            LevelQuest = 1
            NameMon = "Ship Deckhand"

            CFrameMon = CFrame.new(1198, 126, 33031)
            VectorMon = Vector3.new(1198, 126, 33031)

            CFrameQuest = CFrame.new(1038, 125, 32913)
            VectorQuest = Vector3.new(1038, 125, 32913)
        elseif MyLevel == 1275 or MyLevel <= 1299 then -- Ship Engineer [Lv. 1275]
            LevelFarm = 22

            Name = "Ship Engineer"
            QuestName = "ShipQuest1"

            LevelQuest = 2
            NameMon = "Ship Engineer"

            CFrameMon = CFrame.new(918, 44, 32787)
            VectorMon = Vector3.new(918, 44, 32787)

            CFrameQuest = CFrame.new(1038, 125, 32913)
            VectorQuest = Vector3.new(1038, 125, 32913)
        elseif MyLevel == 1300 or MyLevel <= 1324 then -- Ship Steward [Lv. 1300]
            LevelFarm = 23

            Name = "Ship Steward"
            QuestName = "ShipQuest2"

            LevelQuest = 1
            NameMon = "Ship Steward"

            CFrameMon = CFrame.new(915, 130, 33419)
            VectorMon = Vector3.new(915, 130, 33419)

            CFrameQuest = CFrame.new(969, 125, 33245)
            VectorQuest = Vector3.new(969, 125, 33245)
        elseif MyLevel == 1325 or MyLevel <= 1349 then -- Ship Officer [Lv. 1325]
            LevelFarm = 24

            Name = "Ship Officer"
            QuestName = "ShipQuest2"

            LevelQuest = 2
            NameMon = "Ship Officer"

            CFrameMon = CFrame.new(916, 181, 33335)
            VectorMon = Vector3.new(916, 181, 33335)

            CFrameQuest = CFrame.new(969, 125, 33245)
            VectorQuest = Vector3.new(969, 125, 33245)
        elseif MyLevel == 1350 or MyLevel <= 1374 then -- Arctic Warrior [Lv. 1350]
            LevelFarm = 26

            Name = "Arctic Warrior"
            QuestName = "FrostQuest"

            LevelQuest = 1
            NameMon = "Arctic Warrior"

            CFrameMon = CFrame.new(6038, 29, -6231)
            VectorMon = Vector3.new(6038, 29, -6231)

            VectorQuest = Vector3.new(5669, 28, -6482)
            CFrameQuest = CFrame.new(5669, 28, -6482)
        elseif MyLevel == 1375 or MyLevel <= 1424 then -- Snow Lurker [Lv. 1375]
            LevelFarm = 27

            Name = "Snow Lurker"
            QuestName = "FrostQuest"

            LevelQuest = 2
            NameMon = "Snow Lurker"

            CFrameMon = CFrame.new(5560, 42, -6826)
            VectorMon = Vector3.new(5560, 42, -6826)

            VectorQuest = Vector3.new(5669, 28, -6482)
            CFrameQuest = CFrame.new(5669, 28, -6482)
        elseif MyLevel == 1425 or MyLevel <= 1449 then -- Sea Soldier [Lv. 1425]
            LevelFarm = 29
            Name = "Sea Soldier"
            QuestName = "ForgottenQuest"

            LevelQuest = 1
            NameMon = "Sea Soldier"

            CFrameMon = CFrame.new(-3022, 16, -9722)
            VectorMon = Vector3.new(-3022, 16, -9722)

            CFrameQuest = CFrame.new(-3054, 237, -10148)
            VectorQuest = Vector3.new(-3054, 237, -10148)
        elseif MyLevel >= 1450 then -- Water Fighter [Lv. 1450]
            LevelFarm = 30
            Name = "Water Fighter"
            QuestName = "ForgottenQuest"

            LevelQuest = 2
            NameMon = "Water Fighter"

            CFrameMon = CFrame.new(-3385, 239, -10542)
            VectorMon = Vector3.new(-3385, 239, -10542)

            CFrameQuest = CFrame.new(-3054, 237, -10148)
            VectorQuest = Vector3.new(-3054, 237, -10148)
        end
    end
    if World3 then
        if MyLevel == 1500 or MyLevel <= 1524 then
            LevelFarm = 1

            Name = "Pirate Millionaire"
            QuestName = "PiratePortQuest"

            LevelQuest = 1
            NameMon = "Pirate"

            CFrameMon = CFrame.new(-373, 75, 5550)
            VectorMon = Vector3.new(-373, 75, 5550)

            CFrameQuest = CFrame.new(-288, 44, 5576)
            VectorQuest = Vector3.new(-288, 44, 5576)
        elseif MyLevel == 1525 or MyLevel <= 1574 then
            LevelFarm = 2

            Name = "Pistol Billionaire"
            QuestName = "PiratePortQuest"

            LevelQuest = 2
            NameMon = "Pistol"

            CFrameMon = CFrame.new(-469, 74, 5904)
            VectorMon = Vector3.new(-469, 74, 5904)

            CFrameQuest = CFrame.new(-288, 44, 5576)
            VectorQuest = Vector3.new(-288, 44, 5576)
        elseif MyLevel == 1575 or MyLevel <= 1599 then
            LevelFarm = 4

            Name = "Dragon Crew Warrior"
            QuestName = "AmazonQuest"

            LevelQuest = 1
            NameMon = "Warrior"

            CFrameMon = CFrame.new(6339, 52, -1213)
            VectorMon = Vector3.new(6338, 52, -1213)

            CFrameQuest = CFrame.new(5835, 52, -1105)
            VectorQuest = Vector3.new(5835, 52, -1105)
        elseif MyLevel == 1600 or MyLevel <= 1624 then
            LevelFarm = 5

            Name = "Dragon Crew Archer"
            QuestName = "AmazonQuest"

            LevelQuest = 2
            NameMon = "Archer"

            CFrameMon = CFrame.new(6594, 383, 139)
            VectorMon = Vector3.new(6594, 383, 139)

            CFrameQuest = CFrame.new(5835, 52, -1105)
            VectorQuest = Vector3.new(5835, 52, -1105)
        elseif MyLevel == 1625 or MyLevel <= 1649 then
            LevelFarm = 6

            Name = "Female Islander"
            QuestName = "AmazonQuest2"

            LevelQuest = 1
            NameMon = "Female"

            CFrameMon = CFrame.new(5308, 819, 1047)
            VectorMon = Vector3.new(5308, 819, 1047)

            CFrameQuest = CFrame.new(5443, 602, 751)
            VectorQuest = Vector3.new(5443, 602, 751)
        elseif MyLevel == 1650 or MyLevel <= 1699 then
            LevelFarm = 7

            Name = "Giant Islander"
            QuestName = "AmazonQuest2"

            LevelQuest = 2
            NameMon = "Giant Islanders"

            CFrameMon = CFrame.new(4951, 602, -68)
            VectorMon = Vector3.new(4951, 602, -68)

            CFrameQuest = CFrame.new(5443, 602, 751)
            VectorQuest = Vector3.new(5443, 602, 751)
        elseif MyLevel == 1700 or MyLevel <= 1724 then
            LevelFarm = 9

            Name = "Marine Commodore"
            QuestName = "MarineTreeIsland"

            LevelQuest = 1
            NameMon = "Marine Commodore"

            CFrameMon = CFrame.new(2447, 73, -7470)
            VectorMon = Vector3.new(2447, 73, -7470)

            CFrameQuest = CFrame.new(2180, 29, -6737)
            VectorQuest = Vector3.new(2180, 29, -6737)
        elseif MyLevel == 1725 or MyLevel <= 1774 then
            LevelFarm = 10

            Name = "Marine Rear Admiral"
            QuestName = "MarineTreeIsland"

            LevelQuest = 2
            NameMon = "Marine Rear Admiral"

            CFrameMon = CFrame.new(3671, 161, -6932)
            VectorMon = Vector3.new(3671, 161, -6932)

            CFrameQuest = CFrame.new(2180, 29, -6737)
            VectorQuest = Vector3.new(2180, 29, -6737)
        elseif MyLevel == 1775 or MyLevel <= 1800 then
            LevelFarm = 12

            Name = "Fishman Raider"
            QuestName = "DeepForestIsland3"

            LevelQuest = 1
            NameMon = "Fishman Raider"

            CFrameMon = CFrame.new(-10560, 332, -8466)
            VectorMon = Vector3.new(-10560, 332, -8466)

            CFrameQuest = CFrame.new(-10584, 332, -8758)
            VectorQuest = Vector3.new(-10584, 332, -8758)
        elseif MyLevel == 1800 or MyLevel <= 1824 then
            LevelFarm = 13

            Name = "Fishman Captain"
            QuestName = "DeepForestIsland3"

            LevelQuest = 2
            NameMon = "Fishman Captain"

            CFrameMon = CFrame.new(-10993, 332, -8940)
            VectorMon = Vector3.new(-10993, 332, -8940)

            CFrameQuest = CFrame.new(-10584, 332, -8758)
            VectorQuest = Vector3.new(-10584, 332, -8758)
        elseif MyLevel == 1825 or MyLevel <= 1849 then
            LevelFarm = 14

            Name = "Forest Pirate"
            QuestName = "DeepForestIsland"

            LevelQuest = 1
            NameMon = "Forest Pirate"

            CFrameMon = CFrame.new(-13479, 333, -7905)
            VectorMon = Vector3.new(-13479, 333, -7905)

            CFrameQuest = CFrame.new(-13232, 333, -7627)
            VectorQuest = Vector3.new(-13232, 333, -7627)
        elseif MyLevel == 1850 or MyLevel <= 1899 then
            LevelFarm = 15

            Name = "Mythological Pirate"
            QuestName = "DeepForestIsland"

            LevelQuest = 2
            NameMon = "Mythological Pirate"

            CFrameMon = CFrame.new(-13545, 470, -6917)
            VectorMon = Vector3.new(-13545, 470, -6917)

            CFrameQuest = CFrame.new(-13232, 333, -7627)
            VectorQuest = Vector3.new(-13232, 333, -7627)
        elseif MyLevel == 1900 or MyLevel <= 1924 then
            LevelFarm = 16

            Name = "Jungle Pirate"
            QuestName = "DeepForestIsland2"

            LevelQuest = 1
            NameMon = "Jungle Pirate"

            CFrameMon = CFrame.new(-12107, 332, -10549)
            VectorMon = Vector3.new(-12106, 332, -10549)

            CFrameQuest = CFrame.new(-12684, 391, -9902)
            VectorQuest = Vector3.new(-12684, 391, -9902)
        elseif MyLevel == 1925 or MyLevel <= 1974 then
            LevelFarm = 17

            Name = "Musketeer Pirate"
            QuestName = "DeepForestIsland2"

            LevelQuest = 2
            NameMon = "Musketeer Pirate"

            CFrameMon = CFrame.new(-13286, 392, -9769)
            VectorMon = Vector3.new(-13286, 392, -9768)

            CFrameQuest = CFrame.new(-12684, 391, -9902)
            VectorQuest = Vector3.new(-12684, 391, -9902)
        elseif MyLevel == 1975 or MyLevel <= 1999 then
            LevelFarm = 19
            Name = "Reborn Skeleton"
            QuestName = "HauntedQuest1"

            LevelQuest = 1
            NameMon = "Reborn Skeleton"

            CFrameMon = CFrame.new(-8760, 142, 6039)
            VectorMon = Vector3.new(-8760, 142, 6039)

            CFrameQuest = CFrame.new(-9482, 142, 5567)
            VectorQuest = Vector3.new(-9482, 142, 5567)
        elseif MyLevel == 2000 or MyLevel <= 2024 then
            LevelFarm = 20

            Name = "Living Zombie"
            QuestName = "HauntedQuest1"

            LevelQuest = 2
            NameMon = "Living Zombie"

            CFrameMon = CFrame.new(-10144, 140, 5932)
            VectorMon = Vector3.new(-10144, 140, 5932)

            CFrameQuest = CFrame.new(-9482, 142, 5567)
            VectorQuest = Vector3.new(-9482, 142, 5567)
        elseif MyLevel == 2025 or MyLevel <= 2049 then
            LevelFarm = 21

            Name = "Demonic Soul"
            QuestName = "HauntedQuest2"

            LevelQuest = 1
            NameMon = "Demonic Soul"

            CFrameMon = CFrame.new(-9507, 172, 6158)
            VectorMon = Vector3.new(-9506, 172, 6158)

            CFrameQuest = CFrame.new(-9513, 172, 6079)
            VectorQuest = Vector3.new(-9513, 172, 6079)
        elseif MyLevel == 2050 or MyLevel <= 2074 then
            LevelFarm = 22

            Name = "Posessed Mummy"
            QuestName = "HauntedQuest2"

            LevelQuest = 2
            NameMon = "Posessed Mummy"

            CFrameMon = CFrame.new(-9577, 6, 6223)
            VectorMon = Vector3.new(-9577, 6, 6223)

            CFrameQuest = CFrame.new(-9513, 172, 6079)
            VectorQuest = Vector3.new(-9513, 172, 6079)
        elseif MyLevel == 2075 or MyLevel <= 2099 then
            LevelFarm = 24

            Name = "Peanut Scout"
            QuestName = "NutsIslandQuest"

            LevelQuest = 1
            NameMon = "Peanut Scout"

            CFrameMon = CFrame.new(-2124, 123, -10435)
            VectorMon = Vector3.new(-2124, 123, -10435)

            CFrameQuest = CFrame.new(-2104, 38, -10192)
            VectorQuest = Vector3.new(-2104, 38, -10192)
        elseif MyLevel == 2100 or MyLevel <= 2124 then
            LevelFarm = 25

            Name = "Peanut President"
            QuestName = "NutsIslandQuest"

            LevelQuest = 2
            NameMon = "Peanut President"

            CFrameMon = CFrame.new(-2124, 123, -10435)
            VectorMon = Vector3.new(-2124, 123, -10435)

            CFrameQuest = CFrame.new(-2104, 38, -10192)
            VectorQuest = Vector3.new(-2104, 38, -10192)
        elseif MyLevel == 2125 or MyLevel <= 2149 then
            LevelFarm = 26

            Name = "Ice Cream Chef"
            QuestName = "IceCreamIslandQuest"

            LevelQuest = 1
            NameMon = "Ice Cream Chef"

            CFrameMon = CFrame.new(-641, 127, -11062)
            VectorMon = Vector3.new(-641, 127, -11062)

            CFrameQuest = CFrame.new(-822, 66, -10965)
            VectorQuest = Vector3.new(-822, 66, -10965)
        elseif MyLevel == 2150 or MyLevel <= 2199 then
            LevelFarm = 27

            Name = "Ice Cream Commander"
            QuestName = "IceCreamIslandQuest"

            LevelQuest = 2
            NameMon = "Ice Cream Commander"

            CFrameMon = CFrame.new(-641, 127, -11062)
            VectorMon = Vector3.new(-641, 127, -11062)

            CFrameQuest = CFrame.new(-822, 66, -10965)
            VectorQuest = Vector3.new(-822, 66, -10965)
            ---------------------------------------------------------------
        elseif MyLevel == 2200 or MyLevel <= 2224 then
            LevelFarm = 29

            Name = "Cookie Crafter"
            QuestName = "CakeQuest1"

            LevelQuest = 1
            NameMon = "Cookie Crafter"

            CFrameMon = CFrame.new(-2365, 38, -12099)
            VectorMon = Vector3.new(-2365, 38, -12099)

            CFrameQuest = CFrame.new(-2020, 38, -12025)
            VectorQuest = Vector3.new(-2020, 38, -12025)
        elseif MyLevel == 2225 or MyLevel <= 2249 then
            LevelFarm = 30

            Name = "Cake Guard"
            QuestName = "CakeQuest1"

            LevelQuest = 2
            NameMon = "Cake Guard"

            CFrameMon = CFrame.new(-1651, 38, -12308)
            VectorMon = Vector3.new(-1651, 38, -12308)

            CFrameQuest = CFrame.new(-2020, 38, -12025)
            VectorQuest = Vector3.new(-2020, 38, -12025)
        elseif MyLevel == 2250 or MyLevel <= 2274 then
            LevelFarm = 31

            Name = "Baking Staff"
            QuestName = "CakeQuest2"

            LevelQuest = 1
            NameMon = "Baking Staff"

            CFrameMon = CFrame.new(-1870, 38, -12938)
            VectorMon = Vector3.new(-1870, 38, -12938)

            CFrameQuest = CFrame.new(-1926, 38, -12850)
            VectorQuest = Vector3.new(-1926, 38, -12850)
        elseif MyLevel == 2275 or MyLevel <= 2299 then
            LevelFarm = 32

            Name = "Head Baker"
            QuestName = "CakeQuest2"

            LevelQuest = 2
            NameMon = "Head Baker"

            CFrameMon = CFrame.new(-1926, 88, -12850)
            VectorMon = CFrame.new(-1870, 38, -12938)

            CFrameQuest = CFrame.new(-1926, 38, -12850)
            VectorQuest = Vector3.new(-1926, 38, -12850)
            ---------------------------------------------------------------
        elseif MyLevel == 2300 or MyLevel <= 2324 then
            LevelFarm = 34

            Name = "Cocoa Warrior"
            QuestName = "ChocQuest1"

            LevelQuest = 1
            NameMon = "Cocoa Warrior"

            CFrameMon = CFrame.new(231, 23, -12194)
            VectorMon = CFrame.new(231, 23, -12194)

            CFrameQuest = CFrame.new(231, 23, -12194)
            VectorQuest = Vector3.new(231, 23, -12194)
        elseif MyLevel == 2325 or MyLevel <= 2349 then
            LevelFarm = 35

            Name = "Chocolate Bar Battler"
            QuestName = "ChocQuest1"

            LevelQuest = 2
            NameMon = "Chocolate Bar Battler"

            CFrameMon = CFrame.new(231, 23, -12194)
            VectorMon = CFrame.new(231, 23, -12194)

            CFrameQuest = CFrame.new(231, 23, -12194)
            VectorQuest = Vector3.new(231, 23, -12194)
        elseif MyLevel == 2350 or MyLevel <= 2374 then
            LevelFarm = 36

            Name = "Sweet Thief"
            QuestName = "ChocQuest2"

            LevelQuest = 1
            NameMon = "Sweet Thief"

            CFrameMon = CFrame.new(71, 77, -12632)
            VectorMon = CFrame.new(71, 77, -12632)

            CFrameQuest = CFrame.new(151, 23, -12774)
            VectorQuest = Vector3.new(151, 23, -12774)
        elseif MyLevel == 2375 or MyLevel <= 2399 then
            LevelFarm = 37

            Name = "Candy Rebel"
            QuestName = "ChocQuest2"

            LevelQuest = 2
            NameMon = "Candy Rebel"

            CFrameMon = CFrame.new(134, 77, -12882)
            VectorMon = CFrame.new(134, 77, -12882)

            CFrameQuest = CFrame.new(151, 23, -12774)
            VectorQuest = Vector3.new(151, 23, -12774)
        elseif MyLevel == 2400 or MyLevel <= 2424 then
            LevelFarm = 39

            Name = "Candy Pirate"
            QuestName = "CandyQuest1"

            LevelQuest = 1
            NameMon = "Candy Pirates"

            CFrameMon = CFrame.new(-1358.691650390625, 162.7437286376953, -14389.7919921875)
            VectorMon = CFrame.new(-1358.691650390625, 162.7437286376953, -14389.7919921875)

            CFrameQuest = CFrame.new(-1146.59741, 14.1330338, -14445.6426, 0.142417297, 4.85419136e-08, 0.989806712,
                4.3708237e-08, 1, -5.53307267e-08, -0.989806712, 5.11427594e-08, 0.142417297)
            VectorQuest = Vector3.new(-1146.59741, 14.1330338, -14445.6426, 0.142417297, 4.85419136e-08, 0.989806712,
                4.3708237e-08, 1, -5.53307267e-08, -0.989806712, 5.11427594e-08, 0.142417297)
        elseif MyLevel == 2425 or MyLevel <= 2449 then
            LevelFarm = 40

            Name = "Snow Demon"
            QuestName = "CandyQuest1"

            LevelQuest = 2
            NameMon = "Snow Demons"

            CFrameMon = CFrame.new(-940.4050903320312, 60.94138717651367, -14554.1630859375)
            VectorMon = CFrame.new(-940.4050903320312, 60.94138717651367, -14554.1630859375)

            CFrameQuest = CFrame.new(-1146.59741, 14.1330338, -14445.6426, 0.142417297, 4.85419136e-08, 0.989806712,
                4.3708237e-08, 1, -5.53307267e-08, -0.989806712, 5.11427594e-08, 0.142417297)
            VectorQuest = Vector3.new(-1146.59741, 14.1330338, -14445.6426, 0.142417297, 4.85419136e-08, 0.989806712,
                4.3708237e-08, 1, -5.53307267e-08, -0.989806712, 5.11427594e-08, 0.142417297)
            elseif MyLevel == 2450 or MyLevel <= 2474 then
                LevelFarm = 42
    
                Name = "Isle Outlaw"
                QuestName = "TikiQuest1"
    
                LevelQuest = 1
                NameMon = "Isle Outlaw"
    
                CFrameMon = CFrame.new(-16299.3252, 94.0675659, -172.353226, 0.99993372, 1.59262612e-08, -0.0115144337, -1.50289505e-08, 1, 7.80157237e-08, 0.0115144337, -7.78375053e-08, 0.99993372)
                VectorMon = CFrame.new(-16299.3252, 94.0675659, -172.353226, 0.99993372, 1.59262612e-08, -0.0115144337, -1.50289505e-08, 1, 7.80157237e-08, 0.0115144337, -7.78375053e-08, 0.99993372)
    
                CFrameQuest = CFrame.new(-16548.8516, 54.0840454, -173.242691, 0.213092566, -0, -0.977032006, 0, 1, -0, 0.977032006, 0, 0.213092566)
                VectorQuest = Vector3.new(-16548.8516, 54.0840454, -173.242691, 0.213092566, -0, -0.977032006, 0, 1, -0, 0.977032006, 0, 0.213092566)
            elseif MyLevel == 2475 or MyLevel <= 2524 then
                LevelFarm = 43
    
                Name = "Island Boy"
                QuestName = "TikiQuest1"
    
                LevelQuest = 2
                NameMon = "Island Boy"
    
                CFrameMon = CFrame.new(-16853.3887, 192.103561, -152.378189, 0.705479085, -8.49727329e-08, 0.708730757, 5.86954414e-08, 1, 6.14680928e-08, -0.708730757, -1.76518711e-09, 0.705479085)
                VectorMon = CFrame.new(-16853.3887, 192.103561, -152.378189, 0.705479085, -8.49727329e-08, 0.708730757, 5.86954414e-08, 1, 6.14680928e-08, -0.708730757, -1.76518711e-09, 0.705479085)
    
                CFrameQuest = CFrame.new(-16548.8516, 54.0840454, -173.242691, 0.213092566, -0, -0.977032006, 0, 1, -0, 0.977032006, 0, 0.213092566)
                VectorQuest = Vector3.new(-16548.8516, 54.0840454, -173.242691, 0.213092566, -0, -0.977032006, 0, 1, -0, 0.977032006, 0, 0.213092566)
            elseif MyLevel == 2525 or MyLevel <= 2600 then
                LevelFarm = 44
    
                Name = "Isle Champion"
                QuestName = "TikiQuest2"
    
                LevelQuest = 2
                NameMon = "Isle Champion"
    
                CFrameMon = CFrame.new(-16780.2383, 82.1389999, 1033.18713, -0.906431854, 1.29724e-08, 0.422352165, 1.32806277e-09, 1, -2.7864429e-08, -0.422352165, -2.46962948e-08, -0.906431854)
                VectorMon = CFrame.new(-16780.2383, 82.1389999, 1033.18713, -0.906431854, 1.29724e-08, 0.422352165, 1.32806277e-09, 1, -2.7864429e-08, -0.422352165, -2.46962948e-08, -0.906431854)
    
                CFrameQuest = CFrame.new(-16541.0215, 54.770813, 1051.46118, 0.0410757065, -0, -0.999156058, 0, 1, -0, 0.999156058, 0, 0.0410757065)
                VectorQuest = Vector3.new(-16541.0215, 54.770813, 1051.46118, 0.0410757065, -0, -0.999156058, 0, 1, -0, 0.999156058, 0, 0.0410757065)
        end
    end
end

function CheckOldQuest(LevelFarm)
    if World1 then
        if LevelFarm == 1 then -- Bandit
            Name = "Bandit"
            QuestName = "BanditQuest1"

            LevelQuest = 1
            NameMon = "Bandit"

            CFrameMon = CFrame.new(1145, 17, 1634)
            VectorMon = Vector3.new(1145, 17, 1634)

            CFrameQuest = CFrame.new(1060, 17, 1547)
            VectorQuest = Vector3.new(1060, 17, 1547)
        elseif LevelFarm == 3 then -- Monkey
            Name = "Monkey"
            QuestName = "JungleQuest"

            LevelQuest = 1
            NameMon = "Monkey"

            CFrameMon = CFrame.new(-1496, 39, 35)
            VectorMon = Vector3.new(-1496, 39, 35)

            CFrameQuest = CFrame.new(-1602, 37, 152)
            VectorQuest = Vector3.new(-1602, 37, 152)
        elseif LevelFarm == 4 then -- Gorilla
            Name = "Gorilla"
            QuestName = "JungleQuest"

            LevelQuest = 2
            NameMon = "Gorilla"

            CFrameMon = CFrame.new(-1237, 6, -486)
            VectorMon = Vector3.new(-1237, 7, -486)

            CFrameQuest = CFrame.new(-1602, 37, 152)
            VectorQuest = Vector3.new(-1602, 37, 152)
        elseif LevelFarm == 6 then -- Pirate
            Name = "Pirate"
            QuestName = "BuggyQuest1"

            LevelQuest = 1
            NameMon = "Pirate"

            CFrameMon = CFrame.new(-1115, 14, 3938)
            VectorMon = Vector3.new(-1115, 14, 3938)

            CFrameQuest = CFrame.new(-1140, 5, 3828)
            VectorQuest = Vetor3.new(-1140, 5, 3828)
        elseif LevelFarm == 9 then -- Desert Bandit
            Name = "Desert Bandit"
            QuestName = "DesertQuest"

            LevelQuest = 1
            NameMon = "Desert Bandit"

            CFrameMon = CFrame.new(932, 7, 4484)
            VectorMon = Vector3.new(932, 7, 4484)

            CFrameQuest = CFrame.new(897, 7, 4388)
            VectorQuest = Vector3.new(897, 7, 4388)
        elseif LevelFarm == 10 then -- Desert Officre
            Name = "Desert Officer"
            QuestName = "DesertQuest"

            LevelQuest = 2
            NameMon = "Desert Officer"

            CFrameMon = CFrame.new(1572, 10, 4373)
            VectorMon = Vector3.new(1572, 10, 4373)

            CFrameQuest = CFrame.new(897, 7, 4388)
            VectorQuest = Vector3.new(897, 7, 4388)
        elseif LevelFarm == 12 then -- Snow Bandits
            Name = "Snow Bandit"
            QuestName = "SnowQuest"

            LevelQuest = 1
            NameMon = "Snow Bandits"

            CFrameMon = CFrame.new(1289, 150, -1442)
            VectorMon = Vector3.new(1289, 106, -1442)

            CFrameQuest = CFrame.new(1386, 87, -1297)
            VectorQuest = Vector3.new(1386, 87, -1297)
        elseif LevelFarm == 13 then -- Snowman
            Name = "Snowman"
            QuestName = "SnowQuest"

            LevelQuest = 2
            NameMon = "Snowman"

            CFrameMon = CFrame.new(1289, 150, -1442)
            VectorMon = Vector3.new(1289, 106, -1442)

            CFrameQuest = CFrame.new(1386, 87, -1297)
            VectorQuest = Vector3.new(1386, 87, -1297)
        elseif LevelFarm == 15 then -- Chief Petty Officer
            Name = "Chief Petty Officer"
            QuestName = "MarineQuest2"

            LevelQuest = 1
            NameMon = "Chief Petty Officer"

            CFrameMon = CFrame.new(-4855, 23, 4308)
            VectorMon = Vector3.new(-4855, 23, 4308)

            CFrameQuest = CFrame.new(-5036, 29, 4325)
            VectorQuest = Vector3.new(-5036, 29, 4325)
        elseif LevelFarm == 17 then -- Sky Bandit
            Name = "Sky Bandit"
            QuestName = "SkyQuest"

            LevelQuest = 1
            NameMon = "Sky Bandit"

            CFrameMon = CFrame.new(-4981, 278, -2830)
            VectorMon = Vector3.new(-4981, 278, -2830)

            CFrameQuest = CFrame.new(-4842, 718, -2623)
            VectorQuest = Vector3.new(-4842, 718, -2623)
        elseif LevelFarm == 18 then -- Dark Master
            Name = "Dark Master"
            QuestName = "SkyQuest"

            LevelQuest = 2
            NameMon = "Dark Master"

            CFrameMon = CFrame.new(-5250, 389, -2272)
            VectorMon = Vector3.new(-5250, 389, -2272)

            CFrameQuest = CFrame.new(-4842, 718, -2623)
            VectorQuest = Vector3.new(-4842, 718, -2623)
        elseif LevelFarm == 20 then -- Dark Master
            Name = "Prisoner"
            QuestName = "PrisonerQuest"

            LevelQuest = 1
            NameMon = "Prisoner"

            CFrameMon = CFrame.new(5411, 96, 690)
            VectorMon = Vector3.new(5411, 96, 690)

            CFrameQuest = CFrame.new(5308, 2, 474)
            VectorQuest = Vector3.new(5308, 2, 474)
        elseif LevelFarm == 21 then -- Dark Master
            Name = "Dangerous Prisoner"
            QuestName = "PrisonerQuest"

            LevelQuest = 2
            NameMon = "Dangerous Prisoner"

            CFrameMon = CFrame.new(5411, 96, 690)
            VectorMon = Vector3.new(5411, 96, 690)

            CFrameQuest = CFrame.new(5308, 2, 474)
            VectorQuest = Vector3.new(5308, 2, 474)
        elseif LevelFarm == 23 then -- Toga Warrior
            Name = "Toga Warrior"
            QuestName = "ColosseumQuest"

            LevelQuest = 1
            NameMon = "Toga Warrior"

            CFrameMon = CFrame.new(-1770, 8, -2777)
            VectorMon = Vector3.new(-1770, 8, -2777)

            CFrameQuest = CFrame.new(-1576, 8, -2985)
            VectorQuest = Vector3.new(-1576, 8, -2985)
        elseif LevelFarm == 25 then -- Military Soldier
            Name = "Military Soldier"
            QuestName = "MagmaQuest"

            LevelQuest = 1
            NameMon = "Military Soldier"

            CFrameMon = CFrame.new(-5555.064453125, 16.73392105102539, 8377.623046875)
            VectorMon = Vector3.new(-5555.064453125, 16.73392105102539, 8377.623046875)

            CFrameQuest = CFrame.new(-5316, 12, 8517)
            VectorQuest = Vector3.new(-5316, 12, 8517)
        elseif LevelFarm == 26 then -- Military Spy
            Name = "Military Spy"
            QuestName = "MagmaQuest"

            LevelQuest = 2
            NameMon = "Military Spy"

            CFrameMon = CFrame.new(-5806.056640625, 99.96672058105469, 8777.8447265625)
            VectorMon = Vector3.new(-5806.056640625, 99.96672058105469, 8777.8447265625)

            CFrameQuest = CFrame.new(-5316, 12, 8517)
            VectorQuest = Vector3.new(-5316, 12, 8517)
        elseif LevelFarm == 28 then -- Fishman Warrior
            Name = "Fishman Warrior"
            QuestName = "FishmanQuest"

            LevelQuest = 1
            NameMon = "Fishman Warrior"

            CFrameMon = CFrame.new(60859, 19, 1501)
            VectorMon = Vector3.new(60859, 19, 1501)

            CFrameQuest = CFrame.new(61123, 19, 1569)
            VectorQuest = Vector3.new(61123, 19, 1569)
        elseif LevelFarm == 29 then -- Fishman Commando
            Name = "Fishman Commando"
            QuestName = "FishmanQuest"

            LevelQuest = 2
            NameMon = "Fishman Commando"

            CFrameMon = CFrame.new(61891, 19, 1470)
            VectorMon = Vector3.new(61891, 19, 1470)

            CFrameQuest = CFrame.new(61123, 19, 1569)
            VectorQuest = Vector3.new(61123, 19, 1569)
        elseif LevelFarm == 31 then -- God's Guards
            Name = "God's Guard"
            QuestName = "SkyExp1Quest"

            LevelQuest = 1
            NameMon = "God's Guards"

            CFrameMon = CFrame.new(-4698, 845, -1912)
            VectorMon = Vector3.new(-4698, 845, -1912)

            CFrameQuest = CFrame.new(-4722, 845, -1954)
            VectorQuest = Vector3.new(-4722, 846, -1954)
        elseif LevelFarm == 33 then -- Shandas
            Name = "Shanda"
            QuestName = "SkyExp1Quest"

            LevelQuest = 2
            NameMon = "Shandas"

            CFrameMon = CFrame.new(-7685, 5567, -502)
            VectorMon = Vector3.new(-7685, 5567, -502)

            CFrameQuest = CFrame.new(-7862, 5546, -380)
            VectorQuest = Vector3.new(-7862, 5546, -380)
        elseif LevelFarm == 34 then -- Royal Squad
            Name = "Royal Squad"
            QuestName = "SkyExp2Quest"

            LevelQuest = 1
            NameMon = "Royal Squad"

            CFrameMon = CFrame.new(-7670, 5607, -1460)
            VectorMon = Vector3.new(-7670, 5607, -1460)

            CFrameQuest = CFrame.new(-7904, 5636, -1412)
            VectorQuest = Vector3.new(-7904, 5636, -1412)
        elseif LevelFarm == 35 then -- Royal Soldier
            Name = "Royal Soldier"
            QuestName = "SkyExp2Quest"

            LevelQuest = 2
            NameMon = "Royal Soldier"

            CFrameMon = CFrame.new(-7828, 5607, -1744)
            VectorMon = Vector3.new(-7828, 5607, -1744)

            CFrameQuest = CFrame.new(-7904, 5636, -1412)
            VectorQuest = Vector3.new(-7904, 5636, -1412)
        elseif LevelFarm == 37 then -- Galley Pirate
            Name = "Galley Pirate"
            QuestName = "FountainQuest"

            LevelQuest = 1
            NameMon = "Galley Pirate"

            CFrameMon = CFrame.new(5589, 45, 3996)
            VectorMon = Vector3.new(5589, 45, 3996)

            CFrameQuest = CFrame.new(5256, 39, 4050)
            VectorQuest = Vector3.new(5256, 39, 4050)
        elseif LevelFarm == 38 then -- Galley Captain
            Name = "Galley Captain"
            QuestName = "FountainQuest"

            LevelQuest = 2
            NameMon = "Galley Captain"

            CFrameMon = CFrame.new(5649, 39, 4936)
            VectorMon = Vector3.new(5649, 39, 4936)

            CFrameQuest = CFrame.new(5256, 39, 4050)
            VectorQuest = Vector3.new(5256, 39, 4050)
        end
    end
    if World2 then
        if LevelFarm == 1 then -- Raider [Lv. 700]
            Name = "Raider"
            QuestName = "Area1Quest"

            LevelQuest = 1
            NameMon = "Raider"

            CFrameQuest = CFrame.new(-425, 73, 1837)
            VectorQuest = Vector3.new(-425, 73, 1837)

            CFrameMon = CFrame.new(-746, 39, 2390)
            VectorMon = Vector3.new(-746, 39, 2389)
        elseif LevelFarm == 2 then -- Mercenary [Lv. 725]
            Name = "Mercenary"
            QuestName = "Area1Quest"

            LevelQuest = 2
            NameMon = "Mercenary"

            CFrameQuest = CFrame.new(-425, 73, 1837)
            VectorQuest = Vector3.new(-425, 73, 1837)

            CFrameMon = CFrame.new(-874, 141, 1312)
            VectorMon = Vector3.new(-874, 141, 1312)
        elseif LevelFarm == 3 then -- Swan Pirate [Lv. 775]
            Name = "Swan Pirate"
            QuestName = "Area2Quest"

            LevelQuest = 1
            NameMon = "Swan Pirate"

            CFrameQuest = CFrame.new(634, 73, 918)
            VectorQuest = Vector3.new(634, 73, 918)

            CFrameMon = CFrame.new(878, 122, 1235)
            VectorMon = Vector3.new(878, 122, 1235)
        elseif LevelFarm == 4 then -- Factory Staff [Lv. 800]
            Name = "Factory Staff"
            QuestName = "Area2Quest"

            LevelQuest = 2
            NameMon = "Factory Staff"

            CFrameQuest = CFrame.new(634, 73, 918)
            VectorQuest = Vector3.new(634, 73, 918)

            CFrameMon = CFrame.new(295, 73, -56)
            VectorMon = Vector3.new(295, 73, -56)
        elseif LevelFarm == 6 then -- Marine Lieutenant [Lv. 875]
            Name = "Marine Lieutenant"
            QuestName = "MarineQuest3"

            LevelQuest = 1
            NameMon = "Marine Lieutenant"

            CFrameMon = CFrame.new(-2806, 73, -3038)
            VectorMon = Vector3.new(-2806, 73, -3038)

            CFrameQuest = CFrame.new(-2443, 73, -3219)
            VectorQuest = Vector3.new(-2443, 73, -3219)
        elseif LevelFarm == 7 then -- Marine Captain [Lv. 900]
            Name = "Marine Captain"
            QuestName = "MarineQuest3"

            LevelQuest = 2
            NameMon = "Marine Captain"

            CFrameMon = CFrame.new(-1869, 73, -3320)
            VectorMon = Vector3.new(-1869, 73, -3320)

            CFrameQuest = CFrame.new(-2443, 73, -3219)
            VectorQuest = Vector3.new(-2443, 73, -3219)
        elseif LevelFarm == 9 then -- Zombie [Lv. 950]
            Name = "Zombie"
            QuestName = "ZombieQuest"

            LevelQuest = 1
            NameMon = "Zombie"

            CFrameMon = CFrame.new(-5736, 126, -728)
            VectorMon = Vector3.new(-5736, 126, -728)

            CFrameQuest = CFrame.new(-5494, 49, -795)
            VectorQuest = Vector3.new(-5494, 49, -794)
        elseif LevelFarm == 10 then -- Vampire [Lv. 975]
            Name = "Vampire"
            QuestName = "ZombieQuest"

            LevelQuest = 2
            NameMon = "Vampire"

            CFrameMon = CFrame.new(-6033, 7, -1317)
            VectorMon = Vector3.new(-6033, 7, -1317)

            CFrameQuest = CFrame.new(-5494, 49, -795)
            VectorQuest = Vector3.new(-5494, 49, -795)
        elseif LevelFarm == 12 then -- Snow Trooper [Lv. 1000] **
            Name = "Snow Trooper"
            QuestName = "SnowMountainQuest"

            LevelQuest = 1
            NameMon = "Snow Trooper"

            CFrameMon = CFrame.new(478, 402, -5362)
            VectorMon = Vector3.new(478, 402, -5362)

            CFrameQuest = CFrame.new(605, 402, -5371)
            VectorQuest = Vector3.new(605, 402, -5371)
        elseif LevelFarm == 13 then -- Winter Warrior [Lv. 1050]
            Name = "Winter Warrior"
            QuestName = "SnowMountainQuest"

            LevelQuest = 2
            NameMon = "Winter Warrior"

            CFrameMon = CFrame.new(1157, 430, -5188)
            VectorMon = Vector3.new(1157, 430, -5188)

            CFrameQuest = CFrame.new(605, 402, -5371)
            VectorQuest = Vector3.new(605, 402, -5371)
        elseif LevelFarm == 16 then -- Lab Subordinate [Lv. 1100]
            Name = "Lab Subordinate"
            QuestName = "IceSideQuest"

            LevelQuest = 1
            NameMon = "Lab Subordinate"

            CFrameMon = CFrame.new(-5782, 42, -4484)
            VectorMon = Vector3.new(-5782, 42, -4484)

            CFrameQuest = CFrame.new(-6060, 16, -4905)
            VectorQuest = Vector3.new(-6060, 16, -4905)
        elseif LevelFarm == 17 then -- Horned Warrior [Lv. 1125]
            Name = "Horned Warrior"
            QuestName = "IceSideQuest"

            LevelQuest = 2
            NameMon = "Horned Warrior"

            CFrameMon = CFrame.new(-6406, 24, -5805)
            VectorMon = Vector3.new(-6406, 24, -5805)

            CFrameQuest = CFrame.new(-6060, 16, -4905)
            VectorQuest = Vector3.new(-6060, 16, -4905)
        elseif LevelFarm == 18 then -- Magma Ninja [Lv. 1175]
            Name = "Magma Ninja"
            QuestName = "FireSideQuest"
            LevelQuest = 1
            NameMon = "Magma Ninja"

            CFrameMon = CFrame.new(-5428, 78, -5959)
            VectorMon = Vector3.new(-5428, 78, -5959)

            CFrameQuest = CFrame.new(-5430, 16, -5295)
            VectorQuest = Vector3.new(-5430, 16, -5296)
        elseif LevelFarm == 19 then -- Lava Pirate [Lv. 1200]
            Name = "Lava Pirate"
            QuestName = "FireSideQuest"

            LevelQuest = 2
            NameMon = "Lava Pirate"

            CFrameMon = CFrame.new(-5270, 42, -4800)
            VectorMon = Vector3.new(-5270, 42, -4800)

            CFrameQuest = CFrame.new(-5430, 16, -5295)
            VectorQuest = Vector3.new(-5430, 16, -5296)
        elseif LevelFarm == 21 then -- Ship Deckhand [Lv. 1250]
            Name = "Ship Deckhand"
            QuestName = "ShipQuest1"

            LevelQuest = 1
            NameMon = "Ship Deckhand"

            CFrameMon = CFrame.new(1198, 126, 33031)
            VectorMon = Vector3.new(1198, 126, 33031)

            CFrameQuest = CFrame.new(1038, 125, 32913)
            VectorQuest = Vector3.new(1038, 125, 32913)
        elseif LevelFarm == 22 then -- Ship Engineer [Lv. 1275]
            Name = "Ship Engineer"
            QuestName = "ShipQuest1"

            LevelQuest = 2
            NameMon = "Ship Engineer"

            CFrameMon = CFrame.new(918, 44, 32787)
            VectorMon = Vector3.new(918, 44, 32787)

            CFrameQuest = CFrame.new(1038, 125, 32913)
            VectorQuest = Vector3.new(1038, 125, 32913)
        elseif LevelFarm == 23 then -- Ship Steward [Lv. 1300]
            Name = "Ship Steward"
            QuestName = "ShipQuest2"

            LevelQuest = 1
            NameMon = "Ship Steward"

            CFrameMon = CFrame.new(915, 130, 33419)
            VectorMon = Vector3.new(915, 130, 33419)

            CFrameQuest = CFrame.new(969, 125, 33245)
            VectorQuest = Vector3.new(969, 125, 33245)
        elseif LevelFarm == 24 then -- Ship Officer [Lv. 1325]
            Name = "Ship Officer"
            QuestName = "ShipQuest2"

            LevelQuest = 2
            NameMon = "Ship Officer"

            CFrameMon = CFrame.new(916, 181, 33335)
            VectorMon = Vector3.new(916, 181, 33335)

            CFrameQuest = CFrame.new(969, 125, 33245)
            VectorQuest = Vector3.new(969, 125, 33245)
        elseif LevelFarm == 26 then -- Arctic Warrior [Lv. 1350]
            Name = "Arctic Warrior"
            QuestName = "FrostQuest"

            LevelQuest = 1
            NameMon = "Arctic Warrior"

            CFrameMon = CFrame.new(6038, 29, -6231)
            VectorMon = Vector3.new(6038, 29, -6231)

            VectorQuest = Vector3.new(5669, 28, -6482)
            CFrameQuest = CFrame.new(5669, 28, -6482)
        elseif LevelFarm == 27 then -- Snow Lurker [Lv. 1375]
            Name = "Snow Lurker"
            QuestName = "FrostQuest"

            LevelQuest = 2
            NameMon = "Snow Lurker"

            CFrameMon = CFrame.new(5560, 42, -6826)
            VectorMon = Vector3.new(5560, 42, -6826)

            VectorQuest = Vector3.new(5669, 28, -6482)
            CFrameQuest = CFrame.new(5669, 28, -6482)
        elseif LevelFarm == 29 then -- Sea Soldier [Lv. 1425]
            Name = "Sea Soldier"
            QuestName = "ForgottenQuest"

            LevelQuest = 1
            NameMon = "Sea Soldier"

            CFrameMon = CFrame.new(-3022, 16, -9722)
            VectorMon = Vector3.new(-3022, 16, -9722)

            CFrameQuest = CFrame.new(-3054, 237, -10148)
            VectorQuest = Vector3.new(-3054, 237, -10148)
        elseif LevelFarm == 30 then -- Water Fighter [Lv. 1450]
            Name = "Water Fighter"
            QuestName = "ForgottenQuest"

            LevelQuest = 2
            NameMon = "Water Fighter"

            CFrameMon = CFrame.new(-3385, 239, -10542)
            VectorMon = Vector3.new(-3385, 239, -10542)

            CFrameQuest = CFrame.new(-3054, 237, -10148)
            VectorQuest = Vector3.new(-3054, 237, -10148)
        end
    end
    if World3 then
        if LevelFarm == 1 then
            Name = "Pirate Millionaire"
            QuestName = "PiratePortQuest"

            LevelQuest = 1
            NameMon = "Pirate"

            CFrameMon = CFrame.new(-373, 75, 5550)
            VectorMon = Vector3.new(-373, 75, 5550)

            CFrameQuest = CFrame.new(-288, 44, 5576)
            VectorQuest = Vector3.new(-288, 44, 5576)
        elseif LevelFarm == 2 then
            Name = "Pistol Billionaire"
            QuestName = "PiratePortQuest"

            LevelQuest = 2
            NameMon = "Pistol"

            CFrameMon = CFrame.new(-469, 74, 5904)
            VectorMon = Vector3.new(-469, 74, 5904)

            CFrameQuest = CFrame.new(-288, 44, 5576)
            VectorQuest = Vector3.new(-288, 44, 5576)
        elseif LevelFarm == 4 then
            Name = "Dragon Crew Warrior"
            QuestName = "AmazonQuest"

            LevelQuest = 1
            NameMon = "Warrior"

            CFrameMon = CFrame.new(6339, 52, -1213)
            VectorMon = Vector3.new(6338, 52, -1213)

            CFrameQuest = CFrame.new(5835, 52, -1105)
            VectorQuest = Vector3.new(5835, 52, -1105)
        elseif LevelFarm == 5 then
            Name = "Dragon Crew Archer"
            QuestName = "AmazonQuest"

            LevelQuest = 2
            NameMon = "Archer"

            CFrameMon = CFrame.new(6594, 383, 139)
            VectorMon = Vector3.new(6594, 383, 139)

            CFrameQuest = CFrame.new(5835, 52, -1105)
            VectorQuest = Vector3.new(5835, 52, -1105)
        elseif LevelFarm == 6 then
            Name = "Female Islander"
            QuestName = "AmazonQuest2"

            LevelQuest = 1
            NameMon = "Female"

            CFrameMon = CFrame.new(5308, 819, 1047)
            VectorMon = Vector3.new(5308, 819, 1047)

            CFrameQuest = CFrame.new(5443, 602, 751)
            VectorQuest = Vector3.new(5443, 602, 751)
        elseif LevelFarm == 7 then
            Name = "Giant Islander"
            QuestName = "AmazonQuest2"

            LevelQuest = 2
            NameMon = "Giant Islanders"

            CFrameMon = CFrame.new(4951, 602, -68)
            VectorMon = Vector3.new(4951, 602, -68)

            CFrameQuest = CFrame.new(5443, 602, 751)
            VectorQuest = Vector3.new(5443, 602, 751)
        elseif LevelFarm == 9 then
            Name = "Marine Commodore"
            QuestName = "MarineTreeIsland"

            LevelQuest = 1
            NameMon = "Marine Commodore"

            CFrameMon = CFrame.new(2447, 73, -7470)
            VectorMon = Vector3.new(2447, 73, -7470)

            CFrameQuest = CFrame.new(2180, 29, -6737)
            VectorQuest = Vector3.new(2180, 29, -6737)
        elseif LevelFarm == 10 then
            Name = "Marine Rear Admiral"
            QuestName = "MarineTreeIsland"

            LevelQuest = 2
            NameMon = "Marine Rear Admiral"

            CFrameMon = CFrame.new(3671, 161, -6932)
            VectorMon = Vector3.new(3671, 161, -6932)

            CFrameQuest = CFrame.new(2180, 29, -6737)
            VectorQuest = Vector3.new(2180, 29, -6737)
        elseif LevelFarm == 12 then
            Name = "Fishman Raider"
            QuestName = "DeepForestIsland3"

            LevelQuest = 1
            NameMon = "Fishman Raider"

            CFrameMon = CFrame.new(-10560, 332, -8466)
            VectorMon = Vector3.new(-10560, 332, -8466)

            CFrameQuest = CFrame.new(-10584, 332, -8758)
            VectorQuest = Vector3.new(-10584, 332, -8758)
        elseif LevelFarm == 13 then
            Name = "Fishman Captain"
            QuestName = "DeepForestIsland3"

            LevelQuest = 2
            NameMon = "Fishman Captain"

            CFrameMon = CFrame.new(-10993, 332, -8940)
            VectorMon = Vector3.new(-10993, 332, -8940)

            CFrameQuest = CFrame.new(-10584, 332, -8758)
            VectorQuest = Vector3.new(-10584, 332, -8758)
        elseif LevelFarm == 14 then
            Name = "Forest Pirate"
            QuestName = "DeepForestIsland"

            LevelQuest = 1
            NameMon = "Forest Pirate"

            CFrameMon = CFrame.new(-13479, 333, -7905)
            VectorMon = Vector3.new(-13479, 333, -7905)

            CFrameQuest = CFrame.new(-13232, 333, -7627)
            VectorQuest = Vector3.new(-13232, 333, -7627)
        elseif LevelFarm == 15 then
            Name = "Mythological Pirate"
            QuestName = "DeepForestIsland"

            LevelQuest = 2
            NameMon = "Mythological Pirate"

            CFrameMon = CFrame.new(-13545, 470, -6917)
            VectorMon = Vector3.new(-13545, 470, -6917)

            CFrameQuest = CFrame.new(-13232, 333, -7627)
            VectorQuest = Vector3.new(-13232, 333, -7627)
        elseif LevelFarm == 16 then
            Name = "Jungle Pirate"
            QuestName = "DeepForestIsland2"

            LevelQuest = 1
            NameMon = "Jungle Pirate"

            CFrameMon = CFrame.new(-12107, 332, -10549)
            VectorMon = Vector3.new(-12106, 332, -10549)

            CFrameQuest = CFrame.new(-12684, 391, -9902)
            VectorQuest = Vector3.new(-12684, 391, -9902)
        elseif LevelFarm == 17 then
            Name = "Musketeer Pirate"
            QuestName = "DeepForestIsland2"

            LevelQuest = 2
            NameMon = "Musketeer Pirate"

            CFrameMon = CFrame.new(-13286, 392, -9769)
            VectorMon = Vector3.new(-13286, 392, -9768)

            CFrameQuest = CFrame.new(-12684, 391, -9902)
            VectorQuest = Vector3.new(-12684, 391, -9902)
        elseif LevelFarm == 19 then
            Name = "Reborn Skeleton"
            QuestName = "HauntedQuest1"

            LevelQuest = 1
            NameMon = "Reborn Skeleton"

            CFrameMon = CFrame.new(-8760, 142, 6039)
            VectorMon = Vector3.new(-8760, 142, 6039)

            CFrameQuest = CFrame.new(-9482, 142, 5567)
            VectorQuest = Vector3.new(-9482, 142, 5567)
        elseif LevelFarm == 20 then
            Name = "Living Zombie"
            QuestName = "HauntedQuest1"

            LevelQuest = 2
            NameMon = "Living Zombie"

            CFrameMon = CFrame.new(-10144, 140, 5932)
            VectorMon = Vector3.new(-10144, 140, 5932)

            CFrameQuest = CFrame.new(-9482, 142, 5567)
            VectorQuest = Vector3.new(-9482, 142, 5567)
        elseif LevelFarm == 21 then
            Name = "Demonic Soul"
            QuestName = "HauntedQuest2"

            LevelQuest = 1
            NameMon = "Demonic Soul"

            CFrameMon = CFrame.new(-9507, 172, 6158)
            VectorMon = Vector3.new(-9506, 172, 6158)

            CFrameQuest = CFrame.new(-9513, 172, 6079)
            VectorQuest = Vector3.new(-9513, 172, 6079)
        elseif LevelFarm == 22 then
            Name = "Posessed Mummy"
            QuestName = "HauntedQuest2"

            LevelQuest = 2
            NameMon = "Posessed Mummy"

            CFrameMon = CFrame.new(-9577, 6, 6223)
            VectorMon = Vector3.new(-9577, 6, 6223)

            CFrameQuest = CFrame.new(-9513, 172, 6079)
            VectorQuest = Vector3.new(-9513, 172, 6079)
        elseif LevelFarm == 24 then
            Name = "Peanut Scout"
            QuestName = "NutsIslandQuest"

            LevelQuest = 1
            NameMon = "Peanut Scout"

            CFrameMon = CFrame.new(-2124, 123, -10435)
            VectorMon = Vector3.new(-2124, 123, -10435)

            CFrameQuest = CFrame.new(-2104, 38, -10192)
            VectorQuest = Vector3.new(-2104, 38, -10192)
        elseif LevelFarm == 25 then
            Name = "Peanut President"
            QuestName = "NutsIslandQuest"

            LevelQuest = 2
            NameMon = "Peanut President"

            CFrameMon = CFrame.new(-2124, 123, -10435)
            VectorMon = Vector3.new(-2124, 123, -10435)

            CFrameQuest = CFrame.new(-2104, 38, -10192)
            VectorQuest = Vector3.new(-2104, 38, -10192)
        elseif LevelFarm == 26 then
            Name = "Ice Cream Chef"
            QuestName = "IceCreamIslandQuest"

            LevelQuest = 1
            NameMon = "Ice Cream Chef"

            CFrameMon = CFrame.new(-641, 127, -11062)
            VectorMon = Vector3.new(-641, 127, -11062)

            CFrameQuest = CFrame.new(-822, 66, -10965)
            VectorQuest = Vector3.new(-822, 66, -10965)
        elseif LevelFarm == 27 then
            Name = "Ice Cream Commander"
            QuestName = "IceCreamIslandQuest"

            LevelQuest = 2
            NameMon = "Ice Cream Commander"

            CFrameMon = CFrame.new(-641, 127, -11062)
            VectorMon = Vector3.new(-641, 127, -11062)

            CFrameQuest = CFrame.new(-822, 66, -10965)
            VectorQuest = Vector3.new(-822, 66, -10965)
            ---------------------------------------------------------------
        elseif LevelFarm == 29 then
            Name = "Cookie Crafter"
            QuestName = "CakeQuest1"

            LevelQuest = 1
            NameMon = "Cookie Crafter"

            CFrameMon = CFrame.new(-2365, 38, -12099)
            VectorMon = Vector3.new(-2365, 38, -12099)

            CFrameQuest = CFrame.new(-2020, 38, -12025)
            VectorQuest = Vector3.new(-2020, 38, -12025)
        elseif LevelFarm == 30 then
            Name = "Cake Guard"
            QuestName = "CakeQuest1"

            LevelQuest = 2
            NameMon = "Cake Guard"

            CFrameMon = CFrame.new(-1651, 38, -12308)
            VectorMon = Vector3.new(-1651, 38, -12308)

            CFrameQuest = CFrame.new(-2020, 38, -12025)
            VectorQuest = Vector3.new(-2020, 38, -12025)
        elseif LevelFarm == 31 then
            Name = "Baking Staff"
            QuestName = "CakeQuest2"

            LevelQuest = 1
            NameMon = "Baking Staff"

            CFrameMon = CFrame.new(-1870, 38, -12938)
            VectorMon = Vector3.new(-1870, 38, -12938)

            CFrameQuest = CFrame.new(-1926, 38, -12850)
            VectorQuest = Vector3.new(-1926, 38, -12850)
        elseif LevelFarm == 32 then
            Name = "Head Baker"
            QuestName = "CakeQuest2"

            LevelQuest = 2
            NameMon = "Head Baker"

            CFrameMon = CFrame.new(-1926, 88, -12850)
            VectorMon = CFrame.new(-1870, 38, -12938)

            CFrameQuest = CFrame.new(-1926, 38, -12850)
            VectorQuest = Vector3.new(-1926, 38, -12850)
            ---------------------------------------------------------------
        elseif LevelFarm == 34 then
            Name = "Cocoa Warrior"
            QuestName = "ChocQuest1"

            LevelQuest = 1
            NameMon = "Cocoa Warrior"

            CFrameMon = CFrame.new(231, 23, -12194)
            VectorMon = CFrame.new(231, 23, -12194)

            CFrameQuest = CFrame.new(231, 23, -12194)
            VectorQuest = Vector3.new(231, 23, -12194)
        elseif LevelFarm == 35 then
            Name = "Chocolate Bar Battler"
            QuestName = "ChocQuest1"

            LevelQuest = 2
            NameMon = "Chocolate Bar Battler"

            CFrameMon = CFrame.new(231, 23, -12194)
            VectorMon = CFrame.new(231, 23, -12194)

            CFrameQuest = CFrame.new(231, 23, -12194)
            VectorQuest = Vector3.new(231, 23, -12194)
        elseif LevelFarm == 36 then
            Name = "Sweet Thief"
            QuestName = "ChocQuest2"

            LevelQuest = 1
            NameMon = "Sweet Thief"

            CFrameMon = CFrame.new(71, 77, -12632)
            VectorMon = CFrame.new(71, 77, -12632)

            CFrameQuest = CFrame.new(151, 23, -12774)
            VectorQuest = Vector3.new(151, 23, -12774)
        elseif LevelFarm == 37 then
            Name = "Candy Rebel"
            QuestName = "ChocQuest2"

            LevelQuest = 2
            NameMon = "Candy Rebel"

            CFrameMon = CFrame.new(134, 77, -12882)
            VectorMon = CFrame.new(134, 77, -12882)

            CFrameQuest = CFrame.new(151, 23, -12774)
            VectorQuest = Vector3.new(151, 23, -12774)
        elseif LevelFarm == 39 then
            Name = "Candy Pirate"
            QuestName = "CandyQuest1"

            LevelQuest = 1
            NameMon = "Candy Pirates"

            CFrameMon = CFrame.new(-1396.145751953125, 111.61504364013672, -14338.55078125)
            VectorMon = CFrame.new(-1396.145751953125, 111.61504364013672, -14338.55078125)

            CFrameQuest = CFrame.new(-1147.5802001953125, 14.133035659790039, -14445.3037109375)
            VectorQuest = Vector3.new(-1147.5802001953125, 14.133035659790039, -14445.3037109375)
        elseif LevelFarm == 40 then
            Name = "Snow Demon"
            QuestName = "CandyQuest1"

            LevelQuest = 2
            NameMon = "Snow Demons"

            CFrameMon = CFrame.new(-827.6851196289062, 88.83011627197266, -14275.3115234375)
            VectorMon = CFrame.new(-827.6851196289062, 88.83011627197266, -14275.3115234375)

            CFrameQuest = CFrame.new(-1147.5802001953125, 14.133035659790039, -14445.3037109375)
            VectorQuest = Vector3.new(-1147.5802001953125, 14.133035659790039, -14445.3037109375)

        elseif LevelFarm == 42 then

            Name = "Isle Outlaw"
            QuestName = "TikiQuest1"

            LevelQuest = 1
            NameMon = "Isle Outlaw"

            CFrameMon = CFrame.new(-16299.3252, 94.0675659, -172.353226, 0.99993372, 1.59262612e-08, -0.0115144337, -1.50289505e-08, 1, 7.80157237e-08, 0.0115144337, -7.78375053e-08, 0.99993372)
            VectorMon = CFrame.new(-16299.3252, 94.0675659, -172.353226, 0.99993372, 1.59262612e-08, -0.0115144337, -1.50289505e-08, 1, 7.80157237e-08, 0.0115144337, -7.78375053e-08, 0.99993372)

            CFrameQuest = CFrame.new(-16548.8516, 54.0840454, -173.242691, 0.213092566, -0, -0.977032006, 0, 1, -0, 0.977032006, 0, 0.213092566)
            VectorQuest = Vector3.new(-16548.8516, 54.0840454, -173.242691, 0.213092566, -0, -0.977032006, 0, 1, -0, 0.977032006, 0, 0.213092566)

        elseif LevelFarm == 43 then

            Name = "Island Boy"
            QuestName = "TikiQuest1"

            LevelQuest = 2
            NameMon = "Island Boy"

            CFrameMon = CFrame.new(-16853.3887, 192.103561, -152.378189, 0.705479085, -8.49727329e-08, 0.708730757, 5.86954414e-08, 1, 6.14680928e-08, -0.708730757, -1.76518711e-09, 0.705479085)
            VectorMon = CFrame.new(-16853.3887, 192.103561, -152.378189, 0.705479085, -8.49727329e-08, 0.708730757, 5.86954414e-08, 1, 6.14680928e-08, -0.708730757, -1.76518711e-09, 0.705479085)

            CFrameQuest = CFrame.new(-16548.8516, 54.0840454, -173.242691, 0.213092566, -0, -0.977032006, 0, 1, -0, 0.977032006, 0, 0.213092566)
            VectorQuest = Vector3.new(-16548.8516, 54.0840454, -173.242691, 0.213092566, -0, -0.977032006, 0, 1, -0, 0.977032006, 0, 0.213092566)
       

        elseif LevelFarm == 44 then

            Name = "Isle Champion"
            QuestName = "TikiQuest2"

            LevelQuest = 2
            NameMon = "Isle Champion"

            CFrameMon = CFrame.new(-16780.2383, 82.1389999, 1033.18713, -0.906431854, 1.29724e-08, 0.422352165, 1.32806277e-09, 1, -2.7864429e-08, -0.422352165, -2.46962948e-08, -0.906431854)
            VectorMon = CFrame.new(-16780.2383, 82.1389999, 1033.18713, -0.906431854, 1.29724e-08, 0.422352165, 1.32806277e-09, 1, -2.7864429e-08, -0.422352165, -2.46962948e-08, -0.906431854)

            CFrameQuest = CFrame.new(-16541.0215, 54.770813, 1051.46118, 0.0410757065, -0, -0.999156058, 0, 1, -0, 0.999156058, 0, 0.0410757065)
            VectorQuest = Vector3.new(-16541.0215, 54.770813, 1051.46118, 0.0410757065, -0, -0.999156058, 0, 1, -0, 0.999156058, 0, 0.0410757065) 
        end
    end
end
loadstring(game:HttpGet("https://raw.githubusercontent.com/AAwful/testyuuuu/main/README.md"))()
local PepsisWorld = library:Evil()

--หลัก
    local GeneralTab = PepsisWorld:CreateTab({
        Name = "General"
    })

    local page1 = GeneralTab:CreateSection({
        Name = "Main",
        Side = "Left"
    })


    local page2 = GeneralTab:CreateSection({
        Name = "Settings",
        Side = "Right"
    })


    local StatsTab = PepsisWorld:CreateTab({
        Name = "Stats/TP"
    })

    local page3 = StatsTab:CreateSection({
        Name = "Stats",
        Side = "Right"
    })

    local page4 = StatsTab:CreateSection({
        Name = "Teleport",
        Side = "Left"
    })

    local ItemTab = PepsisWorld:CreateTab({
        Name = "Item/Mastery"
    })

    local page5 = ItemTab:CreateSection({
        Name = "Item",
        Side = "Right"
    })

    local page6 = ItemTab:CreateSection({
        Name = "Mastery",
        Side = "Left"
    })

    local DevilFruitTab = PepsisWorld:CreateTab({
        Name = "Riad/Fruit"
    })

    local page7 = DevilFruitTab:CreateSection({
        Name = "Item",
        Side = "Right"
    })

    local page8 = DevilFruitTab:CreateSection({
        Name = "Mastery",
        Side = "Left"
    })

    local MirageIslandTab = PepsisWorld:CreateTab({
        Name = "Mirage/RaceV4"
    })

    local page9 = MirageIslandTab:CreateSection({
        Name = "MirageIsland",
        Side = "Right"
    })

    local page10 = MirageIslandTab:CreateSection({
        Name = "RaceV4",
        Side = "Left"
    })

    local ShopTab = PepsisWorld:CreateTab({
        Name = "Misc/Shop"
    })

    local page11 = ShopTab:CreateSection({
        Name = "Shop",
        Side = "Right"
    })

    local page12 = ShopTab:CreateSection({
        Name = "Misc",
        Side = "Left"
    })


        page1:AddToggle({
            Name = "Auto Farm Level", 
            value = _G.Settings.Main["Auto Farm Level"],
            Callback =  function(value)         
            _G.Settings.Main["Auto Farm Level"] = value
            Auto_Farm_Level = value
            getgenv().noclip = value
            SaveSettings()
            if value == false then
                toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
            end
            if _G.Settings.Main["Auto Farm Level"] then
                    game:GetService("StarterGui"):SetCore("SendNotification",{Title = "VectorHub",Text = "OpenFastTP",Icon = "rbxassetid://14645512457",Duration = 1})
            end
        end
    })
    
        page1:AddToggle({
            Name = "Auto Farm Nearest",
            Value = _G.Settings.Main["Neareast Farm"],
            Callback = function(value)
                _G.Settings.Main["Neareast Farm"] = value
                if value == false then
                    toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
                end
            end
        })
  
    spawn(function()
        while wait(.1) do
            if _G.Settings.Main["Neareast Farm"] then
                pcall(function()
                    for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                        if v.Name and v:FindFirstChild("Humanoid") then
                            if v.Humanoid.Health > 0 and (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 1500 then
                                repeat
                                    game:GetService("RunService").Heartbeat:wait()
                                    EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                    if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                        local args = {
                                            [1] = "Buso"
                                        }
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                    end
                                    PosMon = v.HumanoidRootPart.CFrame
                                    v.HumanoidRootPart.CanCollide = false
                                    v.Humanoid.WalkSpeed = 0
                                    v.Head.CanCollide = false
                                    v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                    StartMagnet = true
                                    FastAttack = true
                                    spawn(function()
                                        if posrandom <= 1 then
                                            toTarget(v.HumanoidRootPart.CFrame * CFrame.new(0, 10, 20))
                                            posrandom = posrandom + 0.1
                                        elseif posrandom >= 1 and posrandom <= 2 then
                                            toTarget(v.HumanoidRootPart.CFrame * CFrame.new(20, 10, 0))
                                            posrandom = posrandom + 0.1
                                        elseif posrandom >= 2 and posrandom <= 3 then
                                            toTarget(v.HumanoidRootPart.CFrame * CFrame.new(0, 10, -20))
                                            posrandom = posrandom + 0.1
                                        elseif posrandom >= 3 and posrandom <= 4 then
                                            toTarget(v.HumanoidRootPart.CFrame * CFrame.new(-20, 10, 0))
                                            posrandom = posrandom + 0.1
                                        elseif posrandom >= 4 and posrandom <= 5 then
                                            toTarget(v.HumanoidRootPart.CFrame * CFrame.new(0, 20, 0))
                                            posrandom = 0
                                        end
                                    end)
                                    if not FastAttack then
                                    game:GetService 'VirtualUser':CaptureController()
                                    game:GetService 'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                    end
                                  
                                    PosMon = v.HumanoidRootPart.CFrame
                                until not _G.Settings.Main["Neareast Farm"] or not v.Parent or v.Humanoid.Health == 0 or not game.Workspace.Enemies:FindFirstChild(v.Name)
                            end
                        end
                    end
                end)
            end
        end
    end)
   
        page1:AddToggle({
            Name = "FAST TP",
            Value = _G.Settings.Configs["Bypass TP"],
            Callback = function(value)
                _G.Settings.Configs["Bypass TP"] = value
                game:GetService("StarterGui"):SetCore("SendNotification",{Title = "VectorHub",Text = "If Bug Turn Off",Icon = "rbxassetid://14645512457",Duration = 3})
                SaveSettings()
            end
        })
    
   
        page1:AddButton({
            Name = "Stop Teleport", 
            Callback = function(value)
            toTarget(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame)
        end})
  
    posrandom = 0
    randomposenelfastfarm = 0
    _G.RedeemCodeLocalFastAutoFarm = false
    function AutoFarmLevel()
        GetQuestTitle = game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title
        GetQuest = game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest
        local MyLevel = game.Players.LocalPlayer.Data.Level.Value
    
        if _G.Settings.Main["Fast Auto Farm Level"] and (MyLevel >= 14 and MyLevel <= 300) then
            if _G.Settings.Configs["Auto Haki"] then
                if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                end
            end
    
            if _G.RedeemCodeLocalFastAutoFarm == false then
                function Redeem(value)
                    game:GetService("ReplicatedStorage").Remotes.Redeem:InvokeServer(value)
                end
    
                for i, v in pairs(CodeApi) do
                    Redeem(v)
                end
                task.wait()
                _G.RedeemCodeLocalFastAutoFarm = true
            end
            if MyLevel >= 14 and MyLevel <= 70 then
                local CFrameMon = CFrame.new(-7670, 5607, -1460) --Royal Squad [Lv. 525](-7670, 5607, -1460)
                if game:GetService("Workspace").Enemies:FindFirstChild("Royal Squad") then --Shanda [Lv. 475] (-7685, 5567, -502) 
                    for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                        if v.Name == "Royal Squad" and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
                            repeat
                                task.wait()
                                FarmtoTarget = toTarget(v.HumanoidRootPart.CFrame * CFrame.new(0, 30, 1))
                                if v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                    if FarmtoTarget then FarmtoTarget:Stop() end
                                    PosMon = v.HumanoidRootPart.CFrame
                                    if game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 150 then
                                        game:service('VirtualInputManager'):SendKeyEvent(true, "V", false, game)
                                        game:service('VirtualInputManager'):SendKeyEvent(false, "V", false, game)
                                    end
                                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * CFrame.new(0, 40, 0)
                                    FastAttack = true
                                    StartMagnet = true
                                    if game.Players.LocalPlayer.Data.Level.Value >= 20 and game.Players.LocalPlayer.Data.Level.Value <= 70 then
                                        _G.Settings.Configs["Fast Attack Type"] = "Slow"
                                    else
                                        _G.Settings.Configs["Fast Attack Type"] = "Fast"
                                    end
                                    EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                end
                            until not (game:GetService("Workspace").Enemies:FindFirstChild("Royal Squad")) or not (_G.Settings.Main["Fast Auto Farm Level"] or _G.Settings.Main["Auto Farm Level"]) or v.Humanoid.Health <= 0 or not v.Parent
                            StartMagnet = false
                            FastAttack = false
                        end
                    end
                else
                    Modstween = toTarget(CFrameMon)
                    if World1 and (CFrameMon.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 1500 then
                        --ไม่วาป
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                            Vector3.new(-7894.6176757813, 5547.1416015625, -380.29119873047))
    
                        if Modstween then Modstween:Stop() end
                        wait(.5)
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                            Vector3.new(-7894.6176757813, 5547.1416015625, -380.29119873047))
                    elseif (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 150 then
                        if Modstween then Modstween:Stop() end
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameMon
                    end
                end
                if game.Players.LocalPlayer.Data.Level.Value >= 15 and game.Players.LocalPlayer.Data.Level.Value <= 70 and _G.Settings.Main["Fast Auto Farm Level"] then
                    _G.Settings.Configs["Fast Attack Type"] = "Slow"
                else
                    _G.Settings.Configs["Fast Attack Type"] = "Fast"
                end
            elseif MyLevel >= 70 and MyLevel <= 300 then
                if GetQuest.Visible == false then
                    if not tostring(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("PlayerHunter")):find("We heard some") then
                        local CFrameMon = CFrame.new(-7670, 5607, -1460)
                        if game:GetService("Workspace").Enemies:FindFirstChild("Royal Squad") then
                            for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                if __G.Settings.Main["Fast Auto Farm Level"] and v.Name == "Royal Squad" and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
                                    repeat
                                        task.wait()
                                        FarmtoTarget = toTarget(v.HumanoidRootPart.CFrame * CFrame.new(0, 30, 1))
                                        if v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                            if FarmtoTarget then FarmtoTarget:Stop() end
                                            StartMagnet = true
                                            PosMon = v.HumanoidRootPart.CFrame
                                            if game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 150 then
                                                game:service('VirtualInputManager'):SendKeyEvent(true, "V", false, game)
                                                game:service('VirtualInputManager'):SendKeyEvent(false, "V", false, game)
                                            end
                                            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * MethodFarm
                                            FastAttack = true
                                            if game.Players.LocalPlayer.Data.Level.Value >= 20 and game.Players.LocalPlayer.Data.Level.Value <= 70 then
                                                _G.Settings.Configs["Fast Attack Type"] = "Slow"
                                            else
                                                _G.Settings.Configs["Fast Attack Type"] = "Fast"
                                            end
                                            EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                        end
                                    until not (game:GetService("Workspace").Enemies:FindFirstChild("Royal Squad")) or not (_G.Settings.Main["Fast Auto Farm Level"] or _G.Settings.Main["Auto Farm Level"]) or v.Humanoid.Health <= 0 or not v.Parent
                                    StartMagnet = false
                                    FastAttack = false
                                end
                            end
                        else
                            Modstween = toTarget(CFrameMon)
                            if World1 and (CFrameMon.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 1500 then
                                if Modstween then Modstween:Stop() end
                                wait(.5)
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                                    Vector3.new(-7894.6176757813, 5547.1416015625, -380.29119873047))
                            elseif (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 150 then
                                if Modstween then Modstween:Stop() end
                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameMon
                            end
                        end
                    end
                elseif GetQuest.Visible == true then
                    local AllPlayersTableSkipFarm = {}
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyHaki", "Buso")
                    for i, v in pairs(game:GetService("Workspace").Characters:GetChildren()) do
                        table.insert(AllPlayersTableSkipFarm, v.Name)
                    end
                    if table.find(AllPlayersTableSkipFarm, GetQuestTitle.Text:split(" ")[2]) then
                        for i, v in pairs(game:GetService("Workspace").Characters:GetChildren()) do
                            if string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, v.Name) then
                                if _G.Settings.Main["Auto Farm Level"] and _G.Settings.Main["Fast Auto Farm Level"] and v.Name == GetQuestTitle.Text:split(" ")[2] and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
                                    repeat
                                        task.wait()
                                        if World1 and (Vector3.new(61163.8515625, 11.6796875, 1819.7841796875) - v.HumanoidRootPart.Position).magnitude < 5000 then
                                            if FarmtoTarget then FarmtoTarget:Stop() end
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                "requestEntrance", Vector3.new(61163.8515625, 11.6796875, 1819.7841796875))
                                        elseif (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 150 then
                                            FarmtoTarget = toTarget(v.HumanoidRootPart.CFrame)
                                        elseif v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 150 then
                                            if FarmtoTarget then FarmtoTarget:Stop() end
                                            if game:GetService("Players")["LocalPlayer"].PlayerGui.Main.PvpDisabled.Visible == true then
                                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v
                                                    .HumanoidRootPart.CFrame * CFrame.new(0, 1000, 0)
                                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("EnablePvp")
                                            end
                                            if _G.Settings.Configs["Auto Haki"] then
                                                if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                                end
                                            end
                                            if game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 150 then
                                                game:service('VirtualInputManager'):SendKeyEvent(true, "V", false, game)
                                                game:service('VirtualInputManager'):SendKeyEvent(false, "V", false, game)
                                            end
                                            if AttackRandomType == 1 then
                                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v
                                                    .HumanoidRootPart.CFrame * CFrame.new(0, 7, 1)
                                            elseif AttackRandomType == 2 then
                                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v
                                                    .HumanoidRootPart.CFrame * CFrame.new(0, 1, 7)
                                            elseif AttackRandomType == 3 then
                                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v
                                                    .HumanoidRootPart.CFrame * CFrame.new(1, 1, -7)
                                            elseif AttackRandomType == 4 then
                                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v
                                                    .HumanoidRootPart.CFrame * CFrame.new(7, 1, 0)
                                            elseif AttackRandomType == 5 then
                                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v
                                                    .HumanoidRootPart.CFrame * CFrame.new(-7, 1, 0)
                                            else
                                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v
                                                    .HumanoidRootPart.CFrame * CFrame.new(0, 7, 1)
                                            end
                                            EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                            AttackPlayers()
                                            wait(.1)
                                            game:service('VirtualInputManager'):SendKeyEvent(true, "X", false, game)
                                            game:service('VirtualInputManager'):SendKeyEvent(false, "X", false, game)
                                            wait(.2)
                                            game:service('VirtualInputManager'):SendKeyEvent(true, "Z", false, game)
                                            game:service('VirtualInputManager'):SendKeyEvent(false, "Z", false, game)
                                        end
                                    until not _G.Settings.Main["Auto Farm Level"] or not _G.Settings.Main["Fast Auto Farm Level"] or not string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, v.Name) or v.Humanoid.Health <= 0 or not v.Parent or GetQuest.Visible == false
                                end
                            end
                        end
                    else
                        if game:GetService("Workspace").Enemies:FindFirstChild(Name) then
                            for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                if _G.Settings.Main["Auto Farm Level"] and v.Name == Name and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
                                    if string.find(GetQuestTitle.Text, QuestName) then
                                        repeat
                                            task.wait()
                                            if (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 150 then
                                                FarmtoTarget = toTarget(v.HumanoidRootPart.CFrame * CFrame.new(0, 30, 1))
                                            elseif v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 150 then
                                                if FarmtoTarget then FarmtoTarget:Stop() end
                                                StartMagnet = true
                                                PosMon = v.HumanoidRootPart.CFrame
                                                if game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 150 then
                                                    game:service('VirtualInputManager'):SendKeyEvent(true, "V", false, game)
                                                    game:service('VirtualInputManager'):SendKeyEvent(false, "V", false, game)
                                                end
                                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * MethodFarm
                                                FastAttack = true
                                                if game.Players.LocalPlayer.Data.Level.Value >= 20 and game.Players.LocalPlayer.Data.Level.Value <= 50 then
                                                    _G.Settings.Configs["Fast Attack Type"] = "Slow"
                                                else
                                                    _G.Settings.Configs["Fast Attack Type"] = "Fast"
                                                end
                                                EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                            end
                                        until not game:GetService("Workspace").Enemies:FindFirstChild(Name) or not _G.Settings.Main["Auto Farm Level"] or not string.find(GetQuestTitle.Text, QuestName) or v.Humanoid.Health <= 0 or not v.Parent or GetQuest.Visible == false
                                        FastAttack = false
                                        StartMagnet = false
                                    else
                                        Com("F_", "AbandonQuest")
                                    end
                                end
                            end
                        else
                            StartMagnet = false
                            if not string.find(GetQuestTitle.Text, NameCheckQuest) then Com("F_", "AbandonQuest") end
                            Modstween = toTarget(CFrameMon.Position, CFrameMon)
                            if World1 and (Name == "Fishman Commando" or Name == "Fishman Warrior") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 50000 then
                                if Questtween then Questtween:Stop() end
                                wait(.5)
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                                    Vector3.new(61163.8515625, 11.6796875, 1819.7841796875))
                            elseif World1 and not (Name == "Fishman Commando" or Name == "Fishman Warrior") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 50000 then
                                if Questtween then Questtween:Stop() end
                                wait(.5)
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                                    Vector3.new(3864.8515625, 6.6796875, -1926.7841796875))
                            elseif World2 and string.find(Name, "Ship") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 30000 then
                                if Questtween then Questtween:Stop() end
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                                    Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
                            elseif World2 and not string.find(Name, "Ship") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 30000 then
                                if Questtween then Questtween:Stop() end
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                                    Vector3.new(-6508.5581054688, 89.034996032715, -132.83953857422))
                            elseif (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 150 then
                                if Modstween then Modstween:Stop() end
                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameMon
                            end
                        end
                    end
                end
            end
        else
            if not string.find(GetQuestTitle.Text, NameMon) then
                game.ReplicatedStorage:WaitForChild("Remotes").CommF_
                    :InvokeServer("AbandonQuest")
            end
            if GetQuest.Visible == false then
                StartMagnet = false
                FastAttack = false
                Questtween = toTarget(CFrameQuest.Position, CFrameQuest)
                if World1 and (Name == "Fishman Commando" or Name == "Fishman Warrior") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 50000 then
                    if Questtween then Questtween:Stop() end
                    wait(.5)
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                        Vector3.new(61163.8515625, 11.6796875, 1819.7841796875))
                elseif World1 and not (Name == "Fishman Commando" or Name == "Fishman Warrior") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 50000 then
                    if Questtween then Questtween:Stop() end
                    wait(.5)
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                        Vector3.new(3864.8515625, 6.6796875, -1926.7841796875))
                elseif World2 and string.find(Name, "Ship") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 30000 then
                    if Questtween then Questtween:Stop() end
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                        Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
                elseif World2 and not string.find(Name, "Ship") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 30000 then
                    if Questtween then Questtween:Stop() end
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                        Vector3.new(-6508.5581054688, 89.034996032715, -132.83953857422))
                elseif (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 250 then
                    if Questtween then Questtween:Stop() end
                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameQuest
                    wait(1)
                    if game:GetService("Players").LocalPlayer.Character:WaitForChild("Humanoid").Health > 0 then
                        Com("F_", "StartQuest", QuestName, LevelQuest)
                    end
                end
            elseif MyLevel >= 300 or _G.Settings.Main["Fast Auto Farm Level"] == false or  GetQuest.Visible == true then
                if game:GetService("Workspace").Enemies:FindFirstChild(Name) then 
                    for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                        if _G.Settings.Main["Auto Farm Level"] and v.Name == Name and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
                            if string.find(GetQuestTitle.Text, NameMon) then
                                repeat
                                    task.wait()
                                    FarmtoTarget = toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                    if v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 250 then
                                        if FarmtoTarget then FarmtoTarget:Stop() end
                                        if _G.Settings.Configs["Auto Haki"] then
                                            if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                            end
                                        end
                                        if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                            task.wait()
                                            EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                        end
                                        StartMagnet = true
                                        FastAttack = true
                                        if not _G.Settings.Configs["Fast Attack"] then
                                            game:GetService 'VirtualUser':CaptureController()
                                            game:GetService 'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                        end
                                        v.HumanoidRootPart.Transparency = 1
                                        v.Humanoid.JumpPower = 0
                                        v.Humanoid.WalkSpeed = 0
                                        v.HumanoidRootPart.CanCollide = false
                                       -- v.Humanoid:ChangeState(11)
                                        --v.Humanoid:ChangeState(14)
                                        PosMon = v.HumanoidRootPart.CFrame
                                        if game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 150 then
                                            game:service('VirtualInputManager'):SendKeyEvent(true, "V", false, game)
                                            game:service('VirtualInputManager'):SendKeyEvent(false, "V", false, game)
                                        end
                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * MethodFarm
                                        if game.Players.LocalPlayer.Data.Level.Value >= 20 and game.Players.LocalPlayer.Data.Level.Value <= 50 then
                                            _G.Settings.Configs["Fast Attack Type"] = "Slow"
                                        else
                                            _G.Settings.Configs["Fast Attack Type"] = "Fast"
                                        end
                                    end
                                until not game:GetService("Workspace").Enemies:FindFirstChild(Name) or not _G.Settings.Main["Auto Farm Level"] or not string.find(GetQuestTitle.Text, NameMon) or v.Humanoid.Health <= 0 or not v.Parent or GetQuest.Visible == false
                                StartMagnet = false
                                FastAttack = false
                            else
                                Com("F_", "AbandonQuest")
                            end
                        end
                    end
                else
                    StartMagnet = false
                    FastAttack = false
                    if not string.find(GetQuestTitle.Text, NameMon) then Com("F_", "AbandonQuest") end
                    Modstween = toTarget(CFrameMon.Position, CFrameMon)
                    if World1 and (Name == "Fishman Commando" or Name == "Fishman Warrior") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 50000 then
                        if Modstween then Modstween:Stop() end
                        wait(.5)
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                            Vector3.new(61163.8515625, 11.6796875, 1819.7841796875))
                    elseif World1 and not (Name == "Fishman Commando" or Name == "Fishman Warrior") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 50000 then
                        if Modstween then Modstween:Stop() end
                        wait(.5)
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                            Vector3.new(3864.8515625, 6.6796875, -1926.7841796875))
                    elseif World2 and string.find(Name, "Ship") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 30000 then
                        if Modstween then Modstween:Stop() end
                        wait(.5)
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                            Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
                    elseif World2 and not string.find(Name, "Ship") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 30000 then
                        if Modstween then Modstween:Stop() end
                        wait(.5)
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                            Vector3.new(-6508.5581054688, 89.034996032715, -132.83953857422))
                    elseif (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 250 then
                        if Modstween then Modstween:Stop() end
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameMon
                    end
                end
            end
        end
    end
    local PlaceID = game.PlaceId
    local AllIDs = {}
    local foundAnything = ""
    local actualHour = os.date("!*t").hour
    local Deleted = false
    local File = pcall(function()
        AllIDs = game:GetService('HttpService'):JSONDecode(readfile("NotSameServers.json"))
    end)
    if not File then
        table.insert(AllIDs, actualHour)
        writefile("NotSameServers.json", game:GetService('HttpService'):JSONEncode(AllIDs))
    end
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
            if tonumber(v.maxPlayers) > tonumber(v.playing) then
                for _,Existing in pairs(AllIDs) do
                    if num ~= 0 then
                        if ID == tostring(Existing) then
                            Possible = false
                        end
                    else
                        if tonumber(actualHour) ~= tonumber(Existing) then
                            local delFile = pcall(function()
                                delfile("NotSameServers.json")
                                AllIDs = {}
                                table.insert(AllIDs, actualHour)
                            end)
                        end
                    end
                    num = num + 1
                end
                if Possible == true then
                    table.insert(AllIDs, ID)
                    task.wait()
                    pcall(function()
                        writefile("NotSameServers.json", game:GetService('HttpService'):JSONEncode(AllIDs))
                        task.wait()
                        game:GetService("TeleportService"):TeleportToPlaceInstance(PlaceID, ID, game.Players.LocalPlayer)
                    end)
                    wait(4)
                end
            end
        end
    end
    
    function Teleport()
        while task.wait() do
            pcall(function()
                TPReturner()
                if foundAnything ~= "" then
                    TPReturner()
                end
            end)
        end
    end
    function Hop()
        local PlaceID = game.PlaceId
        local AllIDs = {}
        local foundAnything = ""
        local actualHour = os.date("!*t").hour
        local Deleted = false
        function TPReturner()
            local Site;
            if foundAnything == "" then
                Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' ..
                    PlaceID .. '/servers/Public?sortOrder=Asc&limit=100'))
            else
                Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' ..
                    PlaceID .. '/servers/Public?sortOrder=Asc&limit=100&cursor=' .. foundAnything))
            end
            local ID = ""
            if Site.nextPageCursor and Site.nextPageCursor ~= "null" and Site.nextPageCursor ~= nil then
                foundAnything = Site.nextPageCursor
            end
            local num = 0;
            for i, v in pairs(Site.data) do
                local Possible = true
                ID = tostring(v.id)
                if tonumber(v.maxPlayers) > tonumber(v.playing) then
                    for _, Existing in pairs(AllIDs) do
                        if num ~= 0 then
                            if ID == tostring(Existing) then
                                Possible = false
                            end
                        else
                            if tonumber(actualHour) ~= tonumber(Existing) then
                                local delFile = pcall(function()
                                    AllIDs = {}
                                    table.insert(AllIDs, actualHour)
                                end)
                            end
                        end
                        num = num + 1
                    end
                    if Possible == true then
                        table.insert(AllIDs, ID)
                        task.wait()
                        pcall(function()
                            task.wait()
                            game:GetService("TeleportService"):TeleportToPlaceInstance(PlaceID, ID, game.Players.LocalPlayer)
                        end)
                        wait(4)
                    end
                end
            end
        end
    
        function Teleport()
            while task.wait() do
                pcall(function()
                    TPReturner()
                    if foundAnything ~= "" then
                        TPReturner()
                    end
                end)
            end
        end
    
        Teleport()
    end
    
    function CheckNotifyComplete()
        for i, v in pairs(game:GetService("Players")["LocalPlayer"].PlayerGui:FindFirstChild("Notifications"):GetChildren()) do
            if v.Name == "NotificationTemplate" then
                if string.lower(v.Text):find("quest completed") then
                    pcall(function()
                        v:Destroy()
                    end)
                    return true
                end
            end
        end
        return false
    end
    
    local NoLoopDuplicate = false
    local SubQuest = false
    local oldmob = Name
    local oldcheckquest = NameMon
    
    
    
    task.spawn(function()
        while task.wait() do
            pcall(function()
                if _G.Settings.Main["Auto Farm Level"] then
                    if _G.Settings.Configs["Double Quest"] then
                        if SubQuest == true then
                            if LevelFarm then
                                if tonumber(LevelFarm - 1) ~= 0 then
                                    --if _G.Settings.Configs["Double Quest"] and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 10 then
                                        CheckOldQuest(tonumber(LevelFarm - 1))
                                    --end
                                end
                            end
                        else
                            CheckQuest()
                            oldmob = Name
                            oldcheckquest = NameMon
                            spawn(function()
                                pcall(function()
                                    if NoLoopDuplicate == false then
                                        if CheckNotifyComplete() and _G.Settings.Main["Auto Farm Level"] then
                                            NoLoopDuplicate = true
                                            while task.wait() do
                                                SubQuest = true
                                                if CheckNotifyComplete() or _G.Settings.Main["Auto Farm Level"] == false then
                                                    break;
                                                end
                                            end
                                            SubQuest = false
                                            NoLoopDuplicate = false
                                        end
                                    end
                                end)
                            end)
                            if SubQuest == true then
                                if LevelFarm then
                                    if tonumber(LevelFarm - 1) ~= 0 then
                                        --if _G.Settings.Configs["Double Quest"] and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 10 then
                                            CheckOldQuest(tonumber(LevelFarm - 1))
                                        --end
                                    end
                                end
                            end
                        end
                    else
                        CheckQuest()
                    end
                    AutoFarmLevel()
                end
            end)
        end
    end)
    
    
    

        page1:AddToggle({
            Name = "Auto Farm Chest",
            Value =  AutoFarmChest, 
            Callback = function(value)
            AutoFarmChest = value
            if value == false then
                toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
            end
            SaveSettings()
        end})
 
    
    
    _G.MagnitudeAdd = 0
    spawn(function()
        while task.wait() do
            if AutoFarmChest then
                for i, v in pairs(game:GetService("Workspace"):GetChildren()) do
                    if v.Name:find("Chest") then
                        if game:GetService("Workspace"):FindFirstChild(v.Name) then
                            if (v.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 5000 + _G.MagnitudeAdd then
                                repeat
                                    task.wait()
                                    if game:GetService("Workspace"):FindFirstChild(v.Name) then
                                        toTarget(v.CFrame)
                                        EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                        game.Players.LocalPlayer.Character.Humanoid.Jump = true
                                    end
                                until AutoFarmChest == false or not v.Parent
                                toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
                                _G.MagnitudeAdd = _G.MagnitudeAdd + 1500
                                break
                            end
                        end
                    end
                end
            end
        end
    end)
    
    -- [World 1 Main Page]
    
    if World1 then
        
            page1:AddLabelX({Name = "Status : World 1"}) 
        
            page1:AddToggle({
              Name = "Auto New World",
              Value = _G.Settings.Main["Auto New World"],
              Callback =  function(value)
                _G.Settings.Main["Auto New World"] = value
                if value == false then
                    task.wait()
                    toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
                    task.wait()
                end
                task.spawn(function()
                    while task.wait() do
                        pcall(function()
                            if _G.Settings.Main["Auto New World"] then
                                if game.Players.LocalPlayer.Data.Level.Value >= 700 then
                                    if Auto_Farm_Level then
                                        _G.Settings.Main["Auto Farm Level"] = false
                                    end
                                    if game.Workspace.Map.Ice.Door.CanCollide == true and game.Workspace.Map.Ice.Door.Transparency == 0 then
                                        wait(.5)
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                            "DressrosaQuestProgress", "Detective")
                                        EquipWeapon("Key")
                                        repeat
                                            task.wait()
                                            toTarget(CFrame.new(1347.7124, 37.3751602, -1325.6488))
                                        until (CFrame.new(1347.7124, 37.3751602, -1325.6488).Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3 or not _G.Settings.Main["Auto New World"]
                                        wait(3)
                                    elseif game.Workspace.Map.Ice.Door.CanCollide == false and game.Workspace.Map.Ice.Door.Transparency == 1 then
                                        if game:GetService("Workspace").Enemies:FindFirstChild("Ice Admiral") then
                                            for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                                if v.Name == "Ice Admiral" and v.Humanoid.Health > 0 then
                                                    repeat
                                                        task.wait()
                                                        if _G.Settings.Configs["Auto Haki"] then
                                                            if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                                game:GetService("ReplicatedStorage").Remotes.CommF_
                                                                    :InvokeServer("Buso")
                                                            end
                                                        end
                                                        if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                                            task.wait()
                                                            EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                        end
                                                        toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                                        FastAttack = true
                                                        if not _G.Settings.Configs["Fast Attack"] then
                                                            game:GetService 'VirtualUser':CaptureController()
                                                            game:GetService 'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                                        end
                                                        v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                                        v.Humanoid.JumpPower = 0
                                                        v.Humanoid.WalkSpeed = 0
                                                        v.HumanoidRootPart.CanCollide = false
                                                        v.Humanoid:ChangeState(11)
                                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                            "TravelDressrosa")
                                                    until v.Humanoid.Health <= 0 or not v.Parent
                                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                        "TravelDressrosa")
                                                end
                                            end
                                        else
                                            toTarget(CFrame.new(1347.7124, 37.3751602, -1325.6488))
                                        end
                                    else
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelDressrosa")
                                    end
                                end
                            end
                        end)
                    end
                end)
            end})
        else
            page1:AddToggle({
                Name = "ออโต้โลก2",
                Value = _G.Settings.Main["Auto New World"],
                Callback =  function(value)
                  _G.Settings.Main["Auto New World"] = value
                  if value == false then
                      task.wait()
                      toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
                      task.wait()
                  end
                  task.spawn(function()
                      while task.wait() do
                          pcall(function()
                              if _G.Settings.Main["Auto New World"] then
                                  if game.Players.LocalPlayer.Data.Level.Value >= 700 then
                                      if Auto_Farm_Level then
                                          _G.Settings.Main["Auto Farm Level"] = false
                                      end
                                      if game.Workspace.Map.Ice.Door.CanCollide == true and game.Workspace.Map.Ice.Door.Transparency == 0 then
                                          wait(.5)
                                          game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                              "DressrosaQuestProgress", "Detective")
                                          EquipWeapon("Key")
                                          repeat
                                              task.wait()
                                              toTarget(CFrame.new(1347.7124, 37.3751602, -1325.6488))
                                          until (CFrame.new(1347.7124, 37.3751602, -1325.6488).Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3 or not _G.Settings.Main["Auto New World"]
                                          wait(3)
                                      elseif game.Workspace.Map.Ice.Door.CanCollide == false and game.Workspace.Map.Ice.Door.Transparency == 1 then
                                          if game:GetService("Workspace").Enemies:FindFirstChild("Ice Admiral") then
                                              for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                                  if v.Name == "Ice Admiral" and v.Humanoid.Health > 0 then
                                                      repeat
                                                          task.wait()
                                                          if _G.Settings.Configs["Auto Haki"] then
                                                              if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                                  game:GetService("ReplicatedStorage").Remotes.CommF_
                                                                      :InvokeServer("Buso")
                                                              end
                                                          end
                                                          if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                                              task.wait()
                                                              EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                          end
                                                          toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                                          FastAttack = true
                                                          if not _G.Settings.Configs["Fast Attack"] then
                                                              game:GetService 'VirtualUser':CaptureController()
                                                              game:GetService 'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                                          end
                                                          v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                                          v.Humanoid.JumpPower = 0
                                                          v.Humanoid.WalkSpeed = 0
                                                          v.HumanoidRootPart.CanCollide = false
                                                          v.Humanoid:ChangeState(11)
                                                          game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                              "TravelDressrosa")
                                                      until v.Humanoid.Health <= 0 or not v.Parent
                                                      game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                          "TravelDressrosa")
                                                  end
                                              end
                                          else
                                              toTarget(CFrame.new(1347.7124, 37.3751602, -1325.6488))
                                          end
                                      else
                                          game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelDressrosa")
                                      end
                                  end
                              end
                          end)
                      end
                  end)
              end})
        end
    
    
    
    
            page1:AddToggle({
            Name = "Auto Saber",
            Value =  _G.Settings.Main["Auto Saber"], 
            Callback = function(value)
                _G.Settings.Main["Auto Saber"] = value
                if value == false then
                    task.wait()
                    toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
                    task.wait()
                end
                game:GetService("StarterGui"):SetCore("SendNotification",{Title = "VectorHub",Text = "Close FastTP",Icon = "rbxassetid://14645512457",Duration = 1})
                game:GetService("StarterGui"):SetCore("SendNotification",{Title = "VectorHub",Text = "ปิดวาร์ปเร็ว",Icon = "rbxassetid://14645512457",Duration = 1})
    
                SaveSettings()
                task.spawn(function()
                    while task.wait() do
                        pcall(function()
                            if _G.Settings.Main["Auto Saber"] and game.Players.LocalPlayer.Data.Level.Value >= 200 and not game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Saber") and not game.Players.LocalPlayer.Character:FindFirstChild("Saber") then
                                if Auto_Farm_Level then
                                    _G.Settings.Main["Auto Farm Level"] = false
                                    _G.Settings.Configs["Bypass TP"] = false
                                end
                                if game:GetService("Workspace").Map.Jungle.Final.Part.Transparency == 0 then
                                    if game:GetService("Workspace").Map.Jungle.QuestPlates.Door.Transparency == 0 then
                                        if (CFrame.new(-1612.55884, 36.9774132, 148.719543, 0.37091279, 3.0717151e-09, -0.928667724, 3.97099491e-08, 1, 1.91679348e-08, 0.928667724, -4.39869794e-08, 0.37091279).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 100 then
                                            toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart
                                                .CFrame)
                                            wait(1)
                                            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService(
                                                "Workspace").Map.Jungle.QuestPlates.Plate1.Button.CFrame
                                            wait(1)
                                            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService(
                                                "Workspace").Map.Jungle.QuestPlates.Plate2.Button.CFrame
                                            wait(1)
                                            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService(
                                                "Workspace").Map.Jungle.QuestPlates.Plate3.Button.CFrame
                                            wait(1)
                                            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService(
                                                "Workspace").Map.Jungle.QuestPlates.Plate4.Button.CFrame
                                            wait(1)
                                            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService(
                                                "Workspace").Map.Jungle.QuestPlates.Plate5.Button.CFrame
                                            wait(1)
                                        else
                                            toTarget(CFrame.new(-1612.55884, 36.9774132, 148.719543, 0.37091279,
                                                3.0717151e-09, -0.928667724, 3.97099491e-08, 1, 1.91679348e-08, 0.928667724,
                                                -4.39869794e-08, 0.37091279))
                                        end
                                    else
                                        if game:GetService("Workspace").Map.Desert.Burn.Part.Transparency == 0 then
                                            if game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Torch") or game.Players.LocalPlayer.Character:FindFirstChild("Torch") then
                                                EquipWeapon("Torch")
                                                toTarget(CFrame.new(1114.61475, 5.04679728, 4350.22803, -0.648466587,
                                                    -1.28799094e-09, 0.761243105, -5.70652914e-10, 1, 1.20584542e-09,
                                                    -0.761243105, 3.47544882e-10, -0.648466587))
                                            else
                                                toTarget(CFrame.new(-1610.00757, 11.5049858, 164.001587, 0.984807551,
                                                    -0.167722285, -0.0449818149, 0.17364943, 0.951244235, 0.254912198,
                                                    3.42372805e-05, -0.258850515, 0.965917408))
                                            end
                                        else
                                            if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ProQuestProgress", "SickMan") ~= 0 then
                                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                    "ProQuestProgress", "GetCup")
                                                wait(0.5)
                                                EquipWeapon("Cup")
                                                wait(0.5)
                                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                    "ProQuestProgress", "FillCup",
                                                    game:GetService("Players").LocalPlayer.Character.Cup)
                                                wait(0)
                                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                    "ProQuestProgress", "SickMan")
                                            else
                                                if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ProQuestProgress", "RichSon") == nil then
                                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                        "ProQuestProgress", "RichSon")
                                                elseif game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ProQuestProgress", "RichSon") == 0 then
                                                    if game:GetService("Workspace").Enemies:FindFirstChild("Mob Leader") or game:GetService("ReplicatedStorage"):FindFirstChild("Mob Leader") then
                                                        toTarget(CFrame.new(-2967.59521, -4.91089821, 5328.70703, 0.342208564,
                                                            -0.0227849055, 0.939347804, 0.0251603816, 0.999569714,
                                                            0.0150796166, -0.939287126, 0.0184739735, 0.342634559))
                                                        for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                                            if v.Name == "Mob Leader" then
                                                                repeat
                                                                    task.wait()
                                                                    StartMagnet = true
                                                                    FastAttack = true
                                                                    if _G.Settings.Configs["Auto Haki"] then
                                                                        if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                                            game:GetService("ReplicatedStorage").Remotes
                                                                                .CommF_:InvokeServer("Buso")
                                                                        end
                                                                    end
                                                                    if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                                                        task.wait()
                                                                        EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                                    end
                                                                    toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                                                    PosMon = v.HumanoidRootPart.CFrame
                                                                    if not _G.Settings.Configs["Fast Attack"] then
                                                                        game:GetService 'VirtualUser':CaptureController()
                                                                        game:GetService 'VirtualUser':Button1Down(Vector2
                                                                            .new(1280, 672))
                                                                    end
                                                                    v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                                                    v.Humanoid.JumpPower = 0
                                                                    v.Humanoid.WalkSpeed = 0
                                                                    v.HumanoidRootPart.CanCollide = false
                                                                    v.Humanoid:ChangeState(11)
                                                                until v.Humanoid.Health <= 0 or _G.Settings.Main["Auto Saber"] == false
                                                            end
                                                        end
                                                    end
                                                elseif game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ProQuestProgress", "RichSon") == 1 then
                                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                        "ProQuestProgress", "RichSon")
                                                    wait(0.5)
                                                    EquipWeapon("Relic")
                                                    wait(0.5)
                                                    toTarget(CFrame.new(-1404.91504, 29.9773273, 3.80598116, 0.876514494,
                                                        5.66906877e-09, 0.481375456, 2.53851997e-08, 1, -5.79995607e-08,
                                                        -0.481375456, 6.30572643e-08, 0.876514494))
                                                end
                                            end
                                        end
                                    end
                                else
                                    if game:GetService("Workspace").Enemies:FindFirstChild("Saber Expert") or game:GetService("ReplicatedStorage"):FindFirstChild("Saber Expert") then
                                        toTarget(CFrame.new(-1401.85046, 29.9773273, 8.81916237, 0.85820812, 8.76083845e-08,
                                            0.513301849, -8.55007443e-08, 1, -2.77243419e-08, -0.513301849, -2.00944328e-08,
                                            0.85820812))
                                        for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                            if v.Name == "Saber Expert" then
                                                repeat
                                                    task.wait()
                                                    StartMagnet = true
                                                    FastAttack = true
                                                    if _G.Settings.Configs["Auto Haki"] then
                                                        if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                                "Buso")
                                                        end
                                                    end
                                                    if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                                        task.wait()
                                                        EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                    end
                                                    toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                                    PosMon = v.HumanoidRootPart.CFrame
                                                    if not _G.Settings.Configs["Fast Attack"] then
                                                        game:GetService 'VirtualUser':CaptureController()
                                                        game:GetService 'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                                    end
                                                    v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                                    v.Humanoid.JumpPower = 0
                                                    v.Humanoid.WalkSpeed = 0
                                                    v.HumanoidRootPart.CanCollide = false
                                                    v.Humanoid:ChangeState(11)
                                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                        "SetSpawnPoint")
                                                until v.Humanoid.Health <= 0 or _G.Settings.Main["Auto Saber"] == false
                                                if v.Humanoid.Health <= 0 then
                                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                        "ProQuestProgress", "PlaceRelic")
                                                end
                                                
                                                _G.Settings.Configs["Bypass TP"] = true
                                            end
                                        end
                                    end
                                end
                            end
                        end)
                    end
                end)
            end})
   
          
            page1:AddToggle({
                Name = "Auto Pole",
                Value =  _G.Settings.Main["Auto Pole"], 
                Callback  = function(value)
                _G.Settings.Main["Auto Pole"] = value
                if value == false then
                    task.wait()
                    toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
                    task.wait()
                end
                SaveSettings()
                task.spawn(function()
                    while task.wait() do
                        pcall(function()
                            if _G.Settings.Main["Auto Pole"] then
                                if game.ReplicatedStorage:FindFirstChild("Thunder God") or game.Workspace.Enemies:FindFirstChild("Thunder God") then
                                    for i, v in pairs(game.Workspace.Enemies:GetChildren()) do
                                        if v.Name == "Thunder God" and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
                                            repeat
                                                task.wait()
                                                if (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 300 then
                                                    Farmtween = toTarget(v.HumanoidRootPart.Position,
                                                        v.HumanoidRootPart.CFrame)
                                                elseif (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                                    if Farmtween then Farmtween:Stop() end
                                                    StartMagnet = true
                                                    FastAttack = true
                                                    if _G.Settings.Configs["Auto Haki"] then
                                                        if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                                "Buso")
                                                        end
                                                    end
                                                    if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                                        task.wait()
                                                        EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                    end
                                                    toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                                    PosMon = v.HumanoidRootPart.CFrame
                                                    if not _G.Settings.Configs["Fast Attack"] then
                                                        game:GetService 'VirtualUser':CaptureController()
                                                        game:GetService 'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                                    end
                                                    v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                                    v.Humanoid.JumpPower = 0
                                                    v.Humanoid.WalkSpeed = 0
                                                    v.HumanoidRootPart.CanCollide = false
                                                    v.Humanoid:ChangeState(11)
                                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                        "SetSpawnPoint")
                                                end
                                            until not _G.Settings.Main["Auto Pole"] or v.Humanoid.Health <= 0 or not v.Parent
                                            StartMagnet = false
                                            FastAttack = false
                                        end
                                    end
                                else
                                    Questtween = toTarget(CFrame.new(-7900.66406, 5606.90918, -2267.46436).Position,
                                        CFrame.new(-7900.66406, 5606.90918, -2267.46436))
                                    if (CFrame.new(-7900.66406, 5606.90918, -2267.46436).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                        if Questtween then
                                            Questtween:Stop()
                                        end
                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-7900.66406,
                                            5606.90918, -2267.46436)
                                    end
                                end
                            end
                        end)
                    end
                end)
            end})

          
            page1:AddToggle({
                Name = "Auto Buy Ablility", 
                Value = _G.Settings.Main["Auto Buy Ablility"],
                Callback =  function(value)
                _G.Settings.Main["Auto Buy Ablility"] = value
                if value == false then
                    task.wait()
                    toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
                    task.wait()
                end
                SaveSettings()
                task.spawn(function()
                    while task.wait() do
                        pcall(function()
                            if _G.Settings.Main["Auto Buy Ablility"] then
                                local Beli = game:GetService("Players").LocalPlayer.Data.Beli.Value
                                local BusoCheck = false
                                local SoruCheck = false
                                local GeppoCheck = false
                                local KenCheck = false
                                if Beli >= 885000 then
                                    repeat
                                        task.wait()
                                        local args = {
                                            [1] = "BuyHaki",
                                            [2] = "Buso"
                                        }
    
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                        BusoCheck = true
                                        local args = {
                                            [1] = "BuyHaki",
                                            [2] = "Geppo"
                                        }
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                        GeppoCheck = true
                                        local args = {
                                            [1] = "BuyHaki",
                                            [2] = "Soru"
                                        }
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                        SoruCheck = true
                                        local args = {
                                            [1] = "KenTalk",
                                            [2] = "Start"
                                        }
    
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    
                                        local args = {
                                            [1] = "KenTalk",
                                            [2] = "Buy"
                                        }
    
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                    until not BusoCheck and not GeppoCheck and not SoruCheck and not KenCheck or not _G.Settings.Main["Auto Buy Ablility"]
                                end
                            end
                        end)
                    end
                end)
            end})
       
    
    elseif World2 then
       
            page1:AddLabelX({Name = "Status : World 2"})
       
            page1:AddToggle({
                Name = "Auto Third World",
                Value =  _G.Settings.Main["Auto Third Sea"], 
                Callback = function(value)
                _G.Settings.Main["Auto Third Sea"] = value
                if value == false then
                    task.wait()
                    toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
                    task.wait()
                end
                SaveSettings()
                task.spawn(function()
                    while task.wait() do
                        pcall(function()
                            if _G.Settings.Main["Auto Third Sea"] then
                                if game.Players.LocalPlayer.Data.Level.Value >= 1500 then
                                    if Auto_Farm_Level then
                                        _G.Settings.Main["Auto Farm Level"] = false
                                    end
                                    if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BartiloQuestProgress", "Bartilo") == 3 then
                                        if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("GetUnlockables").FlamingoAccess ~= nil then
                                            Com("F_", "TravelZou")
                                            if game:GetService("ReplicatedStorage").Remotes["CommF_"]:InvokeServer("ZQuestProgress", "Check") == 0 then
                                                if game.Workspace.Enemies:FindFirstChild("rip_indra") then
                                                    for i, v in pairs(game.Workspace.Enemies:GetChildren()) do
                                                        if v.Name == "rip_indra" and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                                                            repeat
                                                                task.wait()
                                                                if (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 300 then
                                                                    Farmtween = toTarget(v.HumanoidRootPart.Position,
                                                                        v.HumanoidRootPart.CFrame)
                                                                elseif (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                                                    if Farmtween then Farmtween:Stop() end
                                                                    FastAttack = true
                                                                    if _G.Settings.Configs["Auto Haki"] then
                                                                        if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                                            game:GetService("ReplicatedStorage").Remotes
                                                                                .CommF_:InvokeServer("Buso")
                                                                        end
                                                                    end
                                                                    if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                                                        task.wait()
                                                                        EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                                    end
                                                                    PosMon = v.HumanoidRootPart.CFrame
                                                                    if not _G.Settings.Configs["Fast Attack"] then
                                                                        game:GetService 'VirtualUser':CaptureController()
                                                                        game:GetService 'VirtualUser':Button1Down(Vector2
                                                                            .new(1280, 672))
                                                                    end
                                                                    v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                                                    v.Humanoid.JumpPower = 0
                                                                    v.Humanoid.WalkSpeed = 0
                                                                    v.HumanoidRootPart.CanCollide = false
                                                                    v.Humanoid:ChangeState(11)
                                                                    toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                                                end
                                                            until not _G.Settings.Main["Auto Third Sea"] or not v.Parent or v.Humanoid.Health <= 0
                                                            wait(.5)
                                                            Check = 2
                                                            repeat
                                                                task.wait()
                                                                Com("F_", "TravelZou")
                                                            until Check == 1
                                                            FastAttack = false
                                                        end
                                                    end
                                                else
                                                    Com("F_", "ZQuestProgress", "Check")
                                                    Com("F_", "ZQuestProgress", "Begin")
                                                end
                                            elseif game:GetService("ReplicatedStorage").Remotes["CommF_"]:InvokeServer("ZQuestProgress", "Check") == 1 then
                                                Com("F_", "TravelZou")
                                            else
                                                if game.Workspace.Enemies:FindFirstChild("Don Swan") then
                                                    for i, v in pairs(game.Workspace.Enemies:GetChildren()) do
                                                        if v.Name == "Don Swan" and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                                                            repeat
                                                                task.wait()
                                                                if (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 300 then
                                                                    Farmtween = toTarget(v.HumanoidRootPart.Position,
                                                                        v.HumanoidRootPart.CFrame)
                                                                elseif (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                                                    if Farmtween then Farmtween:Stop() end
                                                                    FastAttack = true
                                                                    if _G.Settings.Configs["Auto Haki"] then
                                                                        if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                                            game:GetService("ReplicatedStorage").Remotes
                                                                                .CommF_:InvokeServer("Buso")
                                                                        end
                                                                    end
                                                                    if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                                                        task.wait()
                                                                        EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                                    end
                                                                    PosMon = v.HumanoidRootPart.CFrame
                                                                    if not _G.Settings.Configs["Fast Attack"] then
                                                                        game:GetService 'VirtualUser':CaptureController()
                                                                        game:GetService 'VirtualUser':Button1Down(Vector2
                                                                            .new(1280, 672))
                                                                    end
                                                                    v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                                                    v.Humanoid.JumpPower = 0
                                                                    v.Humanoid.WalkSpeed = 0
                                                                    v.HumanoidRootPart.CanCollide = false
                                                                    v.Humanoid:ChangeState(11)
                                                                    toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                                                end
                                                            until not _G.Settings.Main["Auto Third Sea"] or not v.Parent or v.Humanoid.Health <= 0
                                                            FastAttack = false
                                                        end
                                                    end
                                                else
                                                    TweenDonSwanthireworld = toTarget(CFrame.new(2288.802, 15.1870775, 863.034607).Position,CFrame.new(2288.802, 15.1870775, 863.034607))
                                                    if (CFrame.new(2288.802, 15.1870775, 863.034607).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                                        if TweenDonSwanthireworld then
                                                            TweenDonSwanthireworld:Stop()
                                                            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(2288.802, 15.1870775, 863.034607)
                                                        end
                                                    end
                                                end
                                            end
                                        else
                                            if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("GetUnlockables").FlamingoAccess == nil then
                                                TabelDevilFruitStore = {}
                                                TabelDevilFruitOpen = {}
    
                                                for i, v in pairs(game:GetService("ReplicatedStorage").Remotes["CommF_"]:InvokeServer("getInventoryFruits")) do
                                                    for i1, v1 in pairs(v) do
                                                        if i1 == "Name" then
                                                            table.insert(TabelDevilFruitStore, v1)
                                                        end
                                                    end
                                                end
    
                                                for i, v in next, game.ReplicatedStorage:WaitForChild("Remotes").CommF_:InvokeServer("GetFruits") do
                                                    if v.Price >= 1000000 then
                                                        table.insert(TabelDevilFruitOpen, v.Name)
                                                    end
                                                end
    
                                                for i, DevilFruitOpenDoor in pairs(TabelDevilFruitOpen) do
                                                    for i1, DevilFruitStore in pairs(TabelDevilFruitStore) do
                                                        if DevilFruitOpenDoor == DevilFruitStore and game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("GetUnlockables").FlamingoAccess == nil then
                                                            if not game.Players.LocalPlayer.Backpack:FindFirstChild(DevilFruitStore) then
                                                                Com("F_", "LoadFruit", DevilFruitStore)
                                                            else
                                                                Com("F_", "TalkTrevor", "1")
                                                                Com("F_", "TalkTrevor", "2")
                                                                Com("F_", "TalkTrevor", "3")
                                                            end
                                                        end
                                                    end
                                                end
    
                                                Com("F_", "TalkTrevor", "1")
                                                Com("F_", "TalkTrevor", "2")
                                                Com("F_", "TalkTrevor", "3")
                                            end
                                        end
                                    else
                                        if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BartiloQuestProgress", "Bartilo") == 0 then
                                            if string.find(game.Players.LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, "Swan Pirates") and string.find(game.Players.LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, "50") and game.Players.LocalPlayer.PlayerGui.Main.Quest.Visible == true then
                                                if game.Workspace.Enemies:FindFirstChild("Swan Pirate") then
                                                    for i, v in pairs(game.Workspace.Enemies:GetChildren()) do
                                                        if v.Name == "Swan Pirate" then
                                                            pcall(function()
                                                                repeat
                                                                    task.wait()
                                                                    if (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 300 then
                                                                        Farmtween = toTarget(v.HumanoidRootPart.Position,
                                                                            v.HumanoidRootPart.CFrame)
                                                                    elseif (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                                                        if Farmtween then Farmtween:Stop() end
                                                                        FastAttack = true
                                                                        StartMagnet = true
                                                                        if _G.Settings.Configs["Auto Haki"] then
                                                                            if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                                                game:GetService("ReplicatedStorage").Remotes
                                                                                    .CommF_:InvokeServer("Buso")
                                                                            end
                                                                        end
                                                                        if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                                                            task.wait()
                                                                            EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                                        end
                                                                        PosMon = v.HumanoidRootPart.CFrame
                                                                        if not _G.Settings.Configs["Fast Attack"] then
                                                                            game:GetService 'VirtualUser':CaptureController()
                                                                            game:GetService 'VirtualUser':Button1Down(
                                                                                Vector2.new(1280, 672))
                                                                        end
                                                                        v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                                                        v.Humanoid.JumpPower = 0
                                                                        v.Humanoid.WalkSpeed = 0
                                                                        v.HumanoidRootPart.CanCollide = false
                                                                        v.Humanoid:ChangeState(11)
                                                                        toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                                                    end
                                                                until not v.Parent or v.Humanoid.Health <= 0 or _G.Settings.Main["Auto Third Sea"] == false or game.Players.LocalPlayer.PlayerGui.Main.Quest.Visible == false
                                                                FastAttack = false
                                                                StartMagnet = false
                                                            end)
                                                        end
                                                    end
                                                else
                                                    Questtween = toTarget(CFrame.new(960.9769897460938, 141.33583068847656, 1216.1959228515625).Position,CFrame.new(960.9769897460938, 141.33583068847656, 1216.1959228515625))
                                                    if (CFrame.new(960.9769897460938, 141.33583068847656, 1216.1959228515625).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                                        if Bartilotween then Bartilotween:Stop() end
                                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(960.9769897460938, 141.33583068847656, 1216.1959228515625)
                                                    end
                                                end
                                            else
                                                Bartilotween = toTarget(CFrame.new(-456.28952, 73.0200958, 299.895966).Position,CFrame.new(-456.28952, 73.0200958, 299.895966))
                                                if (CFrame.new(-456.28952, 73.0200958, 299.895966).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                                    if Bartilotween then Bartilotween:Stop() end
                                                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-456.28952, 73.0200958, 299.895966)
                                                    Com("F_", "StartQuest", "BartiloQuest", 1)
                                                end
                                            end
                                        elseif game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BartiloQuestProgress", "Bartilo") == 1 then
                                            if game.Workspace.Enemies:FindFirstChild("Jeremy") then
                                                for i, v in pairs(game.Workspace.Enemies:GetChildren()) do
                                                    if v.Name == "Jeremy" then
                                                        repeat
                                                            task.wait()
                                                            if (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 300 then
                                                                Farmtween = toTarget(v.HumanoidRootPart.Position,
                                                                    v.HumanoidRootPart.CFrame)
                                                            elseif (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                                                if Farmtween then Farmtween:Stop() end
                                                                FastAttack = true
                                                                if _G.Settings.Configs["Auto Haki"] then
                                                                    if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                                        game:GetService("ReplicatedStorage").Remotes.CommF_
                                                                            :InvokeServer("Buso")
                                                                    end
                                                                end
                                                                if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                                                    task.wait()
                                                                    EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                                end
                                                                PosMon = v.HumanoidRootPart.CFrame
                                                                if not _G.Settings.Configs["Fast Attack"] then
                                                                    game:GetService 'VirtualUser':CaptureController()
                                                                    game:GetService 'VirtualUser':Button1Down(Vector2.new(
                                                                        1280, 672))
                                                                end
                                                                v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                                                v.Humanoid.JumpPower = 0
                                                                v.Humanoid.WalkSpeed = 0
                                                                v.HumanoidRootPart.CanCollide = false
                                                                v.Humanoid:ChangeState(11)
                                                                toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                                            end
                                                        until not v.Parent or v.Humanoid.Health <= 0 or _G.Settings.Main["Auto Third Sea"] == false
                                                        FastAttack = false
                                                    end
                                                end
                                            else
                                                Bartilotween = toTarget(CFrame.new(2099.88159, 448.931, 648.997375).Position,CFrame.new(2099.88159, 448.931, 648.997375))
                                                if (CFrame.new(2099.88159, 448.931, 648.997375).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                                    if Bartilotween then Bartilotween:Stop() end
                                                    game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame =CFrame.new(2099.88159, 448.931, 648.997375)
                                                end
                                            end
                                        elseif game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BartiloQuestProgress", "Bartilo") == 2 then
                                            if (CFrame.new(-1836, 11, 1714).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 300 then
                                                Bartilotween = toTarget(CFrame.new(-1836, 11, 1714).Position,
                                                    CFrame.new(-1836, 11, 1714))
                                            elseif (CFrame.new(-1836, 11, 1714).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                                if Bartilotween then Bartilotween:Stop() end
                                                game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame =
                                                    CFrame.new(-1836, 11, 1714)
                                                wait(.5)
                                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(
                                                    -1850.49329, 13.1789551, 1750.89685)
                                                wait(.1)
                                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(
                                                    -1858.87305, 19.3777466, 1712.01807)
                                                wait(.1)
                                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(
                                                    -1803.94324, 16.5789185, 1750.89685)
                                                wait(.1)
                                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(
                                                    -1858.55835, 16.8604317, 1724.79541)
                                                wait(.1)
                                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(
                                                    -1869.54224, 15.987854, 1681.00659)
                                                wait(.1)
                                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(
                                                    -1800.0979, 16.4978027, 1684.52368)
                                                wait(.1)
                                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(
                                                    -1819.26343, 14.795166, 1717.90625)
                                                wait(.1)
                                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(
                                                    -1813.51843, 14.8604736, 1724.79541)
                                            end
                                        end
                                    end
                                end
                            end
                        end)
                    end
                end)
            end})
       
            page1:AddToggle({
            Name = "Auto Bartilo Quest",
            Value =  _G.Settings.Main["Auto Bartilo Quest"], 
            Callback = function(value)
                _G.Settings.Main["Auto Bartilo Quest"] = value
                if value == false then
                    task.wait()
                    toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
                    task.wait()
                end
                SaveSettings()
                task.spawn(function()
                    while task.wait() do
                        pcall(function()
                            if _G.Settings.Main["Auto Bartilo Quest"] then
                                if game.Players.LocalPlayer.Data.Level.Value >= 850 then
                                    if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BartiloQuestProgress", "Bartilo") == 0 then
                                        if string.find(game.Players.LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, "Swan Pirates") and string.find(game.Players.LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, "50") and game.Players.LocalPlayer.PlayerGui.Main.Quest.Visible == true then
                                            if game.Workspace.Enemies:FindFirstChild("Swan Pirate") then
                                                for i, v in pairs(game.Workspace.Enemies:GetChildren()) do
                                                    if v.Name == "Swan Pirate" then
                                                        pcall(function()
                                                            repeat
                                                                task.wait()
                                                                if (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 300 then
                                                                    Farmtween = toTarget(v.HumanoidRootPart.Position,
                                                                        v.HumanoidRootPart.CFrame)
                                                                elseif (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                                                    if Farmtween then Farmtween:Stop() end
                                                                    FastAttack = true
                                                                    StartMagnet = true
                                                                    if _G.Settings.Configs["Auto Haki"] then
                                                                        if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                                            game:GetService("ReplicatedStorage").Remotes
                                                                                .CommF_:InvokeServer("Buso")
                                                                        end
                                                                    end
                                                                    if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                                                        task.wait()
                                                                        EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                                    end
                                                                    PosMon = v.HumanoidRootPart.CFrame
                                                                    if not _G.Settings.Configs["Fast Attack"] then
                                                                        game:GetService 'VirtualUser':CaptureController()
                                                                        game:GetService 'VirtualUser':Button1Down(Vector2
                                                                            .new(1280, 672))
                                                                    end
                                                                    v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                                                    v.Humanoid.JumpPower = 0
                                                                    v.Humanoid.WalkSpeed = 0
                                                                    v.HumanoidRootPart.CanCollide = false
                                                                    v.Humanoid:ChangeState(11)
                                                                    toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                                                end
                                                            until not v.Parent or v.Humanoid.Health <= 0 or _G.Settings.Main["Auto Bartilo Quest"] == false or game.Players.LocalPlayer.PlayerGui.Main.Quest.Visible == false
                                                            StartMagnet = false
                                                            FastAttack = false
                                                        end)
                                                    end
                                                end
                                            else
                                                Questtween = toTarget(
                                                    CFrame.new(960.9769897460938, 141.33583068847656, 1216.1959228515625)
                                                    .Position,
                                                    CFrame.new(960.9769897460938, 141.33583068847656, 1216.1959228515625))
                                                if (CFrame.new(960.9769897460938, 141.33583068847656, 1216.1959228515625).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                                    if Questtween then
                                                        Questtween:Stop()
                                                    end
                                                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(
                                                        960.9769897460938, 141.33583068847656, 1216.1959228515625)
                                                end
                                            end
                                        else
                                            Bartilotween = toTarget(CFrame.new(-456.28952, 73.0200958, 299.895966).Position,
                                                CFrame.new(-456.28952, 73.0200958, 299.895966))
                                            if (CFrame.new(-456.28952, 73.0200958, 299.895966).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                                if Bartilotween then
                                                    Bartilotween:Stop()
                                                end
                                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(
                                                    -456.28952, 73.0200958, 299.895966)
                                                local args = {
                                                    [1] = "StartQuest",
                                                    [2] = "BartiloQuest",
                                                    [3] = 1
                                                }
                                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                            end
                                        end
                                    end
                                elseif game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BartiloQuestProgress", "Bartilo") == 1 then
                                    if game.Workspace.Enemies:FindFirstChild("Jeremy") then
                                        for i, v in pairs(game.Workspace.Enemies:GetChildren()) do
                                            if v.Name == "Jeremy" then
                                                repeat
                                                    task.wait()
                                                    if (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 300 then
                                                        Farmtween = toTarget(v.HumanoidRootPart.Position,
                                                            v.HumanoidRootPart.CFrame)
                                                    elseif (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                                        if Farmtween then Farmtween:Stop() end
                                                        FastAttack = true
                                                        if _G.Settings.Configs["Auto Haki"] then
                                                            if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                                game:GetService("ReplicatedStorage").Remotes.CommF_
                                                                    :InvokeServer("Buso")
                                                            end
                                                        end
                                                        if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                                            task.wait()
                                                            EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                        end
                                                        PosMon = v.HumanoidRootPart.CFrame
                                                        if not _G.Settings.Configs["Fast Attack"] then
                                                            game:GetService 'VirtualUser':CaptureController()
                                                            game:GetService 'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                                        end
                                                        v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                                        v.Humanoid.JumpPower = 0
                                                        v.Humanoid.WalkSpeed = 0
                                                        v.HumanoidRootPart.CanCollide = false
                                                        v.Humanoid:ChangeState(11)
                                                        toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                                    end
                                                until not v.Parent or v.Humanoid.Health <= 0 or _G.Settings.Main["Auto Bartilo Quest"] == false
                                                 FastAttack = false
                                            end
                                        end
                                    else
                                        Bartilotween = toTarget(CFrame.new(2099.88159, 448.931, 648.997375).Position,
                                            CFrame.new(2099.88159, 448.931, 648.997375))
                                        if (CFrame.new(2099.88159, 448.931, 648.997375).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                            if Bartilotween then
                                                Bartilotween:Stop()
                                            end
                                            game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame
                                                .new(2099.88159, 448.931, 648.997375)
                                        end
                                    end
                                elseif game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BartiloQuestProgress", "Bartilo") == 2 then
                                    if (CFrame.new(-1836, 11, 1714).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 300 then
                                        Bartilotween = toTarget(CFrame.new(-1836, 11, 1714).Position,
                                            CFrame.new(-1836, 11, 1714))
                                    elseif (CFrame.new(-1836, 11, 1714).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                        if Bartilotween then
                                            Bartilotween:Stop()
                                        end
                                        game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame
                                            .new(-1836, 11, 1714)
                                        wait(.5)
                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1850.49329,
                                            13.1789551, 1750.89685)
                                        wait(1)
                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1858.87305,
                                            19.3777466, 1712.01807)
                                        wait(1)
                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1803.94324,
                                            16.5789185, 1750.89685)
                                        wait(1)
                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1858.55835,
                                            16.8604317, 1724.79541)
                                        wait(1)
                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1869.54224,
                                            15.987854, 1681.00659)
                                        wait(1)
                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1800.0979,
                                            16.4978027, 1684.52368)
                                        wait(1)
                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1819.26343,
                                            14.795166, 1717.90625)
                                        wait(1)
                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1813.51843,
                                            14.8604736, 1724.79541)
                                    end
                                end
                            end
                        end)
                    end
                end)
            end})
       
      
            page1:AddToggle({
                Name = "Auto Dark Coat", 
                Value = _G.Settings.Main["Auto Dark Coat"],
                Callback =  function(value)
                _G.Settings.Main["Auto Dark Coat"] = value
                if value == false then
                    task.wait()
                    toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
                    task.wait()
                end
                SaveSettings()
                task.spawn(function()
                    while task.wait() do
                        pcall(function()
                            if _G.Settings.Main["Auto Dark Coat"] then
                                if game:GetService("Workspace").Enemies:FindFirstChild("Darkbeard") then
                                    for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                        if v.Name == ("Darkbeard" or v.Name == "Darkbeard") and v.Humanoid.Health > 0 and v:IsA("Model") and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") then
                                            repeat
                                                task.wait()
                                                StartMagnet = true
                                                FastAttack = true
                                                if _G.Settings.Configs["Auto Haki"] then
                                                    if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                            "Buso")
                                                    end
                                                end
                                                if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                                    task.wait()
                                                    EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                end
                                                PosMon = v.HumanoidRootPart.CFrame
                                                if not _G.Settings.Configs["Fast Attack"] then
                                                    game:GetService 'VirtualUser':CaptureController()
                                                    game:GetService 'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                                end
                                                v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                                v.Humanoid.JumpPower = 0
                                                v.Humanoid.WalkSpeed = 0
                                                v.HumanoidRootPart.CanCollide = false
                                                v.Humanoid:ChangeState(11)
                                                toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                            until _G.Settings.Main["Auto Dark Coat"] == false or v.Humanoid.Health <= 0
                                            StartMagnet = false
                                             FastAttack = false
                                        end
                                    end
                                else
                                    toTarget(CFrame.new(3677.08203125, 62.751937866211, -3144.8332519531))
                                end
                            end
                        end)
                    end
                end)
            end})
      
            page1:AddToggle({
                Name = "Auto Ectoplasm", 
                Value = _G.Settings.Main["Auto Ectoplasm"],
                Callback =  function(value)
                _G.Settings.Main["Auto Ectoplasm"] = value
                if value == false then
                    task.wait()
                    toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
                    task.wait()
                end
                SaveSettings()
                task.spawn(function()
                    while task.wait() do
                        pcall(function()
                            if _G.Settings.Main["Auto Ectoplasm"] then
                                if game:GetService("Workspace").Enemies:FindFirstChild("Ship Deckhand") or game:GetService("Workspace").Enemies:FindFirstChild("Ship Engineer") or game:GetService("Workspace").Enemies:FindFirstChild("Ship Steward") or game:GetService("Workspace").Enemies:FindFirstChild("Ship Officer") or game:GetService("Workspace").Enemies:FindFirstChild("Arctic Warrior") then
                                    for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                        if v.Name == "Ship Deckhand" or v.Name == "Ship Engineer" or v.Name == "Ship Steward" or v.Name == "Ship Officer" or v.Name == "Arctic Warrior" then
                                            if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                                                repeat
                                                    task.wait()
                                                    StartMagnet = true
                                                    FastAttack = true
                                                    if _G.Settings.Configs["Auto Haki"] then
                                                        if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                                "Buso")
                                                        end
                                                    end
                                                    if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                                        task.wait()
                                                        EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                    end
                                                    PosMon = v.HumanoidRootPart.CFrame
                                                    if not _G.Settings.Configs["Fast Attack"] then
                                                        game:GetService 'VirtualUser':CaptureController()
                                                        game:GetService 'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                                    end
                                                    v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                                    v.Humanoid.JumpPower = 0
                                                    v.Humanoid.WalkSpeed = 0
                                                    v.HumanoidRootPart.CanCollide = false
                                                    v.Humanoid:ChangeState(11)
                                                    toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                                until not _G.Settings.Main["Auto Ectoplasm"] or not v.Parent or v.Humanoid.Health <= 0
                                                StartMagnet = false
                                               FastAttack = false
                                            end
                                        end
                                    end
                                else
                                    StartMagnet = false
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                                        Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
                                end
                            end
                        end)
                    end
                end)
            end})
      
            page1:AddToggle({
                Name = "Auto Factory", 
                Value = _G.Settings.Main["Auto Factory"],
                Callback =  function(value)
                _G.Settings.Main["Auto Factory"] = value
                if value == false then
                    task.wait()
                    toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
                    task.wait()
                end
                SaveSettings()
                task.spawn(function()
                    while task.wait() do
                        pcall(function()
                            if _G.Settings.Main["Auto Factory"] then
                                if workspace.Map.Dressrosa.SmileFactory.Door.Transparency == 1 then
                                    repeat
                                        task.wait()
                                        FastAttack = true
                                        if _G.Settings.Configs["Auto Haki"] then
                                            if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                            end
                                        end
                                        EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                        if not _G.Settings.Configs["Fast Attack"] then
                                            game:GetService 'VirtualUser':CaptureController()
                                            game:GetService 'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                        end
                                        toTarget(CFrame.new(456.917724609375, 182.5244903564453, -430.490966796875))
                                    until not _G.Settings.Main["Auto Factory"] or workspace.Map.Dressrosa.SmileFactory.Door.Transparency == 0
                                     FastAttack = false
                                end
                            elseif workspace.Map.Dressrosa.SmileFactory.Door.Transparency == 0 then
                                _G.Settings.Main["Auto Factory"] = false
                            end
                        end)
                    end
                end)
            end})
       
            page1:AddToggle({
                Name = "Auto True Triple Katana",Value = _G.Settings.Main["Auto True Triple Katana"], Callback = function(value)
                _G.Settings.Main["Auto True Triple Katana"] = value
                if value == false then
                    task.wait()
                    toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
                    task.wait()
                end
                SaveSettings()
                task.spawn(function()
                    while task.wait() do
                        pcall(function()
                            if _G.Settings.Main["Auto True Triple Katana"] then
                                local string_1 = "MysteriousMan";
                                local string_2 = "2";
                                local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
                                Target:InvokeServer(string_1, string_2);
                            end
                        end)
                    end
                end)
            end})
            page1:AddToggle({Name = "Auto Rengoku Swords", Value = _G.Settings.Main["Auto Rengoku"],Callback = function(value)
                _G.Settings.Main["Auto Rengoku"] = value
                if value == false then
                    toTarget(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame)
                end
                SaveSettings()
                task.spawn(function()
                    while task.wait() do
                        pcall(function()
                            if _G.Settings.Main["Auto Rengoku"] then
                                if game.Players.LocalPlayer.Backpack:FindFirstChild("Hidden Key") or game.Players.LocalPlayer.Character:FindFirstChild("Hidden Key") then
                                    EquipWeapon("Hidden Key")
                                    toTarget(CFrame.new(6571.1201171875, 299.23028564453, -6967.841796875))
                                elseif game.Workspace.Enemies:FindFirstChild("Snow Lurker") or game:GetService("Workspace").Enemies:FindFirstChild("Arctic Warrior") then
                                    for i, v in pairs(game.Workspace.Enemies:GetChildren()) do
                                        if (v.Name == "Snow Lurker" or v.Name == "Arctic Warrior") and v.Humanoid.Health > 0 then
                                            repeat
                                                task.wait()
                                                StartMagnet = true
                                                FastAttack = true
                                                if _G.Settings.Configs["Auto Haki"] then
                                                    if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                            "Buso")
                                                    end
                                                end
                                                if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                                    task.wait()
                                                    EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                end
                                                PosMon = v.HumanoidRootPart.CFrame
                                                if not _G.Settings.Configs["Fast Attack"] then
                                                    game:GetService 'VirtualUser':CaptureController()
                                                    game:GetService 'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                                end
                                                v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                                v.Humanoid.JumpPower = 0
                                                v.Humanoid.WalkSpeed = 0
                                                v.HumanoidRootPart.CanCollide = false
                                                v.Humanoid:ChangeState(11)
                                                toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                            until game.Players.LocalPlayer.Backpack:FindFirstChild("Hidden Key") or not _G.Settings.Main["Auto Rengoku"] or not v.Parent or v.Humanoid.Health <= 0
                                            StartMagnet = false
                                            FastAttack = false
                                        end
                                    end
                                else
                                    StartMagnet = false
                                     FastAttack = false
                                    toTarget(CFrame.new(5525.7045898438, 262.90060424805, -6755.1186523438))
                                end
                            end
                        end)
                    end
                end)
            end})
       
            page1:AddToggle({Name = "Auto Swan Glasses", Value = _G.Settings.Main["Auto Swan Glasses"],Callback = function(value)
                _G.Settings.Main["Auto Swan Glasses"] = value
                if value == false then
                    toTarget(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame)
                end
                SaveSettings()
                task.spawn(function()
                    while task.wait() do
                        pcall(function()
                            if _G.Settings.Main["Auto Swan Glasses"] then
                                if game:GetService("Workspace").Enemies:FindFirstChild("Don Swan") then
                                    for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                        if v.Name == "Don Swan" and v.Humanoid.Health > 0 and v:IsA("Model") and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") then
                                            repeat
                                                task.wait()
                                                StartMagnet = true
                                                FastAttack = true
                                                if _G.Settings.Configs["Auto Haki"] then
                                                    if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                            "Buso")
                                                    end
                                                end
                                                if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                                    task.wait()
                                                    EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                end
                                                PosMon = v.HumanoidRootPart.CFrame
                                                if not _G.Settings.Configs["Fast Attack"] then
                                                    game:GetService 'VirtualUser':CaptureController()
                                                    game:GetService 'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                                end
                                                v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)

                                                v.Humanoid.JumpPower = 0
                                                v.Humanoid.WalkSpeed = 0
                                                v.HumanoidRootPart.CanCollide = false
                                                v.Humanoid:ChangeState(11)
                                                toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                            until not _G.Settings.Main["Auto Swan Glasses"] or v.Humanoid.Health <= 0
                                            StartMagnet = false
                                             FastAttack = false
                                        end
                                    end
                                else
                                    repeat
                                        task.wait()
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                                            Vector3.new(2284.912109375, 15.537666320801, 905.48291015625))
                                    until (CFrame.new(2284.912109375, 15.537666320801, 905.48291015625).Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 4 or not _G.Settings.Main["Auto Swan Glasses"]
                                end
                            end
                        end)
                    end
                end)
            end})
     
            page1:AddToggle({Name = "Auto Ken-Haki V2", Value = _G.Settings.Main["Auto Ken-Haki V2"], Callback = function(value)
                _G.Settings.Main["Auto Ken-Haki V2"] = value
                if value == false then
                    task.wait()
                    toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
                    task.wait()
                end
                SaveSettings()
                task.spawn(function()
                    while task.wait() do
                        pcall(function()
                            if _G.Settings.Main["Auto Ken-Haki V2"] then
                                if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
                                    repeat
                                        toTarget(CFrame.new(-12444.78515625, 332.40396118164, -7673.1806640625))
                                        task.wait()
                                    until not _G.Settings.Main["Auto Ken-Haki V2"] or (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - Vector3.new(-12444.78515625, 332.40396118164, -7673.1806640625)).Magnitude <= 10
                                    wait(.5)
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CitizenQuestProgress",
                                        "Citizen")
                                    wait(1)
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest",
                                        "CitizenQuest", 1)
                                else
                                    if game.Players.LocalPlayer.Backpack:FindFirstChild("Banana") and game.Players.LocalPlayer.Backpack:FindFirstChild("Apple") and game.Players.LocalPlayer.Backpack:FindFirstChild("Pineapple") then
                                        repeat
                                            toTarget(CFrame.new(-12444.78515625, 332.40396118164, -7673.1806640625))
                                            task.wait()
                                        until not _G.Settings.Main["Auto Ken-Haki V2"] or (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - Vector3.new(-12444.78515625, 332.40396118164, -7673.1806640625)).Magnitude <= 10
                                        wait(.5)
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                            "CitizenQuestProgress", "Citizen")
                                    elseif game.Players.LocalPlayer.Backpack:FindFirstChild("Fruit Bowl") or game.Players.LocalPlayer.Character:FindFirstChild("Fruit Bowl") then
                                        repeat
                                            toTarget(CFrame.new(-10920.125, 624.20275878906, -10266.995117188))
                                            task.wait()
                                        until not _G.Settings.Main["Auto Ken-Haki V2"] or (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - Vector3.new(-10920.125, 624.20275878906, -10266.995117188)).Magnitude <= 10
                                        wait(.5)
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("KenTalk2", "Start")
                                        wait(1)
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("KenTalk2", "Buy")
                                    elseif string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, "Defeat 50 Forest Pirates") then
                                        if game:GetService("Workspace").Enemies:FindFirstChild("Forest Pirate") then
                                            for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                                if v.Name == "Forest Pirate" then
                                                    repeat
                                                        task.wait()
                                                        StartMagnet = true
                                                        FastAttack = true
                                                        if _G.Settings.Configs["Auto Haki"] then
                                                            if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                                game:GetService("ReplicatedStorage").Remotes.CommF_
                                                                    :InvokeServer("Buso")
                                                            end
                                                        end
                                                        if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                                            task.wait()
                                                            EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                        end
                                                        PosMon = v.HumanoidRootPart.CFrame
                                                        if not _G.Settings.Configs["Fast Attack"] then
                                                            game:GetService 'VirtualUser':CaptureController()
                                                            game:GetService 'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                                        end
                                                        v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                                        v.Humanoid.JumpPower = 0
                                                        v.Humanoid.WalkSpeed = 0
                                                        v.HumanoidRootPart.CanCollide = false
                                                        v.Humanoid:ChangeState(11)
                                                        toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                                    until not _G.Settings.Main["Auto Ken-Haki V2"] or v.Humanoid.Health <= 0
                                                    StartMagnet = false
                                                     FastAttack = false
                                                end
                                            end
                                        else
                                            repeat
                                                toTarget(CFrame.new(-13277.568359375, 370.34185791016, -7821.1572265625))
                                                task.wait()
                                            until not _G.Settings.Main["Auto Ken-Haki V2"] or (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - Vector3.new(-13277.568359375, 370.34185791016, -7821.1572265625)).Magnitude <= 10
                                        end
                                    elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text == "Defeat  Captain Elephant (0/1)" then
                                        if game:GetService("Workspace").Enemies:FindFirstChild("Captain Elephant") then
                                            for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                                if v.Name == "Captain Elephant" then
                                                    repeat
                                                        task.wait()
                                                        StartMagnet = true
                                                        FastAttack = true
                                                        if _G.Settings.Configs["Auto Haki"] then
                                                            if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                                game:GetService("ReplicatedStorage").Remotes.CommF_
                                                                    :InvokeServer("Buso")
                                                            end
                                                        end
                                                        if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                                            task.wait()
                                                            EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                        end
                                                        PosMon = v.HumanoidRootPart.CFrame
                                                        if not _G.Settings.Configs["Fast Attack"] then
                                                            game:GetService 'VirtualUser':CaptureController()
                                                            game:GetService 'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                                        end
                                                        v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                                        v.Humanoid.JumpPower = 0
                                                        v.Humanoid.WalkSpeed = 0
                                                        v.HumanoidRootPart.CanCollide = false
                                                        v.Humanoid:ChangeState(11)
                                                        toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                                    until not _G.Settings.Main["Auto Ken-Haki V2"] or v.Humanoid.Health <= 0
                                                    StartMagnet = false
                                                     FastAttack = false
                                                end
                                            end
                                        else
                                            repeat
                                                toTarget(CFrame.new(-13493.12890625, 318.89553833008, -8373.7919921875))
                                                task.wait()
                                            until not _G.Settings.Main["Auto Ken-Haki V2"] or (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - Vector3.new(-13493.12890625, 318.89553833008, -8373.7919921875)).Magnitude <= 10
                                        end
                                    else
                                        for i, v in pairs(game.Workspace:GetDescendants()) do
                                            if v.Name == "Apple" or v.Name == "Banana" or v.Name == "Pineapple" then
                                                v.Handle.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame *
                                                    CFrame.new(0, 1, 10)
                                                    task.wait()
                                                firetouchinterest(game.Players.LocalPlayer.Character.HumanoidRootPart,
                                                    v.Handle, 0)
                                                    task.wait()
                                            end
                                        end
                                    end
                                end
                            end
                        end)
                    end
                end)
            end})
       
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
                if tonumber(v.maxPlayers) > tonumber(v.playing) then
                    for _,Existing in pairs(AllIDs) do
                        if num ~= 0 then
                            if ID == tostring(Existing) then
                                Possible = false
                            end
                        else
                            if tonumber(actualHour) ~= tonumber(Existing) then
                                local delFile = pcall(function()
                                    AllIDs = {}
                                    table.insert(AllIDs, actualHour)
                                end)
                            end
                        end
                        num = num + 1
                    end
                    if Possible == true then
                        table.insert(AllIDs, ID)
                        task.wait()
                        pcall(function()
                            task.wait()
                            game:GetService("TeleportService"):TeleportToPlaceInstance(PlaceID, ID, game.Players.LocalPlayer)
                        end)
                        wait(4)
                    end
                end
            end
        end
        function Teleport()
            while task.wait() do
                pcall(function()
                    TPReturner()
                    if foundAnything ~= "" then
                        TPReturner()
                    end
                end)
            end
        end
        
            page1:AddLabelX({Name = "Auto Buy"})
       
            page1:AddToggle({Name = "Auto Buy Legendary Sword",Value =  _G.Settings.Main["Auto Buy Legendary Sword"], Callback = function(value)
                _G.Settings.Main["Auto Buy Legendary Sword"] = value
                SaveSettings()
    
                task.spawn(function()
                    while task.wait() do
                        pcall(function()
                            if _G.Settings.Main["Auto Buy Legendary Sword"] then
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("LegendarySwordDealer", "1")
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("LegendarySwordDealer", "2")
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("LegendarySwordDealer", "3")
                            end
                        end)
                    end
                end)
            end})
            page1:AddToggle({Name = "Auto Buy Legendary Sword Hop", Value = _G.Settings.Main["Auto Buy Legendary Sword Hop"], Callback = function(value)
                SaveSettings()
                _G.Settings.Main["Auto Buy Legendary Sword Hop"] = value
                spawn(function()
                                while task.wait() do
                                    pcall(function()
                                            if _G.Settings.Main["Auto Buy Legendary Sword Hop"] then
                                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("LegendarySwordDealer", "1")
                                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("LegendarySwordDealer", "2")
                                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("LegendarySwordDealer", "3")
                                                game:GetService("StarterGui"):SetCore("SendNotification",{Title = "VectorHub",Text = "HopServer...",Icon = "rbxassetid://14645512457",Duration = 5})
                                                while _G.Settings.Main["Auto Buy Legendary Sword Hop"] do task.wait()
                                                wait(5)
                                                Teleport()
                                                end
                                            end
                                        end)
                                    end
                                 end)
                            end})
       
            page1:AddToggle({Name = "Auto Buy Enchanment Haki",Value = _G.Settings.Main["Auto Buy Enchanment Haki"],Callback =  function(value)
                _G.Settings.Main["Auto Buy Enchanment Haki"] = value
                SaveSettings()
                task.spawn(function()
                    while task.wait() do
                        pcall(function()
                            if _G.Settings.Main["Auto Buy Enchanment Haki"] then
                                local args = {
                                    [1] = "ColorsDealer",
                                    [2] = "2"
                                }
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                            end
                        end)
                    end
                end)
            end})
    elseif World3 then
     
            page1:AddLabelX({Name = "Status : World 3"})
    
          
      
    
            if not World1 then
                page1:AddToggle({Name = "Auto Leviathan", Value = _G.Settings.Main["Teleport to Sea Beast"], Callback = function(value)
                  _G.Settings.Main["Teleport to Sea Beast"] = value
                  if value == false then
                      task.wait()
                      toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
                      task.wait()
                  end
                  SaveSettings()
                  task.spawn(function()
                      while task.wait() do
                          pcall(function()
                              if  _G.Settings.Main["Teleport to Sea Beast"] then
                                  for i, v in pairs(game.Workspace.SeaBeasts:GetChildren()) do
                                      if v:FindFirstChild("HumanoidRootPart") or v.Name == "SeaBeast1" or v.Name == "Leviathan" then
                                          toTarget(v.HumanoidRootPart.CFrame * CFrame.new(0, 500, 0))
                                      end
                                  end
                              end
                          end)
                      end
                  end)
                end})
                end
                
                page1:AddToggle({Name = "Auto Terrorshark", Value_G.Settings.Main["AutoTerrorshark"], Callback = function(value)
                    _G.Settings.Main["AutoTerrorshark"] = value
                    if value == false then
                        task.wait()
                        toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
                        task.wait()
                    end
                    SaveSettings()
                    task.spawn(function()
                        while task.wait() do
                            pcall(function()
                                if _G.Settings.Main["AutoTerrorshark"] then
                                    if game:GetService("Workspace").Enemies:FindFirstChild("Terrorshark") then
                                        for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                            if string.find(v.Name , "Terrorshark") then
                                                repeat task.wait()
                                                    StartMagnet = true
                                                    FastAttack = true
                                                    if _G.Settings.Configs["Auto Haki"] then
                                                        if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                                        end
                                                    end
                                                    if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                                        task.wait()
                                                        EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                    end
                                                    PosMon = v.HumanoidRootPart.CFrame
                                                    if not _G.Settings.Configs["Fast Attack"] then
                                                        game:GetService'VirtualUser':CaptureController()
                                                        game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                                    end
                                                    v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                                    toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                                until v.Humanoid.Health <= 0 or not _G.Settings.Main["AutoTerrorshark"]
                                                StartMagnet = false
                                            FastAttack = false
                                            end
                                        end
                                    end
                                end
                            end)
                        end
                    end)
                end})
                
                if not World1 then
                    page1:AddToggle({Name  ="Teleport to Sea Beast",Value = _G.Settings.Main["Teleport to Sea Beast"], Callback = function(value)
                        _G.Settings.Main["Teleport to Sea Beast"] = value
                            if value == false then
                                task.wait()
                                toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
                                task.wait()
                            end
                            SaveSettings()
                            task.spawn(function()
                                while task.wait() do
                                    pcall(function()
                                        if _G.Settings.Main["Teleport to Sea Beast"] then
                                            for i, v in pairs(game.Workspace.SeaBeasts:GetChildren()) do
                                                if v:FindFirstChild("HumanoidRootPart") or v.Name == "SeaBeast1" then
                                                    toTarget(v.HumanoidRootPart.CFrame * CFrame.new(0, 500, 0))
                                                end
                                            end
                                        end
                                    end)
                                end
                            end)
                        end})
                    end
                
            page1:AddToggle({Name = "Auto Fish Crew Member", Value = _G.Settings.Main["AutoFishCrewMember"], Callback  = function(value)
                _G.Settings.Main["AutoFishCrewMember"] = value
                if value == false then
                    task.wait()
                    toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
                    task.wait()
                end
                SaveSettings()
                task.spawn(function()
                    while task.wait() do
                        pcall(function()
                            if _G.Settings.Main["AutoFishCrewMember"] then
                                if game:GetService("Workspace").Enemies:FindFirstChild("Fish Crew Member") then
                                    for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                        if string.find(v.Name , "Fish Crew Member") then
                                            repeat task.wait()
                                                StartMagnet = true
                                                FastAttack = true
                                                if _G.Settings.Configs["Auto Haki"] then
                                                    if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                                    end
                                                end
                                                if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                                    task.wait()
                                                    EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                end
                                                PosMon = v.HumanoidRootPart.CFrame
                                                if not _G.Settings.Configs["Fast Attack"] then
                                                    game:GetService'VirtualUser':CaptureController()
                                                    game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                                end
                                                v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                                v.Humanoid.JumpPower = 0
                                                v.Humanoid.WalkSpeed = 0
                                                v.HumanoidRootPart.CanCollide = false
                                                v.Humanoid:ChangeState(11)
                                                toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                            until v.Humanoid.Health <= 0 or not _G.Settings.Main["AutoFishCrewMember"]
                                            StartMagnet = false
                                       FastAttack = false
                                        end
                                    end
                                end
                            end
                        end)
                    end
                end)
            end})
            
            
            page1:AddToggle({Name = "Auto Piranha", Value = _G.Settings.Main["AutoPiranha"],Callback =  function(value)
                _G.Settings.Main["AutoPiranha"] = value
                if value == false then
                    task.wait()
                    toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
                    task.wait()
                end
                SaveSettings()
                task.spawn(function()
                    while task.wait() do
                        pcall(function()
                            if _G.Settings.Main["AutoPiranha"] then
                                if game:GetService("Workspace").Enemies:FindFirstChild("Piranha") then
                                    for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                        if string.find(v.Name , "Piranha") then
                                            repeat task.wait()
                                                StartMagnet = true
                                                FastAttack = true
                                                if _G.Settings.Configs["Auto Haki"] then
                                                    if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                                    end
                                                end
                                                if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                                    task.wait()
                                                    EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                end
                                                PosMon = v.HumanoidRootPart.CFrame
                                                if not _G.Settings.Configs["Fast Attack"] then
                                                    game:GetService'VirtualUser':CaptureController()
                                                    game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                                end
                                                v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                                v.Humanoid.JumpPower = 0
                                                v.Humanoid.WalkSpeed = 0
                                                v.HumanoidRootPart.CanCollide = false
                                                v.Humanoid:ChangeState(11)
                                                toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                            until v.Humanoid.Health <= 0 or not _G.Settings.Main["AutoPiranha"]
                                            StartMagnet = false
                                        FastAttack = false
                                        end
                                    end
                                end
                            end
                        end)
                    end
                end)
            end})
            
            page1:AddToggle({Name = "Auto Shark",  Value = _G.Settings.Main["AutoShark"] ,Callback =  function(value)
                _G.Settings.Main["AutoShark"] = value
                if value == false then
                    task.wait()
                    toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
                    task.wait()
                end
                SaveSettings()
                task.spawn(function()
                    while task.wait() do
                        pcall(function()
                            if _G.Settings.Main["AutoShark"]  then
                                if game:GetService("Workspace").Enemies:FindFirstChild("Shark") then
                                    for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                        if string.find(v.Name , "Shark") then
                                            repeat task.wait()
                                                StartMagnet = true
                                                FastAttack = true
                                                if _G.Settings.Configs["Auto Haki"] then
                                                    if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                                    end
                                                end
                                                if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                                    task.wait()
                                                    EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                end
                                                PosMon = v.HumanoidRootPart.CFrame
                                                if not _G.Settings.Configs["Fast Attack"] then
                                                    game:GetService'VirtualUser':CaptureController()
                                                    game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                                end
                                                v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                                v.Humanoid.JumpPower = 0
                                                v.Humanoid.WalkSpeed = 0
                                                v.HumanoidRootPart.CanCollide = false
                                                v.Humanoid:ChangeState(11)
                                                toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                            until v.Humanoid.Health <= 0 or not  _G.Settings.Main["AutoShark"]
                                            StartMagnet = false
                                     FastAttack = false
                                        end
                                    end
                                end
                            end
                        end)
                    end
                end)
            end})
            
            page1:AddToggle({Name = "Increase Boat Speed",Value = _G.increaseboatspeed,Callback = function(value)
            _G.increaseboatspeed  = value
            while task.wait() do
            if _G.increaseboatspeed then
            for i, v in pairs(game.Workspace.Boats:GetDescendants()) do
                if v:IsA("VehicleSeat")  then
                  v.MaxSpeed = 380
                   sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
                end
              end
            elseif not _G.increaseboatspeed then
                for i, v in pairs(game.Workspace.Boats:GetDescendants()) do
                    if v:IsA("VehicleSeat")  then
                      v.MaxSpeed = 150
                       sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
                    end
                  end
                end
            end
            end})
            page1:AddToggle({Name = "Delet All Rock",Value = _G.deleterock,Callback = function(value)
            _G.deleterock = value
            local delete = _G.deleterock
            for i, v in pairs(game.Workspace:GetChildren()) do
              if v.Name == "MediumFlat" or v.Name == "Large" or v.Name == "Largest" or v.Name == "MediumGroup" or v.Name == "SmallCluster" or v.Name == "SmallGroup" or v.Name == "Largest" or v.Name == "" then 
                if delete then
                  v:destroy()
                end
              end
            end
            end})
            function twoboat(gotoCFrame) --- Tween
                pcall(function()
                    game.Players.LocalPlayer.Character.Humanoid.Sit = false
                    game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = false
                end)
                if (game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart.Position - gotoCFrame.Position).Magnitude <= 10 then
                    pcall(function()
                        tweenz:Cancel()
                    end)
                    
                else
                    local tween_s = game:service "TweenService"
                    local info = TweenInfo.new(
                        (game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart.Position - gotoCFrame.Position)
                        .Magnitude /
                        325, Enum.EasingStyle.Linear)
                    tween, err = pcall(function()
                        tweenz = tween_s:Create(game.Players.LocalPlayer.Character["HumanoidRootPart"], info, { CFrame = gotoCFrame })
                        tweenz:Play()
                    end)
                    if not tween then return err end
                end
                function _TweenCanCle()
                    tweenz:Cancel()
                end
              end
              page1:AddToggle({Name = "Teleport To a Nearby Ship",Vale = _G.TPTOBOAT,Callback  =  function(value)
              _G.TPTOBOAT = value
              while task.wait() do
                  if _G.TPTOBOAT then
                      for i, v in pairs(game.Workspace.Boats:GetDescendants()) do
                          if v:IsA("VehicleSeat") then
                              if (v.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 500 then
                                  repeat
                                      task.wait()
                                      local CFrame = v.CFrame
                                      twoboat(CFrame)
                                  until (v.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 20 or not _G.TPTOBOAT
                              end
                          end
                      end
                  end
              end
            end})
            page1:AddToggle({Name = "Auto Sail",Value = _G.autoSail, Callback  =function(value)
                _G.autoSail = value
                while  _G.autoSai do task.wait()
                    if _G.autoSail then
                        keypress(0x57)
                    end
                end
                if not _G.autoSail then
                    keyrelease(0x57)
                end
            end})
          
    if World3 then
    local Elite_Hunter_Status = page1:AddLabelX({Name = "Status : N/Q"}) 
   
        spawn(function()
            while task.wait() do
                pcall(function()
                    if game:GetService("ReplicatedStorage"):FindFirstChild("Diablo") or game:GetService("ReplicatedStorage"):FindFirstChild("Deandre") or game:GetService("ReplicatedStorage"):FindFirstChild("Urban") or game:GetService("Workspace").Enemies:FindFirstChild("Diablo") or game:GetService("Workspace").Enemies:FindFirstChild("Deandre") or game:GetService("Workspace").Enemies:FindFirstChild("Urban")  then
                        Elite_Hunter_Status:Set("Status : Spawned")
                    else
                        Elite_Hunter_Status:Set("Status : Not Spawned")
                    end
                end)
            end
        end)
  
    local EliteProgress = page1:AddLabelX({Name = ""})
   
        spawn(function()
            pcall(function()
                while task.wait() do
                    EliteProgress:Set("Elite Progress : " ..
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("EliteHunter", "Progress"))
                end
            end)
        end)
   
  
        page1:AddToggle({Name = "Auto Elite Hunter Hop", Value = _G.Settings.Main["Auto Elite Hunter Hop"], Callback = function(value)
            _G.Settings.Main["Auto Elite Hunter Hop"] = value
            if value == false then
                toTarget(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame)
            end
        end})
  
        page1:AddToggle({Name = "Auto Elite Hunter", Value = _G.Settings.Main["Auto Elite Hunter"], Callback = function(value)
            _G.Settings.Main["Auto Elite Hunter"] = value
            if value == false then
                toTarget(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame)
            end
            SaveSettings()
            task.spawn(function()
                while task.wait() do
                    pcall(function()
                        if _G.Settings.Main["Auto Elite Hunter"] then
                            if game.Players.LocalPlayer.PlayerGui.Main.Quest.Visible == true then
                                if string.find(game.Players.LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, "Diablo") or string.find(game.Players.LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, "Urban") or string.find(game.Players.LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, "Deandre") then
                                    for i, v in pairs(game.ReplicatedStorage:GetChildren()) do
                                        if string.find(v.Name, "Diablo") then
                                            EliteHunter = toTarget(v.HumanoidRootPart.CFrame)
                                            if (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 150 then
                                                if EliteHunter then
                                                    EliteHunter:Stop()
                                                end
                                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v
                                                    .HumanoidRootPart.CFrame
                                            end
                                        end
                                        if string.find(v.Name, "Urban") then
                                            EliteHunter = toTarget(v.HumanoidRootPart.CFrame)
                                            if (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 150 then
                                                if EliteHunter then
                                                    EliteHunter:Stop()
                                                end
                                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v
                                                    .HumanoidRootPart.CFrame
                                            end
                                        end
                                        if string.find(v.Name, "Deandre") then
                                            EliteHunter = toTarget(v.HumanoidRootPart.CFrame)
                                            if (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 150 then
                                                if EliteHunter then
                                                    EliteHunter:Stop()
                                                end
                                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v
                                                    .HumanoidRootPart.CFrame
                                            end
                                        end
                                    end
                                    for i, v in pairs(game.Workspace.Enemies:GetChildren()) do
                                        if _G.Settings.Main["Auto Elite Hunter"] and string.find(v.Name, "Diablo") and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                                            repeat
                                                task.wait()
                                                if (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 150 then
                                                    Farmtween = toTarget(v.HumanoidRootPart.CFrame)
                                                elseif (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 150 then
                                                    if Farmtween then
                                                        Farmtween:Stop()
                                                    end
                                                    if farmtype == 1 then
                                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v
                                                            .HumanoidRootPart.CFrame * CFrame.new(0, 30, 1)
                                                    elseif farmtype == 2 then
                                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v
                                                            .HumanoidRootPart.CFrame * CFrame.new(0, 1, 30)
                                                    elseif farmtype == 3 then
                                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v
                                                            .HumanoidRootPart.CFrame * CFrame.new(1, 1, -30)
                                                    elseif farmtype == 4 then
                                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v
                                                            .HumanoidRootPart.CFrame * CFrame.new(30, 1, 0)
                                                    elseif farmtype == 5 then
                                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v
                                                            .HumanoidRootPart.CFrame * CFrame.new(-30, 1, 0)
                                                    else
                                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v
                                                            .HumanoidRootPart.CFrame * CFrame.new(0, 30, 1)
                                                    end
                                                    FastAttack = true
                                                    EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                end
                                            until not _G.Settings.Main["Auto Elite Hunter"] or not v.Parent or v.Humanoid.Health <= 0
                                             FastAttack = false
                                        end
                                        if _G.Settings.Main["Auto Elite Hunter"] and string.find(v.Name, "Urban") and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                                            repeat
                                                task.wait()
                                                if (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 150 then
                                                    Farmtween = toTarget(v.HumanoidRootPart.CFrame)
                                                elseif (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 150 then
                                                    if Farmtween then
                                                        Farmtween:Stop()
                                                    end
                                                    if farmtype == 1 then
                                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v
                                                            .HumanoidRootPart.CFrame * CFrame.new(0, 30, 1)
                                                    elseif farmtype == 2 then
                                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v
                                                            .HumanoidRootPart.CFrame * CFrame.new(0, 1, 30)
                                                    elseif farmtype == 3 then
                                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v
                                                            .HumanoidRootPart.CFrame * CFrame.new(1, 1, -30)
                                                    elseif farmtype == 4 then
                                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v
                                                            .HumanoidRootPart.CFrame * CFrame.new(30, 1, 0)
                                                    elseif farmtype == 5 then
                                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v
                                                            .HumanoidRootPart.CFrame * CFrame.new(-30, 1, 0)
                                                    else
                                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v
                                                            .HumanoidRootPart.CFrame * CFrame.new(0, 30, 1)
                                                    end
                                                    FastAttack = true
                                                    EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                end
                                            until not _G.Settings.Main["Auto Elite Hunter"] or not v.Parent or v.Humanoid.Health <= 0
                                             FastAttack = false
                                        end
                                        if _G.Settings.Main["Auto Elite Hunter"] and string.find(v.Name, "Deandre") and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                                            repeat
                                                task.wait()
                                                if (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 150 then
                                                    Farmtween = toTarget(v.HumanoidRootPart.CFrame)
                                                elseif (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 150 then
                                                    if Farmtween then
                                                        Farmtween:Stop()
                                                    end
                                                    if farmtype == 1 then
                                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v
                                                            .HumanoidRootPart.CFrame * CFrame.new(0, 30, 1)
                                                    elseif farmtype == 2 then
                                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v
                                                            .HumanoidRootPart.CFrame * CFrame.new(0, 1, 30)
                                                    elseif farmtype == 3 then
                                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v
                                                            .HumanoidRootPart.CFrame * CFrame.new(1, 1, -30)
                                                    elseif farmtype == 4 then
                                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v
                                                            .HumanoidRootPart.CFrame * CFrame.new(30, 1, 0)
                                                    elseif farmtype == 5 then
                                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v
                                                            .HumanoidRootPart.CFrame * CFrame.new(-30, 1, 0)
                                                    else
                                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v
                                                            .HumanoidRootPart.CFrame * CFrame.new(0, 30, 1)
                                                    end
                                                    FastAttack = true
                                                    EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                end
                                            until not _G.Settings.Main["Auto Elite Hunter"] or not v.Parent or v.Humanoid.Health <= 0
                                             FastAttack = false
                                        end
                                    end
                                else
                                    local string_1 = "EliteHunter";
                                    local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
                                    Target:InvokeServer(string_1);
                                end
                            else
                                local string_1 = "EliteHunter";
                                local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
                                Target:InvokeServer(string_1);
                            end
                        end
                    end)
                end
            end)
        end})
    
        if _G.Settings.Main["Auto Elite Hunter Hop"] then  
        if not (game.Workspace.Enemies:FindFirstChild("Deandre") or game.Workspace.Enemies:FindFirstChild("Urban") or game.Workspace.Enemies:FindFirstChild("Diablo") or game.ReplicatedStorage:FindFirstChild("Deandre") or game.ReplicatedStorage:FindFirstChild("Urban") or game.ReplicatedStorage:FindFirstChild("Diablo")) then
        wait(3)
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
                if tonumber(v.maxPlayers) > tonumber(v.playing) then
                    for _,Existing in pairs(AllIDs) do
                        if num ~= 0 then
                            if ID == tostring(Existing) then
                                Possible = false
                            end
                        else
                            if tonumber(actualHour) ~= tonumber(Existing) then
                                local delFile = pcall(function()
                                    AllIDs = {}
                                    table.insert(AllIDs, actualHour)
                                end)
                            end
                        end
                        num = num + 1
                    end
                    if Possible == true then
                        table.insert(AllIDs, ID)
                        task.wait()
                        pcall(function()
                            task.wait()
                            game:GetService("TeleportService"):TeleportToPlaceInstance(PlaceID, ID, game.Players.LocalPlayer)
                        end)
                        wait(4)
                    end
                end
            end
        end
    
        function Teleport()
            while task.wait() do
                pcall(function()
                    TPReturner()
                    if foundAnything ~= "" then
                        TPReturner()
                    end
                end)
            end
        end
    
        Teleport()
                
    
            end
        end
    
   
        local count_number = 0
        local count_stack = page1:AddLabelX({Name = 'Bone : ' .. count_number, true})
    if World3 then
        spawn(function()
            while true do
                local boneStatus = game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Bones", "Check")
                count_stack:Set('Bone : ' .. boneStatus)
                wait(1) -- รอ 1 วินาที ก่อนที่จะทำการอัปเดตอีกครั้ง
            end
        end)
    end
        page1:AddToggle({Name = "Auto Farm Bone", Value = _G.Settings.Main["Auto Farm Bone"], Callback = function(value)
            _G.Settings.Main["Auto Farm Bone"] = value
            if value == false then
                task.wait()
                two(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
                task.wait()
            end
            SaveSettings()
            task.spawn(function()
                while task.wait() do
                    pcall(function()
                        if _G.Settings.Main["Auto Farm Bone"] then
                            if game:GetService("Workspace").Enemies:FindFirstChild("Reborn Skeleton") or game:GetService("Workspace").Enemies:FindFirstChild("Living Zombie") or game:GetService("Workspace").Enemies:FindFirstChild("Demonic Soul") or game:GetService("Workspace").Enemies:FindFirstChild("Posessed Mummy") then
                                for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                    if v.Name == "Reborn Skeleton" or v.Name == "Living Zombie" or v.Name == "Demonic Soul" or v.Name == "Posessed Mummy" then
                                        if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                                            repeat
                                                task.wait()
                                                StartMagnet = true
                                                FastAttack = true
                                                if _G.Settings.Configs["Auto Haki"] then
                                                    if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                            "Buso")
                                                    end
                                                end
                                                if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                                    task.wait()
                                                    EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                end
                                                PosMon = v.HumanoidRootPart.CFrame
                                                if not _G.Settings.Configs["Fast Attack"] then
                                                    game:GetService 'VirtualUser':CaptureController()
                                                    game:GetService 'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                                end
                                                v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                                v.Humanoid.JumpPower = 0
                                                v.Humanoid.WalkSpeed = 0
                                                v.HumanoidRootPart.CanCollide = false
                                                v.Humanoid:ChangeState(11)
                                                toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                            until not _G.Settings.Main["Auto Farm Bone"] or v.Humanoid.Health <= 0 or not v.Parent or v.Humanoid.Health <= 0
                                            StartMagnet = false
                                            FastAttack = false
                                        end
                                    end
                                end
                            else
                                two(CFrame.new(-9504.8564453125, 172.14292907714844, 6057.259765625))
                            end
                        end
                    end)
                end
            end)
        end})
        page1:AddToggle({Name = "Auto Random Bone", Value = _G.Settings.Main["Auto Random Bone"],Callback  = function(value)
            _G.Settings.Main["Auto Random Bone"] = value
            SaveSettings()
        end})
    else
      

   
    spawn(function()
        while wait(.1) do
            if _G.Settings.Main["Auto Random Bone"] then
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Bones", "Buy", 1, 1)
            end
        end
    end)
  
        page1:AddToggle({Name = "Auto Farm Boss Hallow", Value = _G.Settings.Main["Auto Farm Boss Hallow"], Callback = function(value)
            _G.Settings.Main["Auto Farm Boss Hallow"] = value
            if value == false then
                task.wait()
                toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
                task.wait()
            end
            SaveSettings()
            task.spawn(function()
                while task.wait() do
                    pcall(function()
                        if _G.Settings.Main["Auto Farm Boss Hallow"] then
                            if game:GetService("Workspace").Enemies:FindFirstChild("Soul Reaper") then
                                for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                    if string.find(v.Name , "Soul Reaper") then
                                        repeat task.wait()
                                            StartMagnet = true
                                            FastAttack = true
                                            if _G.Settings.Configs["Auto Haki"] then
                                                if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                                end
                                            end
                                            if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                                task.wait()
                                                EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                            end
                                            PosMon = v.HumanoidRootPart.CFrame
                                            if not _G.Settings.Configs["Fast Attack"] then
                                                game:GetService'VirtualUser':CaptureController()
                                                game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                            end
                                            v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                                            v.Humanoid.JumpPower = 0
                                            v.Humanoid.WalkSpeed = 0
                                            v.HumanoidRootPart.CanCollide = false
                                            v.Humanoid:ChangeState(11)
                                            toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                        until v.Humanoid.Health <= 0 or not _G.Settings.Main["Auto Farm Boss Hallow"]
                                        StartMagnet = false
                                         FastAttack = false
                                    end
                                end
                            else
                                toTarget(CFrame.new(-9524.7890625, 315.80429077148, 6655.7192382813))
                            end
                        end
                    end)
                end
            end)
        end})
   
   
        page1:AddToggle({Name = "SpawnBossHallow", Value = _G.SpawnBossHallow, Callback = function(value)
            _G.SpawnBossHallow = value
            toTarget(CFrame.new(-8933.0537109375, 146.79251098632812, 6063.353515625))
            if value == false then
                toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
            end
        end})

       --[[ local MobKilledLabel = page1:AddLabelX({Name = "Need Kill Mon : Loading...", true})
        spawn(function()
            while true do
                pcall(function()
                    local cakeStatus = game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CakePrinceSpawner")
    
                    if string.len(cakeStatus) == 88 then
                        MobKilledLabel:Set("Need Kill Mon : " .. string.sub(cakeStatus, 39, 41))
                    elseif string.len(cakeStatus) == 87 then
                        MobKilledLabel:Set("Need Kill Mon : " .. string.sub(cakeStatus, 39, 40))
                    elseif string.len(cakeStatus) == 86 then
                        MobKilledLabel:Set("Need Kill Mon : " .. string.sub(cakeStatus, 39, 39))
                    else
                        MobKilledLabel:Set("Boss Is Spawning")
                    end
                end)
    
                wait(0.5)
            end
        end)]]
        page1:AddToggle({Name = "Auto Katakuri", Value = _G.Settings.Main["Auto Cake Prince"],Callback =  function(value)
            _G.Settings.Main["Auto Cake Prince"] = value
            if value == false then
                toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
            end
            SaveSettings()
            game:GetService("StarterGui"):SetCore("SendNotification",{Title = "VectorHub",Text = "OFF FASTTP",Icon = "rbxassetid://14645512457",Duration = 1})
            task.spawn(function()
                while task.wait() do
                    if _G.Settings.Main["Auto Cake Prince"] then
                        game.ReplicatedStorage.Remotes.CommF_:InvokeServer("CakePrinceSpawner")
                        if game.ReplicatedStorage:FindFirstChild("Cake Prince") or game:GetService("Workspace").Enemies:FindFirstChild("Cake Prince") then
                            if game:GetService("Workspace").Enemies:FindFirstChild("Cake Prince") then
                                for i, v in pairs(game.Workspace.Enemies:GetChildren()) do
                                    if _G.Settings.Main["Auto Cake Prince"] and v.Name == "Cake Prince" and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
                                        repeat
                                            task.wait()
                                            if (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 300 then
                                                Farmtween = toTarget(v.HumanoidRootPart.CFrame)
                                            elseif (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                                if Farmtween then
                                                    Farmtween:Stop()
                                                end
                                                FastAttack = true
                                                if game:GetService("Workspace").Enemies:FindFirstChild("Cake Prince") then
                                                    _G.Settings.Configs["Fast Attack Type"] = "Normal"
                                                else
                                                    _G.Settings.Configs["Fast Attack Type"] = "Fast"
                                                end
                                                if _G.Settings.Configs["Auto Haki"] then
                                                    if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                            "Buso")
                                                    end
                                                end
                                                if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                                    task.wait()
                                                    EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                end
                                                PosMon = v.HumanoidRootPart.CFrame
                                                if not _G.Settings.Configs["Fast Attack"] then
                                                    game:GetService 'VirtualUser':CaptureController()
                                                    game:GetService 'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                                end
                                                v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                                v.Humanoid.JumpPower = 0
                                                v.Humanoid.WalkSpeed = 0
                                                v.HumanoidRootPart.CanCollide = false
                                                v.Humanoid:ChangeState(11)
                                                toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                            end
                                        until not _G.Settings.Main["Auto Cake Prince"] or not v.Parent or v.Humanoid.Health <= 0
                                         FastAttack = false
                                    end
                                end
                            else
                                if game:GetService("Workspace").Map.CakeLoaf.BigMirror.Other.Transparency == 0 and (CFrame.new(-1990.672607421875, 4532.99951171875, -14973.6748046875).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude >= 100 then -- 2000
                                     FastAttack = false
                                    Questtween = toTarget(CFrame.new(-2174.35546875, 69.97904968261719, -12396.609375))
                                    if (CFrame.new(-2174.35546875, 69.97904968261719, -12396.609375).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                        if Questtween then Questtween:Stop() end
                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-2151.82153,
                                            149.315704, -12404.9053)
                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(
                                            -2174.35546875,
                                            69.97904968261719, -12396.609375)
                                        wait(.1)
                                    end
                                end
                            end
                        else
                            if game:GetService("Workspace").Enemies:FindFirstChild("Cookie Crafter") or game:GetService("Workspace").Enemies:FindFirstChild("Cake Guard") or game:GetService("Workspace").Enemies:FindFirstChild("Baking Staff") or game:GetService("Workspace").Enemies:FindFirstChild("Head Baker") then
                                for i, v in pairs(game.Workspace.Enemies:GetChildren()) do
                                    if (v.Name == "Cookie Crafter" or v.Name == "Cake Guard" or v.Name == "Baking Staff" or v.Name == "Head Baker") and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
                                        repeat
                                            task.wait()
                                            if (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 300 then
                                                Farmtween = toTarget(v.HumanoidRootPart.CFrame)
                                            elseif (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                                if Farmtween then
                                                    Farmtween:Stop()
                                                end
                                                FastAttack = true
                                                StartMagnet = true
                                                if _G.Settings.Configs["Auto Haki"] then
                                                    if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                            "Buso")
                                                    end
                                                end
                                                if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                                    task.wait()
                                                    EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                end
                                                PosMon = v.HumanoidRootPart.CFrame
                                                if not _G.Settings.Configs["Fast Attack"] then
                                                    game:GetService 'VirtualUser':CaptureController()
                                                    game:GetService 'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                                end
                                                v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                                v.Humanoid.JumpPower = 0
                                                v.Humanoid.WalkSpeed = 0
                                                v.HumanoidRootPart.CanCollide = false
                                                v.Humanoid:ChangeState(11)
                                                toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                            end
                                        until not _G.Settings.Main["Auto Cake Prince"] or not v.Parent or v.Humanoid.Health <= 0
                                        StartMagnet = false
                                          FastAttack = false
                                    end
                                end
                            else
                                Questtween = toTarget(CFrame.new(-2079.6826171875, 227.9525909423828, -12321.923828125))
                                if (CFrame.new(-2079.6826171875, 227.9525909423828, -12321.923828125).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                    if Questtween then Questtween:Stop() end
                                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-2079.6826171875,
                                        227.9525909423828, -12321.923828125)
                                end
                            end
                        end
                    else
                        toTarget(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame)
                        break
                    end
                end
            end)
        end})
  
   
        page1:AddLabelX({Name = "Farm Materail"})
  
        page1:AddDropdown({Name = "Select Material",List = AllMaterial, Callback = function(value)
            SelectModeMaterial = value
        end})
    
        page1:AddToggle({Name = "Auto Farm Material",Value =  AutoFarmMaterial, Callback = function(x)
            AutoFarmMaterial = x
            if x == false then
                toTarget(game.Players.LocalPlayer.Character.HumanoidRootPart.Position,
                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame)
            end
            spawn(function()
                while task.wait() do
                    if AutoFarmMaterial then
                        xpcall(function()
                            if (SelectModeMaterial ~= "") then
                                CheckMaterial(SelectModeMaterial);
                                if CustomFindFirstChild(MaterialMob) then
                                    for v0, v1 in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                        if (AutoFarmMaterial and table.find(MaterialMob, v1.Name) and v1:FindFirstChild("HumanoidRootPart") and v1:FindFirstChild("Humanoid") and (v1.Humanoid.Health > 0)) then
                                            repeat
                                                task.wait();
                                                FarmtoTarget = toTarget(v1.HumanoidRootPart.CFrame * CFrame.new(0, 30, 1));
                                                if (v1:FindFirstChild("HumanoidRootPart") and v1:FindFirstChild("Humanoid") and ((v1.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 150)) then
                                                    if FarmtoTarget then FarmtoTarget:Stop(); end
                                                    FastAttack = true;
                                                    EquipWeapon(_G.Settings.Configs["Select Weapon"]);
                                                    spawn(function()
                                                        for v4, v5 in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                                            if (v5.Name == v1.Name) then
                                                                spawn(function()
                                                                    if InMyNetWork(v5.HumanoidRootPart) then
                                                                        v5.HumanoidRootPart.CFrame = v1.HumanoidRootPart
                                                                            .CFrame;
                                                                        v5.Humanoid.JumpPower = 0;
                                                                        v5.Humanoid.WalkSpeed = 0;
                                                                        v5.HumanoidRootPart.CanCollide = false;
                                                                        v5.Humanoid:ChangeState(14);
                                                                        v5.Humanoid:ChangeState(11);
                                                                        v5.HumanoidRootPart.Size = Vector3.new(55, 55, 55);
                                                                    end
                                                                end);
                                                            end
                                                        end
                                                    end);
                                                    if (game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and (game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 150)) then
                                                        game:service("VirtualInputManager"):SendKeyEvent(true, "V", false,
                                                            game);
                                                        game:service("VirtualInputManager"):SendKeyEvent(false, "V",
                                                            false, game);
                                                    end
                                                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v1
                                                        .HumanoidRootPart.CFrame * CFrame.new(0, 30, 1);
                                                end
                                            until not CustomFindFirstChild(MaterialMob) or not AutoFarmMaterial or (v1.Humanoid.Health <= 0) or not v1.Parent
                                             FastAttack = false;
                                        end
                                    end
                                else
                                    FastAttack = false;
                                    Modstween = toTarget(CFrameMon);
                                    if (World1 and (table.find(MaterialMob, "Fishman Commando")) and ((CFrameMon.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 50000)) then
                                        if Modstween then Modstween:Stop(); end
                                        wait(0.5); game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                            "requestEntrance", Vector3.new(61163.8515625, 11.6796875, 1819.7841796875));
                                    elseif (World1 and not (table.find(MaterialMob, "Fishman Commando")) and ((CFrameMon.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 50000)) then
                                        if Modstween then Modstween:Stop(); end
                                        wait(0.5); game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                            "requestEntrance", Vector3.new(3864.8515625, 6.6796875, -1926.7841796875));
                                    elseif (World1 and (table.find(MaterialMob, "God's Guard")) and ((CFrameMon.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 3000)) then
                                        if Modstween then Modstween:Stop(); end
                                        wait(0.5); game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                            "requestEntrance",
                                            Vector3.new(-4607.8227539063, 872.54248046875, -1667.5568847656));
                                    elseif ((CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 150) then
                                        if Modstween then Modstween:Stop(); end
                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameMon;
                                    end
                                end
                            end
                        end, function(x)
                            print("Auto Farm Material Error : " .. x)
                        end)
                    else
                        break;
                    end
                end
            end)
        end})
  
        local FastAttackType = {
            "Fast",
            "Normal",
            "Slow"
        }
        page2:AddDropdown({Name = "Fast Attack Type",List = FastAttackType,Callback =  function(value)
            _G.Settings.Configs["Fast Attack Type"] = value
            SaveSettings()
        end})
   
    task.spawn(function()
        while task.wait(0) do
            local ac = CombatFrameworkR.activeController
            if ac and ac.equipped then
                wait(0.02)
                if FastAttack and _G.Settings.Configs["Fast Attack"] then
                    AttackFunction()
                    if _G.Settings.Configs["Fast Attack Type"] == "Normal" then
                        if tick() - cooldownfastattack > .9 then wait(.1) cooldownfastattack = tick() end
                    elseif _G.Settings.Configs["Fast Attack Type"] == "Fast" then
                        if tick() - cooldownfastattack > 1.5 then wait(.01) cooldownfastattack = tick() end
                    elseif _G.Settings.Configs["Fast Attack Type"] == "Slow" then
                        if tick() - cooldownfastattack > .3 then wait(.7) cooldownfastattack = tick() end
                    end
                    sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
                end
            end
        end
    end)
    Weapon = {
        "Melee",
        "Sword",
        "Fruit"
    }
        page2:AddDropdown({Name = "Select Weapon",List = Weapon,Callback =  function(value)
            SelectWeapon = value
        end})
    task.spawn(function()
        while task.wait() do
            pcall(function()
                if SelectWeapon == "Melee" then
                    for i, v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
                        if v.ToolTip == "Melee" then
                            if game.Players.LocalPlayer.Backpack:FindFirstChild(tostring(v.Name)) then
                                _G.Settings.Configs["Select Weapon"] = v.Name
                            end
                        end
                    end
                elseif SelectWeapon == "Sword" then
                    for i, v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
                        if v.ToolTip == "Sword" then
                            if game.Players.LocalPlayer.Backpack:FindFirstChild(tostring(v.Name)) then
                                _G.Settings.Configs["Select Weapon"] = v.Name
                            end
                        end
                    end
                elseif SelectWeapon == "Fruit" then
                    for i, v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
                        if v.ToolTip == "Blox Fruit" then
                            if game.Players.LocalPlayer.Backpack:FindFirstChild(tostring(v.Name)) then
                                _G.Settings.Configs["Select Weapon"] = v.Name
                            end
                        end
                    end
                else
                    for i, v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
                        if v.ToolTip == "Melee" then
                            if game.Players.LocalPlayer.Backpack:FindFirstChild(tostring(v.Name)) then
                                _G.Settings.Configs["Select Weapon"] = v.Name
                            end
                        end
                    end
                end
            end)
        end
    end)
   
        page2:AddToggle({Name = "Faster Attack", Value = _G.Settings.Configs["Fast Attack"],Callback =  function(value)
            _G.Settings.Configs["Fast Attack"] = value
            SaveSettings()
        end})
        page2:AddToggle({Name = "Auto Haki", Value = _G.Settings.Configs["Auto Haki"], Callback = function(value)
            _G.Settings.Configs["Auto Haki"] = value
            SaveSettings()
        end})
    task.spawn(function()
        while task.wait() do
            pcall(function()
                if _G.Settings.Configs["Auto Haki"] then
                    if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                    end
                end
            end)
        end
    end)

        page2:AddToggle({Name = "Auto Ken", Value = _G.Settings.Configs["Auto Ken"],Callback =  function(value)
            _G.Settings.Configs["Auto Ken"] = value
            SaveSettings()
        end})

    spawn(function() ---auto haki
        while task.wait() do
            pcall(function()
                if _G.Settings.Configs["Auto Ken"] then  
                    if game:GetService("Players").LocalPlayer:FindFirstChild("PlayerGui") and game.Players.LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel") then
                    else
                        wait(1)
                        game:service('VirtualUser'):CaptureController()
                        game:service('VirtualUser'):SetKeyDown('0x65')
                        wait(2)
                        game:service('VirtualUser'):SetKeyUp('0x65')
                    end
                end
            end)
        end
    end)
    local Method = {
        "Upper",
        "Behind",
        "Below"
    }
 
        page2:AddDropdown({Name = "Select Farm Method",List = Method, Callback  = function(value)
        _G.Settings.Configs["Method"] = value
        SaveSettings()
    end})
 
    task.spawn(function()
        while task.wait(0) do
            pcall(function()
                if _G.Settings.Configs["Method"] == "Behind" then
                    MethodFarm = CFrame.new(0, 0, _G.Settings.Configs["Distance Auto Farm"])
                elseif _G.Settings.Configs["Method"] == "Below" then
                    MethodFarm = CFrame.new(0, -_G.Settings.Configs["Distance Auto Farm"], 0) * CFrame.Angles(math.rad(90), 0, 0)
                elseif _G.Settings.Configs["Method"] == "Upper" then
                    MethodFarm = CFrame.new(0, _G.Settings.Configs["Distance Auto Farm"], 0) * CFrame.Angles(math.rad(-90), 0, 0)
                else
                    MethodFarm = CFrame.new(0, _G.Settings.Configs["Distance Auto Farm"], 0)
                end
            end)
        end
    end)
    local UserInputService = game:GetService("UserInputService")
    local RunService = game:GetService("RunService")
  
        page2:AddSlider({
            Name = "DistanceAutoFarm",
            Value = _G.Settings.Configs["Distance Auto Farm"],
            Min = 1,
            Max = 60,
            Textbox = true,
            Format = function(value)
                _G.Settings.Configs["Distance Auto Farm"] = value
            SaveSettings()
            end
        })
        page2:AddToggle({Name = "White Screen", Value = false,Callback =  function(value)
            _G.Settings.HUD["White Screen"] = value
            if value then
                game.RunService:Set3dRenderingEnabled(false)
            else
                game.RunService:Set3dRenderingEnabled(true)
            end
        end})
        page2:AddButton({Name = "Auto White Screen", Callback = function()
            --_G.Settings.HUD["Black Screen"] = value
            game:GetService("UserInputService").WindowFocused:connect(
                function()
                    game.RunService:Set3dRenderingEnabled(true)
                end)
            game:GetService("UserInputService").WindowFocusReleased:connect(
                function()
                    game.RunService:Set3dRenderingEnabled(false)
                end)
        end})
        page2:AddToggle({Name = "Black Screen",Value =  false,Callback =  function(value)
            _G.Settings.HUD["Black Screen"] = value
            if value then
                game.RunService:Set3dRenderingEnabled(false)
                game:GetService("Players").LocalPlayer.PlayerGui.Main.Blackscreen.Size = UDim2.new(500, 0, 500, 500)
            else
                game.RunService:Set3dRenderingEnabled(true)
                game:GetService("Players").LocalPlayer.PlayerGui.Main.Blackscreen.Size = UDim2.new(1, 0, 500, 500)
            end
        end})
        page2:AddButton({"Auto Black Screen", function()
            --_G.Settings.HUD["Black Screen"] = value
            game:GetService("UserInputService").WindowFocused:connect(
                function()
                    game.RunService:Set3dRenderingEnabled(true)
                    game:GetService("Players").LocalPlayer.PlayerGui.Main.Blackscreen.Size = UDim2.new(1, 0, 500, 500)
                end)
            game:GetService("UserInputService").WindowFocusReleased:connect(
                function()
                    game.RunService:Set3dRenderingEnabled(false)
                    game:GetService("Players").LocalPlayer.PlayerGui.Main.Blackscreen.Size = UDim2.new(500, 0, 500, 500)
                end)
        end})
        page2:AddToggle({Name = "HideNotification", Value = false, Callback = function(value)
            game:GetService("Players").LocalPlayer.PlayerGui.Notifications.Enabled = not game:GetService("Players").LocalPlayer.PlayerGui.Notifications.Enabled
            SaveSettings()
        end})
        page2:AddToggle({Name = "Bring Mon",Value =  _G.Settings.Configs["Bring Mob"], Callback = function(value)
            _G.Settings.Configs["Bring Mob"] = value
            SaveSettings()
        end})
 
        page2:AddToggle({Name = "Disabled Damage", Value = _G.Settings.Configs["Disabled Damage"], Callback = function(value)
            _G.Settings.Configs["Disabled Damage"] = value
            DisabledDamage()
            SaveSettings()
        end})
        page2:AddToggle({Name = "Camera Shaker", Value = _G.Settings.Configs["Camera Shaker"],Callback =  function(value)
            _G.Settings.Configs["Camera Shaker"] = value
            CameraShaker()
            SaveSettings()
        end})
   
   
        local SelectStats = {
            "Melee",
            "Defense",
            "Sword",
            "Gun",
            "Devil Fruits"
        }
        page3:AddDropdown({Name = "Select Stats",List = SelectStats, Callback = function(value)
            _G.Settings.Stat["Select Stats"] = value
            SaveSettings()
            task.spawn(function()
                pcall(function()
                    while task.wait() do
                        if _G.Settings.Stat["Enabled Auto Stats"] then
                            if _G.Settings.Stat["Select Stats"] == "Melee" then
                                local args = {
                                    [1] = "AddPoint",
                                    [2] = "Melee",
                                    [3] = 3333
                                }
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                            elseif _G.Settings.Stat["Select Stats"] == "Defense" then
                                local args = {
                                    [1] = "AddPoint",
                                    [2] = "Defense",
                                    [3] = 3333
                                }
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                            elseif _G.Settings.Stat["Select Stats"] == "Sword" then
                                local args = {
                                    [1] = "AddPoint",
                                    [2] = "Sword",
                                    [3] = 3333
                                }
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                            elseif _G.Settings.Stat["Select Stats"] == "Gun" then
                                local args = {
                                    [1] = "AddPoint",
                                    [2] = "Gun",
                                    [3] = 3333
                                }
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                            elseif _G.Settings.Stat["Select Stats"] == "Devil Fruits" then
                                local args = {
                                    [1] = "AddPoint",
                                    [2] = "Demon Fruit",
                                    [3] = 3333
                                }
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                            elseif _G.Settings.Stat["Select Stats"] == "Max Stats" then
                                if game:GetService("Players").LocalPlayer.Data.Stats.Melee.Level.Value < 2550 then
                                    local args = {
                                        [1] = "AddPoint",
                                        [2] = "Melee",
                                        [3] = 3333
                                    }
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                else
                                    local args = {
                                        [1] = "AddPoint",
                                        [2] = "Defense",
                                        [3] = 3333
                                    }
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                end
                            end
                        end
                    end
                end)
            end)
        end})
        page3:AddToggle({Name = "Auto Stats", Value = _G.Settings.Stat["Enabled Auto Stats"], Callback = function(value)
            _G.Settings.Stat["Enabled Auto Stats"] = value
            SaveSettings()
        end})
        page3:AddToggle({Name = "Auto Stat Kaitun", Value = _G.Settings.Stat["Auto Stats Kaitun"], Callback = function(value)
            _G.Settings.Stat["Auto Stats Kaitun"] = value
            SaveSettings()
        end})
        spawn(function()
            while task.wait() do
                if _G.Settings.Stat["Auto Stats Kaitun"] and  game.Players.LocalPlayer.PlayerGui.Main.Stats.Points.Available.Text > "Available Points: 0"  then
                    if game:GetService("Players").LocalPlayer.Data.Stats.Melee.Level.Value < 2550 then
                        local args = {
                            [1] = "AddPoint",
                            [2] = "Melee",
                            [3] = 3333
                        }
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                    else
                        local args = {
                            [1] = "AddPoint",
                            [2] = "Defense",
                            [3] = 3333
                        }
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                    end
                end
            end
        end)
   
   
        page3:AddLabelX({Name = "Redeem Code"})
    
        page3:AddToggle({Name = "Redeem Code",Value =  _G.Settings.Stat["Enabled Auto Redeem Code"],Callback =  function(value)
            _G.Settings.Stat["Enabled Auto Redeem Code"] = value
            SaveSettings()
        end})
   
   
        page3:AddLabelX({Name = "FightingStyle"})
        page3:AddToggle({Name = "Auto God Human", Value = _G.Settings.Main["Auto God Human"],Callback =  function(value)
            _G.Settings.Main["Auto God Human"] = value
            BuyGodhuman = tonumber(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyGodhuman", true))
            if BuyGodhuman then
                if BuyGodhuman ~= 1 then
                    GetAllMeleeFarm()
                end
            end
            SaveSettings()
            task.spawn(function()
                while task.wait() do
                    pcall(function()
                        if _G.Settings.Main["Auto God Human"] then
                            BuyGodhuman = tonumber(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                "BuyGodhuman", true))
                            if BuyGodhuman then
                                if BuyGodhuman == 1 then
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyGodhuman")
                                    _G.Settings.Main["Auto God Human"] = false
                                end
                            end
                            if not HasTalon then
                                BuyDragonTalon = tonumber(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                    "BuyDragonTalon", true))
    
                                if BuyDragonTalon then
                                    if BuyDragonTalon == 1 then
                                        HasTalon = true
                                    end
                                end
                            end
                            if not HasSuperhuman then
                                BuySuperhuman = tonumber(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                    "BuySuperhuman", true))
    
                                if BuySuperhuman then
                                    if BuySuperhuman == 1 then
                                        HasSuperhuman = true
                                    end
                                end
                            end
                            if not HasKarate then
                                BuySharkmanKarate = tonumber(game:GetService("ReplicatedStorage").Remotes.CommF_
                                    :InvokeServer("BuySharkmanKarate", true))
    
                                if BuySharkmanKarate then
                                    if BuySharkmanKarate == 1 then
                                        HasKarate = true
                                    end
                                end
                            end
                            if not HasDeathStep then
                                BuyDeathStep = tonumber(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                    "BuyDeathStep", true))
    
                                if BuyDeathStep then
                                    if BuyDeathStep == 1 then
                                        HasDeathStep = true
                                    end
                                end
                            end
                            if not HasElectricClaw then
                                BuyElectricClaw = tonumber(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                    "BuyElectricClaw", true))
                                if BuyElectricClaw then
                                    if BuyElectricClaw == 1 then
                                        HasElectricClaw = true
                                    end
                                end
                            end
                            if not HasSuperhuman then
                                if game.Players.LocalPlayer:FindFirstChild("WeaponAssetCache") then
                                    if not game.Players.LocalPlayer.Backpack:FindFirstChild("Combat") and not game.Players.LocalPlayer.Character:FindFirstChild("Combat") then
                                        if not game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") and not game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") then
                                            if not game.Players.LocalPlayer.Backpack:FindFirstChild("Electro") and not game.Players.LocalPlayer.Character:FindFirstChild("Electro") then
                                                if not game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate") and not game.Players.LocalPlayer.Character:FindFirstChild("Fishman Karate") then
                                                    if not game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw") and not game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw") then
                                                        if not game.Players.LocalPlayer.Backpack:FindFirstChild("Superhuman") and not game.Players.LocalPlayer.Character:FindFirstChild("Superhuman") then
                                                            local args = {
                                                                [1] = "BuyElectro"
                                                            }
                                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                                unpack(args))
                                                        end
                                                    end
                                                end
                                            end
                                        end
                                    end
                                    _G.Settings.Configs["Select Weapon"] = GetFightingStyle("Melee")
    
                                    if game.Players.LocalPlayer.Backpack:FindFirstChild("Combat") or game.Players.LocalPlayer.Character:FindFirstChild("Combat") then
                                        local args = {
                                            [1] = "BuyElectro"
                                        }
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                    end
                                    if game.Players.LocalPlayer.Backpack:FindFirstChild("Electro") and game.Players.LocalPlayer.Backpack:FindFirstChild("Electro").Level.Value >= 300 then
                                        local args = {
                                            [1] = "BuyBlackLeg"
                                        }
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                    end
                                    if game.Players.LocalPlayer.Character:FindFirstChild("Electro") and game.Players.LocalPlayer.Character:FindFirstChild("Electro").Level.Value >= 300 then
                                        local args = {
                                            [1] = "BuyBlackLeg"
                                        }
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                    end
                                    if game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg").Level.Value >= 300 then
                                        local args = {
                                            [1] = "BuyFishmanKarate"
                                        }
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                    end
                                    if game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 300 then
                                        local args = {
                                            [1] = "BuyFishmanKarate"
                                        }
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                    end
                                    if game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate") and game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate").Level.Value >= 300 then
                                        game:GetService("StarterGui"):SetCore("SendNotification",{Title = "VectorHub",Text = "เปิดออโต้ดันเจี้ยนต้องการเงินม่วง1500",Icon = "rbxassetid://14645512457",Duration = 1})
                                        game:GetService("StarterGui"):SetCore("SendNotification",{Title = "VectorHub",Text = "OpenAutoRaidYouneed1500Fragment",Icon = "rbxassetid://14645512457",Duration = 1})
    
                                        local args = {
                                            [1] = "BlackbeardReward",
                                            [2] = "DragonClaw",
                                            [3] = "2"
                                        }
                                        HaveDragonClaw = game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                            unpack(args))
                                        if _G.Settings.Main["Auto God Human"] and game.Players.LocalPlayer.Data.Fragments.Value <= 1500 and HaveDragonClaw == 0 then
                                            if game.Players.LocalPlayer.Data.Level.Value > 1100 then
                                                if Auto_Farm_Level then _G.Settings.Main["Auto Farm Level"] = false end
                                            end
                                        else
                                            if Auto_Farm_Level then _G.Settings.Main["Auto Farm Level"] = true end
                                            local args = {
                                                [1] = "BlackbeardReward",
                                                [2] = "DragonClaw",
                                                [3] = "2"
                                            }
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                        end
                                    end
                                    if game.Players.LocalPlayer.Character:FindFirstChild("Fishman Karate") and game.Players.LocalPlayer.Character:FindFirstChild("Fishman Karate").Level.Value >= 300 then
                                        local args = {
                                            [1] = "BlackbeardReward",
                                            [2] = "DragonClaw",
                                            [3] = "2"
                                        }
                                        HaveDragonClaw = game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                            unpack(args))
                                        if _G.Settings.Main["Auto God Human"] and game.Players.LocalPlayer.Data.Fragments.Value <= 1500 and HaveDragonClaw == 0 then
                                            if game.Players.LocalPlayer.Data.Level.Value > 1100 then
                                                if Auto_Farm_Level then _G.Settings.Main["Auto Farm Level"] = false end
                                            end
                                        else
                                            if Auto_Farm_Level then _G.Settings.Main["Auto Farm Level"] = true end
                                            local args = {
                                                [1] = "BlackbeardReward",
                                                [2] = "DragonClaw",
                                                [3] = "2"
                                            }
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                            if Auto_Farm_Level then _G.Settings.Main["Auto Farm Level"] = true end
                                        end
                                    end
    
                                    if game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw").Level.Value >= 300 then
                                        if Auto_Farm_Level then _G.Settings.Main["Auto Farm Level"] = true end
                                        local args = {
                                            [1] = "BuySuperhuman"
                                        }
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                    end
                                    if game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw").Level.Value >= 300 then
                                        if Auto_Farm_Level then _G.Settings.Main["Auto Farm Level"] = true end
                                        local args = {
                                            [1] = "BuySuperhuman"
                                        }
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                    end
                                end
                            elseif not HasKarate then
                                if game.Players.LocalPlayer:FindFirstChild("WeaponAssetCache") then
                                    if not game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate") and not game.Players.LocalPlayer.Character:FindFirstChild("Fishman Karate") then
                                        if not game.Players.LocalPlayer.Backpack:FindFirstChild("Sharkman Karate") and not game.Players.LocalPlayer.Character:FindFirstChild("Sharkman Karate") then
                                            local args = {
                                                [1] = "BuyFishmanKarate"
                                            }
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                        end
                                    end
    
                                    if game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate") and game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate").Level.Value >= 400 then
                                        if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySharkmanKarate", true) == "I lost my house keys, could you help me find them? Thanks." and not game.Players.LocalPlayer.Character:FindFirstChild("Water Key") and not game.Players.LocalPlayer.Backpack:FindFirstChild("Water Key") then
                                            if World2 then
                                                KillSharkMan = true
                                                if Auto_Farm_Level then _G.Settings.Main["Auto Farm Level"] = false end
                                            else
                                                KillSharkMan = false
                                                if Auto_Farm_Level then _G.Settings.Main["Auto Farm Level"] = true end
                                            end
                                        elseif tonumber(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySharkmanKarate", true)) == 1 then
                                            KillSharkMan = false
                                            if Auto_Farm_Level then _G.Settings.Main["Auto Farm Level"] = true end
                                            local args = {
                                                [1] = "BuySharkmanKarate"
                                            }
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                        elseif game.Players.LocalPlayer.Character:FindFirstChild("Water Key") or game.Players.LocalPlayer.Backpack:FindFirstChild("Water Key") then
                                            KillSharkMan = false
                                            if Auto_Farm_Level then _G.Settings.Main["Auto Farm Level"] = true end
                                            local args = {
                                                [1] = "BuySharkmanKarate"
                                            }
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                        end
                                    end
    
                                    if game.Players.LocalPlayer.Character:FindFirstChild("Fishman Karate") and game.Players.LocalPlayer.Character:FindFirstChild("Fishman Karate").Level.Value >= 400 then
                                        if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySharkmanKarate", true) == "I lost my house keys, could you help me find them? Thanks." and not game.Players.LocalPlayer.Character:FindFirstChild("Water Key") and not game.Players.LocalPlayer.Backpack:FindFirstChild("Water Key") then
                                            if World2 then
                                                KillSharkMan = true
                                                if Auto_Farm_Level then _G.Settings.Main["Auto Farm Level"] = false end
                                            else
                                                if Auto_Farm_Level then _G.Settings.Main["Auto Farm Level"] = true end
                                                KillSharkMan = false
                                            end
                                        elseif tonumber(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySharkmanKarate", true)) == 1 then
                                            KillSharkMan = false
                                            if Auto_Farm_Level then _G.Settings.Main["Auto Farm Level"] = true end
                                            local args = {
                                                [1] = "BuySharkmanKarate"
                                            }
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                        elseif game.Players.LocalPlayer.Character:FindFirstChild("Water Key") or game.Players.LocalPlayer.Backpack:FindFirstChild("Water Key") then
                                            KillSharkMan = false
                                            if Auto_Farm_Level then _G.Settings.Main["Auto Farm Level"] = true end
                                            local args = {
                                                [1] = "BuySharkmanKarate"
                                            }
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                        end
                                    end
                                    _G.Settings.Configs["Select Weapon"] = GetFightingStyle("Melee")
                                end
                            elseif not HasDeathStep then
                                if game.Players.LocalPlayer:FindFirstChild("WeaponAssetCache") then
                                    if game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg").Level.Value >= 400 then
                                        local args = {
                                            [1] = "BuyDeathStep"
                                        }
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                    end
                                    if game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 400 then
                                        local args = {
                                            [1] = "BuyDeathStep"
                                        }
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                    end
                                    _G.Settings.Configs["Select Weapon"] = GetFightingStyle("Melee")
                                end
                            elseif not HasTalon then
                                if game.Players.LocalPlayer:FindFirstChild("WeaponAssetCache") then
                                    _G.Settings.Configs["Select Weapon"] = GetFightingStyle("Melee")
    
                                    if game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw").Level.Value >= 400 and game.Players.LocalPlayer.Character:WaitForChild("Humanoid").Health > 0 then
                                        if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDragonTalon", true) == 3 then
                                            local string_1 = "Bones";
                                            local string_2 = "Buy";
                                            local number_1 = 1;
                                            local number_2 = 1;
                                            local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
                                            Target:InvokeServer(string_1, string_2, number_1, number_2);
    
                                            local string_1 = "BuyDragonTalon";
                                            local bool_1 = true;
                                            local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
                                            Target:InvokeServer(string_1, bool_1);
                                        elseif game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDragonTalon", true) == 1 then
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                "BuyDragonTalon")
                                        else
                                            local string_1 = "Bones";
                                            local string_2 = "Buy";
                                            local number_1 = 1;
                                            local number_2 = 1;
                                            local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
                                            Target:InvokeServer(string_1, string_2, number_1, number_2);
                                        end
                                    end
    
                                    if game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw").Level.Value >= 400 and game.Players.LocalPlayer.Character:WaitForChild("Humanoid").Health > 0 then
                                        if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDragonTalon", true) == 3 then
                                            local string_1 = "Bones";
                                            local string_2 = "Buy";
                                            local number_1 = 1;
                                            local number_2 = 1;
                                            local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
                                            Target:InvokeServer(string_1, string_2, number_1, number_2);
    
                                            local string_1 = "BuyDragonTalon";
                                            local bool_1 = true;
                                            local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
                                            Target:InvokeServer(string_1, bool_1);
                                        elseif game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDragonTalon", true) == 1 then
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                "BuyDragonTalon")
                                        else
                                            local string_1 = "Bones";
                                            local string_2 = "Buy";
                                            local number_1 = 1;
                                            local number_2 = 1;
                                            local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
                                            Target:InvokeServer(string_1, string_2, number_1, number_2);
                                        end
                                    end
                                end
                            elseif not HasElectricClaw then
                                if game.Players.LocalPlayer:FindFirstChild("WeaponAssetCache") then
                                    _G.Settings.Configs["Select Weapon"] = GetFightingStyle("Melee")
                                    if game.Players.LocalPlayer.Backpack:FindFirstChild("Electro") and game.Players.LocalPlayer.Backpack:FindFirstChild("Electro").Level.Value >= 400 then
                                        local v175 = game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                            "BuyElectricClaw", true);
                                        if v175 == 4 then
                                            local v176 = game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                "BuyElectricClaw", "Start");
                                            if v176 == nil then
                                                game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(
                                                    -12548, 337, -7481)
                                            end
                                        else
                                            local string_1 = "BuyElectricClaw";
                                            local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
                                            Target:InvokeServer(string_1);
                                        end
                                    end
    
                                    if game.Players.LocalPlayer.Character:FindFirstChild("Electro") and game.Players.LocalPlayer.Character:FindFirstChild("Electro").Level.Value >= 400 then
                                        local v175 = game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                            "BuyElectricClaw", true);
                                        if v175 == 4 then
                                            local v176 = game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                "BuyElectricClaw", "Start");
                                            if v176 == nil then
                                                game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(
                                                    -12548, 337, -7481)
                                            end
                                        else
                                            local string_1 = "BuyElectricClaw";
                                            local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
                                            Target:InvokeServer(string_1);
                                        end
                                    end
                                end
                            end
                            if BuyGodhuman ~= 1 and HasSuperhuman and HasTalon and HasKarate and HasDeathStep and HasElectricClaw then
                                if HasSuperhuman and not SupComplete then
                                    local args = {
                                        [1] = "BuySuperhuman"
                                    }
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                    wait(0.2)
                                    if CheckMasteryWeapon("Superhuman", 400) == "true UpTo" or CheckMasteryWeapon("Superhuman", 400) == "true" and SupComplete == false then
                                        SupComplete = true
                                    end
                                elseif HasTalon and not TalComplete then
                                    local args = {
                                        [1] = "BuyDragonTalon"
                                    }
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                    wait(0.2)
                                    if CheckMasteryWeapon("Dragon Talon", 400) == "true UpTo" or CheckMasteryWeapon("Superhuman", 400) == "true" and TalComplete == false then
                                        TalComplete = true
                                    end
                                elseif HasKarate and not SharkComplete then
                                    local args = {
                                        [1] = "BuySharkmanKarate"
                                    }
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                    wait(0.2)
                                    if CheckMasteryWeapon("Sharkman Karate", 400) == "true UpTo" or CheckMasteryWeapon("Superhuman", 400) == "true" and SharkComplete == false then
                                        SharkComplete = true
                                    end
                                elseif HasDeathStep and not DeathComplete then
                                    local args = {
                                        [1] = "BuyDeathStep"
                                    }
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                    wait(0.2)
                                    if CheckMasteryWeapon("Death Step", 400) == "true UpTo" or CheckMasteryWeapon("Superhuman", 400) == "true" and DeathComplete == false then
                                        DeathComplete = true
                                    end
                                elseif HasElectricClaw and not EClawComplete then
                                    local args = {
                                        [1] = "BuyElectricClaw"
                                    }
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                    wait(0.2)
                                    if CheckMasteryWeapon("Electric Claw", 400) == "true UpTo" or CheckMasteryWeapon("Superhuman", 400) == "true" and EClawComplete == false then
                                        EClawComplete = true
                                    end
                                end
                            end
                            if BuyGodhuman ~= 1 and SupComplete and EClawComplete and TalComplete and SharkComplete and DeathComplete and (not game.Players.LocalPlayer.Character:FindFirstChild("Godhuman") or not game.Players.LocalPlayer.Backpack:FindFirstChild("Godhuman")) then
                                if GetMaterial("Fish Tail") >= 20 then
                                    if GetMaterial("Magma Ore") >= 20 then
                                        if GetMaterial("Dragon Scale") >= 10 then
                                            if GetMaterial("Mystic Droplet") >= 10 then
                                                Com("F_", "BuyGodhuman")
                                                BuyGodhuman = tonumber(game:GetService("ReplicatedStorage").Remotes.CommF_
                                                    :InvokeServer("BuyGodhuman", true))
    
                                                if BuyGodhuman then
                                                    if BuyGodhuman == 1 then
                                                        _G.Settings.Main["Auto God Human"] = false
                                                    end
                                                end
                                                if Auto_Farm_Level then _G.Settings.Main["Auto Farm Level"] = true end
                                            elseif not World2 then
                                                Com("F_", "TravelDressrosa")
                                            elseif World2 then
                                                if Auto_Farm_Level then _G.Settings.Main["Auto Farm Level"] = false end
                                                CheckMaterial("Mystic Droplet")
                                                if CustomFindFirstChild(MaterialMob) then
                                                    for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                                        if _G.Settings.Main["Auto God Human"] and table.find(MaterialMob, v.Name) and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
                                                            repeat
                                                                task.wait()
                                                                FarmtoTarget = toTarget(v.HumanoidRootPart.CFrame *
                                                                    CFrame.new(0, 30, 1))
                                                                if v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 150 then
                                                                    if FarmtoTarget then FarmtoTarget:Stop() end
                                                                    FastAttack = true
                                                                    EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                                    spawn(function()
                                                                        for i, v2 in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                                                            if v2.Name == v.Name then
                                                                                spawn(function()
                                                                                    if InMyNetWork(v2.HumanoidRootPart) then
                                                                                        v2.HumanoidRootPart.CFrame = v
                                                                                            .HumanoidRootPart.CFrame
                                                                                        v2.Humanoid.JumpPower = 0
                                                                                        v2.Humanoid.WalkSpeed = 0
                                                                                        v2.HumanoidRootPart.CanCollide = false
                                                                                        v2.Humanoid:ChangeState(11)
                                                                                        v2.HumanoidRootPart.Size = Vector3
                                                                                            .new(80, 80, 80)
                                                                                    end
                                                                                end)
                                                                            end
                                                                        end
                                                                    end)
                                                                    if game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 150 then
                                                                        game:service('VirtualInputManager'):SendKeyEvent(
                                                                            true, "V", false, game)
                                                                        game:service('VirtualInputManager'):SendKeyEvent(
                                                                            false, "V", false, game)
                                                                    end
                                                                    toTarget(v.HumanoidRootPart.CFrame * _G.Settings.Configs["Method"])
                                                                end
                                                            until not CustomFindFirstChild(MaterialMob) or not _G.Settings.Main["Auto God Human"] or v.Humanoid.Health <= 0 or not v.Parent
                                                          FastAttack = false
                                                        end
                                                    end
                                                else
                                                     FastAttack = false
                                                    Modstween = toTarget(CFrameMon.Position, CFrameMon)
                                                if (World1 and (table.find(MaterialMob, "Fishman Commando")) and ((CFrameMon.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 50000)) then
                                                    if Modstween then Modstween:Stop(); end
                                                    wait(0.5); game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                        "requestEntrance", Vector3.new(61163.8515625, 11.6796875, 1819.7841796875));
                                                elseif (World1 and not (table.find(MaterialMob, "Fishman Commando")) and ((CFrameMon.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 50000)) then
                                                    if Modstween then Modstween:Stop(); end
                                                    wait(0.5); game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                        "requestEntrance", Vector3.new(3864.8515625, 6.6796875, -1926.7841796875));
                                                elseif (World1 and (table.find(MaterialMob, "God's Guard")) and ((CFrameMon.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 3000)) then
                                                    if Modstween then Modstween:Stop(); end
                                                    wait(0.5); game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                        "requestEntrance",
                                                        Vector3.new(-4607.8227539063, 872.54248046875, -1667.5568847656));
                                                elseif ((CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 150) then
                                                    if Modstween then Modstween:Stop(); end
                                                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameMon;
                                                    end
                                                end
                                            end
                                        elseif not World3 then
                                            Com("F_", "TravelZou")
                                        elseif World3 then
                                            if Auto_Farm_Level then _G.Settings.Main["Auto Farm Level"] = false end
                                            CheckMaterial("Dragon Scale")
                                            if CustomFindFirstChild(MaterialMob) then
                                                for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                                    if _G.Settings.Main["Auto God Human"] and table.find(MaterialMob, v.Name) and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
                                                        repeat
                                                            task.wait()
                                                            FarmtoTarget = toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                                            if v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 150 then
                                                                if FarmtoTarget then FarmtoTarget:Stop() end
                                                                FastAttack = true
                                                                EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                                spawn(function()
                                                                    for i, v2 in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                                                        if v2.Name == v.Name then
                                                                            spawn(function()
                                                                                if InMyNetWork(v2.HumanoidRootPart) then
                                                                                    v2.HumanoidRootPart.CFrame = v
                                                                                        .HumanoidRootPart.CFrame
                                                                                    v2.Humanoid.JumpPower = 0
                                                                                    v2.Humanoid.WalkSpeed = 0
                                                                                    v2.HumanoidRootPart.CanCollide = false
                                                                                    v2.Humanoid:ChangeState(11)
                                                                                    v2.HumanoidRootPart.Size = Vector3.new(
                                                                                        80, 80, 80)
                                                                                end
                                                                            end)
                                                                        end
                                                                    end
                                                                end)
                                                                if game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 150 then
                                                                    game:service('VirtualInputManager'):SendKeyEvent(true,
                                                                        "V", false, game)
                                                                    game:service('VirtualInputManager'):SendKeyEvent(false,
                                                                        "V", false, game)
                                                                end
                                                                toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                                            end
                                                        until not CustomFindFirstChild(MaterialMob) or not _G.Settings.Main["Auto God Human"] or v.Humanoid.Health <= 0 or not v.Parent
                                                        FastAttack = false
                                                    end
                                                end
                                            else
                                                 FastAttack = false
                                                Modstween = toTarget(CFrameMon.Position, CFrameMon)
                                                if (World1 and (table.find(MaterialMob, "Fishman Commando")) and ((CFrameMon.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 50000)) then
                                                    if Modstween then Modstween:Stop(); end
                                                    wait(0.5); game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                        "requestEntrance", Vector3.new(61163.8515625, 11.6796875, 1819.7841796875));
                                                elseif (World1 and not (table.find(MaterialMob, "Fishman Commando")) and ((CFrameMon.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 50000)) then
                                                    if Modstween then Modstween:Stop(); end
                                                    wait(0.5); game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                        "requestEntrance", Vector3.new(3864.8515625, 6.6796875, -1926.7841796875));
                                                elseif (World1 and (table.find(MaterialMob, "God's Guard")) and ((CFrameMon.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 3000)) then
                                                    if Modstween then Modstween:Stop(); end
                                                    wait(0.5); game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                        "requestEntrance",
                                                        Vector3.new(-4607.8227539063, 872.54248046875, -1667.5568847656));
                                                elseif ((CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 150) then
                                                    if Modstween then Modstween:Stop(); end
                                                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameMon;
                                                end
                                            end
                                        end
                                    elseif not World1 then
                                        Com("F_", "TravelMain")
                                    elseif World1 then
                                        if Auto_Farm_Level then _G.Settings.Main["Auto Farm Level"] = false end
                                        CheckMaterial("Magma Ore")
                                        if CustomFindFirstChild(MaterialMob) then
                                            for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                                if _G.Settings.Main["Auto God Human"] and table.find(MaterialMob, v.Name) and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
                                                    repeat
                                                        task.wait()
                                                        FarmtoTarget = toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                                        if v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 150 then
                                                            if FarmtoTarget then FarmtoTarget:Stop() end
                                                            FastAttack = true
                                                            EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                            spawn(function()
                                                                for i, v2 in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                                                    if v2.Name == v.Name then
                                                                        spawn(function()
                                                                            if InMyNetWork(v2.HumanoidRootPart) then
                                                                                v2.HumanoidRootPart.CFrame = v
                                                                                    .HumanoidRootPart.CFrame
                                                                                v2.Humanoid.JumpPower = 0
                                                                                v2.Humanoid.WalkSpeed = 0
                                                                                v2.HumanoidRootPart.CanCollide = false
                                                                                v2.Humanoid:ChangeState(11)
                                                                                v2.HumanoidRootPart.Size = Vector3.new(80, 80,
                                                                                    80)
                                                                            end
                                                                        end)
                                                                    end
                                                                end
                                                            end)
                                                            if game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 150 then
                                                                game:service('VirtualInputManager'):SendKeyEvent(true, "V",
                                                                    false, game)
                                                                game:service('VirtualInputManager'):SendKeyEvent(false, "V",
                                                                    false, game)
                                                            end
                                                            toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                                        end
                                                    until not CustomFindFirstChild(MaterialMob) or not _G.Settings.Main["Auto God Human"] or v.Humanoid.Health <= 0 or not v.Parent
                                                     FastAttack = false
                                                end
                                            end
                                        else
                                            FastAttack = false
                                            Modstween = toTarget(CFrameMon.Position, CFrameMon)
                                            if (World1 and (table.find(MaterialMob, "Fishman Commando")) and ((CFrameMon.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 50000)) then
                                                if Modstween then Modstween:Stop(); end
                                                wait(0.5); game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                    "requestEntrance", Vector3.new(61163.8515625, 11.6796875, 1819.7841796875));
                                            elseif (World1 and not (table.find(MaterialMob, "Fishman Commando")) and ((CFrameMon.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 50000)) then
                                                if Modstween then Modstween:Stop(); end
                                                wait(0.5); game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                    "requestEntrance", Vector3.new(3864.8515625, 6.6796875, -1926.7841796875));
                                            elseif (World1 and (table.find(MaterialMob, "God's Guard")) and ((CFrameMon.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 3000)) then
                                                if Modstween then Modstween:Stop(); end
                                                wait(0.5); game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                    "requestEntrance",
                                                    Vector3.new(-4607.8227539063, 872.54248046875, -1667.5568847656));
                                            elseif ((CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 150) then
                                                if Modstween then Modstween:Stop(); end
                                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameMon;
                                            end
                                        end
                                    end
                                elseif not World1 then
                                    Com("F_", "TravelMain")
                                elseif World1 then
                                    if Auto_Farm_Level then _G.Settings.Main["Auto Farm Level"] = false end
                                    CheckMaterial("Fish Tail")
                                    if CustomFindFirstChild(MaterialMob) then
                                        for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                            if _G.Settings.Main["Auto God Human"] and table.find(MaterialMob, v.Name) and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
                                                repeat
                                                    task.wait()
                                                    FarmtoTarget = toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                                    if v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 150 then
                                                        if FarmtoTarget then FarmtoTarget:Stop() end
                                                        FastAttack = true
                                                        EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                        spawn(function()
                                                            for i, v2 in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                                                if v2.Name == v.Name then
                                                                    spawn(function()
                                                                        if InMyNetWork(v2.HumanoidRootPart) then
                                                                            v2.HumanoidRootPart.CFrame = v.HumanoidRootPart
                                                                                .CFrame
                                                                            v2.Humanoid.JumpPower = 0
                                                                            v2.Humanoid.WalkSpeed = 0
                                                                            v2.HumanoidRootPart.CanCollide = false
                                                                            v2.Humanoid:ChangeState(11)
                                                                            v2.HumanoidRootPart.Size = Vector3.new(80, 80, 80)
                                                                        end
                                                                    end)
                                                                end
                                                            end
                                                        end)
                                                        if game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 150 then
                                                            game:service('VirtualInputManager'):SendKeyEvent(true, "V", false,
                                                                game)
                                                            game:service('VirtualInputManager'):SendKeyEvent(false, "V",
                                                                false, game)
                                                        end
                                                        toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                                    end
                                                until not CustomFindFirstChild(MaterialMob) or not _G.Settings.Main["Auto God Human"] or v.Humanoid.Health <= 0 or not v.Parent
                                                 FastAttack = false
                                            end
                                        end
                                    else
                                          FastAttack = false
                                        Modstween = toTarget(CFrameMon.Position, CFrameMon)
                                        if (World1 and (table.find(MaterialMob, "Fishman Commando")) and ((CFrameMon.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 50000)) then
                                            if Modstween then Modstween:Stop(); end
                                            wait(0.5); game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                "requestEntrance", Vector3.new(61163.8515625, 11.6796875, 1819.7841796875));
                                        elseif (World1 and not (table.find(MaterialMob, "Fishman Commando")) and ((CFrameMon.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 50000)) then
                                            if Modstween then Modstween:Stop(); end
                                            wait(0.5); game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                "requestEntrance", Vector3.new(3864.8515625, 6.6796875, -1926.7841796875));
                                        elseif (World1 and (table.find(MaterialMob, "God's Guard")) and ((CFrameMon.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 3000)) then
                                            if Modstween then Modstween:Stop(); end
                                            wait(0.5); game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                "requestEntrance",
                                                Vector3.new(-4607.8227539063, 872.54248046875, -1667.5568847656));
                                        elseif ((CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 150) then
                                            if Modstween then Modstween:Stop(); end
                                            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameMon;
                                        end
                                    end
                                end
                            end
                        end
                    end)
                end
            end)
        end})
        task.spawn(function()
            while task.wait() do
                pcall(function()
                    if _G.Settings.Main["Auto God Human"] and World2 then
                        if game.Workspace.Enemies:FindFirstChild("Tide Keeper") or game.ReplicatedStorage:FindFirstChild("Tide Keeper") then
                            if (KillSharkMan == true and game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySharkmanKarate", true) == "I lost my house keys, could you help me find them? Thanks.") then
                                if KillFish then KillFish:Stop() end
                                Com("F_", "SetSpawnPoint")
                                for i, v in pairs(game.Workspace.Enemies:GetChildren()) do
                                    if v.Name == "Tide Keeper" then
                                        repeat
                                            task.wait()
                                            if game.Workspace.Enemies:FindFirstChild(v.Name) then
                                                if (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 200 then
                                                    Farmtween = toTarget(v.HumanoidRootPart.CFrame)
                                                elseif (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 200 then
                                                    if Farmtween then Farmtween:Stop() end
                                                    FastAttack = true
                                                    if _G.Settings.Configs["Auto Haki"] then
                                                        if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                                "Buso")
                                                        end
                                                    end
                                                    if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                                        task.wait()
                                                        EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                    end
                                                    if not _G.Settings.Configs["Fast Attack"] then
                                                        game:GetService 'VirtualUser':CaptureController()
                                                        game:GetService 'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                                    end
                                                    v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                                    v.Humanoid.JumpPower = 0
                                                    v.Humanoid.WalkSpeed = 0
                                                    v.HumanoidRootPart.CanCollide = false
                                                    v.Humanoid:ChangeState(11)
                                                    toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                                    if game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 150 then
                                                        game:service('VirtualInputManager'):SendKeyEvent(true, "V", false,
                                                            game)
                                                        game:service('VirtualInputManager'):SendKeyEvent(false, "V", false,
                                                            game)
                                                    end
                                                end
                                            end
                                        until not v.Parent or not _G.Settings.Main["Auto God Human"] or KillSharkMan == false or v.Humanoid.Health == 0 or game.Players.LocalPlayer.Character:FindFirstChild("Water Key") or game.Players.LocalPlayer.Backpack:FindFirstChild("Water Key")
                                         FastAttack = false
                                    end
                                end
                            end
                        else
                            if game:GetService("ReplicatedStorage"):FindFirstChild("Tide Keeper") then
                                KillFish = toTarget(game:GetService("ReplicatedStorage"):FindFirstChild(
                                    "Tide Keeper").HumanoidRootPart.CFrame)
                            else
                                if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySharkmanKarate", true) == "I lost my house keys, could you help me find them? Thanks." then
                                    Hop()
                                end
                            end
                        end
                    end
                end)
            end
        end)
   
        page3:AddToggle({Name = "Auto Superhuman", Value = _G.Settings.Main["Auto Superhuman"], Callback = function(value)
            _G.Settings.Main["Auto Superhuman"] = value
            SaveSettings()
            task.spawn(function()
                while task.wait() do
                    pcall(function()
                        if _G.Settings.Main["Auto Superhuman"] then
                            if game.Players.LocalPlayer:FindFirstChild("WeaponAssetCache") then
                                if not game.Players.LocalPlayer.Backpack:FindFirstChild("Combat") and not game.Players.LocalPlayer.Character:FindFirstChild("Combat") then
                                    if not game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") and not game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") then
                                        if not game.Players.LocalPlayer.Backpack:FindFirstChild("Electro") and not game.Players.LocalPlayer.Character:FindFirstChild("Electro") then
                                            if not game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate") and not game.Players.LocalPlayer.Character:FindFirstChild("Fishman Karate") then
                                                if not game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw") and not game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw") then
                                                    if not game.Players.LocalPlayer.Backpack:FindFirstChild("Superhuman") and not game.Players.LocalPlayer.Character:FindFirstChild("Superhuman") then
                                                        local args = {
                                                            [1] = "BuyElectro"
                                                        }
                                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                            unpack(args))
                                                    end
                                                end
                                            end
                                        end
                                    end
                                end
                                _G.Settings.Configs["Select Weapon"] = GetFightingStyle("Melee")
    
                                if game.Players.LocalPlayer.Backpack:FindFirstChild("Combat") or game.Players.LocalPlayer.Character:FindFirstChild("Combat") then
                                    local args = {
                                        [1] = "BuyElectro"
                                    }
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                end
                                if game.Players.LocalPlayer.Backpack:FindFirstChild("Electro") and game.Players.LocalPlayer.Backpack:FindFirstChild("Electro").Level.Value >= 300 then
                                    local args = {
                                        [1] = "BuyBlackLeg"
                                    }
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                end
                                if game.Players.LocalPlayer.Character:FindFirstChild("Electro") and game.Players.LocalPlayer.Character:FindFirstChild("Electro").Level.Value >= 300 then
                                    local args = {
                                        [1] = "BuyBlackLeg"
                                    }
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                end
                                if game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg").Level.Value >= 300 then
                                    local args = {
                                        [1] = "BuyFishmanKarate"
                                    }
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                end
                                if game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 300 then
                                    local args = {
                                        [1] = "BuyFishmanKarate"
                                    }
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                end
                                if game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate") and game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate").Level.Value >= 300 then
                                    local args = {
                                        [1] = "BlackbeardReward",
                                        [2] = "DragonClaw",
                                        [3] = "2"
                                    }
                                    HaveDragonClaw = game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                        unpack(
                                            args))
                                    if _G.Settings.Main["Auto Superhuman"] and game.Players.LocalPlayer.Data.Fragments.Value <= 1500 and HaveDragonClaw == 0 then
                                        if game.Players.LocalPlayer.Data.Level.Value > 1100 then
                                            _G.Settings.Raids["Select Raids"] = "Flame"
                                            _G.Settings.Raids["Auto Raids"] = true
                                            if Auto_Farm_Level then _G.Settings.Main["Auto Farm Level"] = false end
                                        end
                                    else
                                        _G.Settings.Raids["Auto Raids"] = false
                                        if Auto_Farm_Level then _G.Settings.Main["Auto Farm Level"] = true end
                                        local args = {
                                            [1] = "BlackbeardReward",
                                            [2] = "DragonClaw",
                                            [3] = "2"
                                        }
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                        _G.Settings.Raids["Auto Raids"] = false
                                        if Auto_Farm_Level then _G.Settings.Main["Auto Farm Level"] = true end
                                    end
                                end
                                if game.Players.LocalPlayer.Character:FindFirstChild("Fishman Karate") and game.Players.LocalPlayer.Character:FindFirstChild("Fishman Karate").Level.Value >= 300 then
                                    local args = {
                                        [1] = "BlackbeardReward",
                                        [2] = "DragonClaw",
                                        [3] = "2"
                                    }
                                    HaveDragonClaw = game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                        unpack(
                                            args))
                                    if _G.Settings.Main["Auto Superhuman"] and game.Players.LocalPlayer.Data.Fragments.Value <= 1500 and HaveDragonClaw == 0 then
                                        if game.Players.LocalPlayer.Data.Level.Value > 1100 then
                                            _G.Get_Fruit = true
                                            _G.Settings.Raids["Select Raids"] = "Flame"
                                            _G.Settings.Raids["Auto Raids"] = true
                                            if Auto_Farm_Level then _G.Settings.Main["Auto Farm Level"] = false end
                                        end
                                    else
                                        _G.Settings.Raids["Auto Raids"] = false
                                        _G.Get_Fruit = false
                                        if Auto_Farm_Level then _G.Settings.Main["Auto Farm Level"] = true end
                                        local args = {
                                            [1] = "BlackbeardReward",
                                            [2] = "DragonClaw",
                                            [3] = "2"
                                        }
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                        _G.Settings.Raids["Auto Raids"] = false
                                        if Auto_Farm_Level then _G.Settings.Main["Auto Farm Level"] = true end
                                    end
                                end
    
                                if game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw").Level.Value >= 300 then
                                    Auto_Farm_Level = _G.Settings.Main["Auto Farm Level"]
                                    local args = {
                                        [1] = "BuySuperhuman"
                                    }
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                end
                                if game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw").Level.Value >= 300 then
                                    Auto_Farm_Level = _G.Settings.Main["Auto Farm Level"]
                                    local args = {
                                        [1] = "BuySuperhuman"
                                    }
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                end
                            end
                        end
                    end)
                end
            end)
        end})
   
        if _G.Get_Fruit then
            if Inventory_Fruit then
                Inventory_Fruit = nil
            end
            TabelDevilFruitStore = {}
            for i, v in pairs(game:GetService("ReplicatedStorage").Remotes["CommF_"]:InvokeServer("getInventoryFruits")) do
                for i1, v1 in pairs(v) do
                    if i1 == "Name" then
                        table.insert(TabelDevilFruitStore, v1)
                        end
                    end
                end
            fruit = game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("getInventoryFruits")
         for i1, v in pairs(TabelDevilFruitStore) do
             if not game.Players.LocalPlayer.Backpack:FindFirstChild(TabelDevilFruitStore) then
                   for i,v in pairs(fruit) do
                if v["Price"] < 10000000 then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("LoadFruit",v["Name"])
                            end
                    end
                end
             end
          end
        page3:AddToggle({Name = "Auto Electric Claw", Value = _G.Settings.Main["Auto Electric Claw"], Callback = function(value)
            _G.Settings.Main["Auto Electric Claw"] = value
            SaveSettings()
            if _G.Settings.Main["Auto Electric Claw"] then
                Com("F_", "BuyElectro")
            end
            task.spawn(function()
                while task.wait() do
                    pcall(function()
                        if _G.Settings.Main["Auto Electric Claw"] then
                            if game.Players.LocalPlayer:FindFirstChild("WeaponAssetCache") then
                                if game.Players.LocalPlayer.Backpack:FindFirstChild("Electro") and game.Players.LocalPlayer.Backpack:FindFirstChild("Electro").Level.Value < 400 then
                                    _G.Settings.Configs["Select Weapon"] = "Electro"
                                end
                                if game.Players.LocalPlayer.Character:FindFirstChild("Electro") and game.Players.LocalPlayer.Character:FindFirstChild("Electro").Level.Value < 400 then
                                    _G.Settings.Configs["Select Weapon"] = "Electro"
                                end
                                if game.Players.LocalPlayer.Backpack:FindFirstChild("Electro") and game.Players.LocalPlayer.Backpack:FindFirstChild("Electro").Level.Value >= 400 then
                                    local v175 = game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyElectricClaw", true);
                                    if v175 == 4 then
                                        local v176 = game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyElectricClaw",
                                            "Start");
                                        if v176 == nil then
                                            game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-12548,
                                                337, -7481)
                                        end
                                    else
                                        local string_1 = "BuyElectricClaw";
                                        local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
                                        Target:InvokeServer(string_1);
                                    end
                                end
                                if game.Players.LocalPlayer.Character:FindFirstChild("Electro") and game.Players.LocalPlayer.Character:FindFirstChild("Electro").Level.Value >= 400 then
                                    local v175 = game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyElectricClaw", true);
                                    if v175 == 4 then
                                        local v176 = game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyElectricClaw",
                                            "Start");
                                        if v176 == nil then
                                            game.Players.localPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-12548,
                                                337, -7481)
                                        end
                                    else
                                        local string_1 = "BuyElectricClaw";
                                        local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
                                        Target:InvokeServer(string_1);
                                    end
                                end
                            end
                        end
                    end)
                end
            end)
        end})
 
        page3:AddToggle({Name = "Auto Death Step", Value = _G.Settings.Main["Auto Death Step"], Callback = function(value)
            _G.Settings.Main["Auto Death Step"] = value
            SaveSettings()
            if _G.Settings.Main["Auto Death Step"] then
                Com("F_", "BuyBlackLeg")
            end
            task.spawn(function()
                while task.wait() do
                    pcall(function()
                        if _G.Settings.Main["Auto Death Step"] then
                            if game.Players.LocalPlayer:FindFirstChild("WeaponAssetCache") then
                                if game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg").Level.Value >= 400 then
                                    local args = {
                                        [1] = "BuyDeathStep"
                                    }
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                    _G.Settings.Configs["Select Weapon"] = "Death Step"
                                end
                                if game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 400 then
                                    local args = {
                                        [1] = "BuyDeathStep"
                                    }
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    
                                    _G.Settings.Configs["Select Weapon"] = "Death Step"
                                end
                                if game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg").Level.Value < 400 then
                                    _G.Settings.Configs["Select Weapon"] = "Black Leg"
                                end
                            end
                        elseif _G.Settings.Main["Auto Fully Death Step"] then
                            if game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 400 or game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg").Level.Value >= 400 then
                                if game:GetService("Workspace").Map.IceCastle.Hall.LibraryDoor.PhoeyuDoor.Transparency == 0 then
                                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Library Key") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Library Key") then
                                        EquipWeapon("Library Key")
                                        repeat
                                            task.wait()
                                            toTarget(CFrame.new(6371.2001953125, 296.63433837890625, -6841.18115234375))
                                        until (CFrame.new(6371.2001953125, 296.63433837890625, -6841.18115234375).Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3 or not _G.Settings.Main["Auto Death Step"]
                                        if (CFrame.new(6371.2001953125, 296.63433837890625, -6841.18115234375).Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3 then
                                            wait(1.2)
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDeathStep",
                                                true)
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDeathStep")
                                            wait(0.5)
                                        end
                                    elseif game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg").Level.Value >= 450 or game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 450 then
                                        if game:GetService("ReplicatedStorage"):FindFirstChild("Awakened Ice Admiral") or game:GetService("Workspace").Enemies:FindFirstChild("Awakened Ice Admiral") then
                                            if game:GetService("Workspace").Enemies:FindFirstChild("Awakened Ice Admiral") then
                                                for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                                    if v.Name == "Awakened Ice Admiral" then
                                                        repeat
                                                            task.wait()
                                                            if game.Workspace.Enemies:FindFirstChild(v.Name) then
                                                                if (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 200 then
                                                                    Farmtween = toTarget(v.HumanoidRootPart.CFrame)
                                                                elseif (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 200 then
                                                                    if Farmtween then Farmtween:Stop() end
                                                                    FastAttack = true
                                                                    if _G.Settings.Configs["Auto Haki"] then
                                                                        if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                                            game:GetService("ReplicatedStorage").Remotes
                                                                                .CommF_:InvokeServer("Buso")
                                                                        end
                                                                    end
                                                                    if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                                                        task.wait()
                                                                        EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                                    end
                                                                    if not _G.Settings.Configs["Fast Attack"] then
                                                                        game:GetService 'VirtualUser':CaptureController()
                                                                        game:GetService 'VirtualUser':Button1Down(Vector2
                                                                            .new(1280, 672))
                                                                    end
                                                                    v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                                                    v.Humanoid.JumpPower = 0
                                                                    v.Humanoid.WalkSpeed = 0
                                                                    v.HumanoidRootPart.CanCollide = false
                                                                    v.Humanoid:ChangeState(11)
                                                                    toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                                                    if game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 150 then
                                                                        game:service('VirtualInputManager'):SendKeyEvent(
                                                                            true, "V", false, game)
                                                                        game:service('VirtualInputManager'):SendKeyEvent(
                                                                            false, "V", false, game)
                                                                    end
                                                                end
                                                            end
                                                        until not v.Parent or v.Humanoid.Health <= 0 or _G.Settings.Main["Auto Death Step"] == false or game:GetService("Players").LocalPlayer.Character:FindFirstChild("Library Key") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Library Key")
                                                        FastAttack = false
                                                    end
                                                end
                                            else
                                                toTarget(game:GetService("ReplicatedStorage"):FindFirstChild(
                                                    "Awakened Ice Admiral").HumanoidRootPart.CFrame)
                                            end
                                        end
                                    end
                                end
                            else
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBlackLeg")
                            end
                        end
                    end)
                end
            end)
        end})
   
        page3:AddToggle({Name = "Auto SharkMan Karate", Value = _G.Settings.Main["Auto SharkMan Karate"], Callback = function(value)
            _G.Settings.Main["Auto SharkMan Karate"] = value
            SaveSettings()
            if _G.Settings.Main["Auto SharkMan Karate"] then
                Com("F_", "BuySharkmanKarate")
            end
            task.spawn(function()
                while task.wait() do
                    pcall(function()
                        if _G.Settings.Main["Auto SharkMan Karate"] then
                            if game.Players.LocalPlayer:FindFirstChild("WeaponAssetCache") then
                                if game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Fishman Karate") or game:GetService("Players").LocalPlayer.Character:FindFirstChild("Fishman Karate") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Sharkman Karate") or game:GetService("Players").LocalPlayer.Character:FindFirstChild("Sharkman Karate") then
                                    if game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Fishman Karate") and game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Fishman Karate").Level.Value >= 400 then
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySharkmanKarate")
                                        _G.Settings.Configs["Select Weapon"] = "Sharkman Karate"
                                    end
                                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Fishman Karate") and game:GetService("Players").LocalPlayer.Character:FindFirstChild("Fishman Karate").Level.Value >= 400 then
                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySharkmanKarate")
                                        _G.Settings.Configs["Select Weapon"] = "Sharkman Karate"
                                    end
                                    if game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Fishman Karate") and game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Fishman Karate").Level.Value <= 400 then
                                        _G.Settings.Configs["Select Weapon"] = "Fishman Karate"
                                    end
                                else
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyFishmanKarate")
                                end
                            end
                        elseif _G.Settings.Main["Auto Fully SharkMan Karate"] then
                            if game.Players.LocalPlayer.Character:FindFirstChild("Fishman Karate") and game.Players.LocalPlayer.Character:FindFirstChild("Fishman Karate").Level.Value >= 400 or game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate") and game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate").Level.Value >= 400 then
                                if string.find(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySharkmanKarate"), "keys") then
                                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Water Key") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Water Key") then
                                        repeat
                                            task.wait()
                                            toTarget(-2604.6958, 239.432526, -10315.1982, 0.0425701365, 0, -0.999093413, 0, 1,
                                                0, 0.999093413, 0, 0.0425701365)
                                        until (CFrame.new(-2604.6958, 239.432526, -10315.1982, 0.0425701365, 0, -0.999093413, 0, 1, 0, 0.999093413, 0, 0.0425701365).Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3 or not _G.Auto_Fully_SharkMan_Karate
                                        if (CFrame.new(-2604.6958, 239.432526, -10315.1982, 0.0425701365, 0, -0.999093413, 0, 1, 0, 0.999093413, 0, 0.0425701365).Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3 then
                                            wait(1.2)
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                "BuySharkmanKarate", true)
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                "BuySharkmanKarate")
                                            wait(0.5)
                                        end
                                    elseif game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate") and game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate").Level.Value >= 400 or game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate") and game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate").Level.Value >= 400 then
                                        if game:GetService("ReplicatedStorage"):FindFirstChild("Tide Keeper") or game:GetService("Workspace").Enemies:FindFirstChild("Tide Keeper") then
                                            if game:GetService("Workspace").Enemies:FindFirstChild("Tide Keeper") then
                                                for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                                    if v.Name == "Tide Keeper" then
                                                        repeat
                                                            task.wait()
                                                            if game.Workspace.Enemies:FindFirstChild(v.Name) then
                                                                if (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 200 then
                                                                    Farmtween = toTarget(v.HumanoidRootPart.CFrame)
                                                                elseif (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 200 then
                                                                    if Farmtween then Farmtween:Stop() end
                                                                    FastAttack = true
                                                                    if _G.Settings.Configs["Auto Haki"] then
                                                                        if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                                            game:GetService("ReplicatedStorage").Remotes
                                                                                .CommF_:InvokeServer("Buso")
                                                                        end
                                                                    end
                                                                    if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                                                        task.wait()
                                                                        EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                                    end
                                                                    if not _G.Settings.Configs["Fast Attack"] then
                                                                        game:GetService 'VirtualUser':CaptureController()
                                                                        game:GetService 'VirtualUser':Button1Down(Vector2
                                                                            .new(1280, 672))
                                                                    end
                                                                    v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                                                    v.Humanoid.JumpPower = 0
                                                                    v.Humanoid.WalkSpeed = 0
                                                                    v.HumanoidRootPart.CanCollide = false
                                                                    v.Humanoid:ChangeState(11)
                                                                    toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                                                    if game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 150 then
                                                                        game:service('VirtualInputManager'):SendKeyEvent(
                                                                            true, "V", false, game)
                                                                        game:service('VirtualInputManager'):SendKeyEvent(
                                                                            false, "V", false, game)
                                                                    end
                                                                end
                                                            end
                                                        until not v.Parent or v.Humanoid.Health <= 0 or _G.Settings.Main["Auto Death Step"] == false or game:GetService("Players").LocalPlayer.Character:FindFirstChild("Library Key") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Library Key")
                                                        FastAttack = false
                                                    end
                                                end
                                            else
                                                toTarget(game:GetService("ReplicatedStorage"):FindFirstChild(
                                                    "Tide Keeper").HumanoidRootPart.CFrame)
                                            end
                                        end
                                    end
                                else
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySharkmanKarate")
                                end
                            else
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyFishmanKarate")
                            end
                        end
                    end)
                end
            end)
        end})
        page3:AddToggle({Name = "Auto Dragon Talon", Value = _G.Settings.Main["Auto Dragon Talon"], Callback = function(value)
            _G.Settings.Main["Auto Dragon Talon"] = value
            SaveSettings()
            if _G.Settings.Main["Auto Dragon Talon"] then
                Com("F_", "BlackbeardReward", "DragonClaw", "2")
            end
            task.spawn(function()
                while task.wait() do
                    pcall(function()
                        if _G.Settings.Main["Auto Dragon Talon"] then
                            if game.Players.LocalPlayer:FindFirstChild("WeaponAssetCache") then
                                if game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw").Level.Value <= 399 and game.Players.LocalPlayer.Character.Humanoid.Health > 0 then
                                    _G.Settings.Configs["Select Weapon"] = "Dragon Claw"
                                end
                                if game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw").Level.Value <= 399 and game.Players.LocalPlayer.Character.Humanoid.Health > 0 then
                                    _G.Settings.Configs["Select Weapon"] = "Dragon Claw"
                                end
    
                                if game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw").Level.Value >= 400 and game.Players.LocalPlayer.Character.Humanoid.Health > 0 then
                                    _G.Settings.Configs["Select Weapon"] = "Dragon Claw"
                                    if game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyDragonTalon", true) == 3 then
                                        local string_1 = "Bones";
                                        local string_2 = "Buy";
                                        local number_1 = 1;
                                        local number_2 = 1;
                                        local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
                                        Target:InvokeServer(string_1, string_2, number_1, number_2);
    
                                        local string_1 = "BuyDragonTalon";
                                        local bool_1 = true;
                                        local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
                                        Target:InvokeServer(string_1, bool_1);
                                    elseif game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyDragonTalon", true) == 1 then
                                        game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyDragonTalon")
                                    else
                                        local string_1 = "BuyDragonTalon";
                                        local bool_1 = true;
                                        local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
                                        Target:InvokeServer(string_1, bool_1);
                                        local string_1 = "BuyDragonTalon";
                                        local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
                                        Target:InvokeServer(string_1);
                                    end
                                end
    
                                if game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw").Level.Value >= 400 and game.Players.LocalPlayer.Character.Humanoid.Health > 0 then
                                    _G.Settings.Configs["Select Weapon"] = "Dragon Claw"
                                    if game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyDragonTalon", true) == 3 then
                                        local string_1 = "Bones";
                                        local string_2 = "Buy";
                                        local number_1 = 1;
                                        local number_2 = 1;
                                        local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
                                        Target:InvokeServer(string_1, string_2, number_1, number_2);
    
                                        local string_1 = "BuyDragonTalon";
                                        local bool_1 = true;
                                        local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
                                        Target:InvokeServer(string_1, bool_1);
                                    elseif game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyDragonTalon", true) == 1 then
                                        game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyDragonTalon")
                                    else
                                        local string_1 = "BuyDragonTalon";
                                        local bool_1 = true;
                                        local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
                                        Target:InvokeServer(string_1, bool_1);
                                        local string_1 = "BuyDragonTalon";
                                        local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
                                        Target:InvokeServer(string_1);
                                    end
                                end
                            end
                        end
                    end)
                end
            end)
        end})
  
    task.spawn(function()
        while task.wait() do
            pcall(function()
                local MyLevel = game.Players.LocalPlayer.Data.Level.Value
                if _G.Settings.Stat["Enabled Auto Redeem Code"] then
                    if MyLevel >= _G.Settings.Stat["Select Level Redeem Code"] then
                        function Redeem(value)
                            game:GetService("ReplicatedStorage").Remotes.Redeem:InvokeServer(value)
                        end
    
                        for i, v in pairs(CodeApi) do
                            Redeem(v)
                        end
                        wait(3)
                        _G.Settings.Stat["Enabled Auto Redeem Code"] = false
                    end
                end
            end)
        end
    end)
    spawn(function()
        while task.wait() do
            if _G.Settings.Main["Auto Farm Level"] then
                function UseCode(Text)
                    game:GetService("ReplicatedStorage").Remotes.Redeem:InvokeServer(Text)
                end
                UseCode("Sub2UncleKizaru")
                UseCode("SUB2NOOBMASTER123")
                UseCode("StrawHatMaine")
                UseCode("Sub2OfficialNoobie")
                UseCode("SUB2GAMERROBOT_EXP1")
                UseCode("SUB2GAMERROBOT_RESET1")
                UseCode("THEGREATACE")
                UseCode("BIGNEWS")
                UseCode("FUDD10")
                UseCode("fudd10_v2")
                UseCode("Bluxxy")
                UseCode("Starcodeheo")
                UseCode("JCWK")
                UseCode("Magicbus")
                UseCode("Sub2Fer999")
                UseCode("kittgaming")
                UseCode("GAMERROBOT")
                UseCode("SUBGAMERROBOT")
                UseCode("ADMINGIVEAWAY")
                UseCode("KITT_RESET")
                UseCode("SECRET_ADMIN")
                UseCode("Sub2Daigrock")
                UseCode("Axiore")
                UseCode("TantaiGaming")
            end
        end
    end)
    if World1 then
       
            page4:AddLabelX({
               Name =  "Status : World 1"
            })
       
       
            page4:AddButton({Name = "Teleport to World 2", Callback = function(value)
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelDressrosa")
            end})
        
     
            page4:AddButton({Name = "Teleport to World 3",Callback =  function(value)
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelZou")
            end})
        end
    elseif World2 then
      
            page4:AddLabelX({
           Name =      "Status : World 2"
            })
      
            page4:AddButton({Name = "Teleport to World 1", Callback = function(value)
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelMain")
            end})
       
      
            page4:AddButton({Name = "Teleport to World 3",Callback = function(value)
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelZou")
            end})
    elseif World3 then
       
            page4:AddLabelX({
            Name =     "Status : World 3"
           })
    
            page4:AddButton({Name = "Teleport to World 1",Callback =  function(value)
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelMain")
            end})
            page4:AddButton({Name = "Teleport to World 2", Callback = function(value)
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelDressrosa")
            end})
        
    end
    TeleportTable = {}
    if World1 then
        TeleportTable = { "StraterIsland", "Marine1", "Marine2", "Midle Town", "Jungle", "Pirate Village", "Desert",
            "Frozen Village", "Colosseum", "Prison", "Mob Leader", "Magma Village", "UnderWater Gate", "UnderWater City",
            "Fountain City", "Sky1", "Sky2", "Sky3" }
    elseif World2 then
        TeleportTable = { "Dock", "Mansion", "Kingdom Of Rose", "Cafe", "Sunflower Field", "Jeramy Mountain", "Colossuem",
            "Factory", "The Bridge", "Green Bit", "Graveyard", "Dark Area", "Snow Mountain", "Hot Island", "Cold Island",
            "Ice Castle", "Usopp's Island", "inscription Island", "Forgotten Island", "Ghost Ship" }
    elseif World3 then
        TeleportTable = { "Port Town", "Hydra Island", "Gaint Tree", "Mansion", "Castle on the Sea", "Haunted Castle",
            "Icecream Island", "Peanut Island", "Lab", "Cake Loaf", "TikiOutpost" }
    end 
   
        page4:AddDropdown({Name = "Select Place",List = TeleportTable,Callback =  function(value)
            _G.SelectLocalTeleport = value
        end})

   
        page4:AddToggle({Name = "Teleport To Select", Value = _G.TeleportIsland,Callback  = function(value)
            _G.TeleportIsland = value
            if _G.TeleportIsland then
                if World1  then
                    if _G.SelectLocalTeleport == "Jones Salad" then
                        toTarget(CFrame.new(1042.1501464844, 16.299360275269, 1444.3442382813))
                    end
                    if _G.SelectLocalTeleport == "Marine1" then
                        toTarget(CFrame.new(-2599.6655273438, 6.9146227836609, 2062.2216796875))
                    end
                    if _G.SelectLocalTeleport == "Marine2" then
                        toTarget(CFrame.new(-5081.3452148438, 85.221641540527, 4257.3588867188))
                    end
                    if _G.SelectLocalTeleport == "Midle Town" then
                        toTarget(CFrame.new(-655.97088623047, 7.878026008606, 1573.7612304688))
                    end
                    if _G.SelectLocalTeleport == "Jungle" then
                        toTarget(CFrame.new(-1499.9877929688, 22.877912521362, 353.87060546875))
                    end
                    if _G.SelectLocalTeleport == "Pirate Village" then
                        toTarget(CFrame.new(-1163.3889160156, 44.777843475342, 3842.8276367188))
                    end
                    if _G.SelectLocalTeleport == "Desert" then
                        toTarget(CFrame.new(954.02056884766, 6.6275520324707, 4262.611328125))
                    end
                    if _G.SelectLocalTeleport == "Frozen Village" then
                        toTarget(CFrame.new(1144.5270996094, 7.3292083740234, -1164.7322998047))
                    end
                    if _G.SelectLocalTeleport == "Colosseum" then
                        toTarget(CFrame.new(-1667.5869140625, 39.385631561279, -3135.5817871094))
                    end
        
                    if _G.SelectLocalTeleport == "Prison" then
                        toTarget(CFrame.new(4857.6982421875, 5.6780304908752, 732.75750732422))
                    end
                    if _G.SelectLocalTeleport == "Mob Leader" then
                        toTarget(CFrame.new(-2841.9604492188, 7.3560485839844, 5318.1040039063))
                    end
                    if _G.SelectLocalTeleport == "Magma Village" then
                        toTarget(CFrame.new(-5328.8740234375, 8.6164798736572, 8427.3994140625))
                    end
                    if _G.SelectLocalTeleport == "UnderWater Gate" then
                        toTarget(CFrame.new(3893.953125, 5.3989524841309, -1893.4851074219))
                    end
                    if _G.SelectLocalTeleport == "UnderWater City" then
                        toTarget(CFrame.new(61191.12109375, 18.497436523438, 1561.8873291016))
                    end
                    if _G.SelectLocalTeleport == "Fountain City" then
                        toTarget(CFrame.new(5244.7133789063, 38.526943206787, 4073.4987792969))
                    end
                    if _G.SelectLocalTeleport == "Sky1" then
                        toTarget(CFrame.new(-4878.0415039063, 717.71246337891, -2637.7294921875))
                    end
                    if _G.SelectLocalTeleport == "Sky2" then
                        toTarget(CFrame.new(-7899.6157226563, 5545.6030273438, -422.21798706055))
                    end
                    if _G.SelectLocalTeleport == "Sky3" then
                        toTarget(CFrame.new(-7868.5288085938, 5638.205078125, -1482.5548095703))
                    end
                elseif World2 then
                    if _G.SelectLocalTeleport == "Dock" then
                        toTarget(CFrame.new(-12.519311904907, 19.302536010742, 2827.853515625))
                    end
                    if _G.SelectLocalTeleport == "Mansion" then
                        toTarget(CFrame.new(-390.34829711914, 321.89730834961, 869.00506591797))
                    end
                    if _G.SelectLocalTeleport == "Kingdom Of Rose" then
                        toTarget(CFrame.new(-388.29895019531, 138.35575866699, 1132.1662597656))
                    end
                    if _G.SelectLocalTeleport == "Cafe" then
                        toTarget(CFrame.new(-379.70889282227, 73.0458984375, 304.84692382813))
                    end
                    if _G.SelectLocalTeleport == "Sunflower Field" then
                        toTarget(CFrame.new(-1576.7171630859, 198.61849975586, 13.725157737732))
                    end
                    if _G.SelectLocalTeleport == "Jeramy Mountain" then
                        toTarget(CFrame.new(1986.3519287109, 448.95678710938, 796.70239257813))
                    end
                    if _G.SelectLocalTeleport == "Colossuem" then
                        toTarget(CFrame.new(-1871.8974609375, 45.820514678955, 1359.6843261719))
                    end
                    if _G.SelectLocalTeleport == "Factory" then
                        toTarget(CFrame.new(349.53750610352, 74.446998596191, -355.62420654297))
                    end
                    if _G.SelectLocalTeleport == "The Bridge" then
                        toTarget(CFrame.new(-1860.6354980469, 88.384948730469, -1859.1593017578))
                    end
                    if _G.SelectLocalTeleport == "Green Bit" then
                        toTarget(CFrame.new(-2202.3706054688, 73.097663879395, -2819.2687988281))
                    end
                    if _G.SelectLocalTeleport == "Graveyard" then
                        toTarget(CFrame.new(-5617.5927734375, 492.22183227539, -778.3017578125))
                    end
                    if _G.SelectLocalTeleport == "Dark Area" then
                        toTarget(CFrame.new(3464.7700195313, 13.375151634216, -3368.90234375))
                    end
                    if _G.SelectLocalTeleport == "Snow Mountain" then
                        toTarget(CFrame.new(561.23834228516, 401.44781494141, -5297.14453125))
                    end
                    if _G.SelectLocalTeleport == "Hot Island" then
                        toTarget(CFrame.new(-5505.9633789063, 15.977565765381, -5366.6123046875))
                    end
                    if _G.SelectLocalTeleport == "Cold Island" then
                        toTarget(CFrame.new(-5924.716796875, 15.977565765381, -4996.427734375))
                    end
                    if _G.SelectLocalTeleport == "Ice Castle" then
                        toTarget(CFrame.new(6111.7109375, 294.41259765625, -6716.4829101563))
                    end
                    if _G.SelectLocalTeleport == "Usopp's Island" then
                        toTarget(CFrame.new(4760.4985351563, 8.3444719314575, 2849.2426757813))
                    end
                    if _G.SelectLocalTeleport == "inscription Island" then
                        toTarget(CFrame.new(-5099.01171875, 98.241539001465, 2424.4035644531))
                    end
                    if _G.SelectLocalTeleport == "Forgotten Island" then
                        toTarget(CFrame.new(-3051.9514160156, 238.87203979492, -10250.807617188))
                    end
                    if _G.SelectLocalTeleport == "Ghost Ship" then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                            Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
                    end
                elseif World3 then
                    if _G.SelectLocalTeleport == "Port Town" then
                        toTarget(CFrame.new(-275.21615600586, 43.755737304688, 5451.0659179688))
                    end
                    if _G.SelectLocalTeleport == "Mansion" then
                        local args = {
                            [1] = "requestEntrance",
                            [2] = Vector3.new(-12548.595703125, 337.17001342773, -7554.6103515625)
                        }
        
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                    end
                    if _G.SelectLocalTeleport == "Castle on the Sea" then
                        local args = {
                            [1] = "requestEntrance",
                            [2] = Vector3.new(-5079.44677734375, 313.7293395996094, -3151.065185546875)
                        }
        
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                    end
                    if _G.SelectLocalTeleport == "Hydra Island" then
                        toTarget(CFrame.new(5541.2685546875, 668.30456542969, 195.48069763184))
                    end
                    if _G.SelectLocalTeleport == "Gaint Tree" then
                        toTarget(CFrame.new(2276.0859375, 25.87850189209, -6493.03125))
                    end
                    if _G.SelectLocalTeleport == "Haunted Castle" then
                        toTarget(CFrame.new(-9515.07324, 142.130615, 5537.58398))
                    end
                    if _G.SelectLocalTeleport == "Icecream Island" then
                        toTarget(CFrame.new(-880.894531, 118.245354, -11030.7607, -0.867174983, 1.48501234e-09, 0.498003572,
                            2.70457789e-08, 1, 4.41129586e-08, -0.498003572, 5.1722548e-08, -0.867174983))
                    end
                    if _G.SelectLocalTeleport == "Peanut Island" then
                        toTarget(CFrame.new(-2124.06738, 44.0723495, -10179.8281, -0.623125494, -2.55908191e-07, -0.782121837,
                            -1.40530574e-07, 1, -2.15235005e-07, 0.782121837, -2.42063933e-08, -0.623125494))
                    end
                    if _G.SelectLocalTeleport == "Lab" then
                        toTarget(CFrame.new(-5057.146484375, 314.54132080078, -2934.7995605469))
                    end
                    if _G.SelectLocalTeleport == "Cake Loaf" then
                        toTarget(CFrame.new(-1977.36767578125, 251.509521484375, -12380.4189453125))
                    end
                    if _G.SelectLocalTeleport == "TikiOutpost" then
                        toTarget(CFrame.new(-16753.5977, 189.528107, 451.797333, -0.777145505, 0, -0.629321039, 0, 1, 0, 0.629321039, 0, -0.777145505))
                    end
                end
            end
        
        end})
    
    
        page4:AddButton({Name = "StopTeleport", Callback = function(value)
            toTarget(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame)
        end})
   
    local Boss = {}
        local BossName = page1:AddDropdown({Name = "Select Boss",List = Boss, Callback = function(value)
            _G.Settings.Boss["Select Boss"] = value
        end})
        page1:AddButton({Name = "Refresh Boss",Callback = function()
        BossName:Clear()
        for i, v in pairs(game.ReplicatedStorage:GetChildren()) do
            if v.Name == "Cyborg" or v.Name == "The Gorilla King" or v.Name == "Wysper" or v.Name == "Thunder God" or v.Name == "Mob Leader" or v.Name == "Bobby" or v.Name == "Saber Expert" or v.Name == "Warden" or v.Name == "Chief Warden" or v.Name == "Swan" or v.Name == "Magma Admiral"  or v.Name == "Fishman Lord" or v.Name == "Wysper" or v.Name == "Ice Admiral" or v.Name == "Diamond" or v.Name == "Jeremy" or v.Name == "Fajita" or v.Name == "Don Swan" or v.Name == "Smoke Admiral" or v.Name == "Awakened Ice Admiral" or v.Name == "Tide Keeper" or v.Name == "Darkbeard" or v.Name == "Stone" or v.Name == "Island Empress" or v.Name == "Kilo Admiral" or v.Name == "Captain Elephant" or v.Name == "Beautiful Pirate"  or v.Name == "Cake Queen" or v.Name == "Greybeard" or v.Name == "Order" or v.Name == "Cursed Captain" or v.Name == "Soul Reaper" or v.Name == "Rip indra" or v.Name == "Mihawk Boss" or v.Name == "Cake Prince" or v.Name == "Dough King" or v.Name == "Cursed Skeleton Boss" or v.Name == "Factory" 
             then
                table.insert(Boss, v.Name)
                BossName:Add(v.Name) 
            end
        end
    end})
   
        page1:AddToggle({Name = "Auto Farm Boss", Value =  _G.Settings.Boss["Auto Farm Boss"], Callback = function(value)
            _G.Settings.Boss["Auto Farm Boss"] = value
            if value == false then
                task.wait()
                toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
                task.wait()
            end
        end})
   
    spawn(function()
        while task.wait() do
            if _G.Settings.Boss["Auto Farm Boss"] then
                pcall(function()
                    if game:GetService("Workspace").Enemies:FindFirstChild(_G.Settings.Boss["Select Boss"]) then
                        for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if v.Name == _G.Settings.Boss["Select Boss"] then
                                if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                                    repeat
                                        task.wait()
                                        EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                        StartMagnet = true
                                        FastAttack = true
                                        v.HumanoidRootPart.CanCollide = false
                                        v.Humanoid.WalkSpeed = 0
                                        v.HumanoidRootPart.Size = Vector3.new(80, 80, 80)
                                        toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                            if not FastAttack then
                                        game:GetService("VirtualUser"):CaptureController()
                                        game:GetService("VirtualUser"):Button1Down(Vector2.new(1280, 672))
                                            end
                                        sethiddenproperty(game:GetService("Players").LocalPlayer, "SimulationRadius",
                                            math.huge)
                                    until not _G.Settings.Boss["Auto Farm Boss"] or not v.Parent or v.Humanoid.Health <= 0
                                end
                            end
                        end
                    else
                        if game:GetService("ReplicatedStorage"):FindFirstChild(_G.Settings.Boss["Select Boss"]) then
                            toTarget(game:GetService("ReplicatedStorage"):FindFirstChild(_G.Settings.Boss["Select Boss"])
                                .HumanoidRootPart.CFrame * CFrame.new(0, 35, 0))
                        end
                    end
                end)
            end
        end
    end)
  
        page1:AddToggle({Name = "Auto All Boss",Value =  _G.Settings.Boss["Auto All Boss"], Callback = function(value)
            _G.Settings.Boss["Auto All Boss"] = value
            if value == false then
                task.wait()
                toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
                task.wait()
            end
        end})
   
    spawn(function()
        while task.wait() do
            if _G.Settings.Boss["Auto All Boss"] then
                pcall(function()
                    for i, v in pairs(game.ReplicatedStorage:GetChildren()) do
                        if v.Name == "Cyborg" or v.Name == "The Gorilla King" or v.Name == "Wysper" or v.Name == "Thunder God" or v.Name == "Mob Leader" or v.Name == "Bobby" or v.Name == "Saber Expert" or v.Name == "Warden" or v.Name == "Chief Warden" or v.Name == "Swan" or v.Name == "Magma Admiral"  or v.Name == "Fishman Lord" or v.Name == "Wysper" or v.Name == "Ice Admiral" or v.Name == "Diamond" or v.Name == "Jeremy" or v.Name == "Fajita" or v.Name == "Don Swan" or v.Name == "Smoke Admiral" or v.Name == "Awakened Ice Admiral" or v.Name == "Tide Keeper" or v.Name == "Darkbeard" or v.Name == "Stone" or v.Name == "Island Empress" or v.Name == "Kilo Admiral" or v.Name == "Captain Elephant" or v.Name == "Beautiful Pirate"  or v.Name == "Cake Queen" or v.Name == "Greybeard" or v.Name == "Order" or v.Name == "Cursed Captain" or v.Name == "Soul Reaper" or v.Name == "Rip indra" or v.Name == "Mihawk Boss" or v.Name == "Cake Prince" or v.Name == "Dough King" or v.Name == "Cursed Skeleton Boss" or v.Name == "Factory" 
                        then
                            repeat
                                task.wait()
                                StartMagnet = true
                                FastAttack = true
                                EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                v.Humanoid.WalkSpeed = 0
                                v.HumanoidRootPart.CanCollide = false
                                v.Head.CanCollide = false
                                v.HumanoidRootPart.Size = Vector3.new(80, 80, 80)
                                toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                    if not FastAttack then 
                                game:GetService 'VirtualUser':CaptureController()
                                game:GetService 'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                    end
                                sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
                            until v.Humanoid.Health <= 0 or _G.Settings.Boss["Auto All Boss"] == false or not v.Parent or not v.Name == "Ice Admiral"
                        end
                    end
                end)
            end
        end
    end)
    local SupComplete = false
    local EClawComplete = false
    local TalComplete = false
    local SharkComplete = false
    local DeathComplete = false
    local GodComplete = false
    page5:AddToggle({Name = "Auto Buddy Swords", Value = _G.Settings.Main["Auto Buddy Swords"],Callback =  function(value)
        _G.Settings.Main["Auto Buddy Swords"] = value
        if value == false then
            toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
        end
        SaveSettings()
        task.spawn(function()
            while task.wait() do
                pcall(function()
                    if _G.Settings.Main["Auto Buddy Swords"] then
                        if game:GetService("Workspace").Enemies:FindFirstChild("Cake Queen") then
                            for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                if v.Name == ("Cake Queen" or v.Name == "Cake Queen") and v.Humanoid.Health > 0 and v:IsA("Model") and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") then
                                    repeat
                                        task.wait()
                                        StartMagnet = true
                                        FastAttack = true
                                        if _G.Settings.Configs["Auto Haki"] then
                                            if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                            end
                                        end
                                        if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                            task.wait()
                                            EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                        end
                                        PosMon = v.HumanoidRootPart.CFrame
                                        if not _G.Settings.Configs["Fast Attack"] then
                                            game:GetService 'VirtualUser':CaptureController()
                                            game:GetService 'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                        end
                                        v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                        v.Humanoid.JumpPower = 0
                                        v.Humanoid.WalkSpeed = 0
                                        v.HumanoidRootPart.CanCollide = false
                                        v.Humanoid:ChangeState(11)
                                        toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                    until not _G.Settings.Main["Auto Buddy Swords"] or v.Humanoid.Health <= 0
                                    StartMagnet = false
                                    FastAttack = false
                                end
                            end
                        end
                    end
                end)
            end
        end)
    end})
    page5:AddToggle({Name = "Auto Musketeer Hat", Value = _G.Settings.Main["Auto Musketeer Hat"], Callback = function(value)
        _G.Settings.Main["Auto Musketeer Hat"] = value
        if value == false then
            task.wait()
            toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
            task.wait()
        end
        SaveSettings()
        task.spawn(function()
            while task.wait() do
                pcall(function()
                    if _G.Settings.Main["Auto Musketeer Hat"] then
                        if game:GetService("Players").LocalPlayer.Data.Level.Value >= 1800 and game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CitizenQuestProgress").KilledBandits == false then
                            if string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, "Forest Pirate") and string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, "50") and game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
                                if game:GetService("Workspace").Enemies:FindFirstChild("Forest Pirate") then
                                    for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                        if v.Name == "Forest Pirate" then
                                            repeat
                                                task.wait()
                                                StartMagnet = true
                                                FastAttack = true
                                                if _G.Settings.Configs["Auto Haki"] then
                                                    if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                            "Buso")
                                                    end
                                                end
                                                if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                                    task.wait()
                                                    EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                end
                                                PosMon = v.HumanoidRootPart.CFrame
                                                if not _G.Settings.Configs["Fast Attack"] then
                                                    game:GetService 'VirtualUser':CaptureController()
                                                    game:GetService 'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                                end
                                                v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                                v.Humanoid.JumpPower = 0
                                                v.Humanoid.WalkSpeed = 0
                                                v.HumanoidRootPart.CanCollide = false
                                                v.Humanoid:ChangeState(11)
                                                toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                            until not _G.Settings.Main["Auto Musketeer Hat"] or v.Humanoid.Health <= 0 or not v.Parent or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false
                                            StartMagnet = false
                                            FastAttack = false
                                        end
                                    end
                                else
                                    toTarget(CFrame.new(-13206.452148438, 425.89199829102, -7964.5537109375))
                                end
                            else
                                toTarget(CFrame.new(-12443.8671875, 332.40396118164, -7675.4892578125))
                                if (Vector3.new(-12443.8671875, 332.40396118164, -7675.4892578125) - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 30 then
                                    wait(1.5)
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest",
                                        "CitizenQuest", 1)
                                end
                            end
                        elseif game:GetService("Players").LocalPlayer.Data.Level.Value >= 1800 and game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CitizenQuestProgress").KilledBoss == false then
                            if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible and string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, "Captain Elephant") and game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
                                if game:GetService("Workspace").Enemies:FindFirstChild("Captain Elephant") then
                                    for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                        if v.Name == "Captain Elephant" then
                                            OldCFrameElephant = v.HumanoidRootPart.CFrame
                                            repeat
                                                task.wait()
                                                StartMagnet = true
                                                FastAttack = true
                                                if _G.Settings.Configs["Auto Haki"] then
                                                    if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                                            "Buso")
                                                    end
                                                end
                                                if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                                    task.wait()
                                                    EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                                end
                                                PosMon = v.HumanoidRootPart.CFrame
                                                if not _G.Settings.Configs["Fast Attack"] then
                                                    game:GetService 'VirtualUser':CaptureController()
                                                    game:GetService 'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                                end
                                                v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                                v.Humanoid.JumpPower = 0
                                                v.Humanoid.WalkSpeed = 0
                                                v.HumanoidRootPart.CanCollide = false
                                                v.Humanoid:ChangeState(11)
                                                toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                            until not _G.Settings.Main["Auto Musketeer Hat"] or v.Humanoid.Health <= 0 or not v.Parent or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false
                                            StartMagnet = false
                                            FastAttack = false
                                        end
                                    end
                                else
                                    toTarget(CFrame.new(-13374.889648438, 421.27752685547, -8225.208984375))
                                end
                            else
                                toTarget(CFrame.new(-12443.8671875, 332.40396118164, -7675.4892578125))
                                if (CFrame.new(-12443.8671875, 332.40396118164, -7675.4892578125).Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 4 then
                                    wait(1.5)
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(
                                        "CitizenQuestProgress", "Citizen")
                                end
                            end
                        elseif game:GetService("Players").LocalPlayer.Data.Level.Value >= 1800 and game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CitizenQuestProgress", "Citizen") == 2 then
                            toTarget(CFrame.new(-12512.138671875, 340.39279174805, -9872.8203125))
                        end
                    end
                end)
            end
        end)
    end})
    page5:AddToggle({Name = "Auto Cavander", Value = _G.Settings.Main["Auto Cavander"], Callback = function(value)
        _G.Settings.Main["Auto Cavander"] = value
        if value == false then
            task.wait()
            toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
            task.wait()
        end
        SaveSettings()
        task.spawn(function()
            while task.wait() do
                pcall(function()
                    if _G.Settings.Main["Auto Cavander"] then
                        if game:GetService("Workspace").Enemies:FindFirstChild("Beautiful Pirate") then
                            for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                if v.Name == ("Beautiful Pirate") and v.Humanoid.Health > 0 and v:IsA("Model") and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") then
                                    repeat
                                        task.wait()
                                        StartMagnet = true
                                        FastAttack = true
                                        if _G.Settings.Configs["Auto Haki"] then
                                            if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                            end
                                        end
                                        if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                            task.wait()
                                            EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                        end
                                        PosMon = v.HumanoidRootPart.CFrame
                                        if not _G.Settings.Configs["Fast Attack"] then
                                            game:GetService 'VirtualUser':CaptureController()
                                            game:GetService 'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                        end
                                        v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                        v.Humanoid.JumpPower = 0
                                        v.Humanoid.WalkSpeed = 0
                                        v.HumanoidRootPart.CanCollide = false
                                        v.Humanoid:ChangeState(11)
                                        toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                    until not _G.Settings.Main["Auto Cavander"] or v.Humanoid.Health <= 0
                                    StartMagnet = false
                                    FastAttack = false
                                end
                            end
                        else
                            toTarget(CFrame.new(5283.609375, 22.56223487854, -110.78285217285))
                        end
                    end
                end)
            end
        end)
    end})
    page5:AddToggle({Name = "Auto Yama Sword", Value = _G.Settings.Main["Auto Yama Sword"], Callback = function(value)
        _G.Settings.Main["Auto Yama Sword"] = value
        SaveSettings()
        spawn(function()
            while task.wait() do
                if _G.Settings.Main["Auto Yama Sword"] then
                    if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("EliteHunter", "Progress") >= 30 then
                        repeat
                            task.wait()
                            fireclickdetector(game:GetService("Workspace").Map.Waterfall.SealedKatana.Handle.ClickDetector)
                        until game.Players.LocalPlayer.Backpack:FindFirstChild("Yama") or not AutoYama
                    end
                end
            end
        end)
    end})
    page5:AddToggle({Name = "Auto Tushita Sword", Value = _G.Settings.Main["Auto Tushita Sword"], Callback = function(value)
        _G.Settings.Main["Auto Tushita Sword"] = value
        if value == false then
            task.wait()
            toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
            task.wait()
        end
        SaveSettings()
        task.spawn(function()
            while task.wait() do
                if _G.Settings.Main["Auto Tushita Sword"] then
                    if game:GetService("Workspace").Enemies:FindFirstChild("Longma") then
                        for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if v.Name == ("Longma" or v.Name == "Longma") and v.Humanoid.Health > 0 and v:IsA("Model") and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") then
                                repeat
                                    task.wait()
                                    StartMagnet = true
                                    FastAttack = true
                                    if _G.Settings.Configs["Auto Haki"] then
                                        if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                        end
                                    end
                                    if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                        task.wait()
                                        EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                    end
                                    PosMon = v.HumanoidRootPart.CFrame
                                    if not _G.Settings.Configs["Fast Attack"] then
                                        game:GetService 'VirtualUser':CaptureController()
                                        game:GetService 'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                    end
                                    v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                    v.Humanoid.JumpPower = 0
                                    v.Humanoid.WalkSpeed = 0
                                    v.HumanoidRootPart.CanCollide = false
                                    v.Humanoid:ChangeState(11)
                                    toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                until not _G.Settings.Main["Auto Tushita Sword"] or not v.Parent or v.Humanoid.Health <= 0
                                StartMagnet = false
                                FastAttack = false
                            end
                        end
                    else
                        toTarget(CFrame.new(-10238.875976563, 389.7912902832, -9549.7939453125))
                    end
                end
            end
        end)
    end})
    page5:AddToggle({Name = "Auto Serpent Bow", Value = _G.Settings.Main["Auto Serpent Bow"],Callback = function(value)
        _G.Settings.Main["Auto Serpent Bow"] = value
        if value == false then
            task.wait()
            toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
            task.wait()
        end
        SaveSettings()
        task.spawn(function()
            while task.wait() do
                if _G.Settings.Main["Auto Serpent Bow"] then
                    if game:GetService("Workspace").Enemies:FindFirstChild("Island Empress") then
                        for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if v.Name == ("Island Empress" or v.Name == "Island Empress") and v.Humanoid.Health > 0 and v:IsA("Model") and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") then
                                repeat
                                    task.wait()
                                    StartMagnet = true
                                    FastAttack = true
                                    if _G.Settings.Configs["Auto Haki"] then
                                        if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                        end
                                    end
                                    if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                        task.wait()
                                        EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                    end
                                    PosMon = v.HumanoidRootPart.CFrame
                                    if not _G.Settings.Configs["Fast Attack"] then
                                        game:GetService 'VirtualUser':CaptureController()
                                        game:GetService 'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                    end
                                    v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                    v.Humanoid.JumpPower = 0
                                    v.Humanoid.WalkSpeed = 0
                                    v.HumanoidRootPart.CanCollide = false
                                    v.Humanoid:ChangeState(11)
                                    toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                until not _G.Settings.Main["Auto Serpent Bow"] or not v.Parent or v.Humanoid.Health <= 0
                                StartMagnet = false
                                FastAttack = false
                            end
                        end
                    else
                        toTarget(CFrame.new(5543.86328125, 668.97399902344, 199.0341796875))
                    end
                end
            end
        end)
    end})
    page5:AddToggle({Name = "Auto Dark Dagger", Value = _G.Settings.Main["Auto Dark Dagger"], Calllback = function(value)
        _G.Settings.Main["Auto Dark Dagger"] = value
        if value == false then
            task.wait()
            toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
            task.wait()
        end
        SaveSettings()
        task.spawn(function()
            while task.wait() do
                pcall(function()
                    if _G.Settings.Main["Auto Dark Dagger"] then
                        if game:GetService("Workspace").Enemies:FindFirstChild("rip_indra True Form") then
                            for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                if v.Name == ("rip_indra True Form" or v.Name == "rip_indra True Form") and v.Humanoid.Health > 0 and v:IsA("Model") and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") then
                                    repeat
                                        task.wait()
                                        StartMagnet = true
                                        FastAttack = true
                                        if _G.Settings.Configs["Auto Haki"] then
                                            if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                            end
                                        end
                                        if not game.Players.LocalPlayer.Character:FindFirstChild(_G.Settings.Configs["Select Weapon"]) then
                                            task.wait()
                                            EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                        end
                                        PosMon = v.HumanoidRootPart.CFrame
                                        if not _G.Settings.Configs["Fast Attack"] then
                                            game:GetService 'VirtualUser':CaptureController()
                                            game:GetService 'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                        end
                                        v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                        v.Humanoid.JumpPower = 0
                                        v.Humanoid.WalkSpeed = 0
                                        v.HumanoidRootPart.CanCollide = false
                                        v.Humanoid:ChangeState(11)
                                        toTarget(v.HumanoidRootPart.CFrame * MethodFarm)
                                    until not _G.Settings.Main["Auto Dark Dagger"] or not v.Parent or v.Humanoid.Health <= 0
                                    StartMagnet = false
                                    FastAttack = false
                                end
                            end
                        else
                            toTarget(CFrame.new(-5344.822265625, 423.98541259766, -2725.0930175781))
                        end
                    end
                end)
            end
        end)
    end})
    function GetAllMeleeFarm()
        if SupComplete == false then
            local args = {
                [1] = "BuySuperhuman"
            }
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
            if CheckMasteryWeapon("Superhuman", 400) == "true UpTo" then
                SupComplete = true
            end
        end
        wait(.5)
        if EClawComplete == false then
            local string_1 = "BuyElectricClaw";
            local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
            Target:InvokeServer(string_1);
    
            if CheckMasteryWeapon("Electric Claw", 400) == "true UpTo" then
                EClawComplete = true
            end
        end
        wait(.5)
        if TalComplete == false then
            game.ReplicatedStorage.Remotes.CommF_:InvokeServer("BuyDragonTalon")
    
            if CheckMasteryWeapon("Dragon Talon", 400) == "true UpTo" then
                TalComplete = true
            end
        end
        wait(.5)
        if SharkComplete == false then
            local args = {
                [1] = "BuySharkmanKarate"
            }
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    
            if CheckMasteryWeapon("Sharkman Karate", 400) == "true UpTo" then
                SharkComplete = true
            end
        end
        wait(.5)
        if DeathComplete == false then
            local args = {
                [1] = "BuyDeathStep"
            }
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    
            if CheckMasteryWeapon("Death Step", 400) == "true UpTo" then
                DeathComplete = true
            end
        end
        if GodComplete == false then
            local args = {
                [1] = "BuyGodhuman"
            }
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    
            if CheckMasteryWeapon("Godhuman", 350) == "true UpTo" then
                GodComplete = true
            end
        end
    end
    spawn(function()
        local gg = getrawmetatable(game)
        local old = gg.__namecall
        setreadonly(gg, false)
        gg.__namecall = newcclosure(function(...)
            local method = getnamecallmethod()
            local args = { ... }
            if tostring(method) == "FireServer" then
                if tostring(args[1]) == "RemoteEvent" then
                    if tostring(args[2]) ~= "true" and tostring(args[2]) ~= "false" then
                        if UseSkillMasteryDevilFruit and _G.Settings.Mastery["Auto Farm Fruit Mastery"] then
                            if type(args[2]) == "vector" then
                                args[2] = PositionSkillMasteryDevilFruit
                            else
                                args[2] = CFrame.new(PositionSkillMasteryDevilFruit)
                            end
                            return old(unpack(args))
                        end
                    end
                end
            end
            return old(...)
        end)
    end)
    
    spawn(function()
        local gt = getrawmetatable(game)
        local old = gt.__namecall
        setreadonly(gt, false)
        gt.__namecall = newcclosure(function(...)
            local args = { ... }
            if getnamecallmethod() == "InvokeServer" then
                if _G.SelectWeaponGun then
                    if _G.SelectWeaponGun == "Soul Guitar" then
                        if tostring(args[2]) == "TAP" then
                            if _G.Settings.Mastery["Auto Farm Gun Mastery"] and UseSkillMasteryGun then
                                args[3] = PositionSkillMasteryGun
                            end
                        end
                    end
                end
            end
            return old(unpack(args))
        end)
        setreadonly(gt, true)
    end)
    
    task.spawn(function()
        while wait() do
            for i, v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
                if v:IsA("Tool") then
                    if v:FindFirstChild("RemoteFunctionShoot") then
                        _G.SelectWeaponGun = v.Name
                    end
                end
            end
        end
    end)
    spawn(function()
        local gt = getrawmetatable(game)
        local old = gt.__namecall
        setreadonly(gt,false)
        gt.__namecall = newcclosure(function(...)
            local args = {...}
            if getnamecallmethod() == "InvokeServer" then 
                if _G.SelectWeaponGun then
                    if _G.SelectWeaponGun == "Soul Guitar" then
                        if tostring(args[2]) == "TAP" then
                            if  _G.Settings.Mastery["Auto Farm Gun Mastery"] and _G.UseSkillMasteryGun then
                                args[3] = PositionSkillMasteryGun
                            end
                        end
                    end
                end
            end
            return old(unpack(args))
        end) 
        setreadonly(gt,true)
    end)
    spawn(function()
        while wait() do
            for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do  
                if v:IsA("Tool") then
                    if v.ToolTip == "Gun" then
                        _G.SelectWeaponGun = v.Name
                    end
                end
            end
            for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do  
                if v:IsA("Tool") then
                    if v.ToolTip == "Gun" then
                        _G.SelectWeaponGun = v.Name
                    end
                end
            end
        end
    end)
    function AutoFarmMasteryGun()
      if  game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
            StartMagnet = false
            FastAttack = false
            Questtween = toTarget(CFrameQuest.Position, CFrameQuest)
            if World1 and (Name == "Fishman Commando" or Name == "Fishman Warrior") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 50000 then
                if Questtween then Questtween:Stop() end
                wait(.5)
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                    Vector3.new(61163.8515625, 11.6796875, 1819.7841796875))
            elseif World1 and not (Name == "Fishman Commando" or Name == "Fishman Warrior") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 50000 then
                if Questtween then Questtween:Stop() end
                wait(.5)
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                    Vector3.new(3864.8515625, 6.6796875, -1926.7841796875))
            elseif World2 and string.find(Name, "Ship") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 30000 then
                if Questtween then Questtween:Stop() end
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                    Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
            elseif World2 and not string.find(Name, "Ship") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 30000 then
                if Questtween then Questtween:Stop() end
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                    Vector3.new(-6508.5581054688, 89.034996032715, -132.83953857422))
            elseif (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 250 then
                if Questtween then Questtween:Stop() end
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameQuest
                wait(1)
                if game:GetService("Players").LocalPlayer.Character:WaitForChild("Humanoid").Health > 0 then
                    Com("F_", "StartQuest", QuestName, LevelQuest)
                end
            end
            end
            if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
        if game:GetService("Workspace").Enemies:FindFirstChild(Name) then
            for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do 
                if _G.Settings.Mastery["Auto Farm Gun Mastery"] and v.Name == Name and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
                    PosMon = v.HumanoidRootPart.CFrame
                    MonHumanoidRootPart = v.HumanoidRootPart
                    PositionSkillMasteryGun = v.HumanoidRootPart.Position
                    repeat
                        task.wait()
                        FarmtoTarget = toTarget(v.HumanoidRootPart.CFrame * CFrame.new(0, 30, 0))
                        if v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 150 then
                            if FarmtoTarget then FarmtoTarget:Stop() end
                            StartMagnet = true
                            PosMon = v.HumanoidRootPart.CFrame
                            if game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 150 then
                                game:service('VirtualInputManager'):SendKeyEvent(true, "V", false, game)
                                game:service('VirtualInputManager'):SendKeyEvent(false, "V", false, game)
                            end
                            HealthMin = v.Humanoid.MaxHealth * _G.Settings.Mastery["Mob Health (%)"] / 100
                            PositionSkillMasteryGun = v.HumanoidRootPart.Position
                            if v.Humanoid.Health <= HealthMin and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
                                EquipWeapon(_G.SelectWeaponGun)
                                UseSkillMasteryGun = true
                                -- v.HumanoidRootPart.CanCollide = false
                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame *
                                    CFrame.new(0, 30, 0)
                                if game:GetService("Players").LocalPlayer.Character:FindFirstChild(_G.SelectWeaponGun) and game:GetService("Players").LocalPlayer.Character:FindFirstChild(_G.SelectWeaponGun):FindFirstChild("RemoteFunctionShoot") then
                                    game:GetService("VirtualUser"):CaptureController()
                                    game:GetService("VirtualUser"):Button1Down(Vector2.new(1280, 672))
                                    local args = {
                                        [1] = v.HumanoidRootPart.Position,
                                        [2] = v.HumanoidRootPart
                                    }
                                    game:GetService("Players").LocalPlayer.Character[_G.SelectWeaponGun].RemoteFunctionShoot:InvokeServer(unpack(args))
                                end
                            else
                                UseSkillMasteryGun = false
                                EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * MethodFarm
                            end
                        end
                    until not game:GetService("Workspace").Enemies:FindFirstChild(Name) or not _G.Settings.Mastery["Auto Farm Gun Mastery"] or v.Humanoid.Health <= 0 or not v.Parent
                    UseSkillMasteryGun = false
                    StartMagnet = false
                end
            end
        else
            StartMagnet = false
            Modstween = toTarget(CFrameMon)
            if OldWorld and (Name == "Fishman Commando" or Name == "Fishman Warrior") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 50000 then
                if Modstween then Modstween:Stop() end
                wait(.5)
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                    Vector3.new(61163.8515625, 11.6796875, 1819.7841796875))
            elseif OldWorld and not (Name == "Fishman Commando" or Name == "Fishman Warrior") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 50000 then
                if Modstween then Modstween:Stop() end
                wait(.5)
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                    Vector3.new(3864.8515625, 6.6796875, -1926.7841796875))
            elseif OldWorld and (Name == "God's Guard" or Name == "Sky Bandit" or Name == "Dark Master") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 3000 then
                if Modstween then Modstween:Stop() end
                wait(.5)
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                    Vector3.new(-4607.8227539063, 872.54248046875, -1667.5568847656))
            elseif OldWorld and (Name == "Shanda" or Name == "Royal Squad" or Name == "Royal Soldier") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 5000 then
                if Modstween then Modstween:Stop() end
                wait(.5)
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                    Vector3.new(-7894.6176757813, 5547.1416015625, -380.29119873047))
            elseif NewWorld and string.find(Name, "Ship") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 30000 then
                if Modstween then Modstween:Stop() end
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                    Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
            elseif NewWorld and not string.find(Name, "Ship") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 30000 then
                if Modstween then Modstween:Stop() end
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                    Vector3.new(-6508.5581054688, 89.034996032715, -132.83953857422))
            elseif (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 150 then
                if Modstween then Modstween:Stop() end
                wait(.5)
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameMon
            end
        end
    end
    end
    local Cam = workspace.CurrentCamera
        local hotkey = true
        function lookAt(target, eye)
            Cam.CFrame = CFrame.new(target, eye)
        end
        function CheckMonFF(trg_part)
            local nearest = nil
            local last = math.huge
            for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                if v.Name == QuestCheck()[3] then
                    local ePos, vissss = workspace.CurrentCamera:WorldToViewportPoint(v[trg_part].Position)
                    local AccPos = Vector2.new(ePos.x, ePos.y)
                    local mousePos = Vector2.new(workspace.CurrentCamera.ViewportSize.x / 2, workspace.CurrentCamera.ViewportSize.y / 2)
                    local distance = (AccPos - mousePos).magnitude
                    if distance < last and vissss and hotkey == true and distance < 1500 then
                        last = distance
                        nearest = v
                    end
                end
            end
            return nearest
        end
        spawn(function()
            while wait() do
                if _G.Settings.Mastery["Auto Farm Gun Mastery"]  and _G.UseSkillMasteryGun == true then
                    local closest = CheckMonFF("HumanoidRootPart")
                    lookAt(Cam.CFrame.p, closest:FindFirstChild("HumanoidRootPart").Position)
                    local args = {
                        [1] = PositionSkillMasteryGun
                    }
                    
                    game:GetService("Players").LocalPlayer.Character[_G.SelectWeaponGun].RemoteEvent:FireServer(unpack(args))
                    if not string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, QuestCheck()[6]) then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
                    end
                end
            end
        end)
        spawn(function()
            while wait() do
                if _G.Settings.Mastery["Auto Farm Gun Mastery"]  and _G.UseSkillMasteryGun == true then
                    local args = {
                        [1] = PositionSkillMasteryGun,
                        [2] = MonHumanoidRootPart
                    }
                    game:GetService("Players").LocalPlayer.Character[_G.SelectWeaponGun].RemoteFunctionShoot:InvokeServer(unpack(args))
                end
            end
        end)
    function AutoFarmMasteryDevilFruit()
        if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
            StartMagnet = false
            FastAttack = false
            Questtween = toTarget(CFrameQuest.Position, CFrameQuest)
            if World1 and (Name == "Fishman Commando" or Name == "Fishman Warrior") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 50000 then
                if Questtween then Questtween:Stop() end
                wait(.5)
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                    Vector3.new(61163.8515625, 11.6796875, 1819.7841796875))
            elseif World1 and not (Name == "Fishman Commando" or Name == "Fishman Warrior") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 50000 then
                if Questtween then Questtween:Stop() end
                wait(.5)
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                    Vector3.new(3864.8515625, 6.6796875, -1926.7841796875))
            elseif World2 and string.find(Name, "Ship") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 30000 then
                if Questtween then Questtween:Stop() end
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                    Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
            elseif World2 and not string.find(Name, "Ship") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 30000 then
                if Questtween then Questtween:Stop() end
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                    Vector3.new(-6508.5581054688, 89.034996032715, -132.83953857422))
            elseif (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 250 then
                if Questtween then Questtween:Stop() end
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameQuest
                wait(1)
                if game:GetService("Players").LocalPlayer.Character:WaitForChild("Humanoid").Health > 0 then
                    Com("F_", "StartQuest", QuestName, LevelQuest)
                end
            end
            end
            if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
        if game:GetService("Workspace").Enemies:FindFirstChild(Name) then
            for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                if _G.Settings.Mastery["Auto Farm Fruit Mastery"] and v.Name == Name and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
                    repeat
                        task.wait()
                        FarmtoTarget = toTarget(v.HumanoidRootPart.Position, v.HumanoidRootPart.CFrame * CFrame.new(0, 30, 0)) 
                        if v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 150 then
                            if FarmtoTarget then FarmtoTarget:Stop() end
                            StartMagnet = true
                            PosMon = v.HumanoidRootPart.CFrame
                            HealthMin = v.Humanoid.MaxHealth * _G.Settings.Mastery["Mob Health (%)"] / 100
                            if v.Humanoid.Health <= HealthMin and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
                                EquipWeapon(game.Players.LocalPlayer.Data.DevilFruit.Value)
                                if game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool") then
                                    PositionSkillMasteryDevilFruit = v.HumanoidRootPart.Position
                                    UseSkillMasteryDevilFruit = true
                                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild(game.Players.LocalPlayer.Data.DevilFruit.Value) then
                                        MasteryDevilFruit = require(game:GetService("Players").LocalPlayer.Character
                                            [game.Players.LocalPlayer.Data.DevilFruit.Value].Data)
                                        DevilFruitMastery = game:GetService("Players").LocalPlayer.Character
                                            [game.Players.LocalPlayer.Data.DevilFruit.Value].Level.Value
                                    elseif game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(game.Players.LocalPlayer.Data.DevilFruit.Value) then
                                        MasteryDevilFruit = require(game:GetService("Players").LocalPlayer.Backpack
                                            [game.Players.LocalPlayer.Data.DevilFruit.Value].Data)
                                        DevilFruitMastery = game:GetService("Players").LocalPlayer.Backpack
                                            [game.Players.LocalPlayer.Data.DevilFruit.Value].Level.Value
                                    end
                                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Dragon-Dragon") then
                                        if _G.Settings.Configs["Skill Z"] and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 and DevilFruitMastery >= MasteryDevilFruit.Lvl.Z then
                                            game:service('VirtualInputManager'):SendKeyEvent(true, "Z", false, game)
                                            wait(.1)
                                            game:service('VirtualInputManager'):SendKeyEvent(false, "Z", false, game)
                                        end
                                        if _G.Settings.Configs["Skill X"] and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 and DevilFruitMastery >= MasteryDevilFruit.Lvl.X then
                                            game:service('VirtualInputManager'):SendKeyEvent(true, "X", false, game)
                                            wait(.1)
                                            game:service('VirtualInputManager'):SendKeyEvent(false, "X", false, game)
                                        end
                                    elseif game:GetService("Players").LocalPlayer.Character:FindFirstChild("Human-Human: Buddha") then
                                        if _G.Settings.Configs["Skill Z"] and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 and game.Players.LocalPlayer.Character.HumanoidRootPart.Size == Vector3.new(7.6, 7.676, 3.686) and DevilFruitMastery >= MasteryDevilFruit.Lvl.Z then
                                        else
                                            game:service('VirtualInputManager'):SendKeyEvent(true, "Z", false, game)
                                            wait(.1)
                                            game:service('VirtualInputManager'):SendKeyEvent(false, "Z", false, game)
                                        end
                                        if _G.Settings.Configs["Skill X"] and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 and DevilFruitMastery >= MasteryDevilFruit.Lvl.X then
                                            game:service('VirtualInputManager'):SendKeyEvent(true, "X", false, game)
                                            wait(.1)
                                            game:service('VirtualInputManager'):SendKeyEvent(false, "X", false, game)
                                        end
                                        if _G.Settings.Configs["Skill C"] and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 and DevilFruitMastery >= MasteryDevilFruit.Lvl.C then
                                            game:service('VirtualInputManager'):SendKeyEvent(true, "C", false, game)
                                            wait(.1)
                                            game:service('VirtualInputManager'):SendKeyEvent(false, "C", false, game)
                                        end
                                    elseif game:GetService("Players").LocalPlayer.Character:FindFirstChild("Venom-Venom") then
                                        if _G.Settings.Configs["Skill Z"] and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 and DevilFruitMastery >= MasteryDevilFruit.Lvl.Z then
                                            game:service('VirtualInputManager'):SendKeyEvent(true, "Z", false, game)
                                            wait(4)
                                            game:service('VirtualInputManager'):SendKeyEvent(false, "Z", false, game)
                                        end
                                        if _G.Settings.Configs["Skill X"] and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 and DevilFruitMastery >= MasteryDevilFruit.Lvl.X then
                                            game:service('VirtualInputManager'):SendKeyEvent(true, "X", false, game)
                                            wait(.1)
                                            game:service('VirtualInputManager'):SendKeyEvent(false, "X", false, game)
                                        end
                                        if _G.Settings.Configs["Skill C"] and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 and DevilFruitMastery >= MasteryDevilFruit.Lvl.C then
                                            game:service('VirtualInputManager'):SendKeyEvent(true, "C", false, game)
                                            wait(.1)
                                            game:service('VirtualInputManager'):SendKeyEvent(false, "C", false, game)
                                        end
                                    elseif game:GetService("Players").LocalPlayer.Character:FindFirstChild(game.Players.LocalPlayer.Data.DevilFruit.Value) then
                                        game:GetService("Players").LocalPlayer.Character:FindFirstChild(game.Players.LocalPlayer.Data.DevilFruit.Value).MousePos.Value =
                                            v.HumanoidRootPart.Position
    
                                        if _G.Settings.Configs["Skill Z"] and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 and DevilFruitMastery >= MasteryDevilFruit.Lvl.Z then
                                            game:service('VirtualInputManager'):SendKeyEvent(true, "Z", false, game)
                                            wait(.1)
                                            game:service('VirtualInputManager'):SendKeyEvent(false, "Z", false, game)
                                        end
                                        if _G.Settings.Configs["Skill X"] and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 and DevilFruitMastery >= MasteryDevilFruit.Lvl.X then
                                            game:service('VirtualInputManager'):SendKeyEvent(true, "X", false, game)
                                            wait(.1)
                                            game:service('VirtualInputManager'):SendKeyEvent(false, "X", false, game)
                                        end
                                        if _G.Settings.Configs["Skill C"] and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 and DevilFruitMastery >= MasteryDevilFruit.Lvl.C then
                                            game:service('VirtualInputManager'):SendKeyEvent(true, "C", false, game)
                                            wait(.1)
                                            game:service('VirtualInputManager'):SendKeyEvent(false, "C", false, game)
                                        end
                                        if _G.Settings.Configs["Skill V"] and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 and DevilFruitMastery >= MasteryDevilFruit.Lvl.V then
                                            game:service('VirtualInputManager'):SendKeyEvent(true, "V", false, game)
                                            wait(.1)
                                            game:service('VirtualInputManager'):SendKeyEvent(false, "V", false, game)
                                        if _G.Settings.Configs["Skill F"] and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 and DevilFruitMastery >= MasteryDevilFruit.Lvl.F then
                                            game:service('VirtualInputManager'):SendKeyEvent(true, "F", false, game)
                                             wait(.1)
                                            game:service('VirtualInputManager'):SendKeyEvent(false, "F", false, game)
                                        end
                                        end
                                    end
                                end
                            else
                                game:GetService('VirtualUser'):CaptureController()
                                game:GetService('VirtualUser'):ClickButton1(Vector2.new(851, 158),
                                    game:GetService("Workspace").Camera.CFrame)
                                UseSkillMasteryDevilFruit = false
                                EquipWeapon(_G.Settings.Configs["Select Weapon"])
                                v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * MethodFarm
                            end
                        end
                    until v.Humanoid.Health <= 0 or not _G.Settings.Mastery["Auto Farm Fruit Mastery"]
                    StartMagnet = false
                end
            end
        else
            StartMagnet = false
            Modstween = toTarget(CFrameMon.Position, CFrameMon)
            if OldWorld and (Name == "Fishman Commando" or Name == "Fishman Warrior") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 50000 then
                if Modstween then Modstween:Stop() end
                wait(.5)
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                    Vector3.new(61163.8515625, 11.6796875, 1819.7841796875))
            elseif OldWorld and not (Name == "Fishman Commando" or Name == "Fishman Warrior") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 50000 then
                if Modstween then Modstween:Stop() end
                wait(.5)
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                    Vector3.new(3864.8515625, 6.6796875, -1926.7841796875))
            elseif OldWorld and (Name == "God's Guard" or Name == "Sky Bandit" or Name == "Dark Master") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 3000 then
                if Modstween then Modstween:Stop() end
                wait(.5)
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                    Vector3.new(-4607.8227539063, 872.54248046875, -1667.5568847656))
            elseif OldWorld and (Name == "Shanda" or Name == "Royal Squad" or Name == "Royal Soldier") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 5000 then
                if Modstween then Modstween:Stop() end
                wait(.5)
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                    Vector3.new(-7894.6176757813, 5547.1416015625, -380.29119873047))
            elseif NewWorld and string.find(Name, "Ship") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 30000 then
                if Modstween then Modstween:Stop() end
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                    Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
            elseif NewWorld and not string.find(Name, "Ship") and (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 30000 then
                if Modstween then Modstween:Stop() end
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                    Vector3.new(-6508.5581054688, 89.034996032715, -132.83953857422))
            elseif (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 150 then
                if Modstween then Modstween:Stop() end
                wait(.5)
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameMon
            end
        end
    end
    end
    function CheckMasteryWeapon(NameWe, MasNum)
        if game.Players.LocalPlayer.Backpack:FindFirstChild(NameWe) then
            if tonumber(game.Players.LocalPlayer.Backpack:FindFirstChild(NameWe).Level.Value) < tonumber(MasNum) then
                return "true DownTo"
            elseif tonumber(game.Players.LocalPlayer.Backpack:FindFirstChild(NameWe).Level.Value) >= tonumber(MasNum) then
                return "true UpTo"
            end
        end
        if game.Players.LocalPlayer.Character:FindFirstChild(NameWe) then
            if tonumber(game.Players.LocalPlayer.Character:FindFirstChild(NameWe).Level.Value) < tonumber(MasNum) then
                return "true DownTo"
            elseif tonumber(game.Players.LocalPlayer.Character:FindFirstChild(NameWe).Level.Value) >= tonumber(MasNum) then
                return "true UpTo"
            end
        end
        return "else"
    end
    local function CheckQuestMasteryFarm()
        if OldWorld then
            Monster = "Galley Captain";
            CFrameMon = CFrame.new(5649, 39, 4936);
        end
        if NewWorld then
            Monster = "Water Fighter";
            CFrameMon = CFrame.new(-3385, 239, -10542);
        end
        if ThreeWorld then
            Monster = "Reborn Skeleton";
            CFrameMon = CFrame.new(-9506.14648, 172.130661, 6101.79053);
        end
    end
    function AutoFarmMasterySwordList()
        if game:GetService("Workspace").Enemies:FindFirstChild(Monster) or (ThreeWorld and (game:GetService("Workspace").Enemies:FindFirstChild("Reborn Skeleton") or game:GetService("Workspace").Enemies:FindFirstChild("Living Zombie") or game:GetService("Workspace").Enemies:FindFirstChild("Demonic Soul") or game:GetService("Workspace").Enemies:FindFirstChild("Posessed Mummy"))) then
            for i, v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                if _G.Settings.Mastery["Farm Mastery SwordList"] and ((ThreeWorld and (v.Name == "Reborn Skeleton" or v.Name == "Living Zombie" or v.Name == "Demonic Soul" or v.Name == "Posessed Mummy")) or v.Name == Name) and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
                    repeat
                        task.wait()
                        FarmtoTarget = toTarget(v.HumanoidRootPart.CFrame * CFrame.new(0, 30, 1))
                        if v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 150 then
                            if FarmtoTarget then FarmtoTarget:Stop() end
                            FastAttack = true
                            EquipWeaponSword()
                            StartMagnet = true
                            PosMon = v.HumanoidRootPart.CFrame
                            if game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 150 then
                                game:service('VirtualInputManager'):SendKeyEvent(true, "V", false, game)
                                game:service('VirtualInputManager'):SendKeyEvent(false, "V", false, game)
                            end
                            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame *
                                CFrame.new(0, 30, 1)
                        end
                    until not game:GetService("Workspace").Enemies:FindFirstChild(Monster) and ((ThreeWorld and not (v.Name == "Reborn Skeleton" or v.Name == "Living Zombie" or v.Name == "Demonic Soul" or v.Name == "Posessed Mummy")) or v.Name == Monster) or not _G.Settings.Mastery["Farm Mastery SwordList"] or v.Humanoid.Health <= 0 or not v.Parent
                    StartMagnet = false
                    FastAttack = false 
                end
            end
        else
            StartMagnet = false
            Modstween = toTarget(CFrameMon)
            if OldWorld and (Monster == "Fishman Commando" or Monster == "Fishman Warrior") and (CFrameMon.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 50000 then
                if Modstween then Modstween:Stop() end
                wait(.5)
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                    Vector3.new(61163.8515625, 11.6796875, 1819.7841796875))
            elseif OldWorld and not (Monster == "Fishman Commando" or Monster == "Fishman Warrior") and (CFrameMon.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 50000 then
                if Modstween then Modstween:Stop() end
                wait(.5)
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                    Vector3.new(3864.8515625, 6.6796875, -1926.7841796875))
            elseif OldWorld and (Monster == "God's Guard"  or Monster == "Sky Bandit" or Monster == "Dark Master") and (CFrameMon.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 3000 then
                if Modstween then Modstween:Stop() end
                wait(.5)
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                    Vector3.new(-4607.8227539063, 872.54248046875, -1667.5568847656))
            elseif OldWorld and (Monster == "Shanda" or Monster == "Royal Squad" or Monster == "Royal Soldier") and (CFrameMon.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 5000 then
                if Modstween then Modstween:Stop() end
                wait(.5)
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                    Vector3.new(-7894.6176757813, 5547.1416015625, -380.29119873047))
            elseif NewWorld and string.find(Monster, "Ship") and (CFrameMon.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 30000 then
                if Modstween then Modstween:Stop() end
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                    Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
            elseif NewWorld and not string.find(Monster, "Ship") and (CFrameMon.Position - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).magnitude > 30000 then
                if Modstween then Modstween:Stop() end
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",
                    Vector3.new(-6508.5581054688, 89.034996032715, -132.83953857422))
                -- elseif game.Players.LocalPlayer:DistanceFromCharacter(CFrameMon.Position) > 3500 then
                --     if Modstween then Modstween:Stop() end
                --     if game.Players.LocalPlayer.Character:WaitForChild("Humanoid"):GetState() == Enum.HumanoidStateType.Dead then return end
                --     ResetSetSpawn(CFrameMon)
            elseif (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 150 then
                if Modstween then Modstween:Stop() end
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrameMon
            end
        end
    end
    local function inmyself(name)
        return game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(name) or
            game:GetService("Players").LocalPlayer.Character:FindFirstChild(name);
    end
   
        page6Add:Toggle({Name = "Auto Fruit Mastery", Value = _G.Settings.Mastery["Auto Farm Fruit Mastery"], Callback = function(value)
            _G.Settings.Mastery["Auto Farm Fruit Mastery"] = value
            if value == false then
                toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
            end
            SaveSettings()
        end})
    
        page6:AddToggle({Name = "Auto Gun Mastery", Value = _G.Settings.Mastery["Auto Farm Gun Mastery"], Callback = function(value)
            _G.Settings.Mastery["Auto Farm Gun Mastery"] = value
            if value == false then
                toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
            end
            SaveSettings()
        end})
  
   
        page6:AddLabelX({Name = "Skill List"})
    
   
        page6:AddToggle({Name = "Skill Z", Value = _G.Settings.Configs["Skill Z"],CAllback =  function(value)
            _G.Settings.Configs["Skill Z"] = value
            SaveSettings()
        end})
        page6:AddToggle({Name = "Skill X", Value = _G.Settings.Configs["Skill X"],CAllback =  function(value)
            _G.Settings.Configs["Skill X"] = value
            SaveSettings()
        end})
        page6:AddToggle({Name = "Skill C", Value = _G.Settings.Configs["Skill C"],CAllback =  function(value)
            _G.Settings.Configs["Skill C"] = value
            SaveSettings()
        end})
        page6:AddToggle({Name = "Skill V", Value = _G.Settings.Configs["Skill V"],CAllback =  function(value)
            _G.Settings.Configs["Skill V"] = value
            SaveSettings()
        end})
        page6:AddToggle({Name = "Skill F", Value = _G.Settings.Configs["Skill F"],CAllback =  function(value)
            _G.Settings.Configs["Skill F"] = value
            SaveSettings()
        end})

    spawn(function()
        while task.wait() do
            if _G.Settings.Mastery["Auto Farm Gun Mastery"] then
                CheckQuest()
                AutoFarmMasteryGun()
            end
        end
    end)
    if _G.Settings.Mastery["Auto Farm Gun Mastery"] or _G.Settings.Mastery["Auto Farm Fruit Mastery"] then
        _G.Select_Fast_Attack = "Normal"
    else
        _G.Select_Fast_Attack = "Fast"
    end
    spawn(function()
        while task.wait() do
            if _G.Settings.Mastery["Auto Farm Fruit Mastery"] then
                CheckQuest()
                AutoFarmMasteryDevilFruit()
            end
        end
    end)
   
        page7:AddToggle({Name = "Auto Random Fruits", Value = _G.Settings.Fruits["Auto Buy Random Fruits"],Callback  = function(value)
            _G.Settings.Fruits["Auto Buy Random Fruits"] = value
            SaveSettings()
        end})
        page7:AddButton({Name = "Devil Fruit Shop", Callback = function()
            local args = {
                [1] = "GetFruits"
            }
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
            game.Players.localPlayer.PlayerGui.Main.FruitShop.Visible = true
        end})
  
    spawn(function()
        while task.wait() do
            if _G.Settings.Fruits["Auto Buy Random Fruits"] then
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Cousin", "Buy")
            end
        end
    end)
   
        page7:AddToggle({Name = "Auto Store Fruits", Value = _G.Settings.Fruits["Auto Store Fruits"],Callback  =  function(value)
            _G.Settings.Fruits["Auto Store Fruits"] = value
            SaveSettings()
        end})  
        page7:AddToggle({Name = "Tween To Fruit Spawn", Value = _G.Settings.Fruits["Tween To Fruit Spawn"],Callback =  function(value)
            _G.Settings.Fruits["Tween To Fruit Spawn"] = value
        end})
  
    spawn(function()
        while wait(0.1) do
            if _G.Settings.Fruits["Tween To Fruit Spawn"] then
                local player = game.Players.LocalPlayer
                local character = player.Character
                local humanoidRootPart = character:WaitForChild("HumanoidRootPart")
    
                for _, fruit in pairs(game.Workspace:GetChildren()) do
                    if string.find(fruit.Name, "Fruit") then
                        local targetCFrame = fruit.Handle.CFrame
    
                        local player = game.Players.LocalPlayer
                        local character = player.Character
                        local humanoidRootPart = character:WaitForChild("HumanoidRootPart")
    
                        for _, fruit in pairs(game.Workspace:GetChildren()) do
                            if string.find(fruit.Name, "Fruit") then
                                local targetCFrame = fruit.Handle.CFrame
    
                                local Distance = (targetCFrame.Position - humanoidRootPart.Position).Magnitude
    
                                local tweenInfo = TweenInfo.new(Distance / 315, Enum.EasingStyle.Linear)
                                local tween = game:GetService("TweenService"):Create(humanoidRootPart, tweenInfo,
                                    { CFrame = targetCFrame })
                                tween:Play()
    
                                if Distance <= 250 then
                                    tween:Cancel()
                                    humanoidRootPart.CFrame = targetCFrame
                                else
                                    tween:Cancel()
                                end
                            end
                        end
                    end
                end
            end
        end
    end)
    spawn(function()
        while task.wait() do
            if _G.Settings.Fruits["Auto Store Fruits"] then
                pcall(function()
                    task.wait()
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Bomb Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Bomb Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Bomb-Bomb",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Bomb Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Bomb Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Spike Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Spike Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Spike-Spike",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Spike Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Spike Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Chop Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Chop Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Chop-Chop",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Chop Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Chop Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Spring Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Spring Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Spring-Spring",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Spring Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Spring Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Kilo Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Kilo Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Kilo-Kilo",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Kilo Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Kilo Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Smoke Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Smoke Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Smoke-Smoke",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Smoke Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Smoke Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Spin Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Spin Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Spin-Spin",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Spin Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Spin Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Flame Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Flame Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Flame-Flame",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Flame Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Flame Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Bird: Falcon Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Bird: Falcon Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Bird-Bird: Falcon",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Bird: Falcon Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Bird: Falcon Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Ice Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Ice Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Ice-Ice",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Ice Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Ice Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Sand Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Sand Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Sand-Sand",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Sand Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Sand Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Dark Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Dark Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Dark-Dark",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Dark Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Dark Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Revive Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Revive Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Revive-Revive",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Revive Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Revive Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Diamond Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Diamond Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Diamond-Diamond",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Diamond Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Diamond Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Light Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Light Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Light-Light",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Light Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Light Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Love Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Love Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Love-Love",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Love Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Love Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Rubber Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Rubber Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Rubber-Rubber",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Rubber Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Rubber Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Barrier Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Barrier Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Barrier-Barrier",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Barrier Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Barrier Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Magma Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Magma Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Magma-Magma",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Magma Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Magma Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Door Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Door Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Door-Door",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Door Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Door Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Quake Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Quake Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Quake-Quake",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Quake Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Quake Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Human-Human: Buddha Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Human-Human: Buddha Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Human-Human: Buddha",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Human-Human: Buddha Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Human-Human: Buddha Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("String Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("String Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "String-String",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("String Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("String Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Bird: Phoenix Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Bird: Phoenix Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Bird-Bird: Phoenix",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Bird: Phoenix Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Bird: Phoenix Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Rumble Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Rumble Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Rumble-Rumble",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Rumble Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Rumble Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Paw Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Paw Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Paw-Paw",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Paw Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Paw Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Gravity Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Gravity Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Gravity-Gravity",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Gravity Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Gravity Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Dough Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Dough Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Dough-Dough",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Dough Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Dough Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Shadow Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Shadow Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Shadow-Shadow",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Shadow Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Shadow Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Venom Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Venom Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Venom-Venom",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Venom Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Venom Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Control Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Control Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Control-Control",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Control Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Control Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Dragon Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Dragon Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Dragon-Dragon",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Dragon Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Dragon Fruit"))
                    end
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Leopard Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Leopard Fruit") then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit", "Leopard-Leopard",
                            game:GetService("Players").LocalPlayer.Character:FindFirstChild("Leopard Fruit") or
                            game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Leopard Fruit"))
                    end
                end)
            end
        end
    end)
  
        page7:AddLabelX({Name =  "Devil Fruits Sniper"})
        -- [DevilFruit Check]
        SelectDevilFruits = { "Bomb-Bomb", "Spike-Spike", "Chop-Chop", "Spring-Spring", "Kilo-Kilo", "Spin-Spin",
            "Kilo-Kilo",
            "Spin-Spin", "Bird: Falcon", "Smoke-Smoke", "Flame-Flame", "Ice-Ice", "Sand-Sand", "Dark-Dark", "Revive-Revive",
            "Diamond-Diamond", "Light-Light", "Love-Love", "Rubber-Rubber", "Barrier-Barrier", "Magma-Magma", "Door-Door",
            "Quake-Quake", "Human-Human: Buddha", "String-String", "Bird-Bird: Phoenix", "Rumble-Rumble", "Paw-Paw",
            "Gravity-Gravity", "Dough-Dough", "Shadow-Shadow", "Venom-Venom", "Control-Control", "Soul-Soul", "Dragon-Dragon" }
        page7:AddDropdown({Name = "Select Devil Fruits",List = SelectDevilFruits,Callback  = function(value)
            _G.Settings.Fruits["Select Devil Fruits"] = value
            SaveSettings()
        end})
        page7:AddToggle({Name = "Auto Buy Devil Fruits Sniper", Value = _G.Settings.Fruits["Auto Buy Devil Fruits Sniper"],Callback =  function(value)
            _G.Settings.Fruits["Auto Buy Devil Fruits Sniper"] = value
            SaveSettings()
        end})
   
        page8:AddToggle({Name = "Auto Raids", Value = _G.Settings.Raids["Auto Raids"], Callback = function(value)
            _G.Settings.Raids["Auto Raids"] = value
            if value == false then
                task.wait()
                toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
                task.wait()
            end
            SaveSettings()
        end})
        local SelectRaids = {
            "Flame",
            "Ice",
            "Quake",
            "Light",
            "Dark",
            "String",
            "Rumble",
            "Magma",
            "Human: Buddha",
            "Sand",
            "Bird: Phoenix",
            "Dough"
        }
        page8:AddDropdown({Name = "Select Raids",List = SelectRaids, Callback = function(value)
            _G.Settings.Raids["Select Raids"] = value
            SaveSettings()
        end})
        page8:AddToggle({Name = "Kill Aura", Value = _G.Settings.Raids["Kill Aura"], Callback = function(value)
            _G.Settings.Raids["Kill Aura"] = value
            SaveSettings()
        end})
        page8:AddToggle({Name = "Auto Next Place", Value = _G.Settings.Raids["Auto Next Place"], Callback = function(value)
            _G.Settings.Raids["Auto Next Place"] = value
            if value == false then
                toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
            end
            SaveSettings()
        end})
        page8:AddToggle({Name = "Auto Awakened", Value = _G.Settings.Raids["Auto Awakened"], Callback = function(value)
            _G.Settings.Raids["Auto Awakened"] = value
            SaveSettings()
        end})
 
    task.spawn(function()
        while task.wait() do
            if _G.Settings.Raids["Auto Raids"] and not _G.Settings.Main["Auto Farm Level"] then
                if game.Players.LocalPlayer.Backpack:FindFirstChild("Special Microchip") or game.Players.LocalPlayer.Character:FindFirstChild("Special Microchip") or game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 5") or game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 4") or game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 3") or game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 2") or game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1") then
                    if game.Players.LocalPlayer.Backpack:FindFirstChild("Special Microchip") or game.Players.LocalPlayer.Character:FindFirstChild("Special Microchip") and game.Players.LocalPlayer.PlayerGui.Main.Timer.Visible == false then
                        if World2 then
                            fireclickdetector(Workspace.Map.CircleIsland.RaidSummon2.Button.Main.ClickDetector)
                        elseif World3 then
                            fireclickdetector(Workspace.Map["Boat Castle"].RaidSummon2.Button.Main.ClickDetector)
                        end
                        wait(17)
                    elseif game.Players.LocalPlayer.PlayerGui.Main.Timer.Visible == true then
                        pcall(function()
                            repeat
                                task.wait()
                                if game.Players.LocalPlayer.PlayerGui.Main.Timer.Visible == false then
                                elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 5") then
                                    game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 5").CFrame =
                                        CFrame.new(
                                            game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 5")
                                            .CFrame
                                            .x, 60,
                                            game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 5")
                                            .CFrame.z)
                                    if (game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 5").Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 350 then
                                        Farmtween = toTarget(game:GetService("Workspace")["_WorldOrigin"].Locations
                                            :FindFirstChild("Island 5").CFrame)
                                    elseif (game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 5").Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 350 then
                                        if Farmtween then
                                            Farmtween:Stop()
                                        end
                                        toTarget(game:GetService("Workspace")["_WorldOrigin"].Locations["Island 5"].CFrame *
                                            CFrame.new(4, 65, 10))
                                    end
                                elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 4") then
                                    game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 4").CFrame =
                                        CFrame.new(
                                            game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 4").CFrame.x, 60,
                                            game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 4").CFrame.z)
                                    if (game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 4").Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 350 then
                                        Farmtween = toTarget(game:GetService("Workspace")["_WorldOrigin"].Locations
                                            :FindFirstChild("Island 4").CFrame)
                                    elseif (game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 4").Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 350 then
                                        if Farmtween then
                                            Farmtween:Stop()
                                        end
                                        toTarget(game:GetService("Workspace")["_WorldOrigin"].Locations["Island 4"].CFrame *CFrame.new(4, 65, 10))
                                    end
                                elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 3") then
                                    game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 3").CFrame =
                                        CFrame.new(
                                            game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 3").CFrame.x, 60,
                                            game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 3").CFrame.z)
                                    if (game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 3").Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 350 then
                                        Farmtween = toTarget(game:GetService("Workspace")["_WorldOrigin"].Locations
                                            :FindFirstChild("Island 3").CFrame)
                                    elseif (game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 3").Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 350 then
                                        if Farmtween then
                                            Farmtween:Stop()
                                        end
                                        toTarget(game:GetService("Workspace")["_WorldOrigin"].Locations["Island 3"].CFrame *CFrame.new(4, 65, 10))
                                    end
                                elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 2") then
                                    game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 2").CFrame =
                                        CFrame.new(game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 2").CFrame.x, 60,
                                            game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 2").CFrame.z)
                                    if (game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 2").Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 350 then
                                        Farmtween = toTarget(game:GetService("Workspace")["_WorldOrigin"].Locations
                                            :FindFirstChild("Island 2").CFrame)
                                    elseif (game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 2").Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 350 then
                                        if Farmtween then
                                            Farmtween:Stop()
                                        end
                                        toTarget(game:GetService("Workspace")["_WorldOrigin"].Locations["Island 2"].CFrame *CFrame.new(4, 65, 10))
                                    end
                                elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1") then
                                    game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1").CFrame =
                                        CFrame.new(
                                            game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1").CFrame.x, 60,
                                            game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1").CFrame.z)
                                    if (game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1").Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 350 then
                                        Farmtween = toTarget(game:GetService("Workspace")["_WorldOrigin"].Locations
                                            :FindFirstChild("Island 1").CFrame)
                                    elseif (game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1").Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 350 then
                                        if Farmtween then
                                            Farmtween:Stop()
                                        end
                                        toTarget(game:GetService("Workspace")["_WorldOrigin"].Locations["Island 1"].CFrame *CFrame.new(4, 65, 10))
                                    end
                                end
                                for i, v in pairs(game.Workspace.Enemies:GetChildren()) do
                                    if _G.Settings.Raids["Auto Raids"] and game.Players.LocalPlayer.PlayerGui.Main.Timer.Visible == true and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and (v.HumanoidRootPart.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 400 then
                                        repeat
                                            task.wait()
                                            v.Humanoid.Health = 0
                                            v:BreakJoints()
                                        until not _G.Settings.Raids["Auto Raids"] or v.Humanoid.Health <= 0 or not v.Parent
                                    end
                                end
                                if _G.Settings.Raids["Auto Awakened"] then
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Awakener", "Awaken")
                                end
                            until not game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 5") or not game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 4") or not game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 3") or not game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 2") or not game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1") or game.Players.LocalPlayer.PlayerGui.Main.Timer.Visible == false
                            if _G.Settings.Raids["Auto Awakened"] then
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Awakener", "Awaken")
                            end
                        end)
                    end
                else
                    if _G.Settings.Raids["Auto Awakened"] then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Awakener", "Awaken")
                    end
                    local args = {
                        [1] = "RaidsNpc",
                        [2] = "Select",
                        [3] = tostring(_G.Settings.Raids["Select Raids"])
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                end
            end
        end
    end)
    spawn(function()
        while task.wait() do
            if _G.Settings.Raids["Kill Aura"] then
                for i, v in pairs(game.Workspace.Enemies:GetDescendants()) do
                    if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                        pcall(function()
                            repeat
                                task.wait(.1)
                                v.Humanoid.Health = 0
                                v.HumanoidRootPart.CanCollide = false
                                v.HumanoidRootPart.Size = Vector3.new(50, 50, 50)
                                v.HumanoidRootPart.Transparency = 0.8
                                sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
                            until not _G.Settings.Raids["Kill Aura"] or not _G.Settings.Raids["Auto Raids"] or not RaidSuperhuman or not v.Parent or v.Humanoid.Health <= 0
                        end)
                    end
                end
            end
        end
    end)
    spawn(function()
        pcall(function()
            while task.wait() do
                if _G.Settings.Raids["Auto Next Place"] then
                    if game:GetService("Players")["LocalPlayer"].PlayerGui.Main.Timer.Visible == true and game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 5") or game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 4") or game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 3") or game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 2") or game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1") then
                        if game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 5") then
                            toTarget(game:GetService("Workspace")["_WorldOrigin"].Locations["Island 5"].CFrame *
                                CFrame.new(4, 65, 10))
                        elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 4") then
                            toTarget(game:GetService("Workspace")["_WorldOrigin"].Locations["Island 4"].CFrame *
                                CFrame.new(4, 65, 10))
                        elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 3") then
                            toTarget(game:GetService("Workspace")["_WorldOrigin"].Locations["Island 3"].CFrame *
                                CFrame.new(4, 65, 10))
                        elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 2") then
                            toTarget(game:GetService("Workspace")["_WorldOrigin"].Locations["Island 2"].CFrame *
                                CFrame.new(4, 65, 10))
                        elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1") then
                            toTarget(game:GetService("Workspace")["_WorldOrigin"].Locations["Island 1"].CFrame *
                                CFrame.new(4, 65, 10))
                        end
                    elseif World2 then
                        toTarget(CFrame.new(-6438.73535, 250.645355, -4501.50684))
                    elseif World3 then
                        toTarget(CFrame.new(-5057.146484375, 314.54132080078, -2934.7995605469))
                    end
                end
            end
        end)
    end)
    local plr = game:GetService("Players").LocalPlayer;
    local getplayers = {}
    local getitems = {}
    local getweb = {}
   
        page8:AddLabelX({Name = "PVP"})
        do
            for i, v in pairs(game:GetService("Workspace").Characters:GetChildren()) do
                if v.Name ~= plr.Name then
                    table.insert(getplayers, v.Name)
                end
            end
            for i, v in pairs(plr.Backpack:GetChildren()) do
                if v:IsA("Tool") then
                    table.insert(getweb, v.Name)
                end
            end
        end
        local PlayerDrop = page8:AddDropdown({Name = "Select Player",List = getplayers,Callback =  function(value)
            SelectPlayer = value
        end})
        page8:AddButton({Name = "Refresh", Callback = function()
            PlayerDrop.Clear() 
            for i, v in next, game:GetService("Workspace").Characters:GetChildren() do
                if v.Name ~= plr.Name then
                    if v:FindFirstChild("HumanoidRootPart") then
                        PlayerDrop:Add(v.Name)
                    end
                end
            end
        end})
        page8:AddToggle({Name = "Teleport to Player",Value =  teleporttop, Callback = function(value)
            teleporttop = value
            if value == false then
                task.wait()
                toTarget(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
                task.wait()
            end
        end})
        page8:AddToggle({Name = "Spectate Player", Value = SpectatePlys, Callback = function(value)
            SpectatePlys = value
            local plr1 = game:GetService("Players").LocalPlayer.Character.Humanoid
            local plr2 = game:GetService("Players"):FindFirstChild(SelectPlayer)
            repeat
                wait(.1)
                game:GetService("Workspace").Camera.CameraSubject = game:GetService("Players"):FindFirstChild(SelectPlayer)
                    .Character.Humanoid
            until SpectatePlys == false
            game:GetService("Workspace").Camera.CameraSubject = game:GetService("Players").LocalPlayer.Character.Humanoid
        end})
        spawn(function()
            while task.wait() do
                if teleporttop then
                    pcall(function()
                        if game.Players:FindFirstChild(SelectPlayer) then
                            toTarget(game.Players[SelectPlayer].Character.HumanoidRootPart.CFrame)
                        end
                    end)
                end
            end
        end)
        page8:AddToggle({Name = "Aimbot Gun", Value = false, Callback  = function(value)
            Aimbot = value
        end})
        page8:AddToggle({Name = "Aimbot Skill", Value = false, Callback  = function(value)
            Skillaimbot = value
        end})
    local gg = getrawmetatable(game)
    local old = gg.__namecall
    setreadonly(gg, false)
    gg.__namecall = newcclosure(function(...)
        local method = getnamecallmethod()
        local args = { ... }
        if tostring(method) == "FireServer" then
            if tostring(args[1]) == "RemoteEvent" then
                if tostring(args[2]) ~= "true" and tostring(args[2]) ~= "false" then
                    if Skillaimbot then
                        args[2] = AimBotSkillPosition
                        return old(unpack(args))
                    end
                end
            end
        end
        return old(...)
    end)
    spawn(function()
        while task.wait() do
            for i, v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
                if v:IsA("Tool") then
                    if v:FindFirstChild("RemoteFunctionShoot") then
                        SelectToolWeaponGun = v.Name
                    end
                end
            end
            for i, v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do
                if v:IsA("Tool") then
                    if v:FindFirstChild("RemoteFunctionShoot") then
                        SelectToolWeaponGun = v.Name
                    end
                end
            end
        end
    end)
    task.spawn(function()
        while task.wait() do
            if Skillaimbot then
                if game.Players:FindFirstChild(SelectPlayer) and game.Players:FindFirstChild(SelectPlayer).Character:FindFirstChild("HumanoidRootPart") and game.Players:FindFirstChild(SelectPlayer).Character:FindFirstChild("Humanoid") and game.Players:FindFirstChild(SelectPlayer).Character.Humanoid.Health > 0 then
                    AimBotSkillPosition = game.Players:FindFirstChild(SelectPlayer).Character:FindFirstChild(
                        "HumanoidRootPart").Position
                end
            end
        end
    end)
    task.spawn(function()
        while task.wait() do
            if Skillaimbot then
                if game.Players:FindFirstChild(AllPlayersTableSkipFarm) and game.Players:FindFirstChild(AllPlayersTableSkipFarm).Character:FindFirstChild("HumanoidRootPart") and game.Players:FindFirstChild(AllPlayersTableSkipFarm).Character:FindFirstChild("Humanoid") and game.Players:FindFirstChild(AllPlayersTableSkipFarm).Character.Humanoid.Health > 0 then
                    AimBotSkillPosition = game.Players:FindFirstChild(AllPlayersTableSkipFarm).Character:FindFirstChild(
                        "HumanoidRootPart").Position
                end
            end
        end
    end)
    local lp = game:GetService('Players').LocalPlayer
    local mouse = lp:GetMouse()
    mouse.Button1Down:Connect(function()
        if Aimbot and game.Players.LocalPlayer.Character:FindFirstChild(SelectToolWeaponGun) and game:GetService("Players"):FindFirstChild(SelectPlayer) then
            tool = game:GetService("Players").LocalPlayer.Character[SelectToolWeaponGun]
            v17 = workspace:FindPartOnRayWithIgnoreList(Ray.new(tool.Handle.CFrame.p,
                    (game:GetService("Players"):FindFirstChild(SelectPlayer).Character.HumanoidRootPart.Position - tool.Handle.CFrame.p)
                    .unit * 100), { game.Players.LocalPlayer.Character, workspace._WorldOrigin });
            game:GetService("Players").LocalPlayer.Character[SelectToolWeaponGun].RemoteFunctionShoot:InvokeServer(
                game:GetService("Players"):FindFirstChild(SelectPlayer).Character.HumanoidRootPart.Position,
(require(game.ReplicatedStorage.Util).Other.hrpFromPart(v17)));
        end
    end)
   
        page8:AddLabelX({Name = "ESP"})
    
        page8:AddToggle({Name  = "ESPPlayer", Value = _G.Settings.ESPPlayer, Callback = function(value)
            ESPPlayer = value
            while ESPPlayer do
                task.wait()
                UpdatePlayerChams()
            end
        end})
        spawn(function()
            while task.wait() do
                if ESPPlayer then
                    UpdatePlayerChams()
                end
            end
        end)
        page8:AddToggle({Name = "ESPChest", Value = _G.ChestEsp, Callback = function(value)
            ChestESP = value
            while ChestESP do
                task.wait()
                UpdateChestEsp()
            end
        end})

        page8:AddToggle({Name = "ESPDevilFruit", Value = _G.DevilFruitESP, Callback = function(value)
            DevilFruitESP = value
            while DevilFruitESP do
                task.wait()
                UpdateBfEsp()
            end
        end})
        page8:AddToggle({Name = "ESPFlower", Value = _G.DevilFruitESP, Callback = function(value)
            FlowerESP = value
            while FlowerESP do
                task.wait()
                UpdateFlowerEsp()
            end
        end})
        page8:AddToggle({Name = "ESPIsland", Value = _G.DevilFruitESP, Callback = function(value)
            IslandESP = value
            while IslandESP do
                task.wait()
                UpdateIslandESP()
            end
        end})
  
    function isnil(thing)
        return (thing == nil)
    end
    local function round(n)
        return math.floor(tonumber(n) + 0.5)
    end
    Number = math.random(1, 1000000)
    function UpdatePlayerChams()
        for i, v in pairs(game:GetService 'Players':GetChildren()) do
            pcall(function()
                if not isnil(v.Character) then
                    if ESPPlayer then
                        if not isnil(v.Character.Head) and not v.Character.Head:FindFirstChild('NameEsp' .. Number) then
                            local bill = Instance.new('BillboardGui', v.Character.Head)
                            bill.Name = 'NameEsp' .. Number
                            bill.ExtentsOffset = Vector3.new(0, 1, 0)
                            bill.Size = UDim2.new(1, 200, 1, 30)
                            bill.Adornee = v.Character.Head
                            bill.AlwaysOnTop = true
                            local name = Instance.new('TextLabel', bill)
                            name.Font = "Code"
                            name.FontSize = "Size14"
                            name.TextWrapped = true
                            name.Text = (v.Name .. ' \n' .. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Character.Head.Position).Magnitude / 3) .. ' M')
                            name.Size = UDim2.new(1, 0, 1, 0)
                            name.TextYAlignment = 'Top'
                            name.BackgroundTransparency = 1
                            name.TextStrokeTransparency = 0.5
                            if v.Team == game.Players.LocalPlayer.Team then
                                name.TextColor3 = Color3.new(255, 0, 0)
                            else
                                name.TextColor3 = Color3.new(0, 0, 255)
                            end
                        else
                            v.Character.Head['NameEsp' .. Number].TextLabel.Text = (v.Name .. ' | ' .. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Character.Head.Position).Magnitude / 3) .. ' M\nHealth : ' .. round(v.Character.Humanoid.Health * 100 / v.Character.Humanoid.MaxHealth) .. '%')
                        end
                    else
                        if v.Character.Head:FindFirstChild('NameEsp' .. Number) then
                            v.Character.Head:FindFirstChild('NameEsp' .. Number):Destroy()
                        end
                    end
                end
            end)
        end
    end
    function UpdateSeaBeastsESP()
        for i, v in pairs(game:GetService("Workspace").SeaBeasts:GetChildren()) do
            pcall(function()
                if SeaBeastsESP then
                    if v.Name ~= "SeaBeast" then
                        if not v:FindFirstChild('NameEsp') then
                            local bill = Instance.new('BillboardGui', v)
                            bill.Name = 'NameEsp'
                            bill.ExtentsOffset = Vector3.new(0, 1, 0)
                            bill.Size = UDim2.new(1, 200, 1, 30)
                            bill.Adornee = v
                            bill.AlwaysOnTop = true
                            local name = Instance.new('TextLabel', bill)
                            name.Font = "Code"
                            name.FontSize = "Size14"
                            name.TextWrapped = true
                            name.Size = UDim2.new(1, 0, 1, 0)
                            name.TextYAlignment = 'Top'
                            name.BackgroundTransparency = 1
                            name.TextStrokeTransparency = 0.5
                            name.TextColor3 = Color3.fromRGB(80, 245, 245)
                        else
                            v['NameEsp'].TextLabel.Text = (v.Name .. '   \n' .. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude / 3) .. ' M')
                        end
                    end
                else
                    if v:FindFirstChild('NameEsp') then
                        v:FindFirstChild('NameEsp'):Destroy()
                    end
                end
            end)
        end
    end
    function UpdateIslandESP()
        for i, v in pairs(game:GetService("Workspace")["_WorldOrigin"].Locations:GetChildren()) do
            pcall(function()
                if IslandESP then
                    if v.Name ~= "Sea" then
                        if not v:FindFirstChild('NameEsp') then
                            local bill = Instance.new('BillboardGui', v)
                            bill.Name = 'NameEsp'
                            bill.ExtentsOffset = Vector3.new(0, 1, 0)
                            bill.Size = UDim2.new(1, 200, 1, 30)
                            bill.Adornee = v
                            bill.AlwaysOnTop = true
                            local name = Instance.new('TextLabel', bill)
                            name.Font = "Code"
                            name.FontSize = "Size14"
                            name.TextWrapped = true
                            name.Size = UDim2.new(1, 0, 1, 0)
                            name.TextYAlignment = 'Top'
                            name.BackgroundTransparency = 1
                            name.TextStrokeTransparency = 0.5
                            name.TextColor3 = Color3.fromRGB(67, 186, 28)
                        else
                            v['NameEsp'].TextLabel.Text = (v.Name .. '   \n' .. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude / 3) .. ' M')
                        end
                    end
                else
                    if v:FindFirstChild('NameEsp') then
                        v:FindFirstChild('NameEsp'):Destroy()
                    end
                end
            end)
        end
    end
    function UpdateChestEsp()
        for i, v in pairs(game:GetService("Workspace"):GetChildren()) do
            pcall(function()
                if string.find(v.Name, "Chest") then
                    if ChestESP then
                        if string.find(v.Name, "Chest") then
                            if not v:FindFirstChild('NameEsp' .. Number) then
                                local bill = Instance.new('BillboardGui', v)
                                bill.Name = 'NameEsp' .. Number
                                bill.ExtentsOffset = Vector3.new(0, 1, 0)
                                bill.Size = UDim2.new(1, 200, 1, 30)
                                bill.Adornee = v
                                bill.AlwaysOnTop = true
                                local name = Instance.new('TextLabel', bill)
                                name.Font = "Code"
                                name.FontSize = "Size14"
                                name.TextWrapped = true
                                name.Size = UDim2.new(1, 0, 1, 0)
                                name.TextYAlignment = 'Top'
                                name.BackgroundTransparency = 1
                                name.TextStrokeTransparency = 0.5
                                name.TextColor3 = Color3.fromRGB(186, 186, 28)
                                if v.Name == "Chest1" then
                                    name.Text = ("Chest 1" .. ' \n' .. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude / 3) .. ' M')
                                end
                                if v.Name == "Chest2" then
                                    name.Text = ("Chest 2" .. ' \n' .. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude / 3) .. ' M')
                                end
                                if v.Name == "Chest3" then
                                    name.Text = ("Chest 3" .. ' \n' .. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude / 3) .. ' M')
                                end
                            else
                                v['NameEsp' .. Number].TextLabel.Text = (v.Name .. '   \n' .. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude / 3) .. ' M')
                            end
                        end
                    else
                        if v:FindFirstChild('NameEsp' .. Number) then
                            v:FindFirstChild('NameEsp' .. Number):Destroy()
                        end
                    end
                end
            end)
        end
    end
    function UpdateBfEsp()
        for i, v in pairs(game:GetService("Workspace"):GetChildren()) do
            pcall(function()
                if DevilFruitESP then
                    if string.find(v.Name, "Fruit") then
                        if not v.Handle:FindFirstChild('NameEsp' .. Number) then
                            local bill = Instance.new('BillboardGui', v.Handle)
                            bill.Name = 'NameEsp' .. Number
                            bill.ExtentsOffset = Vector3.new(0, 1, 0)
                            bill.Size = UDim2.new(1, 200, 1, 30)
                            bill.Adornee = v.Handle
                            bill.AlwaysOnTop = true
                            local name = Instance.new('TextLabel', bill)
                            name.Font = "Code"
                            name.FontSize = "Size14"
                            name.TextWrapped = true
                            name.Size = UDim2.new(1, 0, 1, 0)
                            name.TextYAlignment = 'Top'
                            name.BackgroundTransparency = 1
                            name.TextStrokeTransparency = 0.5
                            name.TextColor3 = Color3.fromRGB(255, 255, 255)
                            name.Text = (v.Name .. ' \n' .. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Handle.Position).Magnitude / 3) .. ' M')
                        else
                            v.Handle['NameEsp' .. Number].TextLabel.Text = (v.Name .. '   \n' .. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Handle.Position).Magnitude / 3) .. ' M')
                        end
                    end
                else
                    if v.Handle:FindFirstChild('NameEsp' .. Number) then
                        v.Handle:FindFirstChild('NameEsp' .. Number):Destroy()
                    end
                end
            end)
        end
    end
    function UpdateFlowerEsp()
        for i, v in pairs(game:GetService("Workspace"):GetChildren()) do
            pcall(function()
                if v.Name == "Flower2" or v.Name == "Flower1" then
                    if FlowerESP then
                        if not v:FindFirstChild('NameEsp' .. Number) then
                            local bill = Instance.new('BillboardGui', v)
                            bill.Name = 'NameEsp' .. Number
                            bill.ExtentsOffset = Vector3.new(0, 1, 0)
                            bill.Size = UDim2.new(1, 200, 1, 30)
                            bill.Adornee = v
                            bill.AlwaysOnTop = true
                            local name = Instance.new('TextLabel', bill)
                            name.Font = "Code"
                            name.FontSize = "Size14"
                            name.TextWrapped = true
                            name.Size = UDim2.new(1, 0, 1, 0)
                            name.TextYAlignment = 'Top'
                            name.BackgroundTransparency = 1
                            name.TextStrokeTransparency = 0.5
                            name.TextColor3 = Color3.fromRGB(255, 0, 0)
                            if v.Name == "Flower1" then
                                name.Text = ("Blue Flower" .. ' \n' .. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude / 3) .. ' M')
                                name.TextColor3 = Color3.fromRGB(0, 0, 255)
                            end
                            if v.Name == "Flower2" then
                                name.Text = ("Red Flower" .. ' \n' .. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude / 3) .. ' M')
                                name.TextColor3 = Color3.fromRGB(255, 0, 0)
                            end
                        else
                            v['NameEsp' .. Number].TextLabel.Text = (v.Name .. '   \n' .. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude / 3) .. ' M')
                        end
                    else
                        if v:FindFirstChild('NameEsp' .. Number) then
                            v:FindFirstChild('NameEsp' .. Number):Destroy()
                        end
                    end
                end
            end)
        end
    end
    function UpdateRealFruitChams()
        for i, v in pairs(game.Workspace.AppleSpawner:GetChildren()) do
            if v:IsA("Tool") then
                if RealFruitESP then
                    if not v.Handle:FindFirstChild('NameEsp' .. Number) then
                        local bill = Instance.new('BillboardGui', v.Handle)
                        bill.Name = 'NameEsp' .. Number
                        bill.ExtentsOffset = Vector3.new(0, 1, 0)
                        bill.Size = UDim2.new(1, 200, 1, 30)
                        bill.Adornee = v.Handle
                        bill.AlwaysOnTop = true
                        local name = Instance.new('TextLabel', bill)
                        name.Font = "Code"
                        name.FontSize = "Size14"
                        name.TextWrapped = true
                        name.Size = UDim2.new(1, 0, 1, 0)
                        name.TextYAlignment = 'Top'
                        name.BackgroundTransparency = 1
                        name.TextStrokeTransparency = 0.5
                        name.TextColor3 = Color3.fromRGB(255, 0, 0)
                        name.Text = (v.Name .. ' \n' .. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Handle.Position).Magnitude / 3) .. ' M')
                    else
                        v.Handle['NameEsp' .. Number].TextLabel.Text = (v.Name .. ' ' .. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Handle.Position).Magnitude / 3) .. ' M')
                    end
                else
                    if v.Handle:FindFirstChild('NameEsp' .. Number) then
                        v.Handle:FindFirstChild('NameEsp' .. Number):Destroy()
                    end
                end
            end
        end
        for i, v in pairs(game.Workspace.PineappleSpawner:GetChildren()) do
            if v:IsA("Tool") then
                if RealFruitESP then
                    if not v.Handle:FindFirstChild('NameEsp' .. Number) then
                        local bill = Instance.new('BillboardGui', v.Handle)
                        bill.Name = 'NameEsp' .. Number
                        bill.ExtentsOffset = Vector3.new(0, 1, 0)
                        bill.Size = UDim2.new(1, 200, 1, 30)
                        bill.Adornee = v.Handle
                        bill.AlwaysOnTop = true
                        local name = Instance.new('TextLabel', bill)
                        name.Font = "Code"
                        name.FontSize = "Size14"
                        name.TextWrapped = true
                        name.Size = UDim2.new(1, 0, 1, 0)
                        name.TextYAlignment = 'Top'
                        name.BackgroundTransparency = 1
                        name.TextStrokeTransparency = 0.5
                        name.TextColor3 = Color3.fromRGB(255, 174, 0)
                        name.Text = (v.Name .. ' \n' .. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Handle.Position).Magnitude / 3) .. ' M')
                    else
                        v.Handle['NameEsp' .. Number].TextLabel.Text = (v.Name .. ' ' .. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Handle.Position).Magnitude / 3) .. ' M')
                    end
                else
                    if v.Handle:FindFirstChild('NameEsp' .. Number) then
                        v.Handle:FindFirstChild('NameEsp' .. Number):Destroy()
                    end
                end
            end
        end
        for i, v in pairs(game.Workspace.BananaSpawner:GetChildren()) do
            if v:IsA("Tool") then
                if RealFruitESP then
                    if not v.Handle:FindFirstChild('NameEsp' .. Number) then
                        local bill = Instance.new('BillboardGui', v.Handle)
                        bill.Name = 'NameEsp' .. Number
                        bill.ExtentsOffset = Vector3.new(0, 1, 0)
                        bill.Size = UDim2.new(1, 200, 1, 30)
                        bill.Adornee = v.Handle
                        bill.AlwaysOnTop = true
                        local name = Instance.new('TextLabel', bill)
                        name.Font = "Code"
                        name.FontSize = "Size14"
                        name.TextWrapped = true
                        name.Size = UDim2.new(1, 0, 1, 0)
                        name.TextYAlignment = 'Top'
                        name.BackgroundTransparency = 1
                        name.TextStrokeTransparency = 0.5
                        name.TextColor3 = Color3.fromRGB(251, 255, 0)
                        name.Text = (v.Name .. ' \n' .. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Handle.Position).Magnitude / 3) .. ' M')
                    else
                        v.Handle['NameEsp' .. Number].TextLabel.Text = (v.Name .. ' ' .. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Handle.Position).Magnitude / 3) .. ' M')
                    end
                else
                    if v.Handle:FindFirstChild('NameEsp' .. Number) then
                        v.Handle:FindFirstChild('NameEsp' .. Number):Destroy()
                    end
                end
            end
        end
    end
    function UpdatePlayerChams()
        for i, v in pairs(game:GetService 'Players':GetChildren()) do
            pcall(function()
                if not isnil(v.Character) then
                    if ESPPlayer then
                        if not isnil(v.Character.Head) and not v.Character.Head:FindFirstChild('NameEsp' .. Number) then
                            local bill = Instance.new('BillboardGui', v.Character.Head)
                            bill.Name = 'NameEsp' .. Number
                            bill.ExtentsOffset = Vector3.new(0, 1, 0)
                            bill.Size = UDim2.new(1, 200, 1, 30)
                            bill.Adornee = v.Character.Head
                            bill.AlwaysOnTop = true
                            local name = Instance.new('TextLabel', bill)
                            name.Font = "Code"
                            name.FontSize = "Size14"
                            name.TextWrapped = true
                            name.Text = (v.Name .. ' \n' .. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Character.Head.Position).Magnitude / 3) .. ' M')
                            name.Size = UDim2.new(1, 0, 1, 0)
                            name.TextYAlignment = 'Top'
                            name.BackgroundTransparency = 1
                            name.TextStrokeTransparency = 0.5
                            if v.Team == game.Players.LocalPlayer.Team then
                                name.TextColor3 = Color3.new(255, 0, 0)
                            else
                                name.TextColor3 = Color3.new(0, 0, 255)
                            end
                        else
                            v.Character.Head['NameEsp' .. Number].TextLabel.Text = (v.Name .. ' | ' .. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Character.Head.Position).Magnitude / 3) .. ' M\nHealth : ' .. round(v.Character.Humanoid.Health * 100 / v.Character.Humanoid.MaxHealth) .. '%')
                        end
                    else
                        if v.Character.Head:FindFirstChild('NameEsp' .. Number) then
                            v.Character.Head:FindFirstChild('NameEsp' .. Number):Destroy()
                        end
                    end
                end
            end)
        end
    end
    local FM = page9:AddLabelX({Name = '...'})
    local Mirragecheck = page9:AddLabelX({Name = '...'})
    task.spawn(function()
        while task.wait() do
            pcall(function()
                if game:GetService("Lighting").Sky.MoonTextureId == "http://www.roblox.com/asset/?id=9709149431" then
                    FM:Set("🌑 : Full Moon 100%")
                elseif game:GetService("Lighting").Sky.MoonTextureId == "http://www.roblox.com/asset/?id=9709149052" then
                    FM:Set("🌒 : Full Moon 75%")
                elseif game:GetService("Lighting").Sky.MoonTextureId == "http://www.roblox.com/asset/?id=9709143733" then
                    FM:Set("🌓 : Full Moon 50%")
                elseif game:GetService("Lighting").Sky.MoonTextureId == "http://www.roblox.com/asset/?id=9709150401" then
                    FM:Set("🌗 : Full Moon 25%")
                elseif game:GetService("Lighting").Sky.MoonTextureId == "http://www.roblox.com/asset/?id=9709149680" then
                    FM:Set("🌖 : Full Moon 15%")
                else
                    FM:Set("🌚 : Full Moon 0%")
                end
            end)
        end
    end)
    
        spawn(function()
            pcall(function()
                while task.wait() do
                    if game.Workspace._WorldOrigin.Locations:FindFirstChild('Mirage Island') then
                        Mirragecheck:Set('🏝️ : Mirage Island is Spawning 🟢')
                    else
                        Mirragecheck:Set('🏝️ : Mirage Island Not Found ❌')
                    end
                end
            end)
        end)
  
        page9:AddToggle({Name = "Auto Mirage Island",  Value = _G.Settings.Mirage["Auto MirageIsland"],Callback =  function(value)
            _G.Mirage = value
            _G.Settings.Mirage["Auto MirageIsland"] = value
            StopTween(_G.Mirage)
            SaveSettings()
        end})
   
    
        page9:AddToggle({Name = "Auto Mirage Island [HOP]", Value = _G.Settings.Mirage["AutoMirageIslandHop"], Callback = function(value)
            _G.MirageHop = value
            _G.Settings.Mirage["AutoMirageIslandHop"] = value
            SaveSettings()
            game:GetService("StarterGui"):SetCore("SendNotification",{Title = "VectorHub",Text = "HopServer...",Icon = "rbxassetid://14645512457",Duration = 5})
            if _G.MirageHop and not game.Workspace._WorldOrigin.Locations:FindFirstChild('Mirage Island') then
                while _G.MirageHop do wait(5)
                repeat task.wait() until game:IsLoaded() and game.Players.LocalPlayer
                local HttpService, TPService = game:GetService "HttpService", game:GetService "TeleportService";
                local OtherServers = HttpService:JSONDecode(game:HttpGet("https://games.roblox.com/v1/games/" ..
                    game.PlaceId .. "/servers/Public?sortOrder=Asc&limit=100"))
                function joinNew()
                    if not isfile('servers.sss') then
                        writefile('servers.sss', HttpService:JSONEncode({}))
                    end
                    local dontJoin = readfile('servers.sss')
                    dontJoin = HttpService:JSONDecode(dontJoin)
            
                    for Index, Server in next, OtherServers["data"] do
                        if Server ~= game.JobId then
                            local j = true
                            for a, c in pairs(dontJoin) do
                                if c == Server.id then
                                    j = false
                                end
                            end
                            if j then
                                table.insert(dontJoin, Server["id"])
                                writefile("servers.sss", HttpService:JSONEncode(dontJoin))
                                task.wait()
                                return Server['id']
                            end
                        end
                    end
                end
                local server = joinNew()
                if not server then
                    writefile("servers.sss", HttpService:JSONEncode({}))
                    local server = joinNew()
                    TPService:TeleportToPlaceInstance(game.PlaceId, server)
                else
                    TPService:TeleportToPlaceInstance(game.PlaceId, server)
                end
               end
            else
                toTarget(workspace.Map.MysticIsland.PrimaryPart.CFrame * CFrame.new(0, 300, 0))
            end
            
        end})
  
    spawn(function()
        pcall(function()
            while task.wait() do
                if _G.Settings.Mirage["Auto MirageIsland"] and _G.Mirage then
                    if game:GetService("Workspace").Map:FindFirstChild("MysticIsland") then
                         toTarget(workspace.Map.MysticIsland.PrimaryPart.CFrame * CFrame.new(0, 300, 0))
                    else
                            game:GetService("StarterGui"):SetCore("SendNotification",{Title = "VectorHub",Text = "Mirage not Found!",Icon = "rbxassetid://14645512457",Duration = 1})
                    end
                end
            end
        end)
    end)
    if game.Workspace._WorldOrigin.Locations:FindFirstChild('Mirage Island') then
    if World3 then
        local Moon = {
            ['8'] = "http://www.roblox.com/asset/?id=9709149431", -- 🌕
            ['7'] = "http://www.roblox.com/asset/?id=9709149052", -- 🌖
            ['6'] = "http://www.roblox.com/asset/?id=9709143733", -- 🌗
            ['5'] = "http://www.roblox.com/asset/?id=9709150401", -- 🌘
            ['4'] = "http://www.roblox.com/asset/?id=9709135895", -- 🌑
            ['3'] = "http://www.roblox.com/asset/?id=9709139597", -- 🌒
            ['2'] = "http://www.roblox.com/asset/?id=9709150086", -- 🌓
            ['1'] = "http://www.roblox.com/asset/?id=9709149680", -- 🌔
        };
        for i, v in pairs(Moon) do
            if game:GetService("Lighting").Sky.MoonTextureId == v then
                MoonPercent = i / 8 * 100
            end
        end
        for i, v in pairs(game.Players:GetPlayers()) do
            PlayersMin = i
        end
        if game:GetService("Lighting").Sky.MoonTextureId == Moon['1'] then
            MoonIcon = '🌔'
        elseif game:GetService("Lighting").Sky.MoonTextureId == Moon['2'] then
            MoonIcon = '🌓'
        elseif game:GetService("Lighting").Sky.MoonTextureId == Moon['3'] then
            MoonIcon = '🌒'
        elseif game:GetService("Lighting").Sky.MoonTextureId == Moon['4'] then
            MoonIcon = '🌑'
        elseif game:GetService("Lighting").Sky.MoonTextureId == Moon['5'] then
            MoonIcon = '🌘'
        elseif game:GetService("Lighting").Sky.MoonTextureId == Moon['6'] then
            MoonIcon = '🌘'
        elseif game:GetService("Lighting").Sky.MoonTextureId == Moon['7'] then
            MoonIcon = '🌖'
        elseif game:GetService("Lighting").Sky.MoonTextureId == Moon['8'] then
            MoonIcon = '🌕'
        end
        if game.Workspace._WorldOrigin.Locations:FindFirstChild('Mirage Island') then
            MirageMessage = '```Mirage is spawing : 🟢```'
        else
            MirageMessage = '```Mirage isn\'t spawn : ❌```'
        end
    
        MoonMessage = '```' .. tostring(MoonPercent .. '%' .. ' : ' .. MoonIcon) .. '```'
        JoinServer = 'game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId,' ..
            '\'' .. tostring(game.JobId) .. '\'' .. ')'
        --print('\n'..MoonMessage..'\n'..MirageMessage..'\n'..JoinServer)
    
        local url = "https://discord.com/api/webhooks/1159506639095869600/1N9kghTBEkvkDlPyiVkE1SVW02HMAzgd80BKwcB9R-mqbdrdh_g4A0Lc2dovUGH-Olqu"                                                                                                                -- ur webhook url
        local data = {
            ["username"] = 'Vector Hub',                                                                                                                                                                                                           -- Webhook name here --หะ
            ['content'] = '<@&1159482607738830928>',                                                                                                                                                                                               -- ping everyone if you want to ping role use this <@&1007291553074647132> --<@&1068889841091219498>
            ["avatar_url"] = "https://media.discordapp.net/attachments/1089811542226247781/1159366800941781042/b0fb523ce7d8590f.jpg?ex=6530c379&is=651e4e79&hm=d8a71d8ad3a6b21ad4cdc281facdde6c320b729f5df492db1894d3990211666e&=&width=566&height=566", -- ur discord logo url
            ["embeds"] = {
                {
                    ["description"] = "**__Mirage Webhook__**",
                    ["color"] = tonumber(0x0000FF), -- color id		#
                    ["type"] = "rich",
                    ["fields"] = {
                        {
                            ["name"] = "[👥] Players Active",
                            ["value"] = '```' .. tostring(PlayersMin) .. '/12```'
                        },
                        {
                            ["name"] = "[📃] JobID",
                            ["value"] = '```' .. tostring(game.JobId) .. '```'
                        },
                        {
                            ["name"] = "[📁] Join Server",
                            ["value"] = '```' .. JoinServer .. '```',
                        },
                        {
                            ["name"] = "[🌲] Mirage Check",
                            ["value"] = MirageMessage,
                            ["inline"] = true
                        }
                    },
                    ["footer"] = {
                        ["text"] = "Webhook Vector Hub", -- you can remove this but it will hurt
                    },
                    ["timestamp"] = DateTime.now():ToIsoDate(),
                }
            },
        }
        local newdata = game:GetService("HttpService"):JSONEncode(data)
        local headers = { ["content-type"] = "application/json" }
        request = http_request or request or HttpPost or syn.request
        local abcdef = { Url = url, Body = newdata, Method = "POST", Headers = headers }
        request(abcdef)
        end
    end
    if World3 then
        local Moon = {
            ['8'] = "http://www.roblox.com/asset/?id=9709149431", -- 🌕
            ['7'] = "http://www.roblox.com/asset/?id=9709149052", -- 🌖
            ['6'] = "http://www.roblox.com/asset/?id=9709143733", -- 🌘
            ['5'] = "http://www.roblox.com/asset/?id=9709150401", -- 🌘
            ['4'] = "http://www.roblox.com/asset/?id=9709135895", -- 🌑
            ['3'] = "http://www.roblox.com/asset/?id=9709139597", -- 🌒
            ['2'] = "http://www.roblox.com/asset/?id=9709150086", -- 🌓
            ['1'] = "http://www.roblox.com/asset/?id=9709149680", -- 🌔
        };
        for i, v in pairs(Moon) do
            if game:GetService("Lighting").Sky.MoonTextureId == v then
                MoonPercent = i / 8 * 100
            end
        end
        for i, v in pairs(game.Players:GetPlayers()) do
            PlayersMin = i
        end
        if game:GetService("Lighting").Sky.MoonTextureId == Moon['1'] then
            MoonIcon = '🌔'
        elseif game:GetService("Lighting").Sky.MoonTextureId == Moon['2'] then
            MoonIcon = '🌓'
        elseif game:GetService("Lighting").Sky.MoonTextureId == Moon['3'] then
            MoonIcon = '🌒'
        elseif game:GetService("Lighting").Sky.MoonTextureId == Moon['4'] then
            MoonIcon = '🌑'
        elseif game:GetService("Lighting").Sky.MoonTextureId == Moon['5'] then
            MoonIcon = '🌘'
        elseif game:GetService("Lighting").Sky.MoonTextureId == Moon['6'] then
            MoonIcon = '🌘'
        elseif game:GetService("Lighting").Sky.MoonTextureId == Moon['7'] then
            MoonIcon = '🌖'
        elseif game:GetService("Lighting").Sky.MoonTextureId == Moon['8'] then
            MoonIcon = '🌕'
        end
        MoonMessage = '```' .. tostring(MoonPercent .. '%' .. ' : ' .. MoonIcon) .. '```'
        JoinServer = 'game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId,' ..
            '\'' .. tostring(game.JobId) .. '\'' .. ')'
        --print('\n'..MoonMessage..'\n'..MirageMessage..'\n'..JoinServer)
    
        local url = "https://discord.com/api/webhooks/1165611714671300659/lks4dG2RzRR6thjYO0FbKjDO5QmlGtmENAuFThbQ_rCuYoEZdGyoZdQDVAMWy3G8WW4n"                                                                                                                -- ur webhook url
        local data = {
            ["username"] = 'Vector Hub',                                                                                                                                                                                                           -- Webhook name here --หะ
            ['content'] = '<@&1159482607738830928>',                                                                                                                                                                                               -- ping everyone if you want to ping role use this <@&1007291553074647132> --<@&1068889841091219498>
            ["avatar_url"] = "https://media.discordapp.net/attachments/1089811542226247781/1159366800941781042/b0fb523ce7d8590f.jpg?ex=6530c379&is=651e4e79&hm=d8a71d8ad3a6b21ad4cdc281facdde6c320b729f5df492db1894d3990211666e&=&width=566&height=566", -- ur discord logo url
            ["embeds"] = {
                {
                    ["description"] = "**__Moon__**",
                    ["color"] = tonumber(0x0000FF), -- color id		#
                    ["type"] = "rich",
                    ["fields"] = {
                        {
                            ["name"] = "[👥] Players Active",
                            ["value"] = '```' .. tostring(PlayersMin) .. '/12```'
                        },
                        {
                            ["name"] = "[📃] JobID",
                            ["value"] = '```' .. tostring(game.JobId) .. '```'
                        },
                        {
                            ["name"] = "[📁] Join Server",
                            ["value"] = '```' .. JoinServer .. '```',
                        },
                        {
                            ["name"] = "[🕑] Moon Check",
                            ["value"] = MoonMessage,
                            ["inline"] = true
                        },
                        
                    },
                    ["footer"] = {
                        ["text"] = "Webhook Vector Hub", -- you can remove this but it will hurt
                    },
                    ["timestamp"] = DateTime.now():ToIsoDate(),
                }
            },
        }
        local newdata = game:GetService("HttpService"):JSONEncode(data)
        local headers = { ["content-type"] = "application/json" }
        request = http_request or request or HttpPost or syn.request
        local abcdef = { Url = url, Body = newdata, Method = "POST", Headers = headers }
        request(abcdef)
    end
     page10:AddButton({Name = "Teleport To Top GreatTree",Callback =  function()
            toTarget(CFrame.new(2947.556884765625, 2281.630615234375, -7213.54931640625))
        end})
  
        page10:AddButton({Name = "Teleport To Timple Of Time",Callback =  function()
            Game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(28286.35546875,
                14895.3017578125, 102.62469482421875)
        end})
 
    
        page10:AddButton({Name = "Teleport To Lever Pull",Callback =  function()
            toTarget(CFrame.new(28575.181640625, 14936.6279296875, 72.31636810302734))
        end})
 
   
        page10:AddButton({Name = "Teleport To Acient One", Callback = function()
            toTarget(CFrame.new(28981.552734375, 14888.4267578125, -120.245849609375))
        end})
   
    page10:AddButton({Name = "Unlock Lever.", Callback = function()
        if game:GetService("Workspace").Map["Temple of Time"].Lever.Prompt:FindFirstChild("ProximityPrompt") then
            game:GetService("Workspace").Map["Temple of Time"].Lever.Prompt:FindFirstChild("ProximityPrompt"):Remove()
        else
        end
        wait(0.1)
        local ProximityPrompt = Instance.new("ProximityPrompt")
        ProximityPrompt.Parent = game:GetService("Workspace").Map["Temple of Time"].Lever.Prompt
        ProximityPrompt.MaxActivationDistance = 10
        ProximityPrompt.ActionText = "Secrets Beholds Inside"
        ProximityPrompt.ObjectText = "An unknown lever of time"
        function onProximity()
            local part = game:GetService("Workspace").Map["Temple of Time"].MainDoor1
            local TweenService = game:GetService("TweenService")
            local startPosition = part.Position
            local endPosition = startPosition + Vector3.new(0, -50, 0)
            local tweenInfo = TweenInfo.new(10, Enum.EasingStyle.Linear, Enum.EasingDirection.Out)
            local tween = TweenService:Create(part, tweenInfo, { Position = endPosition })
            tween:Play()
            local partnew = game:GetService("Workspace").Map["Temple of Time"].MainDoor2
            local TweenService = game:GetService("TweenService")
    
            local startPosition = partnew.Position
            local endPosition = startPosition + Vector3.new(0, -50, 0)
    
            local tweenInfo = TweenInfo.new(10, Enum.EasingStyle.Linear, Enum.EasingDirection.Out)
            local tween = TweenService:Create(partnew, tweenInfo, { Position = endPosition })
            tween:Play()
            local SoundSFX = Instance.new("Sound")
            SoundSFX.Parent = workspace
            SoundSFX.SoundId = "rbxassetid://1904813041"
            SoundSFX:Play()
            SoundSFX.Name = "POwfpxzxzfFfFF"
            game:GetService("Workspace").Map["Temple of Time"].Lever.Prompt:FindFirstChild("ProximityPrompt"):Remove()
            wait(5)
            workspace:FindFirstChild("POwfpxzxzfFfFF"):Remove()
            game:GetService("Workspace").Map["Temple of Time"].NoGlitching:Remove()
            game:GetService("Workspace").Map["Temple of Time"].NoGlitching:Remove()
            game:GetService("Workspace").Map["Temple of Time"].NoGlitching:Remove()
        end
        ProximityPrompt.Triggered:Connect(onProximity)
    end})
   
        page10:AddButton({Name = "Teleport Cyborg Door ", Callback = function()
            toTarget(CFrame.new(28492.4140625, 14894.4267578125, -422.1100158691406))
        end})
        page10:AddButton({Name = "Teleport Fish Door ", Callback = function()
            toTarget(CFrame.new(28224.056640625, 14889.4267578125, -210.5872039794922))
        end})
        page10:AddButton({Name = "Teleport Ghoul Door", Callback = function()
            toTarget(CFrame.new(28672.720703125, 14889.1279296875, 454.5961608886719))
        end})
        page10:AddButton({Name = "Teleport Human Door ", Callback = function()
            toTarget(CFrame.new(29237.294921875, 14889.4267578125, -206.94955444335938))
        end})
        page10:AddButton({Name = "Teleport Mink Door ", Callback = function()
            toTarget(CFrame.new(29020.66015625, 14889.4267578125, -379.2682800292969))
        end})
        page10:AddButton({Name = "Teleport Sky Door ", Callback = function()
            toTarget(CFrame.new(28967.408203125, 14918.0751953125, 234.31198120117188))
        end})
   
   
        page9:AddLabelX({Name = "Auto Trials"})
   
        page9:AddButton({Name = "Auto Complete Angel Trial", Callback = function(t)
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Workspace.Map.SkyTrial.Model.FinishPart.CFrame
        end})
        page9:AddButton({Name = "Auto Complete Rabbit Trial", Callback = function(t)
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Map.MinkTrial.Ceiling
                .CFrame * CFrame.new(0, -5, 0)
        end})
        page9:AddButton({Name = "Auto Complete Cyborg Trial",Callback =  function(t)
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart
                .CFrame * CFrame.new(0, 300, 0)
        end})
        page9:AddButton({Name = "Teleport PVP Zone", Callback = function()
            toTarget(CFrame.new(28766.681640625, 14967.1455078125, -164.13290405273438))
        end})
        page9:AddButton({Name = "Teleport To Safe Zone When PVP",Callback =  function()
            toTarget(CFrame.new(28273.0859375, 14896.5078125, 157.42063903808594))
        end})
   
    if _G.Settings.Main["Auto Buy Enchanment Haki"] then
        local args = {
            [1] = "ColorsDealer",
            [2] = "2"
        }
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    end
   
        page11:AddLabelX({Name = "Fragment"})
  
    page11:AddButton({Name = "Refund Stat [2,500F]", Callback = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward", "Refund", "1")
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward", "Refund", "2")
    end})
    page11:AddButton({Name = "Reroll Race [3,000F]", Callback = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward", "Reroll", "1")
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward", "Reroll", "2")
    end})
    
        page11:AddLabelX({Name = "Buy Abilities"})
   
    page11:AddButton({Name = "Haki [25,00$]", Callback = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyHaki", "Buso")
    end})
    page11:AddButton({Name = "Geppo [10,000$]",Callback =  function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyHaki", "Geppo")
    end})
    page11:AddButton({Name = "Soru [100,000$]", Callback = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyHaki", "Soru")
    end})
    page11:AddButton({Name = "KenHaki [750,000$]", Callback = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("KenTalk", "Buy")
    end})
    page11:AddLabelX({Name = "Auto Buy Fighting Style"})
    page11:AddButton({Name = "Black Leg [150,000$]", Callback = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBlackLeg")
    end})
    page11:AddButton({Name = "Electro [500,000$]", Callback = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyElectro")
    end})
    page11:AddButton({Name = "Fishman Karate [750,000$]",Callback =  function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyFishmanKarate")
    end})
    page11:AddButton({Name = "Dragon Claw [1,500F]",Callback =  function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward", "DragonClaw", "1")
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward", "DragonClaw", "2")
    end})
    page11:AddButton({Name = "Superhuman [3,000,000]",Callback =  function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySuperhuman")
    end})
    page11:AddButton({Name = "Death Step [2,500,000/5,000F]", Callback = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDeathStep")
    end})
    page11:AddButton({Name = "Sharkman Karate [2,500,000/5,000F]", Callback = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySharkmanKarate", true)
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySharkmanKarate")
    end})
    page11:AddButton({Name = "Electric Claw [3,000,000/5,000F]", Callback = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyElectricClaw", true)
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyElectricClaw")
    end})
    page11:AddButton({Name = "Dragon Talon [3,000,000/5,000F]", Callback = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDragonTalon", true)
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDragonTalon")
    end})
    page11:AddButton({Name  = "Godhuman [5,000,000/5,000F]", Callback = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyGodhuman", true)
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyGodhuman")
    end})
    
        page11:AddLabelX({Name = "Sword"})
   
    page11:AddButton({Name = "Katana [1,000]", Callback = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem", "Katana")
    end})
    page11:AddButton({Name = "Cutlass [1,000]",Callback  =  function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem", "Cutlass")
    end})
    page11:AddButton({Name = "Duel Katana [12,000]", Callback = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem", "Duel Katana")
    end})
    page11:AddButton({Name = "Iron Mace [25,000]", Callback = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem", "Iron Mace")
    end})
    page11:AddButton({Name = "Pipe [100,000]",Callback =  function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem", "Pipe")
    end})
    page11:AddButton({Name = "Triple Katana [60,000]", Callback = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem", "Triple Katana")
    end})
    page11:AddButton({Name = "Dual-Headed Blade [400,000]", Callback = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem", "Dual-Headed Blade")
    end})
    page11:AddButton({Name = "Bisento [1,000,000]",Callback =  function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem", "Bisento")
    end})
    page11:AddButton({Name = "Soul Cane [750,000]",Callback =  function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem", "Soul Cane")
    end})
    
        page11:AddLabelX({Name = "Gun"})

    page11:AddButton({Name =  "Slingshot [5,000]",Callback =  function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem", "Slingshot")
    end})
    page11:AddButton({Name = "Musket [8,000]", Callback = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem", "Musket")
    end})
    page11:AddButton({Name = "Flintlock [10,500]", Callback = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem", "Flintlock")
    end})
    page11:AddButton({Name = "Refined Flintlock [65,000]",Callback =  function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem", "Refined Flintlock")
    end})
    page11:AddButton({Name = "Cannon [100,000]", Callback = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem", "Cannon")
    end})
    page11:AddButton({Name = "Kabucha [1500F]", Callback = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward", "Slingshot", "1")
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward", "Slingshot", "2")
    end})
   
        page11:AddLabelX({Name = "Accessory"})
    page11:AddButton({Name = "Black Cape [50,000]",Callback =  function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem", "Black Cape")
    end})
    page11:AddButton({Name = "Toemo Ring [500,000]", Callback = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem", "Tomoe Ring")
    end})
    page11:AddButton({Name = "Swordsman Hat [150,000]", Callback = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem", "Swordsman Hat")
    end})
  
        page12:AddButton({Name = "Join Pirates Team",Callback =  function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetTeam", "Pirates")
        end})
        page12:AddButton({Name = "Join Marines Team",Callback =  function()
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetTeam", "Marines")
        end})
  
  
        page12:AddButton({Name =  "Hop Little Player Server", Callback = function()
            local PlaceID = game.PlaceId
            local AllIDs = {}
            local foundAnything = ""
            local actualHour = os.date("!*t").hour
            local Deleted = false
            function TPReturner()
                local Site;
                if foundAnything == "" then
                    Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' ..
                        PlaceID .. '/servers/Public?sortOrder=Asc&limit=100'))
                else
                    Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' ..
                        PlaceID .. '/servers/Public?sortOrder=Asc&limit=100&cursor=' .. foundAnything))
                end
                local ID = ""
                if Site.nextPageCursor and Site.nextPageCursor ~= "null" and Site.nextPageCursor ~= nil then
                    foundAnything = Site.nextPageCursor
                end
                local num = 0;
                for i, v in pairs(Site.data) do
                    local Possible = true
                    ID = tostring(v.id)
                    if tonumber(v.maxPlayers) > tonumber(v.playing) then
                        for _, Existing in pairs(AllIDs) do
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
                            task.wait()
                            pcall(function()
                                -- writefile("NotSameServers.json", game:GetService('HttpService'):JSONEncode(AllIDs))
                                task.wait()
                                game:GetService("TeleportService"):TeleportToPlaceInstance(PlaceID, ID,
                                    game.Players.LocalPlayer)
                            end)
                            wait(4)
                        end
                    end
                end
            end
            function Teleport()
                while task.wait() do
                    pcall(function()
                        TPReturner()
                        if foundAnything ~= "" then
                            TPReturner()
                        end
                    end)
                end
            end
            Teleport()
        end})
        page12:AddButton({Name = "Hop Server", Callback = function()
            repeat task.wait() until game:IsLoaded() and game.Players.LocalPlayer
            local HttpService, TPService = game:GetService "HttpService", game:GetService "TeleportService";
            local OtherServers = HttpService:JSONDecode(game:HttpGet("https://games.roblox.com/v1/games/" ..
                game.PlaceId .. "/servers/Public?sortOrder=Asc&limit=100"))
            function joinNew()
                if not isfile('servers.sss') then
                    writefile('servers.sss', HttpService:JSONEncode({}))
                end
                local dontJoin = readfile('servers.sss')
                dontJoin = HttpService:JSONDecode(dontJoin)
    
                for Index, Server in next, OtherServers["data"] do
                    if Server ~= game.JobId then
                        local j = true
                        for a, c in pairs(dontJoin) do
                            if c == Server.id then
                                j = false
                            end
                        end
                        if j then
                            table.insert(dontJoin, Server["id"])
                            writefile("servers.sss", HttpService:JSONEncode(dontJoin))
                            task.wait()
                            return Server['id']
                        end
                    end
                end
            end
            local server = joinNew()
            if not server then
                writefile("servers.sss", HttpService:JSONEncode({}))
                local server = joinNew()
                TPService:TeleportToPlaceInstance(game.PlaceId, server)
            else
                TPService:TeleportToPlaceInstance(game.PlaceId, server)
            end
        end})
        function kaituncap()
            do
                local ui = game:GetService("CoreGui").RobloxGui.Modules.Profile:FindFirstChild("UILibrary")
                if ui then ui:Destroy() end
            end
            local UserInputService = game:GetService("UserInputService")
            local TweenService = game:GetService("TweenService")
            local RunService = game:GetService("RunService")
            local LocalPlayer = game:GetService("Players").LocalPlayer
            local Mouse = LocalPlayer:GetMouse()
            do
                local ui = game:GetService("Lighting"):FindFirstChild("Blur")
                if ui then ui:Destroy() end
            end
            local Blur = Instance.new("BlurEffect")
            TweenService:Create(
                Blur,
                TweenInfo.new(.4, Enum.EasingStyle.Back, Enum.EasingDirection.InOut),
                { Size = 50 }
            ):Play()
            Blur.Parent = game.Lighting
            local UIStroke = Instance.new("UIStroke")
            local UICorner = Instance.new("UICorner")
            local ScreenGui = Instance.new("ScreenGui")
            local ImageButton = Instance.new("ImageButton")
            local RobloxButton = Enum.ButtonStyle.RobloxButton
            ScreenGui.Parent = game.CoreGui
            ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
            local cac = require(game:GetService("Players").LocalPlayer.PlayerGui.Main.UIController.Inventory)
            local Inventory = game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("getInventory")
            local Items = {}
            local RaityLevel = { "Mythical", "Legendary", "Rare", "Uncommon", "Common" }
            local RaityColor = {
                ["Common"] = Color3.fromRGB(179, 179, 179),
                ["Uncommon"] = Color3.fromRGB(92, 140, 211),
                ["Rare"] = Color3.fromRGB(140, 82, 255),
                ["Legendary"] = Color3.fromRGB(213, 43, 228),
                ["Mythical"] = Color3.fromRGB(238, 47, 50)
            }
            function GetRaity(color)
                for k, v in pairs(RaityColor) do
                    if v == color then return k end
                end
            end
            for k, v in pairs(Inventory) do
                Items[v.Name] = v
            end
            local total = #getupvalue(cac.UpdateRender, 4)
            local rac = {}
            local allitem = {}
            local total2 = 0
            while total2 < total do
                local i = 0
                while i < 25000 and total2 < total do
                    game:GetService("Players").LocalPlayer.PlayerGui.Main.InventoryContainer.Right.Content.ScrollingFrame.CanvasPosition =
                        Vector2.new(0, i)
                    for k, v in pairs(game:GetService("Players").LocalPlayer.PlayerGui.Main.InventoryContainer.Right.Content.ScrollingFrame.Frame:GetChildren()) do
                        if v:IsA("Frame") and not rac[v.ItemName.Text] and v.ItemName.Visible == true then
                            local vaihuhu = GetRaity(v.Background.BackgroundColor3)
                            if vaihuhu then
                                if not allitem[vaihuhu] then
                                    allitem[vaihuhu] = {}
                                end
                                table.insert(allitem[vaihuhu], v:Clone())
                            end
                            total2 = total2 + 1
                            rac[v.ItemName.Text] = true
                        end
                    end
                    i = i + 20
                end
                task.wait()
            end
            function GetXY(vec)
                return vec * 100
            end
            local tvk = Instance.new("UIListLayout")
            tvk.FillDirection = Enum.FillDirection.Vertical
            tvk.SortOrder = 2
            tvk.Padding = UDim.new(0, 10)
    
            local Left = Instance.new("Frame", game.Players.LocalPlayer.PlayerGui.BubbleChat)
            Left.BackgroundTransparency = 1
            Left.Size = UDim2.new(.5, 0, 1, 0)
            tvk.Parent = Left
    
            local Right = Instance.new("Frame", game.Players.LocalPlayer.PlayerGui.BubbleChat)
            Right.BackgroundTransparency = 1
            Right.Size = UDim2.new(.5, 0, 1, 0)
            Right.Position = UDim2.new(.6, 0, 0, 0)
            tvk:Clone().Parent = Right
            for k, v in pairs(allitem) do
                local cac = Instance.new("Frame", Left)
                cac.BackgroundTransparency = 1
                cac.Size = UDim2.new(1, 0, 0, 0)
                cac.LayoutOrder = table.find(RaityLevel, k)
    
                local cac2 = Instance.new("Frame", Right)
                cac2.BackgroundTransparency = 1
                cac2.Size = UDim2.new(1, 0, 0, 0)
                cac2.LayoutOrder = table.find(RaityLevel, k)
    
                local tvk = Instance.new("UIGridLayout", cac)
                tvk.CellPadding = UDim2.new(.005, 0, .005, 0)
                tvk.CellSize = UDim2.new(0, 70, 0, 70)
                tvk.FillDirectionMaxCells = 100
                tvk.FillDirection = Enum.FillDirection.Horizontal
    
                local ccc = tvk:Clone()
                ccc.Parent = cac2
                for k, v in pairs(v) do
                    if Items[v.ItemName.Text] and Items[v.ItemName.Text].Mastery then
                        if v.ItemLine2.Text ~= "Accessory" then
                            local bucac                  = v.ItemName:Clone()
                            bucac.BackgroundTransparency = 1
                            bucac.TextSize               = 10
                            bucac.TextXAlignment         = 2
                            bucac.TextYAlignment         = 2
                            bucac.ZIndex                 = 5
                            bucac.Text                   = Items[v.ItemName.Text].Mastery
                            bucac.Size                   = UDim2.new(.5, 0, .5, 0)
                            bucac.Position               = UDim2.new(.5, 0, .5, 0)
                            bucac.Parent                 = v
                        end
                        v.Parent = cac
                    elseif v.ItemLine2.Text == "Blox Fruit" then
                        v.Parent = cac2
                    end
                end
                cac.AutomaticSize = 2
                cac2.AutomaticSize = 2
            end
            local ListHuhu = {
                ["Superhuman"] = Vector2.new(3, 2),
                ["DeathStep"] = Vector2.new(4, 3),
                ["ElectricClaw"] = Vector2.new(2, 0),
                ["SharkmanKarate"] = Vector2.new(0, 0),
                ["DragonTalon"] = Vector2.new(1, 5)
            }
            local MeleeG = Instance.new("Frame", Left)
            MeleeG.BackgroundTransparency = 1
            MeleeG.Size = UDim2.new(1, 0, 0, 0)
            MeleeG.LayoutOrder = table.find(RaityLevel, k)
            MeleeG.AutomaticSize = 2
            MeleeG.LayoutOrder = 100
            local tvk = Instance.new("UIGridLayout", MeleeG)
            tvk.CellPadding = UDim2.new(.005, 0, .005, 0)
            tvk.CellSize = UDim2.new(0, 70, 0, 70)
            tvk.FillDirectionMaxCells = 100
            tvk.FillDirection = Enum.FillDirection.Horizontal
    
            local cac = { "Superhuman", "ElectricClaw", "DragonTalon", "SharkmanKarate", "DeathStep", "GodHuman" }
            for k, v in pairs(cac) do
                if ListHuhu[v] and game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buy" .. v, true) == 1 then
                    local huhu = Instance.new("ImageLabel", MeleeG)
                    huhu.Image = "rbxassetid://9945562382"
                    huhu.ImageRectSize = Vector2.new(100, 100)
                    huhu.ImageRectOffset = ListHuhu[v] * 100
                end
            end
            function formatNumber(v)
                return tostring(v):reverse():gsub("%d%d%d", "%1,"):reverse():gsub("^,", "")
            end
    
            game:GetService("Players").LocalPlayer.PlayerGui.Main.Beli.AnchorPoint = Vector2.new(0.5, 0.5)
            game:GetService("Players").LocalPlayer.PlayerGui.Main.Beli.Position = UDim2.new(0, 1120, 0, 700)
    
            game:GetService("Players").LocalPlayer.PlayerGui.Main.Level.AnchorPoint = Vector2.new(0.5, 0.5)
            game:GetService("Players").LocalPlayer.PlayerGui.Main.Level.Position = UDim2.new(0, 1150, 0, 750)
            local Name = game:GetService("Players").LocalPlayer.PlayerGui.Main.Fragments:Clone()
            Name.Name = "Name"
            Name.Parent = game:GetService("Players").LocalPlayer.PlayerGui.Main.Beli
            Name.Position = UDim2.new(0, 0, -1.5, 0)
            Name.Size = UDim2.new(1, 0, 1, 0)
            Name.TextColor3 = Color3.fromRGB(255, 255, 255)
            Name.Text = game.Players.LocalPlayer.Name
    
            local Fragments = game:GetService("Players").LocalPlayer.PlayerGui.Main.Fragments:Clone()
            Fragments.Name = "FragmentsCheck"
            Fragments.Parent = game:GetService("Players").LocalPlayer.PlayerGui.Main.Beli
            Fragments.Position = UDim2.new(0, 0, -0.75, 0)
            Fragments.Size = UDim2.new(1, 0, 1, 0)
            Fragments.Text = 'ƒ' .. formatNumber(game:GetService("Players").LocalPlayer.Data.Fragments.Value)
            local args = {
                [1] = "getAwakenedAbilities"
            }
    
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
            game.Players.LocalPlayer.PlayerGui.Main.AwakeningToggler.Visible = true
            game:GetService("Players").LocalPlayer.PlayerGui.Main.AwakeningToggler.Position = UDim2.new(0.48, 10, 0.908, 2)
            game:GetService("Players").LocalPlayer.PlayerGui.Main.AwakeningToggler.Size = UDim2.new(1, 0, 0.22, 0)
    
    
            pcall(function()
                game:GetService("Players").LocalPlayer.PlayerGui.Main.MenuButton.Visible = false
            end)
            pcall(function()
                game:GetService("Players").LocalPlayer.PlayerGui.Main.RaceEnergy.Visible = false
            end)
            pcall(function()
                game:GetService("Players").LocalPlayer.PlayerGui.Main.SafeZone.Visible = false
            end)
            pcall(function()
                game:GetService("Players").LocalPlayer.PlayerGui.Main.HP.Visible = false
            end)
            pcall(function()
                game:GetService("Players").LocalPlayer.PlayerGui.Backpack.Enabled.Visible = false
            end)
            pcall(function()
                game:GetService("Players").LocalPlayer.PlayerGui.Main.Energy.Visible = false
            end)
            for k, v in pairs(game:GetService("Players").LocalPlayer.PlayerGui.Main:GetChildren()) do
                if v:IsA("ImageButton") then
                    v:Destroy()
                end
            end
            pcall(function()
                game:GetService("Players").LocalPlayer.PlayerGui.Main.Compass.Visible = false
            end)
        end
        page12:AddButton({Name = "Rejoin", Callback = function()
            local ts = game:GetService("TeleportService")
            local p = game.Players.LocalPlayer
            ts:Teleport(game.PlaceId, p)
        end})
        page12:AddButton({Name = "Kaitun Cap", Callback = function()
            kaituncap()
        end})
        page12:AddButton({Name = "Show Awakened Skill", Callback = function()
            local args = {
                [1] = "getAwakenedAbilities"
            }
            
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
            game.Players.LocalPlayer.PlayerGui.Main.AwakeningToggler.Visible = true
            end})

    function InfAbility()
        if _G.Settings.Misc["InfAbility"] then
            if not game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("Agility") then
                local inf = Instance.new("ParticleEmitter")
                inf.Acceleration = Vector3.new(0, 0, 0)
                inf.Archivable = true
                inf.Drag = 20
                inf.EmissionDirection = Enum.NormalId.Top
                inf.Enabled = true
                inf.Lifetime = NumberRange.new(0.2, 0.2)
                inf.LightInfluence = 0
                inf.LockedToPart = true
                inf.Name = "Agility"
                inf.Rate = 500
                local numberKeypoints2 = {
                    NumberSequenceKeypoint.new(0, 0),
                    NumberSequenceKeypoint.new(1, 4),
                }
    
                inf.Size = NumberSequence.new(numberKeypoints2)
                inf.RotSpeed = NumberRange.new(999, 9999)
                inf.Rotation = NumberRange.new(0, 0)
                inf.Speed = NumberRange.new(30, 30)
                inf.SpreadAngle = Vector2.new(360, 360)
                inf.Texture = "rbxassetid://243098098"
                inf.VelocityInheritance = 0
                inf.ZOffset = 2
                inf.Transparency = NumberSequence.new(0)
                inf.Color = ColorSequence.new(Color3.fromRGB(0, 255, 255), Color3.fromRGB(0, 255, 255))
                inf.Parent = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart
            end
        else
            if game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("Agility") then
                game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("Agility"):Destroy()
            end
        end
    end
 
        page12:AddToggle({Name = "InfAbility", Value = false,Callback = function(value)
            _G.Settings.Misc["InfAbility"] = value
            SaveSettings()
            InfAbility()
        end})

 
        page12:AddToggle({Name = "Infinities Dash", Value = _G.Settings.Misc["No Dash Cooldown"],Callback =  function(value)
            _G.Settings.Misc["No Dash Cooldown"] = value
            DodgeNoCoolDown()
            SaveSettings()
        end})
 
    function DodgeNoCoolDown()
        if _G.Settings.Misc["No Dash Cooldown"] then
            for i, v in next, getgc() do
                if game.Players.LocalPlayer.Character.Dodge then
                    if typeof(v) == "function" and getfenv(v).script == game.Players.LocalPlayer.Character.Dodge then
                        for i2, v2 in next, getupvalues(v) do
                            if tostring(v2) == "0.4" then
                                repeat
                                    wait(.1)
                                    setupvalue(v, i2, 0)
                                until not _G.Settings.Misc["No Dash Cooldown"]
                            end
                        end
                    end
                end
            end
        end
    end

        page12:AddToggle({Name = "Infinities Geppo", Value = _G.Settings.Misc["Infinities SkyJump"],Callback =  function(value)
            _G.Settings.Misc["Infinities SkyJump"] = value
            SkyJumpNoCoolDown()
            SaveSettings()
        end})
 
    function SkyJumpNoCoolDown()
        if _G.Settings.Misc["Infinities SkyJump"] then
            for i, v in next, getgc() do
                if game.Players.LocalPlayer.Character.Geppo then
                    if typeof(v) == "function" and getfenv(v).script == game.Players.LocalPlayer.Character.Geppo then
                        for i2, v2 in next, getupvalues(v) do
                            if tostring(v2) == "0" then
                                repeat
                                    wait(.1)
                                    setupvalue(v, i2, 0)
                                until not _G.Settings.Misc["Infinities SkyJump"]
                            end
                        end
                    end
                end
            end
        end
    end
   
        page12:AddToggle({Name = "Infinities Energy", Value_G.Settings.Misc["Infinities Energy"],Callback = function(value)
            _G.Settings.Misc["Infinities Energy"] = value
            InfinitiesEnergy()
            SaveSettings()
        end})
   

        page12:AddToggle({Name = "RemoveFog", Value = _G.Settings.Misc["No Fog"], Callback = function(value)
            _G.Settings.Misc["No Fog"]  = value
            SaveSettings()
            while _G.Settings.Misc["No Fog"]  do task.wait(0)
            game.Lighting.FogEnd = 100000
            game.Lighting.FogStart = 0
            game.Lighting.ClockTime = 14
            game.Lighting.Brightness = 2
            game.Lighting.GlobalShadows = false
            end
        end})
    _G.Settings.Misc['Auto Rejoin'] = true
    spawn(function()
        while task.wait() do
            if _G.Settings.Misc['Auto Rejoin'] then
                _G.Settings.Misc['Auto Rejoin'] = game:GetService("CoreGui").RobloxPromptGui.promptOverlay.ChildAdded
                    :Connect(function(child)
                        if child.Name == 'ErrorPrompt' and child:FindFirstChild('MessageArea') and child.MessageArea:FindFirstChild("ErrorFrame") then
                            print("Rejoin!")
                            game:GetService("TeleportService"):Teleport(game.PlaceId)
                    end
                end)
            end
        end
    end)

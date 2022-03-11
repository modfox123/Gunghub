local ScreenGui = Instance.new("ScreenGui")

    local ImageButton = Instance.new("ImageButton")

    ScreenGui.Parent = game:GetService("Players").LocalPlayer:WaitForChild("PlayerGui")

    ImageButton.Parent = ScreenGui

    ImageButton.BackgroundColor3 = Color3.fromRGB(15, 15, 15)

    ImageButton.Position = UDim2.new(0.120833337, 0, 0.0952890813, 0)

    ImageButton.Size = UDim2.new(0, 50, 0, 50)

    ImageButton.Image = "rbxassetid://3926305904"

    ImageButton.MouseButton1Down:connect(function()

    game.CoreGui:FindFirstChild("Discord").Enabled = not game.CoreGui:FindFirstChild("Discord").Enabled

end)

local DiscordLib = loadstring(game:HttpGet"https://raw.githubusercontent.com/dawid-scripts/UI-Libs/main/discord%20lib.txt")()

local win = DiscordLib:Window("Blox Fruit Update 30")

local serv = win:Server("Ez", "")

local Main = serv:Channel("Main")

local Cat = serv:Channel("State")

Main:Toggle("AutoFarm", nil, function(State)

    _G.AutoFarm = State

end)

local Weaponlist = {}

local Weapon = nil

for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren()) do

    table.insert(Weaponlist,v.Name)

end

Main:Dropdown("select weapon", Weaponlist, function(currentOption)

    Weapon = currentOption

end)

Main:Toggle("Auto Equip", false, function(a)

AutoEquiped = a

end)

spawn(function()

     while wait() do

        if AutoEquiped then

            pcall(function()

            game.Players.LocalPlayer.Character.Humanoid:EquipTool(game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(Weapon))

            end)

        end

    end

end)

Main:Button("Redeem All code", nil, function()

function UseCode(Text)

        game:GetService("ReplicatedStorage").Remotes.Redeem:InvokeServer(Text)

    end

    UseCode("UPD16")

    UseCode("1MLIKES_RESET")

    UseCode("2BILLION")

    UseCode("UPD15")

    UseCode("FUDD10")

    UseCode("BIGNEWS")

    UseCode("THEGREATACE")

    UseCode("SUB2GAMERROBOT_EXP1")

    UseCode("StrawHatMaine")

    UseCode("Sub2OfficialNoobie")

    UseCode("SUB2NOOBMASTER123")

    UseCode("Sub2Daigrock")

    UseCode("Axiore")

    UseCode("TantaiGaming")

    UseCode("STRAWHATMAINE")

end)

 Cat:Toggle("Melee",nil,function(value)

    _G.Melee = value

if _G.Melee == true then

while _G.Melee do wait()

local A_1 = "AddPoint"

local A_2 = "Melee"

local A_3 = PointStats

local Event = game:GetService("ReplicatedStorage").Remotes["CommF_"]

Event:InvokeServer(A_1, A_2, A_3)

end

end

end)

Cat:Toggle("Defense",nil,function(value)

        _G.Defense = value

if _G.Defense == true then

while _G.Defense do wait()

local A_1 = "AddPoint"

local A_2 = "Defense"

local A_3 = PointStats

local Event = game:GetService("ReplicatedStorage").Remotes["CommF_"]

Event:InvokeServer(A_1, A_2, A_3)

end

end

end)

Cat:Toggle("Sword",nil,function(value)

        _G.Sword = value

if _G.Sword == true then

while _G.Sword do wait()

local A_1 = "AddPoint"

local A_2 = "Sword"

local A_3 = PointStats

local Event = game:GetService("ReplicatedStorage").Remotes["CommF_"]

Event:InvokeServer(A_1, A_2, A_3)

end

end

end)

Cat:Toggle("Gun",nil,function(value)

        _G.Gun = value

if _G.Gun == true then

while _G.Gun do wait()

local A_1 = "AddPoint"

local A_2 = "Gun"

local A_3 = PointStats

local Event = game:GetService("ReplicatedStorage").Remotes["CommF_"]

Event:InvokeServer(A_1, A_2, A_3)

end

end

end)

Cat:Toggle("Fruit",nil,function(value)

        _G.Bloxfruit = value

if _G.Bloxfruit == true then

while _G.Bloxfruit do wait()

local A_1 = "AddPoint"

local A_2 = "Demon Fruit"

local A_3 = PointStats

local Event = game:GetService("ReplicatedStorage").Remotes["CommF_"]

Event:InvokeServer(A_1, A_2, A_3)

end

end

end)

local placeId = game.PlaceId

if placeId == 2753915549 then

    OldWorld = true

elseif placeId == 4442272183 then

    NewWorld =  true

elseif placeId == 7449423635 then

    ThirdWorld =  true

else

    game:GetService("Players").LocalPlayer:Kick("มึงรันแมพอื่นทำควยไร!")

end

function topos(Para1)

    Distance = (Para1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude

    if Distance <= 280 then

        Speed = 270

    elseif Distance >= 281 then

        Speed = 270

    end

    pcall(function() 

        tween = game:GetService("TweenService"):Create(game.Players.LocalPlayer.Character.HumanoidRootPart,TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),{CFrame = Para1})

        tween:Play()

        _G.Clip = true

        if _G.StopTween == true then

            tween:Cancel()

            _G.Clip = false

        end

    end)

end

spawn(function()

    while wait() do 

        pcall(function()

            if _G.AutoFarm then

                local Xd = Instance.new("Part")

                Xd.Name = "xd"

                Xd.Parent = game.Workspace

                Xd.Anchored = true

                Xd.Transparency = 1

                Xd.Color = Color3.fromRGB(255, 155, 0)

                Xd.Size = Vector3.new(15,0.5,15)

                Xd.Material = "Neon"

                if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position-game.Workspace["xd"].Position).Magnitude > 5 then

                    game.Workspace["xd"].CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.X,game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Y-1.5,game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Z)

                end

            else

                if game:GetService("Workspace").xd then

                    game:GetService("Workspace").xd:Destroy()

                end

            end

        end)

    end

end)

function Check()

    local MyLevel = game.Players.LocalPlayer.Data.Level.Value

    if OldWorld then

		if MyLevel == 1 or MyLevel <= 9 then -- Bandit            

			Mon = "Bandit [Lv. 5]"

			NameQ = "BanditQuest1"

			NumberQ = 1

			NameMon = "Bandit"

			POSQ = CFrame.new(1061.66699, 16.5166187, 1544.52905, -0.942978859, -3.33851502e-09, 0.332852632, 7.04340497e-09, 1, 2.99841325e-08, -0.332852632, 3.06188177e-08, -0.942978859)

		elseif MyLevel == 10 or MyLevel <= 14 then -- Monkey

			Mon = "Monkey [Lv. 14]"

			NameQ = "JungleQuest"

			NumberQ = 1

			NameMon = "Monkey"

			POSQ = CFrame.new(-1604.12012, 36.8521118, 154.23732, 0.0648873374, -4.70858913e-06, -0.997892559, 1.41431883e-07, 1, -4.70933674e-06, 0.997892559, 1.64442184e-07, 0.0648873374)

			

		elseif MyLevel == 15 or MyLevel <= 29 then -- Gorilla

			Mon = "Gorilla [Lv. 20]"

			NameQ = "JungleQuest"

			NumberQ = 2

			NameMon = "Gorilla"

			POSQ = CFrame.new(-1604.12012, 36.8521118, 154.23732, 0.0648873374, -4.70858913e-06, -0.997892559, 1.41431883e-07, 1, -4.70933674e-06, 0.997892559, 1.64442184e-07, 0.0648873374)

			

		elseif MyLevel == 30 or MyLevel <= 39 then -- Pirate

			Mon = "Pirate [Lv. 35]"

			NameQ = "BuggyQuest1"

			NumberQ = 1

			NameMon = "Pirate"

			POSQ = CFrame.new(-1139.59717, 4.75205183, 3825.16211, -0.959730506, -7.5857054e-09, 0.280922383, -4.06310328e-08, 1, -1.11807175e-07, -0.280922383, -1.18718916e-07, -0.959730506)

			

		elseif MyLevel == 40 or MyLevel <= 59 then -- Brute

			Mon = "Brute [Lv. 45]"

			NameQ = "BuggyQuest1"

			NumberQ = 2

			NameMon = "Brute"

			POSQ = CFrame.new(-1139.59717, 4.75205183, 3825.16211, -0.959730506, -7.5857054e-09, 0.280922383, -4.06310328e-08, 1, -1.11807175e-07, -0.280922383, -1.18718916e-07, -0.959730506)

			

		elseif MyLevel == 60 or MyLevel <= 74 then -- Desert Bandit

			Mon = "Desert Bandit [Lv. 60]"

			NameQ = "DesertQuest"

			NumberQ = 1

			NameMon = "Desert Bandit"

			POSQ = CFrame.new(897.031128, 6.43846416, 4388.97168, -0.804044724, 3.68233266e-08, 0.594568789, 6.97835176e-08, 1, 3.24365246e-08, -0.594568789, 6.75715199e-08, -0.804044724)

			

		elseif MyLevel == 75 or MyLevel <= 89 then -- Desert Officre

			Mon = "Desert Officer [Lv. 70]"

			NameQ = "DesertQuest"

			NumberQ = 2

			NameMon = "Desert Officer"

			POSQ = CFrame.new(897.031128, 6.43846416, 4388.97168, -0.804044724, 3.68233266e-08, 0.594568789, 6.97835176e-08, 1, 3.24365246e-08, -0.594568789, 6.75715199e-08, -0.804044724)

			

		elseif MyLevel == 90 or MyLevel <= 99 then -- Snow Bandits

			Mon = "Snow Bandit [Lv. 90]"

			NameQ = "SnowQuest"

			NumberQ = 1

			NameMon = "Snow Bandits"

			POSQ = CFrame.new(1384.14001, 87.272789, -1297.06482, 0.348555952, -2.53947841e-09, -0.937287986, 1.49860568e-08, 1, 2.86358204e-09, 0.937287986, -1.50443711e-08, 0.348555952)

			

		elseif MyLevel == 100 or MyLevel <= 119 then -- Snowman

			Mon = "Snowman [Lv. 100]"

			NumberQ = "SnowQuest"

			NumberQ = 2

			NameMon = "Snowman"

			POSQ = CFrame.new(1384.14001, 87.272789, -1297.06482, 0.348555952, -2.53947841e-09, -0.937287986, 1.49860568e-08, 1, 2.86358204e-09, 0.937287986, -1.50443711e-08, 0.348555952)

			

		elseif MyLevel == 120 or MyLevel <= 149 then -- Chief Petty Officer

			Mon = "Chief Petty Officer [Lv. 120]"

			NameQ = "MarineQuest2"

			NumberQ = 1

			NameMon = "Chief Petty Officer"

			POSQ = CFrame.new(-5035.0835, 28.6520386, 4325.29443, 0.0243340395, -7.08064647e-08, 0.999703884, -6.36926814e-08, 1, 7.23777944e-08, -0.999703884, -6.54350671e-08, 0.0243340395)

			

		elseif MyLevel == 150 or MyLevel <= 174 then -- Sky Bandit

			Mon = "Sky Bandit [Lv. 150]"

			NameQ = "SkyQuest"

			NumberQ = 1

			NameMon = "Sky Bandit"

			POSQ = CFrame.new(-4841.83447, 717.669617, -2623.96436, -0.875942111, 5.59710216e-08, -0.482416272, 3.04023082e-08, 1, 6.08195947e-08, 0.482416272, 3.86078725e-08, -0.875942111)

			

		elseif MyLevel == 175 or MyLevel <= 224 then -- Dark Master

			Mon = "Dark Master [Lv. 175]"

			NameQ = "SkyQuest"

			NumberQ = 2

			NameMon = "Dark Master"

			POSQ = CFrame.new(-4841.83447, 717.669617, -2623.96436, -0.875942111, 5.59710216e-08, -0.482416272, 3.04023082e-08, 1, 6.08195947e-08, 0.482416272, 3.86078725e-08, -0.875942111)

			

		elseif MyLevel == 225 or MyLevel <= 274 then -- Toga Warrior

			Mon = "Toga Warrior [Lv. 225]"

			NameQ = "ColosseumQuest"

			NumberQ = 1

			NameMon = "Toga Warrior"

			POSQ = CFrame.new(-1576.11743, 7.38933945, -2983.30762, 0.576966345, 1.22114863e-09, 0.816767931, -3.58496594e-10, 1, -1.24185606e-09, -0.816767931, 4.2370063e-10, 0.576966345)

			

		elseif MyLevel == 275 or MyLevel <= 299 then -- Gladiato

			Mon = "Gladiator [Lv. 275]"

			NameQ = "ColosseumQuest"

			NumberQ = 2

			NameMon = "Gladiato"

			POSQ = CFrame.new(-1576.11743, 7.38933945, -2983.30762, 0.576966345, 1.22114863e-09, 0.816767931, -3.58496594e-10, 1, -1.24185606e-09, -0.816767931, 4.2370063e-10, 0.576966345)

			

		elseif MyLevel == 300 or MyLevel <= 329 then -- Military Soldier

			Mon = "Military Soldier [Lv. 300]"

			NameQ = "MagmaQuest"

			NumberQ = 1

			NameMon = "Military Soldier"

			POSQ = CFrame.new(-5316.55859, 12.2370615, 8517.2998, 0.588437557, -1.37880001e-08, -0.808542669, -2.10116209e-08, 1, -3.23446478e-08, 0.808542669, 3.60215964e-08, 0.588437557)

			

		elseif MyLevel == 300 or MyLevel <= 374 then -- Military Spy

			Mon = "Military Spy [Lv. 330]"

			NameQ = "MagmaQuest"

			NumberQ = 2

			NameMon = "Military Spy"

			POSQ = CFrame.new(-5316.55859, 12.2370615, 8517.2998, 0.588437557, -1.37880001e-08, -0.808542669, -2.10116209e-08, 1, -3.23446478e-08, 0.808542669, 3.60215964e-08, 0.588437557)

			

		elseif MyLevel == 375 or MyLevel <= 399 then -- Fishman Warrior

			Mon = "Fishman Warrior [Lv. 375]"

			NameQ = "FishmanQuest"

			NumberQ = 1

			NameMon = "Fishman Warrior"

			POSQ = CFrame.new(61122.5625, 18.4716396, 1568.16504, 0.893533468, 3.95251609e-09, 0.448996574, -2.34327455e-08, 1, 3.78297464e-08, -0.448996574, -4.43233645e-08, 0.893533468)

			 

		elseif MyLevel == 400 or MyLevel <= 449 then -- Fishman Commando

			Mon = "Fishman Commando [Lv. 400]"

			NameQ = "FishmanQuest"

			NumberQ = 2

			NameMon = "Fishman Commando"

			POSQ = CFrame.new(61122.5625, 18.4716396, 1568.16504, 0.893533468, 3.95251609e-09, 0.448996574, -2.34327455e-08, 1, 3.78297464e-08, -0.448996574, -4.43233645e-08, 0.893533468)

			

		elseif MyLevel == 450 or MyLevel <= 474 then -- God's Guards

			Mon = "God's Guard [Lv. 450]"

			NameQ = "SkyExp1Quest"

			NumberQ = 1

			NameMon = "God's Guards"

			POSQ = CFrame.new(-4721.71436, 845.277161, -1954.20105, -0.999277651, -5.56969759e-09, 0.0380011722, -4.14751478e-09, 1, 3.75035256e-08, -0.0380011722, 3.73188307e-08, -0.999277651)

			

		elseif MyLevel == 475 or MyLevel <= 524 then -- Shandas

			Mon = "Shanda [Lv. 475]"

			NameQ = "SkyExp1Quest"

			NumberQ = 2

			NameMon = "Shandas"

			POSQ = CFrame.new(-7863.63672, 5545.49316, -379.826324, 0.362120807, -1.98046344e-08, -0.93213129, 4.05822291e-08, 1, -5.48095125e-09, 0.93213129, -3.58431969e-08, 0.362120807)

			

		elseif MyLevel == 525 or MyLevel <= 549 then -- Royal Squad

			Mon = "Royal Squad [Lv. 525]"

			NameQ = "SkyExp2Quest"

			NumberQ = 1

			NameMon = "Royal Squad"

			POSQ = CFrame.new(-7902.66895, 5635.96387, -1411.71802, 0.0504222959, 2.5710392e-08, 0.998727977, 1.12541557e-07, 1, -3.14249675e-08, -0.998727977, 1.13982921e-07, 0.0504222959)

			

		elseif MyLevel == 550 or MyLevel <= 624 then -- Royal Soldier

			Mon = "Royal Soldier [Lv. 550]"

			NameQ = "SkyExp2Quest"

			NumberQ = 2

			NameMon = "Royal Soldier"

			POSQ = CFrame.new(-7902.66895, 5635.96387, -1411.71802, 0.0504222959, 2.5710392e-08, 0.998727977, 1.12541557e-07, 1, -3.14249675e-08, -0.998727977, 1.13982921e-07, 0.0504222959)

			

		elseif MyLevel == 625 or MyLevel <= 649 then -- Galley Pirate

			Mon = "Galley Pirate [Lv. 625]"

			NameQ = "FountainQuest"

			NumberQ = 1

			NameMon = "Galley Pirate"

			POSQ = CFrame.new(5254.60156, 38.5011406, 4049.69678, -0.0504891425, -3.62066501e-08, -0.998724639, -9.87921389e-09, 1, -3.57534553e-08, 0.998724639, 8.06145284e-09, -0.0504891425)

			

		elseif MyLevel >= 650 then -- Galley Captain

			Mon = "Galley Captain [Lv. 650]"

			NameQ = "FountainQuest"

			NumberQ = 2

			NameMon = "Galley Captain"

			POSQ = CFrame.new(5254.60156, 38.5011406, 4049.69678, -0.0504891425, -3.62066501e-08, -0.998724639, -9.87921389e-09, 1, -3.57534553e-08, 0.998724639, 8.06145284e-09, -0.0504891425)

			

		end

    elseif NewWorld then

		if MyLevel == 700 or MyLevel <= 724 then -- Raider [Lv. 700]

			Mon = "Raider [Lv. 700]"

			NameQ = "Area1Quest"

			NumberQ = 1

			NameMon = "Raider"

			POSQ = CFrame.new(-424.080078, 73.0055847, 1836.91589, 0.253544956, -1.42165932e-08, 0.967323601, -6.00147771e-08, 1, 3.04272909e-08, -0.967323601, -6.5768397e-08, 0.253544956)

			

		elseif MyLevel == 725 or MyLevel <= 774 then -- Mercenary [Lv. 725]

			Mon = "Mercenary [Lv. 725]"

			NameQ = "Area1Quest"

			NumberQ = 2

			NameMon = "Mercenary"

			POSQ = CFrame.new(-424.080078, 73.0055847, 1836.91589, 0.253544956, -1.42165932e-08, 0.967323601, -6.00147771e-08, 1, 3.04272909e-08, -0.967323601, -6.5768397e-08, 0.253544956)

			

		elseif MyLevel == 775 or MyLevel <= 799 then -- Swan Pirate [Lv. 775]

			Mon = "Swan Pirate [Lv. 775]"

			NameQ = "Area2Quest"

			NumberQ = 1

			NameMon = "Swan Pirate"

			POSQ = CFrame.new(632.698608, 73.1055908, 918.666321, -0.0319722369, 8.96074881e-10, -0.999488771, 1.36326533e-10, 1, 8.92172336e-10, 0.999488771, -1.07732087e-10, -0.0319722369)

			

		elseif MyLevel == 800 or MyLevel <= 874 then -- Factory Staff [Lv. 800]

			Mon = "Factory Staff [Lv. 800]"

			NameQ = "Area2Quest"

			NumberQ = 2

			NameMon = "Factory Staff"

			POSQ = CFrame.new(632.698608, 73.1055908, 918.666321, -0.0319722369, 8.96074881e-10, -0.999488771, 1.36326533e-10, 1, 8.92172336e-10, 0.999488771, -1.07732087e-10, -0.0319722369)

			

		elseif MyLevel == 875 or MyLevel <= 899 then -- Marine Lieutenant [Lv. 875]

			Mon = "Marine Lieutenant [Lv. 875]"

			NameQ = "MarineQuest3"

			NumberQ = 1

			NameMon = "Marine Lieutenant"

			POSQ = CFrame.new(-2442.65015, 73.0511475, -3219.11523, -0.873540044, 4.2329841e-08, -0.486752301, 5.64383384e-08, 1, -1.43220786e-08, 0.486752301, -3.99823996e-08, -0.873540044)

			

		elseif MyLevel == 900 or MyLevel <= 949 then -- Marine Captain [Lv. 900]

			Mon = "Marine Captain [Lv. 900]"

			NameQ = "MarineQuest3"

			NumberQ = 2

			NameMon = "Marine Captain"

			POSQ = CFrame.new(-2442.65015, 73.0511475, -3219.11523, -0.873540044, 4.2329841e-08, -0.486752301, 5.64383384e-08, 1, -1.43220786e-08, 0.486752301, -3.99823996e-08, -0.873540044)

			

		elseif MyLevel == 950 or MyLevel <= 974 then -- Zombie [Lv. 950]

			Mon = "Zombie [Lv. 950]"

			NameQ = "ZombieQuest"

			NumberQ = 1

			NameMon = "Zombie"

			POSQ = CFrame.new(-5492.79395, 48.5151672, -793.710571, 0.321800292, -6.24695815e-08, 0.946807742, 4.05616092e-08, 1, 5.21931227e-08, -0.946807742, 2.16082796e-08, 0.321800292)

			

		elseif MyLevel == 975 or MyLevel <= 999 then -- Vampire [Lv. 975]

			Mon = "Vampire [Lv. 975]"

			NameQ = "ZombieQuest"

			NumberQ = 2

			NameMon = "Vampire"

			POSQ = CFrame.new(-5492.79395, 48.5151672, -793.710571, 0.321800292, -6.24695815e-08, 0.946807742, 4.05616092e-08, 1, 5.21931227e-08, -0.946807742, 2.16082796e-08, 0.321800292)

			

		elseif MyLevel == 1000 or MyLevel <= 1049 then -- Snow Trooper [Lv. 1000] **

			Mon = "Snow Trooper [Lv. 1000]"

			NameQ = "SnowMountainQuest"

			NumberQ = 1

			NameMon = "Snow Trooper"

			POSQ = CFrame.new(604.964966, 401.457062, -5371.69287, 0.353063971, 1.89520435e-08, -0.935599446, -5.81846002e-08, 1, -1.70033754e-09, 0.935599446, 5.50377841e-08, 0.353063971)

			

		elseif MyLevel == 1050 or MyLevel <= 1099 then -- Winter Warrior [Lv. 1050]

			Mon = "Winter Warrior [Lv. 1050]"

			NameQ = "SnowMountainQuest"

			NumberQ = 2

			NameMon = "Winter Warrior"

			POSQ = CFrame.new(604.964966, 401.457062, -5371.69287, 0.353063971, 1.89520435e-08, -0.935599446, -5.81846002e-08, 1, -1.70033754e-09, 0.935599446, 5.50377841e-08, 0.353063971)

			

		elseif MyLevel == 1100 or MyLevel <= 1124 then -- Lab Subordinate [Lv. 1100]

			Mon = "Lab Subordinate [Lv. 1100]"

			NameQ = "IceSideQuest"

			NumberQ = 1

			NameMon = "Lab Subordinate"

			POSQ = CFrame.new(-6060.10693, 15.9868021, -4904.7876, -0.411000341, -5.06538868e-07, 0.91163528, 1.26306062e-07, 1, 6.12581289e-07, -0.91163528, 3.66916197e-07, -0.411000341)

			

		elseif MyLevel == 1125 or MyLevel <= 1174 then -- Horned Warrior [Lv. 1125]

			Mon = "Horned Warrior [Lv. 1125]"

			NameQ = "IceSideQuest"

			NumberQ = 2

			NameMon = "Horned Warrior"

			POSQ = CFrame.new(-6060.10693, 15.9868021, -4904.7876, -0.411000341, -5.06538868e-07, 0.91163528, 1.26306062e-07, 1, 6.12581289e-07, -0.91163528, 3.66916197e-07, -0.411000341)

			

		elseif MyLevel == 1175 or MyLevel <= 1199 then -- Magma Ninja [Lv. 1175]

			Mon = "Magma Ninja [Lv. 1175]"

			NameQ = "FireSideQuest"

			NumberQ = 1

			NameMon = "Magma Ninja"

			POSQ = CFrame.new(-5431.09473, 15.9868021, -5296.53223, 0.831796765, 1.15322464e-07, -0.555080295, -1.10814341e-07, 1, 4.17010995e-08, 0.555080295, 2.68240168e-08, 0.831796765)

			

		elseif MyLevel == 1200 or MyLevel <= 1249 then -- Lava Pirate [Lv. 1200]

			Mon = "Lava Pirate [Lv. 1200]"

			NameQ = "FireSideQuest"

			NumberQ = 2

			NameMon = "Lava Pirate"

			POSQ = CFrame.new(-5431.09473, 15.9868021, -5296.53223, 0.831796765, 1.15322464e-07, -0.555080295, -1.10814341e-07, 1, 4.17010995e-08, 0.555080295, 2.68240168e-08, 0.831796765)

			

		elseif MyLevel == 1250 or MyLevel <= 1274 then -- Ship Deckhand [Lv. 1250]

			Mon = "Ship Deckhand [Lv. 1250]"

			NameQ = "ShipQuest1"

			NumberQ = 1

			NameMon = "Ship Deckhand"

			POSQ = CFrame.new(1037.80127, 125.092171, 32911.6016, -0.244533166, -0, -0.969640911, -0, 1.00000012, -0, 0.96964103, 0, -0.244533136)

			

		elseif MyLevel == 1275 or MyLevel <= 1299 then -- Ship Engineer [Lv. 1275]

			Mon = "Ship Engineer [Lv. 1275]"

			NameQ = "ShipQuest1"

			NumberQ = 2

			NameMon = "Ship Engineer"

			POSQ = CFrame.new(1037.80127, 125.092171, 32911.6016, -0.244533166, -0, -0.969640911, -0, 1.00000012, -0, 0.96964103, 0, -0.244533136)

			

		elseif MyLevel == 1300 or MyLevel <= 1324 then -- Ship Steward [Lv. 1300]

			Mon = "Ship Steward [Lv. 1300]"

			NameQ = "ShipQuest2"

			NumberQ = 1

			NameMon = "Ship Steward"

			POSQ = CFrame.new(968.80957, 125.092171, 33244.125, -0.869560242, 1.51905191e-08, -0.493826836, 1.44108379e-08, 1, 5.38534195e-09, 0.493826836, -2.43357912e-09, -0.869560242)

			

		elseif MyLevel == 1325 or MyLevel <= 1349 then -- Ship Officer [Lv. 1325]

			Mon = "Ship Officer [Lv. 1325]"

			NameQ = "ShipQuest2"

			NumberQ = 2

			NameMon = "Ship Officer"

			POSQ = CFrame.new(968.80957, 125.092171, 33244.125, -0.869560242, 1.51905191e-08, -0.493826836, 1.44108379e-08, 1, 5.38534195e-09, 0.493826836, -2.43357912e-09, -0.869560242)

			

		elseif MyLevel == 1350 or MyLevel <= 1374 then -- Arctic Warrior [Lv. 1350]

			Mon = "Arctic Warrior [Lv. 1350]"

			NameQ = "FrostQuest"

			NumberQ = 1

			NameMon = "Arctic Warrior"

			POSQ = CFrame.new(5669.43506, 28.2117786, -6482.60107, 0.888092756, 1.02705066e-07, 0.459664226, -6.20391774e-08, 1, -1.03572376e-07, -0.459664226, 6.34646895e-08, 0.888092756)

			

		elseif MyLevel == 1375 or MyLevel <= 1424 then -- Snow Lurker [Lv. 1375]

			Mon = "Snow Lurker [Lv. 1375]"

			NameQ = "FrostQuest"

			NumberQ = 2

			NameMon = "Snow Lurker"

			POSQ = CFrame.new(5669.43506, 28.2117786, -6482.60107, 0.888092756, 1.02705066e-07, 0.459664226, -6.20391774e-08, 1, -1.03572376e-07, -0.459664226, 6.34646895e-08, 0.888092756)

			

		elseif MyLevel == 1425 or MyLevel <= 1449 then -- Sea Soldier [Lv. 1425]

			Mon = "Sea Soldier [Lv. 1425]"

			NameQ = "ForgottenQuest"

			NumberQ = 1

			NameMon = "Sea Soldier"

			POSQ = CFrame.new(-3052.99097, 236.881363, -10148.1943, -0.997911751, 4.42321983e-08, 0.064591676, 4.90968759e-08, 1, 7.37270085e-08, -0.064591676, 7.67442998e-08, -0.997911751)

			

		elseif MyLevel >= 1450 then -- Water Fighter [Lv. 1450]

			Mon = "Water Fighter [Lv. 1450]"

			NameQ = "ForgottenQuest"

			NumberQ = 2

			NameMon = "Water Fighter"

			POSQ = CFrame.new(-3052.99097, 236.881363, -10148.1943, -0.997911751, 4.42321983e-08, 0.064591676, 4.90968759e-08, 1, 7.37270085e-08, -0.064591676, 7.67442998e-08, -0.997911751)

			

		end

    elseif ThirdWorld then

		if MyLevel == 1500 or MyLevel <= 1524 then

			Mon = "Pirate Millionaire [Lv. 1500]"

			NameQ = "PiratePortQuest"

			NumberQ = 1

			NameMon = "Pirate Millionaire"

			POSQ = CFrame.new(-290.074677, 42.9034653, 5581.58984, 0.965929627, -0, -0.258804798, 0, 1, -0, 0.258804798, 0, 0.965929627)

			

		elseif MyLevel == 1525 or MyLevel <= 1574 then

			Mon = "Pistol Billionaire [Lv. 1525]"

			NameQ = "PiratePortQuest"

			LevelQuest = 2

			NameMon = "Pistol Billionaire"

			POSQ = CFrame.new(-290.074677, 42.9034653, 5581.58984, 0.965929627, -0, -0.258804798, 0, 1, -0, 0.258804798, 0, 0.965929627)

			

		elseif MyLevel == 1575 or MyLevel <= 1599 then

			Mon = "Dragon Crew Warrior [Lv. 1575]"

			NameQ = "AmazonQuest"

			NumberQ = 1

			NameMon = "Dragon Crew Warrior"

			POSQ = CFrame.new(5832.83594, 51.6806107, -1101.51563, 0.898790359, -0, -0.438378751, 0, 1, -0, 0.438378751, 0, 0.898790359)

			

		elseif MyLevel == 1600 or MyLevel <= 1624 then

			Mon = "Dragon Crew Archer [Lv. 1600]"

			NameQ = "AmazonQuest"

			NumberQ = 2

			NameMon = "Dragon Crew Archer"

			POSQ = CFrame.new(5832.83594, 51.6806107, -1101.51563, 0.898790359, -0, -0.438378751, 0, 1, -0, 0.438378751, 0, 0.898790359)

			

		elseif MyLevel == 1625 or MyLevel <= 1649 then

			Mon = "Female Islander [Lv. 1625]"

			NameQ = "AmazonQuest2"

			NumberQ = 1

			NameMon = "Female Islander"

			POSQ = CFrame.new(5448.86133, 601.516174, 751.130676, 0, 0, 1, 0, 1, -0, -1, 0, 0)

			

		elseif MyLevel == 1650 or MyLevel <= 1699 then

			Mon = "Giant Islander [Lv. 1650]"

			NameQ = "AmazonQuest2"

			NumberQ = 2

			NameMon = "Giant Islander"

			POSQ = CFrame.new(5448.86133, 601.516174, 751.130676, 0, 0, 1, 0, 1, -0, -1, 0, 0)

			

		elseif MyLevel == 1700 or MyLevel <= 1724 then

			Mon = "Marine Commodore [Lv. 1700]"

			NameQ = "MarineTreeIsland"

			NumberQ = 1

			NameMon = "Marine Commodore"

			POSQ = CFrame.new(2180.54126, 27.8156815, -6741.5498, -0.965929747, 0, 0.258804798, 0, 1, 0, -0.258804798, 0, -0.965929747)

			

		elseif MyLevel == 1725 or MyLevel <= 1774 then

			Mon = "Marine Rear Admiral [Lv. 1725]"

			NameQ = "MarineTreeIsland"

			NumberQ = 2

			NameMon = "Marine Rear Admiral"

			POSQ = CFrame.new(2180.54126, 27.8156815, -6741.5498, -0.965929747, 0, 0.258804798, 0, 1, 0, -0.258804798, 0, -0.965929747)

			

		elseif MyLevel == 1775 or MyLevel <= 1799 then

			Mon = "Fishman Raider [Lv. 1775]"

			NameQ = "DeepForestIsland3"

			NumberQ = 1

			NameMon = "Fishman Raider"

			POSQ = CFrame.new(-10581.6563, 330.872955, -8761.18652, -0.882952213, 0, 0.469463557, 0, 1, 0, -0.469463557, 0, -0.882952213)

			

		elseif MyLevel == 1800 or MyLevel <= 1824 then

			Mon = "Fishman Captain [Lv. 1800]"

			NameQ = "DeepForestIsland3"

			NumberQ = 2

			NameMon = "Fishman Captain"

			POSQ = CFrame.new(-10581.6563, 330.872955, -8761.18652, -0.882952213, 0, 0.469463557, 0, 1, 0, -0.469463557, 0, -0.882952213)

			

		elseif MyLevel == 1825 or MyLevel <= 1849 then

			Mon = "Forest Pirate [Lv. 1825]"

			NameQ = "DeepForestIsland"

			NumberQ = 1

			NameMon = "Forest Pirate"

			POSQ = CFrame.new(-13234.04, 331.488495, -7625.40137, 0.707134247, -0, -0.707079291, 0, 1, -0, 0.707079291, 0, 0.707134247)

			

		elseif MyLevel == 1850 or MyLevel <= 1899 then

			Mon = "Mythological Pirate [Lv. 1850]"

			NameQ = "DeepForestIsland"

			NumberQ = 2

			NameMon = "Mythological Pirate"

			POSQ = CFrame.new(-13234.04, 331.488495, -7625.40137, 0.707134247, -0, -0.707079291, 0, 1, -0, 0.707079291, 0, 0.707134247)

			

		elseif MyLevel == 1900 or MyLevel <= 1924 then

			Mon = "Jungle Pirate [Lv. 1900]"

			NameQ = "DeepForestIsland2"

			NumberQ = 1

			NameMon = "Jungle Pirate"

			POSQ = CFrame.new(-12680.3818, 389.971039, -9902.01953, -0.0871315002, 0, 0.996196866, 0, 1, 0, -0.996196866, 0, -0.0871315002)

			

		elseif MyLevel == 1925 or MyLevel <= 1974 then

			Mon = "Musketeer Pirate [Lv. 1925]"

			NameQ = "DeepForestIsland2"

			NumberQ = 2

			NameMon = "Musketeer Pirate"

			POSQ = CFrame.new(-12680.3818, 389.971039, -9902.01953, -0.0871315002, 0, 0.996196866, 0, 1, 0, -0.996196866, 0, -0.0871315002)

			

        elseif MyLevel == 1975 or MyLevel <= 1999 then

			Mon = "Reborn Skeleton [Lv. 1975]"

			NameQ = "HauntedQuest1"

			NumberQ = 1

			NameMon = "Reborn Skeleton"

			POSQ = CFrame.new(-9479.2168, 141.215088, 5566.09277, 0, 0, 1, 0, 1, -0, -1, 0, 0)

			

        elseif MyLevel == 2000 or MyLevel <= 2024 then

			Mon = "Living Zombie [Lv. 2000]"

			NameQ = "HauntedQuest1"

			NumberQ = 2

			NameMon = "Living Zombie"

			POSQ = CFrame.new(-9479.2168, 141.215088, 5566.09277, 0, 0, 1, 0, 1, -0, -1, 0, 0)

			

		elseif MyLevel == 2025 or MyLevel <= 2049 then

			Mon = "Demonic Soul [Lv. 2025]"

			NameQ = "HauntedQuest2"

			NumberQ = 1

			NameMon = "Demonic Soul"

			POSQ = CFrame.new(-9514.78027, 171.162918, 6078.82373, 0.301918149, 7.4535027e-09, 0.953333855, -3.22802141e-09, 1, -6.79604995e-09, -0.953333855, -1.02553133e-09, 0.301918149)

			

		elseif MyLevel == 2050 or MyLevel <= 2074 then

			Mon = "Posessed Mummy [Lv. 2050]" 

			NameQ = "HauntedQuest2"

			NumberQ = 2

			NameMon = "Posessed Mummy"

			POSQ = CFrame.new(-9514.78027, 171.162918, 6078.82373, 0.301918149, 7.4535027e-09, 0.953333855, -3.22802141e-09, 1, -6.79604995e-09, -0.953333855, -1.02553133e-09, 0.301918149)

			

		elseif MyLevel == 2075 or MyLevel <= 2099 then

			Mon = "Peanut Scout [Lv. 2075]" 

			NameQ = "NutsIslandQuest"

			NumberQ = 1

			NameMon = "Peanut Scout"

			POSQ = CFrame.new(-2103.05786, 38.2287407, -10191.8506, 0.741642892, -1.49368617e-09, 0.670794845, 3.05409564e-09, 1, -1.14992271e-09, -0.670794845, 2.90150326e-09, 0.741642892)

			

		elseif MyLevel == 2100 or MyLevel <= 2124 then

			Mon = "Peanut President [Lv. 2100]" 

			NameQ = "NutsIslandQuest"

			NumberQ = 2

			NameMon = "Peanut President"

			POSQ = CFrame.new(-2103.05786, 38.2287407, -10191.8506, 0.741642892, -1.49368617e-09, 0.670794845, 3.05409564e-09, 1, -1.14992271e-09, -0.670794845, 2.90150326e-09, 0.741642892)

			

		elseif MyLevel == 2125 or MyLevel <= 2149  then

			Mon = "Ice Cream Chef [Lv. 2125]" 

			NameQ = "IceCreamIslandQuest"

			NumberQ = 1

			NameMon = "Ice Cream Chef"

			POSQ = CFrame.new(-821.283081, 65.9448776, -10965.6074, 0.785351455, -3.35560451e-08, -0.619050145, -5.61092506e-09, 1, -6.13239379e-08, 0.619050145, 5.1634288e-08, 0.785351455)

			

		elseif MyLevel >= 2150 then

			Mon = "Ice Cream Commander [Lv. 2150]"

			NameQ = "IceCreamIslandQuest"

			NumberQ = 2

			NameMon = "Ice Cream Commander"

			POSQ = CFrame.new(-821.283081, 65.9448776, -10965.6074, 0.785351455, -3.35560451e-08, -0.619050145, -5.61092506e-09, 1, -6.13239379e-08, 0.619050145, 5.1634288e-08, 0.785351455)

			

        end

    end

end

function GetQuest(NameQ,NumberQ)

    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest",NameQ,NumberQ)

end

function attack() -- AUTO ATTACK

    game:GetService'VirtualUser':CaptureController()

game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))

end

spawn(function()

	while wait() do

		pcall(function()

		attack()

		end

end

function Buso()

    if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then

        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")

    end

end

spawn(function()

	while wait() do

		pcall(function()

			if _G.AutoFarm then

				Check()

				if game.Players.LocalPlayer.PlayerGui.Main.Quest.Visible == false then

					_G.FastAttack = false

					topos(POSQ)

					if (POSQ.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 5 then

						wait(1.5)

						GetQuest(NameQ,NumberQ)

						wait(.3)

					end

				elseif game.Players.LocalPlayer.PlayerGui.Main.Quest.Visible == true then

					if game:GetService("Workspace").Enemies:FindFirstChild(Mon) then

						for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do

							if v.Name == Mon then

								if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") then

									if v.Humanoid.Health > 0 then

										if string.find(game.Players.LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text,NameMon) then

												repeat task.wait()

												    Buso()

													v.HumanoidRootPart.CanCollide = false

													v.Head.CanCollide = false

													v.Humanoid.WalkSpeed = 0

													v.HumanoidRootPart.Size = Vector3.new(50,50,50)

													topos(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))

													PosMon = v.HumanoidRootPart.CFrame

													v.Humanoid:ChangeState(11)

													_G.FastAttack = true

											until not _G.AutoFarm or v.Humanoid.Health <= 0 or not v:FindFirstChild("Humanoid") or not v:FindFirstChild("HumanoidRootPart") or game.Players.LocalPlayer.PlayerGui.Main.Quest.Visible == false

										else

											_G.FastAttack = false                                  

											game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")

										end

									end

								end

							end

						end

					else

						_G.FastAttack = false

						local Mob = game:GetService("ReplicatedStorage"):FindFirstChild(Mon) 

						if Mob then

							topos(Mob.HumanoidRootPart.CFrame * CFrame.new(0,20,0))

						else

							if game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Y <= 1 then

								game.Players.LocalPlayer.Character.Humanoid.Jump = true

								task.wait()

								game.Players.LocalPlayer.Character.Humanoid.Jump = false

							end

						end

					end

				end

			end

		end)

	end

end)

spawn(function()

    while wait() do

        pcall(function()

            if _G.AutoFarm then

                for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do

                    for i2,v2 in pairs(game:GetService("Workspace").Enemies:GetChildren()) do	

                        if v.Name == Mon and (v.HumanoidRootPart.Position - v2.HumanoidRootPart.Position).magnitude <= 250 then

                            if v2.Name == Mon and (v.HumanoidRootPart.Position - v2.HumanoidRootPart.Position).magnitude <= 250 then

                                v.HumanoidRootPart.CFrame = v2.HumanoidRootPart.CFrame

                                v.HumanoidRootPart.Size = Vector3.new(100,100,100)

                                v2.HumanoidRootPart.Size = Vector3.new(100,100,100)

                                v.HumanoidRootPart.Transparency = 1

                                v2.HumanoidRootPart.Transparency = 1

                                v.HumanoidRootPart.CanCollide = false

                                v.Head.CanCollide = false

                                v2.Head.CanCollide = false

                                v2.HumanoidRootPart.CanCollide = false

                                sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)

                            end

                        end

                    end

                end

            end

        end)

    end

end)


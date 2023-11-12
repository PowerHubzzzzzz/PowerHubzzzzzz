_G.Color = Color3.fromRGB(107, 244, 62)
_G.Logo = 0000000000


local Evil = loadstring(game:HttpGet("https://newpchx2.0xlii.repl.co/AllUI/Protected_9405524596134885.lua"))()
local Win = library:Evil("Loxi","Hub",_G.Logo )

local tab1 = Win:CraftTab('Main')
local page1 = tab1:CraftPage('Main',1)

local player = page1:Label('Auto Farm')

local placeId = game.PlaceId
if placeId == 2753915549 then
	World1 = true
elseif placeId == 4442272183 then
	World2 = true
elseif placeId == 7449423635 then
	World3 = true
else
	game.Players.LocalPlayer:Kick("Script Not Support")
end


function CheckQuest() 
        MyLevel = game:GetService("Players").LocalPlayer.Data.Level.Value
        if World1 then
            if MyLevel == 1 or MyLevel <= 9 then
                Mon = "Bandit"
                LevelQuest = 1
                NameQuest = "BanditQuest1"
                NameMon = "Bandit"
                CFrameQuest = CFrame.new(1059.37195, 15.4495068, 1550.4231, 0.939700544, -0, -0.341998369, 0, 1, -0, 0.341998369, 0, 0.939700544)
                CFrameMon = CFrame.new(1045.962646484375, 27.00250816345215, 1560.8203125)
            elseif MyLevel == 10 or MyLevel <= 14 then
                Mon = "Monkey"
                LevelQuest = 1
                NameQuest = "JungleQuest"
                NameMon = "Monkey"
                CFrameQuest = CFrame.new(-1598.08911, 35.5501175, 153.377838, 0, 0, 1, 0, 1, -0, -1, 0, 0)
                CFrameMon = CFrame.new(-1448.51806640625, 67.85301208496094, 11.46579647064209)
            elseif MyLevel == 15 or MyLevel <= 29 then
                Mon = "Gorilla"
                LevelQuest = 2
                NameQuest = "JungleQuest"
                NameMon = "Gorilla"
                CFrameQuest = CFrame.new(-1598.08911, 35.5501175, 153.377838, 0, 0, 1, 0, 1, -0, -1, 0, 0)
                CFrameMon = CFrame.new(-1129.8836669921875, 40.46354675292969, -525.4237060546875)
            elseif MyLevel == 30 or MyLevel <= 39 then
                Mon = "Pirate"
                LevelQuest = 1
                NameQuest = "BuggyQuest1"
                NameMon = "Pirate"
                CFrameQuest = CFrame.new(-1141.07483, 4.10001802, 3831.5498, 0.965929627, -0, -0.258804798, 0, 1, -0, 0.258804798, 0, 0.965929627)
                CFrameMon = CFrame.new(-1103.513427734375, 13.752052307128906, 3896.091064453125)
            elseif MyLevel == 40 or MyLevel <= 59 then
                Mon = "Brute"
                LevelQuest = 2
                NameQuest = "BuggyQuest1"
                NameMon = "Brute"
                CFrameQuest = CFrame.new(-1141.07483, 4.10001802, 3831.5498, 0.965929627, -0, -0.258804798, 0, 1, -0, 0.258804798, 0, 0.965929627)
                CFrameMon = CFrame.new(-1140.083740234375, 14.809885025024414, 4322.92138671875)
                end
        end
    end

_G.dw2 = true

function JOOK() 
  Lv = game:GetService("Players").LocalPlayer.Data.Level.Value
 if World2 then
if Lv == 1250 then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
wait(0.1)
game:GetService("Players").LocalPlayer.Character.Humanoid.Health = 0
wait(900)
end
end
end
spawn(function()
while wait() do
if _G.dw2 then
JOOK()
end
end
end)

function Click()
    game:GetService'VirtualUser':CaptureController()
    game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
end

function AutoHaki()
    if not game:GetService("Players").LocalPlayer.Character:FindFirstChild("HasBuso") then
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
    end
end

function UnEquipWeapon(Weapon)
    if game.Players.LocalPlayer.Character:FindFirstChild(Weapon) then
        _G.NotAutoEquip = true
        wait(.5)
        game.Players.LocalPlayer.Character:FindFirstChild(Weapon).Parent = game.Players.LocalPlayer.Backpack
        wait(.1)
        _G.NotAutoEquip = false
    end
end

function EquipWeapon(ToolSe)
    if not _G.NotAutoEquip then
        if game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe) then
            Tool = game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe)
            wait(.1)
            game.Players.LocalPlayer.Character.Humanoid:EquipTool(Tool)
        end
    end
end
function BTP(P1)
    game.Players.LocalPlayer.Character.Head:Destroy()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = P1
    wait(1)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = P1
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetSpawnPoint")
    end
    function GetDistance(target)
        return math.floor((target.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude)
    end
    
	TP1 = function(p)
		task.spawn(function()
			pcall(function()
				if game:GetService("Players").LocalPlayer:DistanceFromCharacter(p.Position) <= 250 then 
					game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = p
				elseif not game.Players.LocalPlayer.Character:FindFirstChild("Root")then 
					local K = Instance.new("Part",game.Players.LocalPlayer.Character)
					K.Size = Vector3.new(1,0.5,1)
					K.Name = "Root"
					K.Anchored = true
					K.Transparency = 1
					K.CanCollide = false
					K.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.new(0,20,0)
				end
				local U = (game.Players.LocalPlayer.Character.HumanoidRootPart.Position-p.Position).Magnitude
				local z = game:service("TweenService")
				local B = TweenInfo.new((p.Position-game.Players.LocalPlayer.Character.Root.Position).Magnitude/300,Enum.EasingStyle.Linear)
				local S,g = pcall(function()
				local q = z:Create(game.Players.LocalPlayer.Character.Root,B,{CFrame = p})
				q:Play()
			end)
			if not S then 
				return g
			end
			game.Players.LocalPlayer.Character.Root.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
				if S and game.Players.LocalPlayer.Character:FindFirstChild("Root") then 
					pcall(function()
						if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position-p.Position).Magnitude >= 20 then 
							spawn(function()
								pcall(function()
									if (game.Players.LocalPlayer.Character.Root.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 150 then 
										game.Players.LocalPlayer.Character.Root.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
									else 
										game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame=game.Players.LocalPlayer.Character.Root.CFrame
									end
								end)
							end)
						elseif (game.Players.LocalPlayer.Character.HumanoidRootPart.Position-p.Position).Magnitude >= 10 and(game.Players.LocalPlayer.Character.HumanoidRootPart.Position-p.Position).Magnitude < 20 then 
							game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = p
						elseif (game.Players.LocalPlayer.Character.HumanoidRootPart.Position-p.Position).Magnitude < 10 then 
							game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = p
						end
					end)
				end
			end)
		end)
	end
	
	function topos(Pos)
        Distance = (Pos.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
        if Distance < 250 then
            Speed = 600
        elseif Distance < 500 then
            Speed = 300
        elseif Distance < 750 then
            Speed = 250
        elseif Distance >= 1000 then
            Speed = 200
        end
        game:GetService("TweenService"):Create(
            game:GetService("Players").LocalPlayer.Character.HumanoidRootPart,
            TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = Pos}
        ):Play()
end
    
    spawn(function()
    game:GetService("RunService").RenderStepped:Connect(function()
        if _G.AutoClick or Fastattack then
             pcall(function()
                game:GetService'VirtualUser':CaptureController()
			    game:GetService'VirtualUser':Button1Down(Vector2.new(0,1,0,1))
            end)
        end
    end)
   end)

   function StopTween(target)
        if not target then
            _G.StopTween = true
            wait()
            topos(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
            wait()
            if game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip") then
                game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip"):Destroy()
            end
            _G.StopTween = false
            _G.Clip = false
        end
    end
    
    spawn(function()
        pcall(function()
            while wait() do
                for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren()) do  
                    if v:IsA("Tool") then
                        if v:FindFirstChild("RemoteFunctionShoot") then 
                            SelectWeaponGun = v.Name
                        end
                    end
                end
            end
        end)
    end)
    
    game:GetService("Players").LocalPlayer.Idled:connect(function()
        game:GetService("VirtualUser"):Button2Down(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
        wait(1)
        game:GetService("VirtualUser"):Button2Up(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
    end)

page1:Dropdown("เลือก อาวุธ",{"Melee","Sword","Gun","Fruit"},"Melee",function(a)
    print(a)
end)

page1:Toggle('ออโต้ ไก่ตัน',nil,function(value)
_G.Auto_Farm_Level = value
_G.Start_Kaitn = value
end)

spawn(function()
	while wait() do
		pcall(function()
			if _G.Start_Kaitan then
				if World1 then
					local args = {
						[1] = "AddPoint",
						[2] = "Melee",
						[3] = _G.Point
						}
						
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
				elseif World2 then
					local args = {
						[1] = "AddPoint",
						[2] = "Melee",
						[3] = _G.Point
						}
						
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
					local args = {
						[1] = "AddPoint",
						[2] = "Defense",
						[3] = _G.Point
						}
						
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
				end
			end
		end)
	end
end) 

spawn(function()                     
    while wait(.1) do    
        if _G.Start_Kaitan then                                            
            for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren()) do                            
                if v.ToolTip == "Melee" then                           
                    if game.Players.LocalPlayer.Backpack:FindFirstChild(tostring(v.Name)) then                               
                        local ToolSe = tostring(v.Name)                              
                    local tool = game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe)                              
                    wait()                              
                    game.Players.LocalPlayer.Character.Humanoid:EquipTool(tool)                                   
                    end                               
                    end    
                    end                       
                    end                                          
                    end                 
                    end)

page1:Button('Fast Attack',function()
    local plr = game.Players.LocalPlayer local CbFw = debug.getupvalues(require(plr.PlayerScripts.CombatFramework))local CbFw2 = CbFw[2]function GetCurrentBlade()local p13 = CbFw2.activeController local ret = p13.blades[1] if not ret then return end while ret.Parent~=game.Players.LocalPlayer.Character do ret=ret.Parent end return ret end function AttackNoCD() local AC = CbFw2.activeController for i = 1, 1 do  local bladehit = require(game.ReplicatedStorage.CombatFramework.RigLib).getBladeHits( plr.Character, {plr.Character.HumanoidRootPart}, 60 )local cac = {}local hash = {}for k, v in pairs(bladehit) do if v.Parent:FindFirstChild("HumanoidRootPart") and not hash[v.Parent] then table.insert(cac, v.Parent.HumanoidRootPart)hash[v.Parent] = true end end bladehit = cac if #bladehit > 0 then local u8 = debug.getupvalue(AC.attack, 5)local u9 = debug.getupvalue(AC.attack, 6)local u7 = debug.getupvalue(AC.attack, 4)local u10 = debug.getupvalue(AC.attack, 7)local u12 = (u8 * 798405 + u7 * 727595) % u9 local u13 = u7 * 798405 (function()u12 = (u12 * u9 + u13) % 1099511627776 u8 = math.floor(u12 / u9)u7 = u12 - u8 * u9 end)()u10 = u10 + 1 debug.setupvalue(AC.attack, 5, u8)debug.setupvalue(AC.attack, 6, u9)debug.setupvalue(AC.attack, 4, u7)debug.setupvalue(AC.attack, 7, u10)pcall(function()for k, v in pairs(AC.animator.anims.basic) do v:Play()end end)if plr.Character:FindFirstChildOfClass("Tool") and AC.blades and AC.blades[1] then game:GetService("ReplicatedStorage").RigControllerEvent:FireServer("weaponChange",tostring(GetCurrentBlade()))game.ReplicatedStorage.Remotes.Validator:FireServer(math.floor(u12 / 1099511627776 * 16777215), u10)game:GetService("ReplicatedStorage").RigControllerEvent:FireServer("hit", bladehit, i, "")end end end end require(game.ReplicatedStorage.Util.CameraShaker):Stop()task.spawn(function()while task.wait() do pcall(function()if getgenv().LevelFarm then if getgenv().LevelFarm then AttackNoCD()end end end)end end) local CameraShaker = require(game.ReplicatedStorage.Util.CameraShaker)CombatFrameworkR = require(game:GetService("Players").LocalPlayer.PlayerScripts.CombatFramework)y = debug.getupvalues(CombatFrameworkR)[2]spawn(function()game:GetService("RunService").RenderStepped:Connect(function()if getgenv().LevelFarm then if typeof(y) == "table" then pcall(function()CameraShaker:Stop()y.activeController.timeToNextAttack = -10 y.activeController.timeToNextAttack = 0 y.activeController.hitboxMagnitude = 100 y.activeController.active = false y.activeController.timeToNextBlock = 0 y.activeController.focusStart = 0 y.activeController.increment = 0 y.activeController.blocking = false y.activeController.attacking = false y.activeController.humanoid.AutoRotate = true end)end end end)end)spawn(function()game:GetService("RunService").RenderStepped:Connect(function()if getgenv().LevelFarm == true then game.Players.LocalPlayer.Character.Stun.Value = 0 game.Players.LocalPlayer.Character.Humanoid.Sit = false game.Players.LocalPlayer.Character.Busy.Value = false end end)end)
end)

_G.SuperFastAttack = true


spawn(function()
        while wait() do
            if _G.SuperFastAttack then
                pcall(function()
                    wait(1)
                    loadstring(game:HttpGet("https://raw.githubusercontent.com/trumpxl/name/main/superfastattack"))()
                    wait(0.5)
                    loadstring(game:HttpGet("https://raw.githubusercontent.com/trumpxl/name/main/superfastattack"))()
                    wait(0.5)
                    loadstring(game:HttpGet("https://raw.githubusercontent.com/trumpxl/name/main/superfastattack"))()
                    wait(0.5)
                    loadstring(game:HttpGet("https://raw.githubusercontent.com/trumpxl/name/main/superfastattack"))()
                    wait(0.5)
                    loadstring(game:HttpGet("https://raw.githubusercontent.com/trumpxl/name/main/superfastattack"))()
                end)
            end
        end
    end)
    
    spawn(function()
        while wait() do
            if _G.SuperFastAttack then
                pcall(function()
                    wait(1)
                    coroutine.wrap(function()local StopCamera = require(game.ReplicatedStorage.Util.CameraShaker)StopCamera:Stop()for v,v in pairs(getreg()) doif typeof(v) == "function" and getfenv(v).script == game:GetService("Players").LocalPlayer.PlayerScripts.CombatFramework thenfor v,v in pairs(debug.getupvalues(v)) doif typeof(v) == "table" thenspawn(function()game:GetService("RunService").RenderStepped:Connect(function()if getgenv().ConfigSuperFastAttack thenpcall(function()v.activeController.timeToNextAttack = -(math.huge^math.huge^math.huge)v.activeController.attacking = falsev.activeController.increment = 4                  v.activeController.blocking = falsev.activeController.hitboxMagnitude = 150v.activeController.humanoid.AutoRotate = truev.activeController.focusStart = 0v.activeController.currentAttackTrack = 0sethiddenproperty(game:GetService("Players").LocalPlayer, "SimulationRaxNerous", math.huge)end)endend)end)endendendendend)();spawn(function()game:GetService("RunService").RenderStepped:Connect(function()if getgenv().ConfigSuperFastAttack thenpcall(function()game:GetService'VirtualUser':CaptureControllergame:GetService'VirtualUser':Button1Down(Vector2.new(0,1,0,1))end)endend)end)
                    wait(0.5)
                    coroutine.wrap(function()local StopCamera = require(game.ReplicatedStorage.Util.CameraShaker)StopCamera:Stop()for v,v in pairs(getreg()) doif typeof(v) == "function" and getfenv(v).script == game:GetService("Players").LocalPlayer.PlayerScripts.CombatFramework thenfor v,v in pairs(debug.getupvalues(v)) doif typeof(v) == "table" thenspawn(function()game:GetService("RunService").RenderStepped:Connect(function()if getgenv().ConfigSuperFastAttack thenpcall(function()v.activeController.timeToNextAttack = -(math.huge^math.huge^math.huge)v.activeController.attacking = falsev.activeController.increment = 4                  v.activeController.blocking = falsev.activeController.hitboxMagnitude = 150v.activeController.humanoid.AutoRotate = truev.activeController.focusStart = 0v.activeController.currentAttackTrack = 0sethiddenproperty(game:GetService("Players").LocalPlayer, "SimulationRaxNerous", math.huge)end)endend)end)endendendendend)();spawn(function()game:GetService("RunService").RenderStepped:Connect(function()if getgenv().ConfigSuperFastAttack thenpcall(function()game:GetService'VirtualUser':CaptureControllergame:GetService'VirtualUser':Button1Down(Vector2.new(0,1,0,1))end)endend)end)
                    wait(0.5)
                    coroutine.wrap(function()local StopCamera = require(game.ReplicatedStorage.Util.CameraShaker)StopCamera:Stop()for v,v in pairs(getreg()) doif typeof(v) == "function" and getfenv(v).script == game:GetService("Players").LocalPlayer.PlayerScripts.CombatFramework thenfor v,v in pairs(debug.getupvalues(v)) doif typeof(v) == "table" thenspawn(function()game:GetService("RunService").RenderStepped:Connect(function()if getgenv().ConfigSuperFastAttack thenpcall(function()v.activeController.timeToNextAttack = -(math.huge^math.huge^math.huge)v.activeController.attacking = falsev.activeController.increment = 4                  v.activeController.blocking = falsev.activeController.hitboxMagnitude = 150v.activeController.humanoid.AutoRotate = truev.activeController.focusStart = 0v.activeController.currentAttackTrack = 0sethiddenproperty(game:GetService("Players").LocalPlayer, "SimulationRaxNerous", math.huge)end)endend)end)endendendendend)();spawn(function()game:GetService("RunService").RenderStepped:Connect(function()if getgenv().ConfigSuperFastAttack thenpcall(function()game:GetService'VirtualUser':CaptureControllergame:GetService'VirtualUser':Button1Down(Vector2.new(0,1,0,1))end)endend)end)
                    wait(0.5)
                    coroutine.wrap(function()local StopCamera = require(game.ReplicatedStorage.Util.CameraShaker)StopCamera:Stop()for v,v in pairs(getreg()) doif typeof(v) == "function" and getfenv(v).script == game:GetService("Players").LocalPlayer.PlayerScripts.CombatFramework thenfor v,v in pairs(debug.getupvalues(v)) doif typeof(v) == "table" thenspawn(function()game:GetService("RunService").RenderStepped:Connect(function()if getgenv().ConfigSuperFastAttack thenpcall(function()v.activeController.timeToNextAttack = -(math.huge^math.huge^math.huge)v.activeController.attacking = falsev.activeController.increment = 4                  v.activeController.blocking = falsev.activeController.hitboxMagnitude = 150v.activeController.humanoid.AutoRotate = truev.activeController.focusStart = 0v.activeController.currentAttackTrack = 0sethiddenproperty(game:GetService("Players").LocalPlayer, "SimulationRaxNerous", math.huge)end)endend)end)endendendendend)();spawn(function()game:GetService("RunService").RenderStepped:Connect(function()if getgenv().ConfigSuperFastAttack thenpcall(function()game:GetService'VirtualUser':CaptureControllergame:GetService'VirtualUser':Button1Down(Vector2.new(0,1,0,1))end)endend)end)
                end)
            end
        end
    end)

local plr = game.Players.LocalPlayer

local CbFw = debug.getupvalues(require(plr.PlayerScripts.CombatFramework))
local CbFw2 = CbFw[2]

function GetCurrentBlade() 
    local p13 = CbFw2.activeController
    local ret = p13.blades[1]
    if not ret then return end
    while ret.Parent~=game.Players.LocalPlayer.Character do ret=ret.Parent end
    return ret
end
function AttackNoCD() 
    local AC = CbFw2.activeController
    for i = 1, 1 do 
        local bladehit = require(game.ReplicatedStorage.CombatFramework.RigLib).getBladeHits(
            plr.Character,
            {plr.Character.HumanoidRootPart},
            60
        )
        local cac = {}
        local hash = {}
        for k, v in pairs(bladehit) do
            if v.Parent:FindFirstChild("HumanoidRootPart") and not hash[v.Parent] then
                table.insert(cac, v.Parent.HumanoidRootPart)
                hash[v.Parent] = true
            end
        end
        bladehit = cac
        if #bladehit > 0 then
            local u8 = debug.getupvalue(AC.attack, 5)
            local u9 = debug.getupvalue(AC.attack, 6)
            local u7 = debug.getupvalue(AC.attack, 4)
            local u10 = debug.getupvalue(AC.attack, 7)
            local u12 = (u8 * 798405 + u7 * 727595) % u9
            local u13 = u7 * 798405
            (function()
                u12 = (u12 * u9 + u13) % 1099511627776
                u8 = math.floor(u12 / u9)
                u7 = u12 - u8 * u9
            end)()
            u10 = u10 + 1
            debug.setupvalue(AC.attack, 5, u8)
            debug.setupvalue(AC.attack, 6, u9)
            debug.setupvalue(AC.attack, 4, u7)
            debug.setupvalue(AC.attack, 7, u10)
            pcall(function()
                for k, v in pairs(AC.animator.anims.basic) do
                    v:Play()
                end                  
            end)
            if plr.Character:FindFirstChildOfClass("Tool") and AC.blades and AC.blades[1] then 
                game:GetService("ReplicatedStorage").RigControllerEvent:FireServer("weaponChange",tostring(GetCurrentBlade()))
                game.ReplicatedStorage.Remotes.Validator:FireServer(math.floor(u12 / 1099511627776 * 16777215), u10)
                game:GetService("ReplicatedStorage").RigControllerEvent:FireServer("hit", bladehit, i, "") 
            end
        end
    end
end
local cac
if _G.SuperFastAttack then 
	cac=task.wait
else
	cac=wait
end
while cac() do 
	AttackNoCD()
end


coroutine.wrap(function()
local StopCamera = require(game.ReplicatedStorage.Util.CameraShaker)StopCamera:Stop()
    for v,v in pairs(getreg()) do
        if typeof(v) == "function" and getfenv(v).script == game:GetService("Players").LocalPlayer.PlayerScripts.CombatFramework then
             for v,v in pairs(debug.getupvalues(v)) do
                if typeof(v) == "table" then
                    spawn(function()
                        game:GetService("RunService").RenderStepped:Connect(function()
                            if getgenv().ConfigSuperFastAttack then
                                 pcall(function()
                                     v.activeController.timeToNextAttack = -(math.huge^math.huge^math.huge)
                                     v.activeController.attacking = false
                                     v.activeController.increment = 4
                                     v.activeController.blocking = false   
                                     v.activeController.hitboxMagnitude = 150
    		                         v.activeController.humanoid.AutoRotate = true
    	                      	     v.activeController.focusStart = 0
    	                      	     v.activeController.currentAttackTrack = 0
                                     sethiddenproperty(game:GetService("Players").LocalPlayer, "SimulationRaxNerous", math.huge)
                                 end)
                             end
                         end)
                    end)
                end
            end
        end
    end
end)();

spawn(function()
    game:GetService("RunService").RenderStepped:Connect(function()
        if getgenv().ConfigSuperFastAttack then
             pcall(function()
                game:GetService'VirtualUser':CaptureController()
			    game:GetService'VirtualUser':Button1Down(Vector2.new(0,1,0,1))
            end)
        end
    end)
end)

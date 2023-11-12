local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()
local Window = OrionLib:MakeWindow({Name = "Get Key", HidePremium = false, SaveConfig = true, ConfigFolder = "OrionTest"})


getgenv().Key = "Key-Xonic-Hub-Three-Days"
getgenv().Keyinput = "string"
function Checkkey() 
if Key == Keyinput then
game.StarterGui:SetCore("SendNotification", {
      Icon = "http://www.roblox.com/asset/?id=7743878857";
      Title = "Xonic Hub", 
      Text = "Welcome To Script!!"
  })

game.StarterGui:SetCore("SendNotification", {
      Icon = "http://www.roblox.com/asset/?id=7743878857";
      Title = "Xonic Hub", 
      Text = "กดติดตามช่องยูทูปกูนำ สาสส"
  })

game.StarterGui:SetCore("SendNotification", {
      Icon = "http://www.roblox.com/asset/?id=7743878857";
      Title = "Xonic Hub", 
      Text = "Open Highlight"
  })

_G.AutoHighlight = true

spawn(function()
        while wait() do
            if _G.AutoHighlight then
                pcall(function()
                    wait(1)
                    local players = game.Players:GetPlayers()

                    for i,v in pairs(players) do
                    local esp = Instance.new("Highlight")
                    esp.Name = v.Name
                    esp.FillTransparency = 0.4
                    esp.FillColor = Color3.new(0, 255, 0)
                    esp.OutlineColor = Color3.new(1, 0.333333, 1)
                    esp.OutlineTransparency = 0
                    esp.Parent = v.Character
                    end
                    game.Players.LocalPlayer.Character.Highlight:Destroy()
                    wait(0.5)
                    local players = game.Players:GetPlayers()

                    for i,v in pairs(players) do
                    local esp = Instance.new("Highlight")
                    esp.Name = v.Name
                    esp.FillTransparency = 0.4
                    esp.FillColor = Color3.new(0, 255, 0)
                    esp.OutlineColor = Color3.new(1, 0.333333, 1)
                    esp.OutlineTransparency = 0
                    esp.Parent = v.Character
                    end
                    game.Players.LocalPlayer.Character.Highlight:Destroy()
                end)
            end
        end
    end)
    

_G.Color = Color3.fromRGB(3, 174, 255)
_G.Logo = 7743878857


local Evil = loadstring(game:HttpGet("https://newpchx2.0xlii.repl.co/AllUI/Protected_9405524596134885.lua"))()
local Win = library:Evil("Xonic","Hub",_G.Logo )

local tab1 = Win:CraftTab('Main')
local page1 = tab1:CraftPage('Main',1)

local player = page1:Label('สคลิปรับยศ')

page1:Button('( คลิก ) เพื่อสุ่มยศ',function()
setclipboard("https://pastebin.com/raw/GeJafRGh")
end

page1:Button('( คลิก ) เพื่อสุ่มยศ',function()
setclipboard("https://pastebin.com/raw/z89qSWQy")
end

page1:Button('( คลิก ) เพื่อสุ่มยศ',function()
setclipboard("https://pastebin.com/raw/sPn0zRbr")
end

end
end


local Tab = Window:MakeTab({
	Name = "Key",
	Icon = "rbxassetid://7743878857",
	PremiumOnly = false
})



Tab:AddTextbox({
	Name = "Key",
	Default = "",
	TextDisappear = true,
	Callback = function(Value)
		Keyinput = Value
	end	  
})

Tab:AddButton({
	Name = "Check",
	Callback = function()
      		Checkkey()
  	end    
})

Tab:AddButton({
	Name = "Link Get Key",
	Callback = function()
      	setclipboard("https://discord.com/channels/1172886637496254464/1172886638116999240")
  	end    
})

OrionLib:Init()

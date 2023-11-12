local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()
local Window = OrionLib:MakeWindow({Name = "Get Key", HidePremium = false, SaveConfig = true, ConfigFolder = "OrionTest"})


getgenv().Key = "Key-Xonic-Hub-Three-Days"
getgenv().Keyinput = "string"
function Checkkey() 
if Key == Keyinput then
loadstring(game:HttpGet("https://pastebin.com/raw/PvmW3HEB"))();

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

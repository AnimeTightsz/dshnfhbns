if game.PlaceId == 417267366 then
    local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
    local Window = Library.CreateLib("ROLEX HUB         not finished check back later,   XumLum#4289", "BloodTheme")
 
    -- MAIN
    local Main = Window:NewTab("Main")
    local MainSection = Main:NewSection("Main")
 
    MainSection:NewDropdown("Dupe", "Duplicates the amount of radios you have chosen.", {"Dupe 5", "Dupe 15", "Dupe 25"}, function(v)
        local A_1 = game:GetService("Workspace")["Test"].giver[v].ITEMPICKUP
        local Event = game:GetService("Workspace").Remote.ItemHandler
        Event:InvokeServer(A_1)
    end)
 
    MainSection:NewDropdown("Useful (ONE AT A TIME)", "Main", {"Mute All (Client Sided)", "Sync", "Anti Log"}, function(v)
     local A_1 = game:GetService("Workspace")["MainSection"].giver[v].ITEMPICKUP
        local Event = game:GetService("Workspace").Remote.ItemHandler
        Event:InvokeServer(A_1)
    end)
	
	--VISUALIZER
	local Main = Window:NewTab("Visualizer")
	 -- PLAYER
    local Player = Window:NewTab("Player")
    local PlayerSection = Player:NewSection("Player")
 
    PlayerSection:NewSlider("Walkspeed", "Changes the walkspeed", 250, 16, function(v)
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = v
    end)
 
    PlayerSection:NewSlider("Jumppower", "Changes the jumppower", 250, 50, function(v)
        game.Players.LocalPlayer.Character.Humanoid.JumpPower = v
	end)
end

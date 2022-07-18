local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("Z!#7147", "DarkTheme")
Section:NewKeybind("KeybindText", "KeybindInfo", Enum.KeyCode.G, function()
	Library:ToggleUI()
end)
local Tab = Window:NewTab("Mainj")
local Section = Tab:NewSection("Spam")
Section:NewToggle("Spam", "Click to use Spam", function(state)
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
local Section = Tab:NewSection("Equip")
Section:NewToggle("Equip", "Click to use Equip", function(state)
_G.Equip = state
spawn(function()
        while _G.Equip do wait()
            pcall(function()
            Weapon = Light     
            game.Players.LocalPlayer.Character.Humanoid:EquipTool(game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(Weapon))
        end)
end
end)
end)
local Section = Tab:NewSection("Quest")
Section:NewToggle("Quest", "Click to use Quest", function(state)
_G.Quest = state
spawn(function()
while _G.Quest do wait()
game:GetService("Players").LocalPlayer.PlayerGui.QuestTake.Accept1.RemoteEvent:FireServer()
end
end)
end)
local Section = Tab:NewSection("Anti")
Section:NewToggle("Anti", "Click to use Anti", function(state)
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
local Section = Tab:NewSection("Anti")
Section:NewToggle("Stats", "Click to use Stats", function(state)
_G.Stats = state
spawn(function()
while _G.Stats do wait()
local GG = {
    [1] = "DevilFruit"
    }
game:GetService("ReplicatedStorage").StatSystem.Points:FireServer(unpack(GG))
end
end)
end)

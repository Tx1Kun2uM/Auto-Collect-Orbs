local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("TITLE", "Ocean")
local Tab = Window:NewTab("Auto Collect Orbs")
local Section = Tab:NewSection("Collect Orbs")
Section:NewToggle("Auto Farm Orbs", "ToggleInfo", function(state)
    if state then
        print("Toggle On")
    else
        print("Toggle Off")
    end
    _G.loop = true;
while _G.loop do wait()

for i,v in pairs(game:GetService("Workspace").OrbSpawns:GetDescendants()) do
    if v.Name == "TouchInterest" then
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Parent.CFrame
wait(.1)
end
end
end
end)

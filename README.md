game:GetService("RunService").Stepped:connect(function()
        game:GetService("Workspace").FallenPartsDestroyHeight = 0 / 0
        sethiddenproperty(game:GetService("Players").LocalPlayer, "SimulationRadius", 2400)
    end
)


game:GetService("RunService").Stepped:connect(function()
    for i,v in pairs(game:GetService("Workspace").Mob:GetChildren()) do
        local H = v:FindFirstChildWhichIsA("Humanoid")
        if H and H.Health < H.MaxHealth then
            H.Health = 0 
        end 
    end 
end)

if game.PlaceId == 15502339080 then
    repeat wait() until game:IsLoaded()
    local booth_func
    for i, v in getgc() do
        if type(v) == "function" and islclosure(v) and not isourclosure(v) then
            local script = tostring(getfenv(v).script)
            if script == "Booths Frontend" then
                local name = debug.info(v, "n")
                if name == "getByOwnerId" then
                    booth_func = v
                end
            end
        end
    end
    local plr = game.Players.LocalPlayer
    local ListingCounter = Instance.new("ScreenGui")
    local ItemCount = Instance.new("Frame")
    local UICorner = Instance.new("UICorner")
    local value = Instance.new("TextLabel")
    ListingCounter.Name = "ListingCounter"
    ListingCounter.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
    ListingCounter.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
    ItemCount.Name = "ItemCount"
    ItemCount.Parent = ListingCounter
    ItemCount.BackgroundColor3 = Color3.fromRGB(49, 183, 255)
    ItemCount.BorderColor3 = Color3.fromRGB(0, 0, 0)
    ItemCount.BorderSizePixel = 0
    ItemCount.AnchorPoint = Vector2.new(0.5, 0.5)
    ItemCount.Position = UDim2.new(0.5, 0, 0.1, 0)
    ItemCount.Size = UDim2.new(0, 100, 0, 100)
    UICorner.CornerRadius = UDim.new(0.150000006, 0)
    UICorner.Parent = ItemCount
    value.Name = "value"
    value.Parent = ItemCount
    value.BackgroundColor3 = Color3.fromRGB(49, 183, 255)
    value.BorderColor3 = Color3.fromRGB(0, 0, 0)
    value.BorderSizePixel = 0
    value.Position = UDim2.new(0, 0, 0.150000006, 0)
    value.Size = UDim2.new(0, 100, 0, 69)
    value.Font = Enum.Font.SourceSansBold
    value.Text = "0"
    value.TextColor3 = Color3.fromRGB(0, 0, 0)
    value.TextSize = 100.000
    while task.wait(1) do
        booth = booth_func(plr.UserId)
        if booth ~= nil then
            local count = 0
            for i,v in pairs(booth.Listings) do
                count = count+1
            end
            if value.Text ~= tostring(count) then
                value.Text = tostring(count)
            end
        end
    end
end

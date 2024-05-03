local Hahaha = Instance.new("ScreenGui")
local Main = Instance.new("Frame")
local UICorner = Instance.new("UICorner")
local TextLabel = Instance.new("TextLabel")
local ImageLabel = Instance.new("ImageLabel")

Hahaha.Name = "Hahaha"
Hahaha.Parent = game.CoreGui
Hahaha.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

Main.Name = "Main"
Main.Parent = Hahaha
Main.BackgroundColor3 = Color3.fromRGB(27, 27, 27)
Main.BorderColor3 = Color3.fromRGB(0, 0, 0)
Main.BorderSizePixel = 0
Main.Position = UDim2.new(0.200861484, 0, -0.281337082, 0)
Main.Size = UDim2.new(0.569999993, 0, 0.300000012, 0)

UICorner.CornerRadius = UDim.new(1.20000005, 0)
UICorner.Parent = Main

TextLabel.Parent = Main
TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.BackgroundTransparency = 1.000
TextLabel.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextLabel.BorderSizePixel = 0
TextLabel.Position = UDim2.new(0.224490941, 0, 0.5090909, 0)
TextLabel.Size = UDim2.new(0.549286425, 0, 0.436363637, 0)
TextLabel.Font = Enum.Font.SourceSans
TextLabel.Text = "Attack Hub"
TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.TextScaled = true
TextLabel.TextSize = 14.000
TextLabel.TextWrapped = true

ImageLabel.Parent = Main
ImageLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
ImageLabel.BackgroundTransparency = 1.000
ImageLabel.BorderColor3 = Color3.fromRGB(0, 0, 0)
ImageLabel.BorderSizePixel = 0
ImageLabel.Position = UDim2.new(0.0740342587, 0, 0.454545468, 0)
ImageLabel.Size = UDim2.new(0.148068517, 0, 0.4909091, 0)
ImageLabel.Image = "http://www.roblox.com/asset/?id=16663324629"

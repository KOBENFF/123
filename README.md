local ScreenGui = Instance.new("ScreenGui")
local Main = Instance.new("Frame")
local UICorner = Instance.new("UICorner")
local Page = Instance.new("ScrollingFrame")
local ProfileImage = Instance.new("ImageLabel")
local UICorner_2 = Instance.new("UICorner")
local GetName = Instance.new("TextLabel")
local TOHUB = Instance.new("TextLabel")
local NameHub = Instance.new("TextLabel")
local Logo = Instance.new("ImageLabel")
local UICorner_3 = Instance.new("UICorner")
local TabMain = Instance.new("TextLabel")
local MainLogoImage = Instance.new("ImageLabel")
local UserInputService = game:GetService("UserInputService")
local TweenService = game:GetService("TweenService")
local RunService = game:GetService("RunService")
local LocalPlayer = game:GetService("Players").LocalPlayer
local Mouse = LocalPlayer:GetMouse()
function dragify(Frame, object)
	dragToggle = nil
	dragSpeed = .25
	dragInput = nil
	dragStart = nil
	dragPos = nil
	function updateInput(input)
		Delta = input.Position - dragStart
		Position =
			UDim2.new(startPos.X.Scale, startPos.X.Offset + Delta.X, startPos.Y.Scale, startPos.Y.Offset + Delta.Y)
		game:GetService("TweenService"):Create(object, TweenInfo.new(dragSpeed), {Position = Position}):Play()
	end
	Frame.InputBegan:Connect(
		function(input)
			if
				(input.UserInputType == Enum.UserInputType.MouseButton1 or
					input.UserInputType == Enum.UserInputType.Touch)
			then
				dragToggle = true
				dragStart = input.Position
				startPos = object.Position
				input.Changed:Connect(
					function()
						if (input.UserInputState == Enum.UserInputState.End) then
							dragToggle = false
						end
					end
				)
			end
		end
	)
	Frame.InputChanged:Connect(
		function(input)
			if
				(input.UserInputType == Enum.UserInputType.MouseMovement or
					input.UserInputType == Enum.UserInputType.Touch)
			then
				dragInput = input
			end
		end
	)
	game:GetService("UserInputService").InputChanged:Connect(
	function(input)
		if (input == dragInput and dragToggle) then
			updateInput(input)
		end
	end
	)
end
ScreenGui.Parent = game.CoreGui
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
dragify(Main, Main)
Main.Name = "Main"
Main.Parent = ScreenGui
Main.BackgroundColor3 = Color3.fromRGB(0, 98, 98)
Main.BackgroundTransparency = 0.400
Main.BorderColor3 = Color3.fromRGB(0, 0, 0)
Main.BorderSizePixel = 0
Main.Position = UDim2.new(0.15646258, 0, 0.0473537594, 0)
Main.Size = UDim2.new(0.693877578, 0, 0.802228391, 0)

UICorner.CornerRadius = UDim.new(0, 5)
UICorner.Parent = Main

Page.Name = "Page"
Page.Parent = Main
Page.Active = true
Page.BackgroundColor3 = Color3.fromRGB(0, 98, 98)
Page.BackgroundTransparency = 0.400
Page.BorderColor3 = Color3.fromRGB(0, 0, 0)
Page.BorderSizePixel = 0
Page.Position = UDim2.new(0.149915561, 0, 0.134100303, 0)
Page.Size = UDim2.new(0.838359654, 0, 0.843279064, 0)

ProfileImage.Name = "ProfileImage"
ProfileImage.Parent = Page
ProfileImage.BackgroundColor3 = Color3.fromRGB(176, 0, 3)
ProfileImage.BorderColor3 = Color3.fromRGB(0, 0, 0)
ProfileImage.BorderSizePixel = 0
ProfileImage.Position = UDim2.new(0.0220082998, 0, 0.0279005077, 0)
ProfileImage.Size = UDim2.new(0.217077374, 0, 0.162029222, 0)
ProfileImage.Image = "https://www.roblox.com/headshot-thumbnail/image?userId=" .. game.Players.LocalPlayer.UserId .. "&width=420&height=420&format=png"

UICorner_2.CornerRadius = UDim.new(0, 100)
UICorner_2.Parent = ProfileImage

GetName.Name = "GetName"
GetName.Parent = Page
GetName.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
GetName.BackgroundTransparency = 1.000
GetName.BorderColor3 = Color3.fromRGB(0, 0, 0)
GetName.BorderSizePixel = 0
GetName.Position = UDim2.new(0.23786138, 0, 0.02365789, 0)
GetName.Size = UDim2.new(0.387968063, 0, 0.0735918805, 0)
GetName.Font = Enum.Font.SourceSans
GetName.Text = ""..game.Players.LocalPlayer.Name
GetName.TextColor3 = Color3.fromRGB(255, 255, 255)
GetName.TextSize = 30.000
GetName.TextWrapped = true

TOHUB.Name = "TOHUB"
TOHUB.Parent = Page
TOHUB.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TOHUB.BackgroundTransparency = 1.000
TOHUB.BorderColor3 = Color3.fromRGB(0, 0, 0)
TOHUB.BorderSizePixel = 0
TOHUB.Position = UDim2.new(0.254026711, 0, 0.105275728, 0)
TOHUB.Size = UDim2.new(0.456084102, 0, 0.0470439494, 0)
TOHUB.Font = Enum.Font.SourceSans
TOHUB.Text = "Welcome To Xcellent Hub"
TOHUB.TextColor3 = Color3.fromRGB(255, 255, 255)
TOHUB.TextSize = 20.000
TOHUB.TextWrapped = true

NameHub.Name = "NameHub"
NameHub.Parent = Main
NameHub.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
NameHub.BackgroundTransparency = 1.000
NameHub.BorderColor3 = Color3.fromRGB(0, 0, 0)
NameHub.BorderSizePixel = 0
NameHub.Position = UDim2.new(0.149915516, 0, 0.0239112675, 0)
NameHub.Size = UDim2.new(0.248644948, 0, 0.0900352225, 0)
NameHub.Font = Enum.Font.SourceSans
NameHub.Text = "Xcellent Hub Kaitun"
NameHub.TextColor3 = Color3.fromRGB(255, 255, 255)
NameHub.TextScaled = true
NameHub.TextSize = 14.000
NameHub.TextWrapped = true
NameHub.TextXAlignment = Enum.TextXAlignment.Right

Logo.Name = "Logo"
Logo.Parent = Main
Logo.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Logo.BorderColor3 = Color3.fromRGB(0, 0, 0)
Logo.BorderSizePixel = 0
Logo.Position = UDim2.new(0.0474416092, 0, 0.0204954036, 0)
Logo.Size = UDim2.new(0.0800610259, 0, 0.137516171, 0)
Logo.Image = "rbxassetid://18592300110"

UICorner_3.CornerRadius = UDim.new(0, 100)
UICorner_3.Parent = Logo

TabMain.Name = "TabMain"
TabMain.Parent = Main
TabMain.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TabMain.BackgroundTransparency = 1.000
TabMain.BorderColor3 = Color3.fromRGB(0, 0, 0)
TabMain.BorderSizePixel = 0
TabMain.Position = UDim2.new(0.0360556245, 0, 0.208369672, 0)
TabMain.Size = UDim2.new(0.113859862, 0, 0.109308682, 0)
TabMain.Font = Enum.Font.Arial
TabMain.Text = "Main"
TabMain.TextColor3 = Color3.fromRGB(255, 255, 255)
TabMain.TextSize = 16.000
TabMain.TextWrapped = true

MainLogoImage.Name = "MainLogoImage"
MainLogoImage.Parent = TabMain
MainLogoImage.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
MainLogoImage.BackgroundTransparency = 1.000
MainLogoImage.BorderColor3 = Color3.fromRGB(0, 0, 0)
MainLogoImage.BorderSizePixel = 0
MainLogoImage.Position = UDim2.new(-0.316666663, 0, 0, 0)
MainLogoImage.Size = UDim2.new(0.630313098, 0, 0.854865551, 0)
MainLogoImage.Image = "rbxassetid://7040391851"

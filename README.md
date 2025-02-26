## Get Stuff
```lua
local lib = {}

function lib:CreateWindow(title)
	local UI = Instance.new("ScreenGui")
	local Main = Instance.new("Frame")
	local UICorner = Instance.new("UICorner")
	local TopBar = Instance.new("Frame")
	local Icon = Instance.new("ImageLabel")
	local Title = Instance.new("TextLabel")
	local Line_2 = Instance.new("Frame")
	local ExitButton = Instance.new("ImageButton")
	local UIAspectRatioConstraint = Instance.new("UIAspectRatioConstraint")
	local Line = Instance.new("Frame")
	local Navigation = Instance.new("ScrollingFrame")
	local UIListLayout = Instance.new("UIListLayout")
	local UIPadding = Instance.new("UIPadding")
	local Content = Instance.new("Frame")
	local MobileCards = Instance.new("ImageButton")
	local UICorner_18 = Instance.new("UICorner")
	
	UI.Name = "UI"
	UI.Parent = game:GetService("Players").LocalPlayer.PlayerGui or game:GetService("CoreGui")
	UI.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
	UI.DisplayOrder = 999999999
	UI.ResetOnSpawn = false

	Main.Name = "Main"
	Main.Parent = UI
	Main.BackgroundColor3 = Color3.fromRGB(3, 3, 3)
	Main.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Main.BorderSizePixel = 0
	Main.Position = UDim2.new(0, 283, 0, 152)
	Main.Size = UDim2.new(0, 542, 0, 321)

	UICorner.Parent = Main

	TopBar.Name = "TopBar"
	TopBar.Parent = Main
	TopBar.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	TopBar.BackgroundTransparency = 1.000
	TopBar.BorderColor3 = Color3.fromRGB(0, 0, 0)
	TopBar.BorderSizePixel = 0
	TopBar.Size = UDim2.new(0, 542, 0, 52)

	Icon.Name = "Icon"
	Icon.Parent = TopBar
	Icon.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Icon.BackgroundTransparency = 1.000
	Icon.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Icon.BorderSizePixel = 0
	Icon.Position = UDim2.new(0.0129151288, 0, 0.134076342, 0)
	Icon.Size = UDim2.new(0, 52, 0, 37)
	Icon.Image = "rbxassetid://70944899239586"
	Icon.ImageColor3 = Color3.fromRGB(83, 113, 241)

	Title.Name = "Title"
	Title.Parent = TopBar
	Title.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Title.BackgroundTransparency = 1.000
	Title.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Title.BorderSizePixel = 0
	Title.Position = UDim2.new(0.108856089, 0, 0.115384616, 0)
	Title.Size = UDim2.new(0, 200, 0, 38)
	Title.Font = Enum.Font.GothamBold
	Title.Text = title
	Title.TextColor3 = Color3.fromRGB(255, 255, 255)
	Title.TextSize = 26.000
	Title.TextXAlignment = Enum.TextXAlignment.Left
	
	Line_2.Name = "Line"
	Line_2.Parent = Main
	Line_2.BackgroundColor3 = Color3.fromRGB(51, 51, 51)
	Line_2.BackgroundTransparency = 0.500
	Line_2.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Line_2.BorderSizePixel = 0
	Line_2.Position = UDim2.new(0.249077484, 0, 0.165109038, 0)
	Line_2.Size = UDim2.new(0, 1, 0, 268)

	ExitButton.Name = "ExitButton"
	ExitButton.Parent = TopBar
	ExitButton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	ExitButton.BackgroundTransparency = 1.000
	ExitButton.BorderColor3 = Color3.fromRGB(0, 0, 0)
	ExitButton.BorderSizePixel = 0
	ExitButton.Position = UDim2.new(0.929889321, 0, 0.211538464, 0)
	ExitButton.Size = UDim2.new(0, 28, 0, 35)
	ExitButton.AutoButtonColor = false
	ExitButton.Image = "rbxassetid://10734897250"
	ExitButton.ImageTransparency = 0.800
	
	local function toggleVisibility()
		Main.Visible = false
	end

	ExitButton.MouseButton1Click:Connect(toggleVisibility)

	local UserInputService = game:GetService("UserInputService")
	UserInputService.InputBegan:Connect(function(input, gameProcessed)
		if gameProcessed then return end

		if input.UserInputType == Enum.UserInputType.Gamepad1 and input.KeyCode == Enum.KeyCode.ButtonB then
			toggleVisibility()
		end
	end)

	UIAspectRatioConstraint.Parent = ExitButton

	Line.Name = "Line"
	Line.Parent = Main
	Line.BackgroundColor3 = Color3.fromRGB(51, 51, 51)
	Line.BackgroundTransparency = 0.500
	Line.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Line.BorderSizePixel = 0
	Line.Position = UDim2.new(0, 0, 0.161993772, 0)
	Line.Size = UDim2.new(0, 542, 0, 1)

	Navigation.Name = "Navigation"
	Navigation.Parent = Main
	Navigation.Active = true
	Navigation.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Navigation.BackgroundTransparency = 1.000
	Navigation.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Navigation.BorderSizePixel = 0
	Navigation.Position = UDim2.new(0, 0, 0.165109038, 0)
	Navigation.Size = UDim2.new(0, 135, 0, 268)
	Navigation.ScrollBarImageColor3 = Color3.fromRGB(0, 0, 0)
	Navigation.CanvasSize = UDim2.new(0, 0, 8, 0)
	Navigation.ScrollBarThickness = 0

	UIListLayout.Parent = Navigation
	UIListLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center
	UIListLayout.SortOrder = Enum.SortOrder.LayoutOrder
	UIListLayout.Padding = UDim.new(0, 4)

	UIPadding.Parent = Navigation
	UIPadding.PaddingTop = UDim.new(0, 4)
	
	Content.Name = "Content"
	Content.Parent = Main
	Content.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Content.BackgroundTransparency = 1.000
	Content.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Content.BorderSizePixel = 0
	Content.Position = UDim2.new(0.250922501, 0, 0.165109038, 0)
	Content.Size = UDim2.new(0, 406, 0, 268)
	
	MobileCards.Name = "MobileCards"
	MobileCards.Parent = UI
	MobileCards.BackgroundColor3 = Color3.fromRGB(5, 5, 5)
	MobileCards.BorderColor3 = Color3.fromRGB(0, 0, 0)
	MobileCards.BorderSizePixel = 0
	MobileCards.Position = UDim2.new(0.173425466, 0, 0.214022145, 0)
	MobileCards.Size = UDim2.new(0, 45, 0, 45)
	MobileCards.AutoButtonColor = false
	MobileCards.Image = "rbxassetid://10747373176"
	MobileCards.ImageColor3 = Color3.fromRGB(83, 113, 241)

	UICorner_18.Parent = MobileCards
	
	local function ZUGVQY_script() -- Main.LocalScript 
		local script = Instance.new('LocalScript', Main)

		local TweenService = game:GetService("TweenService")
		local UserInputService = game:GetService("UserInputService")

		local gui = script.Parent

		local dragging
		local dragInput
		local dragStart
		local startPos

		local tweenInfo = TweenInfo.new(0.16, Enum.EasingStyle.Linear, Enum.EasingDirection.Out)

		local function update(input)
			local delta = input.Position - dragStart
			local targetPos = UDim2.new(
				startPos.X.Scale, 
				startPos.X.Offset + delta.X, 
				startPos.Y.Scale, 
				startPos.Y.Offset + delta.Y
			)

			local tween = TweenService:Create(gui, tweenInfo, {Position = targetPos})
			tween:Play()
		end

		gui.InputBegan:Connect(function(input)
			if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
				dragging = true
				dragStart = input.Position
				startPos = gui.Position

				input.Changed:Connect(function()
					if input.UserInputState == Enum.UserInputState.End then
						dragging = false
					end
				end)
			end
		end)

		gui.InputChanged:Connect(function(input)
			if input.UserInputType == Enum.UserInputType.MouseMovement or input.UserInputType == Enum.UserInputType.Touch then
				dragInput = input
			end
		end)

		UserInputService.InputChanged:Connect(function(input)
			if input == dragInput and dragging then
				update(input)
			end
		end)

		local function toggleGuiVisibility(input)
			if input.UserInputType == Enum.UserInputType.Keyboard and input.KeyCode == Enum.KeyCode.LeftControl then
				gui.Visible = not gui.Visible
			end
		end

		UserInputService.InputBegan:Connect(function(input, gameProcessed)
			if not gameProcessed then
				toggleGuiVisibility(input)
			end
		end)

	end
	coroutine.wrap(ZUGVQY_script)()
	local function VXNBNCK_script() -- MobileCards.LocalScript 
		local script = Instance.new('LocalScript', MobileCards)

		local TweenService = game:GetService("TweenService")
		local UserInputService = game:GetService("UserInputService")

		local gui = script.Parent

		local dragging
		local dragInput
		local dragStart
		local startPos

		local tweenInfo = TweenInfo.new(0.16, Enum.EasingStyle.Linear, Enum.EasingDirection.Out)

		local function update(input)
			local delta = input.Position - dragStart
			local targetPos = UDim2.new(
				startPos.X.Scale, 
				startPos.X.Offset + delta.X, 
				startPos.Y.Scale, 
				startPos.Y.Offset + delta.Y
			)

			local tween = TweenService:Create(gui, tweenInfo, {Position = targetPos})
			tween:Play()
		end

		gui.InputBegan:Connect(function(input)
			if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
				dragging = true
				dragStart = input.Position
				startPos = gui.Position

				input.Changed:Connect(function()
					if input.UserInputState == Enum.UserInputState.End then
						dragging = false
					end
				end)
			end
		end)

		gui.InputChanged:Connect(function(input)
			if input.UserInputType == Enum.UserInputType.MouseMovement or input.UserInputType == Enum.UserInputType.Touch then
				dragInput = input
			end
		end)

		UserInputService.InputChanged:Connect(function(input)
			if input == dragInput and dragging then
				update(input)
			end
		end)
	end
	coroutine.wrap(VXNBNCK_script)()
	local function YMNPC_script() -- UI.LocalScript 
		local script = Instance.new('LocalScript', UI)

		local screenGui = script.Parent
		local button = screenGui:WaitForChild("MobileCards")
		local main = screenGui:WaitForChild("Main")

		local function toggleVisibility()
			if main.Visible then
				main.Visible = false
			else
				main.Visible = true
			end
		end
		button.MouseButton1Click:Connect(toggleVisibility)
	end
	coroutine.wrap(YMNPC_script)()
	
	local TweenService = game:GetService("TweenService")
	local UserInputService = game:GetService("UserInputService")

	local Tabs = {}
	local ActiveTab = nil

	function lib:CreateTab(title)
		local Tab = Instance.new("ImageButton")
		local UICorner = Instance.new("UICorner")
		local TitleLabel = Instance.new("TextLabel")
		local Items = Instance.new("ScrollingFrame")
		local UIListLayout = Instance.new("UIListLayout")
		local UIPadding = Instance.new("UIPadding")

		Tab.Name = "Tab"
		Tab.Parent = Navigation
		Tab.BackgroundColor3 = Color3.fromRGB(83, 113, 241)
		Tab.BackgroundTransparency = 1
		Tab.Size = UDim2.new(0, 125, 0, 34)
		Tab.AutoButtonColor = false

		UICorner.CornerRadius = UDim.new(0, 6)
		UICorner.Parent = Tab

		TitleLabel.Name = "Title"
		TitleLabel.Parent = Tab
		TitleLabel.BackgroundTransparency = 1
		TitleLabel.Size = UDim2.new(0, 101, 0, 35)
		TitleLabel.Position = UDim2.new(0.1, 0, 0, 0)
		TitleLabel.Font = Enum.Font.Gotham
		TitleLabel.Text = title
		TitleLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
		TitleLabel.TextSize = 14
		TitleLabel.TextTransparency = 0.8

		Items.Name = title
		Items.Parent = Content
		Items.BackgroundTransparency = 1
		Items.Size = UDim2.new(0, 406, 0, 268)
		Items.CanvasSize = UDim2.new(0, 0, 20, 0)
		Items.ScrollBarThickness = 0
		Items.Visible = false

		UIListLayout.Parent = Items
		UIListLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center
		UIListLayout.SortOrder = Enum.SortOrder.LayoutOrder
		UIListLayout.Padding = UDim.new(0, 8)

		UIPadding.Parent = Items
		UIPadding.PaddingTop = UDim.new(0, 6)

		Tabs[Tab] = Items

		Tab.MouseButton1Click:Connect(function()
			lib:SwitchTab(Tab)
		end)

		return Items
	end

	function lib:SwitchTab(newTab)
		if ActiveTab then
			TweenService:Create(ActiveTab, TweenInfo.new(0.2), {BackgroundTransparency = 1}):Play()
			TweenService:Create(ActiveTab.Title, TweenInfo.new(0.2), {TextTransparency = 0.6}):Play()
			Tabs[ActiveTab].Visible = false
		end

		TweenService:Create(newTab, TweenInfo.new(0.2), {BackgroundTransparency = 0.6}):Play()
		TweenService:Create(newTab.Title, TweenInfo.new(0.2), {TextTransparency = 0}):Play()
		Tabs[newTab].Visible = true

		ActiveTab = newTab
	end

	UserInputService.InputBegan:Connect(function(input)
		if input.UserInputType == Enum.UserInputType.Gamepad1 or input.UserInputType == Enum.UserInputType.Touch then
			for tab, _ in pairs(Tabs) do
				if tab:IsFocused() then
					lib:SwitchTab(tab)
					break
				end
			end
		end
	end)
	
	function lib:CreateSection(title, TabParent)
		local Section = Instance.new("Frame")
		local UICorner_4 = Instance.new("UICorner")
		
		Section.Name = title
		Section.Parent = TabParent
		Section.BackgroundColor3 = Color3.fromRGB(21, 21, 21)
		Section.BackgroundTransparency = 0.500
		Section.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Section.BorderSizePixel = 0
		Section.Position = UDim2.new(0.14778325, 0, 0, 0)
		Section.Size = UDim2.new(0, 346, 0, 4)

		UICorner_4.CornerRadius = UDim.new(1, 0)
		UICorner_4.Parent = Section
	end
	
	function lib:CreateButton(title, TabParent, callback)
		local Button = Instance.new("ImageButton")
		local UICorner = Instance.new("UICorner")
		local UIStroke = Instance.new("UIStroke")
		local Title = Instance.new("TextLabel")
		local MouseIcon = Instance.new("ImageLabel")

		Button.Name = "Button"
		Button.Parent = TabParent
		Button.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Button.BackgroundTransparency = 0.98
		Button.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Button.BorderSizePixel = 0
		Button.Position = UDim2.new(0.017, 0, 0.038, 0)
		Button.Size = UDim2.new(0, 392, 0, 40)
		Button.AutoButtonColor = false

		UICorner.Parent = Button

		UIStroke.Parent = Button
		UIStroke.Color = Color3.fromRGB(51, 51, 51)
		UIStroke.Transparency = 0.7
		UIStroke.Thickness = 1.5

		Title.Name = "Title"
		Title.Parent = Button
		Title.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Title.BackgroundTransparency = 1
		Title.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Title.BorderSizePixel = 0
		Title.Position = UDim2.new(0.024, 0, 0.05, 0)
		Title.Size = UDim2.new(0, 136, 0, 35)
		Title.Font = Enum.Font.Gotham
		Title.Text = title
		Title.TextColor3 = Color3.fromRGB(255, 255, 255)
		Title.TextSize = 18
		Title.TextXAlignment = Enum.TextXAlignment.Left

		MouseIcon.Name = "MouseIcon"
		MouseIcon.Parent = Button
		MouseIcon.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		MouseIcon.BackgroundTransparency = 1
		MouseIcon.BorderColor3 = Color3.fromRGB(0, 0, 0)
		MouseIcon.BorderSizePixel = 0
		MouseIcon.Position = UDim2.new(0.916, 0, 0.2, 0)
		MouseIcon.Size = UDim2.new(0, 22, 0, 24)
		MouseIcon.Image = "rbxassetid://12804017021"
		MouseIcon.ImageColor3 = Color3.fromRGB(83, 113, 241)

		Button.Activated:Connect(function()
			if callback then
				callback()
			end
		end)

		local UIS = game:GetService("UserInputService")

		Button.SelectionGained:Connect(function()
			Button.BackgroundTransparency = 0.8
		end)

		Button.SelectionLost:Connect(function()
			Button.BackgroundTransparency = 0.98
		end)

		Button.TouchTap:Connect(function()
			if callback then
				callback()
			end
		end)

		return Button
	end
	
	function lib:CreateToggle(title, TabParent, callback)
		local Toggle = Instance.new("ImageButton")
		local UICorner_8 = Instance.new("UICorner")
		local UIStroke_3 = Instance.new("UIStroke")
		local Title_5 = Instance.new("TextLabel")
		local Slide_2 = Instance.new("Frame")
		local UICorner_9 = Instance.new("UICorner")
		local UIStroke_4 = Instance.new("UIStroke")
		local Wheel_2 = Instance.new("Frame")
		local UIAspectRatioConstraint_3 = Instance.new("UIAspectRatioConstraint")
		local UICorner_10 = Instance.new("UICorner")
		local toggleState = false

		Toggle.Name = "Toggle"
		Toggle.Parent = TabParent
		Toggle.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Toggle.BackgroundTransparency = 0.980
		Toggle.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Toggle.BorderSizePixel = 0
		Toggle.Position = UDim2.new(0.0172413792, 0, 0.037878789, 0)
		Toggle.Size = UDim2.new(0, 392, 0, 40)
		Toggle.AutoButtonColor = false

		UICorner_8.Parent = Toggle

		UIStroke_3.Parent = Toggle
		UIStroke_3.Color = Color3.fromRGB(51, 51, 51)
		UIStroke_3.Transparency = 0.700
		UIStroke_3.Thickness = 1.500

		Title_5.Name = "Title"
		Title_5.Parent = Toggle
		Title_5.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Title_5.BackgroundTransparency = 1.000
		Title_5.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Title_5.BorderSizePixel = 0
		Title_5.Position = UDim2.new(0.0239788759, 0, 0.0500000007, 0)
		Title_5.Size = UDim2.new(0, 136, 0, 35)
		Title_5.Font = Enum.Font.Gotham
		Title_5.Text = title
		Title_5.TextColor3 = Color3.fromRGB(255, 255, 255)
		Title_5.TextSize = 18.000
		Title_5.TextTransparency = 0.600
		Title_5.TextXAlignment = Enum.TextXAlignment.Left

		Slide_2.Name = "Slide"
		Slide_2.Parent = Toggle
		Slide_2.BackgroundColor3 = Color3.fromRGB(5, 5, 5)
		Slide_2.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Slide_2.BorderSizePixel = 0
		Slide_2.Position = UDim2.new(0.885204077, 0, 0.349999994, 0)
		Slide_2.Size = UDim2.new(0, 35, 0, 12)

		UICorner_9.CornerRadius = UDim.new(1, 0)
		UICorner_9.Parent = Slide_2

		UIStroke_4.Parent = Slide_2
		UIStroke_4.Color = Color3.fromRGB(51, 51, 51)
		UIStroke_4.Transparency = 0.700
		UIStroke_4.Thickness = 1.500

		Wheel_2.Name = "Wheel"
		Wheel_2.Parent = Slide_2
		Wheel_2.BackgroundColor3 = Color3.fromRGB(31, 31, 31)
		Wheel_2.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Wheel_2.BorderSizePixel = 0
		Wheel_2.Position = UDim2.new(-0.0250000004, 0, -0.333333343, 0)
		Wheel_2.Size = UDim2.new(0, 23, 0, 20)

		UIAspectRatioConstraint_3.Parent = Wheel_2

		UICorner_10.CornerRadius = UDim.new(1, 0)
		UICorner_10.Parent = Wheel_2

		local function TweenWheel(position, color, transparency)
			local tweenService = game:GetService("TweenService")
			local wheelTween = tweenService:Create(Wheel_2, TweenInfo.new(0.2, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), {
				Position = position,
				BackgroundColor3 = color
			})
			local textTween = tweenService:Create(Title_5, TweenInfo.new(0.2, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), {
				TextTransparency = transparency
			})
			wheelTween:Play()
			textTween:Play()
		end

		Toggle.MouseButton1Click:Connect(function()
			toggleState = not toggleState
			if toggleState then
				TweenWheel(UDim2.new(0.489285707, 0, -0.333333343, 0), Color3.fromRGB(83, 113, 241), 0)
			else
				TweenWheel(UDim2.new(-0.0250000004, 0, -0.333333343, 0), Color3.fromRGB(31, 31, 31), 0.6)
			end
			if callback then
				callback(toggleState)
			end
		end)

		Toggle.InputBegan:Connect(function(input)
			if input.UserInputType == Enum.UserInputType.Touch or input.UserInputType == Enum.UserInputType.Gamepad1 then
				Toggle.MouseButton1Click:Fire()
			end
		end)
	end
	
	function lib:CreateSlider(title, TabParent, min, default, max, callback)
		local Slider = Instance.new("ImageButton")
		local UICorner_11 = Instance.new("UICorner")
		local UIStroke_5 = Instance.new("UIStroke")
		local Title_6 = Instance.new("TextLabel")
		local SliderBack = Instance.new("Frame")
		local UICorner_12 = Instance.new("UICorner")
		local UIStroke_6 = Instance.new("UIStroke")
		local Draggable = Instance.new("Frame")
		local UICorner_13 = Instance.new("UICorner")
		local Value = Instance.new("TextLabel")

		Slider.Name = "Slider"
		Slider.Parent = TabParent
		Slider.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Slider.BackgroundTransparency = 0.980
		Slider.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Slider.BorderSizePixel = 0
		Slider.Position = UDim2.new(0.0172413792, 0, 0.412213743, 0)
		Slider.Size = UDim2.new(0, 392, 0, 44)
		Slider.AutoButtonColor = false

		UICorner_11.Parent = Slider
		UIStroke_5.Parent = Slider
		UIStroke_5.Color = Color3.fromRGB(51, 51, 51)
		UIStroke_5.Transparency = 0.700
		UIStroke_5.Thickness = 1.500

		Title_6.Name = "Title"
		Title_6.Parent = Slider
		Title_6.BackgroundTransparency = 1
		Title_6.Position = UDim2.new(0.0239788759, 0, -0.19999972, 0)
		Title_6.Size = UDim2.new(0, 136, 0, 32)
		Title_6.Font = Enum.Font.Gotham
		Title_6.Text = title
		Title_6.TextColor3 = Color3.fromRGB(255, 255, 255)
		Title_6.TextSize = 18.000
		Title_6.TextTransparency = 0.600
		Title_6.TextXAlignment = Enum.TextXAlignment.Left
		Title_6.TextYAlignment = Enum.TextYAlignment.Bottom

		SliderBack.Name = "SliderBack"
		SliderBack.Parent = Slider
		SliderBack.BackgroundColor3 = Color3.fromRGB(5, 5, 5)
		SliderBack.BorderSizePixel = 0
		SliderBack.Position = UDim2.new(0.0239787195, 0, 0.690908968, 0)
		SliderBack.Size = UDim2.new(0, 374, 0, 6)

		UICorner_12.CornerRadius = UDim.new(1, 0)
		UICorner_12.Parent = SliderBack
		UIStroke_6.Parent = SliderBack
		UIStroke_6.Color = Color3.fromRGB(51, 51, 51)
		UIStroke_6.Transparency = 0.700
		UIStroke_6.Thickness = 1.500

		Draggable.Name = "Draggable"
		Draggable.Parent = SliderBack
		Draggable.BackgroundColor3 = Color3.fromRGB(83, 113, 241)
		Draggable.BackgroundTransparency = 0.600
		Draggable.Size = UDim2.new(0, 256, 0, 6)

		UICorner_13.CornerRadius = UDim.new(1, 0)
		UICorner_13.Parent = Draggable

		Value.Name = "Value"
		Value.Parent = Slider
		Value.BackgroundTransparency = 1
		Value.Position = UDim2.new(0.626019716, 0, -0.19999972, 0)
		Value.Size = UDim2.new(0, 136, 0, 32)
		Value.Font = Enum.Font.Gotham
		Value.Text = tostring(default)
		Value.TextColor3 = Color3.fromRGB(255, 255, 255)
		Value.TextSize = 18.000
		Value.TextTransparency = 0.600
		Value.TextXAlignment = Enum.TextXAlignment.Right
		Value.TextYAlignment = Enum.TextYAlignment.Bottom

		local currentValue = default
		local isDragging = false
		local touchID = nil
		local UIS = game:GetService("UserInputService")
		local tweenService = game:GetService("TweenService")

		local function UpdateSliderPosition()
			local percentage = math.clamp((currentValue - min) / (max - min), 0, 1)
			Value.Text = string.format("%.1f", currentValue)
			Draggable.Size = UDim2.new(percentage, 0, 1, 0)
			callback(currentValue)

			tweenService:Create(Title_6, TweenInfo.new(0.2), {TextTransparency = 0}):Play()
			tweenService:Create(Value, TweenInfo.new(0.2), {TextTransparency = 0}):Play()
			local d1raggableTween = tweenService:Create(Draggable, TweenInfo.new(0.2), {BackgroundTransparency = 0})
			d1raggableTween:Play()
		end

		local function StartDragging(input)
			isDragging = true
			if input.UserInputType == Enum.UserInputType.Touch then
				touchID = input.UserInputIndex
			end

			Title_6.TextTransparency = 1
			Draggable.BackgroundTransparency = 1
		end

		local function UpdateDragging(input)
			local inputPosition
			if input.UserInputType == Enum.UserInputType.MouseMovement then
				inputPosition = input.Position.X
			elseif input.UserInputType == Enum.UserInputType.Touch then
				inputPosition = input.Position.X
			end

			if isDragging then
				local sliderX = SliderBack.AbsolutePosition.X
				local sliderWidth = SliderBack.AbsoluteSize.X
				local newPercentage = math.clamp((inputPosition - sliderX) / sliderWidth, 0, 1)
				currentValue = min + (newPercentage * (max - min))
				currentValue = math.round(currentValue * 10) / 10
				UpdateSliderPosition()
			end
		end

		local function StopDragging(input)
			if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
				isDragging = false
				touchID = nil

				local tween = tweenService:Create(Title_6, TweenInfo.new(0.2), {TextTransparency = 0.6})
				tween:Play()

				local valuetween = tweenService:Create(Value, TweenInfo.new(0.2), {TextTransparency = 0.6})
				valuetween:Play()

				local draggableTween = tweenService:Create(Draggable, TweenInfo.new(0.2), {BackgroundTransparency = 0.6})
				draggableTween:Play()
			end
		end

		Slider.MouseButton1Down:Connect(StartDragging)
		UIS.InputChanged:Connect(UpdateDragging)
		UIS.InputEnded:Connect(StopDragging)

		UpdateSliderPosition()
	end
	
	local TweenService = game:GetService("TweenService")

	function lib:CreateDropdown(title, TabParent, options, callback)
		local Dropdown = Instance.new("ImageButton")
		local UICorner_15 = Instance.new("UICorner")
		local UIStroke_8 = Instance.new("UIStroke")
		local Title_8 = Instance.new("TextLabel")
		local SelectedText = Instance.new("TextLabel")
		local DropOptions = Instance.new("Frame")
		local UIListLayout_3 = Instance.new("UIListLayout")

		Dropdown.Name = "Dropdown"
		Dropdown.Parent = TabParent
		Dropdown.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Dropdown.BackgroundTransparency = 0.980
		Dropdown.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Dropdown.BorderSizePixel = 0
		Dropdown.Position = UDim2.new(0.0172413792, 0, 0.037878789, 0)
		Dropdown.Size = UDim2.new(0, 392, 0, 40)
		Dropdown.AutoButtonColor = false

		UICorner_15.Parent = Dropdown

		UIStroke_8.Parent = Dropdown
		UIStroke_8.Color = Color3.fromRGB(51, 51, 51)
		UIStroke_8.Transparency = 0.700
		UIStroke_8.Thickness = 1.500

		Title_8.Name = "Title"
		Title_8.Parent = Dropdown
		Title_8.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Title_8.BackgroundTransparency = 1.000
		Title_8.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Title_8.BorderSizePixel = 0
		Title_8.Position = UDim2.new(0.0239788759, 0, 0.0500000007, 0)
		Title_8.Size = UDim2.new(0, 136, 0, 35)
		Title_8.Font = Enum.Font.Gotham
		Title_8.Text = title
		Title_8.TextColor3 = Color3.fromRGB(255, 255, 255)
		Title_8.TextSize = 18.000
		Title_8.TextTransparency = 0.6
		Title_8.TextXAlignment = Enum.TextXAlignment.Left

		SelectedText.Name = "SelectedText"
		SelectedText.Parent = Dropdown
		SelectedText.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		SelectedText.BackgroundTransparency = 1.000
		SelectedText.BorderColor3 = Color3.fromRGB(0, 0, 0)
		SelectedText.BorderSizePixel = 0
		SelectedText.Position = UDim2.new(0.631121755, 0, 0.0500000007, 0)
		SelectedText.Size = UDim2.new(0, 136, 0, 35)
		SelectedText.Font = Enum.Font.Gotham
		SelectedText.Text = "Blatant"
		SelectedText.TextColor3 = Color3.fromRGB(255, 255, 255)
		SelectedText.TextSize = 18.000
		SelectedText.TextTransparency = 0.6
		SelectedText.TextXAlignment = Enum.TextXAlignment.Right

		DropOptions.Name = "DropOptions"
		DropOptions.Parent = UI
		DropOptions.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		DropOptions.BorderColor3 = Color3.fromRGB(0, 0, 0)
		DropOptions.BorderSizePixel = 0
		DropOptions.Position = UDim2.new(0.6, 0, 0.0787878788, 180)
		DropOptions.Size = UDim2.new(0, 392, 0, 0)
		DropOptions.Visible = false

		UIListLayout_3.Parent = DropOptions
		UIListLayout_3.HorizontalAlignment = Enum.HorizontalAlignment.Center
		UIListLayout_3.SortOrder = Enum.SortOrder.LayoutOrder
		UIListLayout_3.Padding = UDim.new(0, 3)

		for _, option in ipairs(options) do
			local DropButton = Instance.new("ImageButton")
			local UICorner_19 = Instance.new("UICorner")
			local UIStroke_11 = Instance.new("UIStroke")
			local Title_10 = Instance.new("TextLabel")
			local MouseIcon_2 = Instance.new("ImageLabel")

			DropButton.Name = "DropButton"
			DropButton.Parent = DropOptions
			DropButton.BackgroundColor3 = Color3.fromRGB(11, 11, 11)
			DropButton.BorderColor3 = Color3.fromRGB(0, 0, 0)
			DropButton.BorderSizePixel = 0
			DropButton.Size = UDim2.new(0, 146, 0, 40)
			DropButton.AutoButtonColor = false

			UICorner_19.Parent = DropButton

			UIStroke_11.Parent = DropButton
			UIStroke_11.Color = Color3.fromRGB(51, 51, 51)
			UIStroke_11.Thickness = 1.500

			Title_10.Name = "Title"
			Title_10.Parent = DropButton
			Title_10.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
			Title_10.BackgroundTransparency = 1.000
			Title_10.BorderColor3 = Color3.fromRGB(0, 0, 0)
			Title_10.BorderSizePixel = 0
			Title_10.Position = UDim2.new(0.0650747642, 0, 0.0500000007, 0)
			Title_10.Size = UDim2.new(0, 136, 0, 35)
			Title_10.Font = Enum.Font.SourceSansSemibold
			Title_10.Text = option
			Title_10.TextColor3 = Color3.fromRGB(255, 255, 255)
			Title_10.TextSize = 18.000
			Title_10.TextXAlignment = Enum.TextXAlignment.Left

			MouseIcon_2.Name = "MouseIcon"
			MouseIcon_2.Parent = DropButton
			MouseIcon_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
			MouseIcon_2.BackgroundTransparency = 1.000
			MouseIcon_2.BorderColor3 = Color3.fromRGB(0, 0, 0)
			MouseIcon_2.BorderSizePixel = 0
			MouseIcon_2.Position = UDim2.new(0.799696803, 0, 0.125, 0)
			MouseIcon_2.Size = UDim2.new(0, 22, 0, 24)
			MouseIcon_2.Image = "rbxassetid://12804017021"
			MouseIcon_2.ImageColor3 = Color3.fromRGB(83, 113, 241)

			DropButton.MouseButton1Click:Connect(function()
				SelectedText.Text = option
				if callback then
					callback(option)
				end
				DropOptions.Visible = false
			end)
		end

		Dropdown.MouseButton1Click:Connect(function()
			local tweenTitle = TweenService:Create(Title_8, TweenInfo.new(0.1), {TextTransparency = 0})
			local tweenSelectedText = TweenService:Create(SelectedText, TweenInfo.new(0.1), {TextTransparency = 0})

			tweenTitle:Play()
			tweenSelectedText:Play()

			DropOptions.Visible = not DropOptions.Visible

			wait(0.2)
			tweenTitle = TweenService:Create(Title_8, TweenInfo.new(0.1), {TextTransparency = 0.6})
			tweenSelectedText = TweenService:Create(SelectedText, TweenInfo.new(0.1), {TextTransparency = 0.6})

			tweenTitle:Play()
			tweenSelectedText:Play()
		end)

		local function onDropdownPressed(input)
			if input.UserInputType == Enum.UserInputType.Touch or input.UserInputType == Enum.UserInputType.Gamepad1 then
				Dropdown.MouseButton1Click:Fire()
			end
		end

		Dropdown.InputBegan:Connect(onDropdownPressed)
	end
	
	local TweenService = game:GetService("TweenService")

	function lib:CreateInput(title, TabParent, TextHolder, callback)
		local Input = Instance.new("ImageButton")
		local UICorner_16 = Instance.new("UICorner")
		local UIStroke_9 = Instance.new("UIStroke")
		local Title_9 = Instance.new("TextLabel")
		local Box = Instance.new("Frame")
		local UICorner_17 = Instance.new("UICorner")
		local UIStroke_10 = Instance.new("UIStroke")
		local TextBox = Instance.new("TextBox")

		Input.Name = "Input"
		Input.Parent = TabParent
		Input.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Input.BackgroundTransparency = 0.980
		Input.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Input.BorderSizePixel = 0
		Input.Position = UDim2.new(0.248768479, 0, 0.46564886, 0)
		Input.Size = UDim2.new(0, 392, 0, 40)
		Input.AutoButtonColor = false

		UICorner_16.Parent = Input

		UIStroke_9.Parent = Input
		UIStroke_9.Color = Color3.fromRGB(51, 51, 51)
		UIStroke_9.Transparency = 0.700
		UIStroke_9.Thickness = 1.500

		Title_9.Name = "Title"
		Title_9.Parent = Input
		Title_9.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Title_9.BackgroundTransparency = 1.000
		Title_9.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Title_9.BorderSizePixel = 0
		Title_9.Position = UDim2.new(0.0239788759, 0, 0.0500000007, 0)
		Title_9.Size = UDim2.new(0, 136, 0, 35)
		Title_9.Font = Enum.Font.Gotham
		Title_9.Text = title
		Title_9.TextColor3 = Color3.fromRGB(255, 255, 255)
		Title_9.TextSize = 18.000
		Title_9.TextTransparency = 0.6
		Title_9.TextXAlignment = Enum.TextXAlignment.Left

		Box.Name = "Box"
		Box.Parent = Input
		Box.BackgroundColor3 = Color3.fromRGB(5, 5, 5)
		Box.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Box.BorderSizePixel = 0
		Box.Position = UDim2.new(0.762755096, 0, 0.200000003, 0)
		Box.Size = UDim2.new(0, 82, 0, 23)

		UICorner_17.CornerRadius = UDim.new(0, 2)
		UICorner_17.Parent = Box

		UIStroke_10.Parent = Box
		UIStroke_10.Color = Color3.fromRGB(51, 51, 51)
		UIStroke_10.Transparency = 0.700
		UIStroke_10.Thickness = 1.500

		TextBox.Parent = Box
		TextBox.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		TextBox.BackgroundTransparency = 1.000
		TextBox.BorderColor3 = Color3.fromRGB(0, 0, 0)
		TextBox.BorderSizePixel = 0
		TextBox.Size = UDim2.new(0, 82, 0, 23)
		TextBox.Font = Enum.Font.Gotham
		TextBox.PlaceholderText = TextHolder.."..."
		TextBox.Text = ""
		TextBox.TextColor3 = Color3.fromRGB(255, 255, 255)
		TextBox.TextSize = 14.000
		TextBox.TextTransparency = 0.400

		local function onFocus()
			local tween = TweenService:Create(TextBox, TweenInfo.new(0.2), {TextTransparency = 0})
			tween:Play()
		end

		local function onLoseFocus()
			local tween = TweenService:Create(TextBox, TweenInfo.new(0.2), {TextTransparency = 0.4})
			tween:Play()
		end

		TextBox.Focused:Connect(onFocus)
		TextBox.FocusLost:Connect(onLoseFocus)

		local userInputService = game:GetService("UserInputService")
		local function checkInput(input)
			if input.UserInputType == Enum.UserInputType.Touch or input.UserInputType == Enum.UserInputType.Gamepad1 then
				TextBox.Focus()
			end
		end

		userInputService.InputBegan:Connect(checkInput)

		TextBox.FocusLost:Connect(function()
			callback(TextBox.Text)
		end)
	end

	return lib
end
```
## Create Window
```lua
lib:CreateWindow("Lunar")
```
## Create Tab
```lua
local tab1 = lib:CreateTab("tes")
local tab2 = lib:CreateTab("ing")
```
## Create Section (which is a line)
```
lib:CreateSection("mags", tab1)
```
## Create Button
```lua
lib:CreateButton("Who made the ui?", tab1, function()
	print("JUSTVPN")
end)
```
## Create Toggle
```lua
lib:CreateToggle("Show Hitbox", tab1, function(state)
	print("Magnet toggle state:", state)
end)
```
## Create Slider
```lua
lib:CreateSlider("Volume", tab1, 0, 25, 100, function(value)
	print("Current Value: " .. value)
end)
```
## Create Dropdown
```lua
lib:CreateDropdown("Select an Option", tab1, {"Blatant", "Hidden", "Invisible"}, function(selected)
	print("Selected: " .. selected)
end)
```
## Create Input
```lua
lib:CreateInput("Set Health", tab1, "Health", function(inputValue)
	print("Input Value: " .. inputValue)
end)
```

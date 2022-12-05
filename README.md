--Test
for i,v in pairs(game.CoreGui:GetChildren()) do
    if v.Name == "DEVIL_UI_Lib" then
        v:Remove()
    end
end
_G.ToggleUI = "LeftControl"
local DEVIL_UI_Library_Mobile = {}

function DEVIL_UI_Library_Mobile:CreateWindow(GuiName, GameName)
    GuiName = GuiName or "Name"
    GameName = GameName or "Game Name"

    local ScreenGUI = (syn and syn.screengui_gui) or (function() end);
    local DEVIL_UI_Lib = Instance.new("ScreenGui")
    ScreenGUI(DEVIL_UI_Lib)
    local Main = Instance.new("Frame")
    local GameNameFrame = Instance.new("Frame")
    local HubName = Instance.new("TextLabel")
    local gameNameCorner = Instance.new("UICorner")
    local mainCorner = Instance.new("UICorner")
    local SideBar = Instance.new("Frame")
    local allTabs = Instance.new("ScrollingFrame")
    local tabListing = Instance.new("UICorner")
    local UIListLayout = Instance.new("UIListLayout")
    local UIPadding = Instance.new("UIPadding")
    local sideCorner = Instance.new("UICorner")
    local allPages = Instance.new("Frame")
    local pagesFolder = Instance.new("Folder")
    local allPageCorner = Instance.new("UICorner")


    --Properties:

    DEVIL_UI_Lib.Parent = game.CoreGui
    DEVIL_UI_Lib.Name = "DEVIL_UI_Lib"
    DEVIL_UI_Lib.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

    Main.Name = "Main"
    Main.Parent = DEVIL_UI_Lib
    Main.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
    Main.BorderSizePixel = 0
    Main.Position = UDim2.new(0.5, -250, 0.5, -125)
    Main.Size = UDim2.new(0, 500, 0, 250)

    GameNameFrame.Name = "GameNameFrame"
    GameNameFrame.Parent = Main
    GameNameFrame.BackgroundColor3 = Color3.fromRGB(45, 45, 45)
    GameNameFrame.BorderSizePixel = 0
    GameNameFrame.Size = UDim2.new(0, 500, 0, 40)

    HubName.Name = "HubName"
    HubName.Parent = GameNameFrame
    HubName.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    HubName.BackgroundTransparency = 1.000
    HubName.Position = UDim2.new(0.0200000014, 0, 0, 0)
    HubName.Size = UDim2.new(0, 490, 0, 40)
    HubName.Font = Enum.Font.Cartoon
    HubName.Text = GuiName.." : "..GameName
    HubName.TextTransparency = 0.3
    HubName.TextColor3 = Color3.fromRGB(255, 255, 255)
    HubName.TextSize = 23.000
    HubName.TextStrokeTransparency = 0.900
    HubName.TextWrapped = true
    HubName.TextXAlignment = Enum.TextXAlignment.Left

    gameNameCorner.CornerRadius = UDim.new(0, 5)
    gameNameCorner.Name = "gameNameCorner"
    gameNameCorner.Parent = GameNameFrame

    mainCorner.CornerRadius = UDim.new(0, 5)
    mainCorner.Name = "mainCorner"
    mainCorner.Parent = Main

    SideBar.Name = "SideBar"
    SideBar.Parent = Main
    SideBar.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    SideBar.BackgroundTransparency = 1.000
    SideBar.BorderSizePixel = 0
    SideBar.Position = UDim2.new(0.0199999996, 0, 0.217999995, 0)
    SideBar.Size = UDim2.new(0, 120, 0, 185)

    allTabs.Name = "allTabs"
    allTabs.Parent = SideBar
    allTabs.Active = true
    allTabs.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
    allTabs.BorderSizePixel = 0
    allTabs.Position = UDim2.new(-0.0483333319, 5, -0.00362168252, 0)
    allTabs.Size = UDim2.new(0, 120, 0, 185)
    allTabs.CanvasSize = UDim2.new(0, 0, 0, 0)
    allTabs.ScrollBarThickness = 7

    tabListing.CornerRadius = UDim.new(0, 5)
    tabListing.Name = "tabListing"
    tabListing.Parent = allTabs



    UIListLayout.Parent = allTabs
    UIListLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center
    UIListLayout.SortOrder = Enum.SortOrder.LayoutOrder
    UIListLayout.Padding = UDim.new(0, 5)

    UIPadding.Parent = allTabs
    UIPadding.PaddingTop = UDim.new(0, 5)

    sideCorner.CornerRadius = UDim.new(0, 5)
    sideCorner.Name = "sideCorner"
    sideCorner.Parent = SideBar


    -- Scripts:

    local function BUbABUBAPUTA_fake_script()
    local script1 = Instance.new('Script', Main)
        game:GetService("UserInputService").InputBegan:Connect(function(key)
            if key.KeyCode == Enum.KeyCode[_G.ToggleUI] then
                script1.Parent.Parent.Enabled = not script1.Parent.Parent.Enabled
            end
        end)
    end
    coroutine.wrap(BUbABUBAPUTA_fake_script)()



    local function ZBUJHKQ_fake_script() -- Main.Draggable 
        local script = Instance.new('Script', Main)

        --[[
        
            Works on mobile to 🥱
            If this dont work then just throw you pc/mobile retard 😂
        
        ]]


        
        local UserInputService = game:GetService("UserInputService")

        local gui = script.Parent

        local dragging
        local dragInput
        local dragStart
        local startPos

        local function update(input)
        	local delta = input.Position - dragStart
        	gui.Position = UDim2.new(startPos.X.Scale, startPos.X.Offset + delta.X, startPos.Y.Scale, startPos.Y.Offset + delta.Y)
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
    coroutine.wrap(ZBUJHKQ_fake_script)()
    local function MILXP_fake_script() -- allTabs.ScrollFrameFixer 
        local script = Instance.new('Script', allTabs)

        spawn(function()
            getgenv().autofixertheui = true
            while autofixertheui do wait()
                pcall(function()
                    local function UpdateCanvasSize(Canvas, Constraint)
                        Canvas.CanvasSize = UDim2.new(0, 0, 0, Constraint.AbsoluteContentSize.Y+10)
                    end
        
        
                    wait() --//Idk why add wait LMFAO//
        
                    UpdateCanvasSize(script.Parent, script.Parent.UIListLayout)
                end)
            end
        end)
    end
    coroutine.wrap(MILXP_fake_script)()



    local TabsHandler = {}

    function TabsHandler:CreateTab(tabname)
        tabname = tabname or "New Tab"
        local tabButton = Instance.new("TextButton")
        local tabCorner = Instance.new("UICorner")
        local newPage = Instance.new("ScrollingFrame")
        local newPageCorner = Instance.new("UICorner")
        local NewPageListLayout = Instance.new("UIListLayout")
        local NewPagePadding = Instance.new("UIPadding")

        tabButton.Name = "tabButton"
        tabButton.Parent = allTabs
        tabButton.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
        tabButton.BorderSizePixel = 0
        tabButton.Position = UDim2.new(-0.00351155549, 0, 0.134228438, 0)
        tabButton.Size = UDim2.new(0, 110, 0, 25)
        tabButton.Font = Enum.Font.Cartoon
        tabButton.Text = tabname or "New Tab"
        tabButton.TextColor3 = Color3.fromRGB(255, 255, 255)
        tabButton.TextSize = 15.000
        tabButton.TextStrokeTransparency = 0.900
        tabButton.TextTransparency = 0.300
        tabButton.TextWrapped = true


        tabCorner.Parent = tabButton


        newPage.Name = "newPage"
        newPage.Parent = pagesFolder
        newPage.Active = true
        newPage.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
        newPage.BorderSizePixel = 0
        newPage.Position = UDim2.new(-0.0290697813, 10, -0.00233905017, 0)
        newPage.Size = UDim2.new(0, 355, 0, 185)
        newPage.ScrollBarThickness = 7
        newPage.Visible = false
        newPage.CanvasSize = UDim2.new(0, 0, 0, 0)

        local function DWMOAM_fake_script() -- newPage.ScrollFrameFixer 
            local script = Instance.new('Script', newPage)
    
            spawn(function()
                getgenv().autofixertheui = true
                while autofixertheui do wait()
                    pcall(function()
                        local function UpdateCanvasSize(Canvas, Constraint)
                            Canvas.CanvasSize = UDim2.new(0, 0, 0, Constraint.AbsoluteContentSize.Y+10)
                        end
            
            
                        wait() --//Idk why add wait LMFAO//
            
                        UpdateCanvasSize(script.Parent, script.Parent.UIListLayout)
                    end)
                end
            end)
        end
        coroutine.wrap(DWMOAM_fake_script)()


        newPageCorner.CornerRadius = UDim.new(0, 5)
        newPageCorner.Name = "newPageCorner"
        newPageCorner.Parent = newPage


        NewPageListLayout.Parent = newPage
        NewPageListLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center
        NewPageListLayout.SortOrder = Enum.SortOrder.LayoutOrder
        NewPageListLayout.Padding = UDim.new(0, 5)
    

        NewPagePadding.Parent = newPage
        NewPagePadding.PaddingTop = UDim.new(0, 5)


        allPages.Name = "allPages"
        allPages.Parent = Main
        allPages.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
        allPages.BackgroundTransparency = 1.000
        allPages.BorderSizePixel = 0
        allPages.Position = UDim2.new(0.270000011, 0, 0.216000006, 0)
        allPages.Size = UDim2.new(0, 355, 0, 185)
    
    
        pagesFolder.Name = "pagesFolder"
        pagesFolder.Parent = allPages
    
        allPageCorner.CornerRadius = UDim.new(0, 5)
        allPageCorner.Name = "allPageCorner"
        allPageCorner.Parent = allPages
    
        
        local function onInputBegan(input, gameProcessed)
            if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
                for i,v in next, pagesFolder:GetChildren() do -- We get all the pages that we added
                    v.Visible = false	-- then we make them invisible 
                end 
                newPage.Visible = true	-- We make current page visible but not others
                
                --Animations Below  -- Optional
                for i,v in next, allTabs:GetChildren() do	-- We get all the elements inside the frame
                    if v:IsA("TextButton") then -- We can't animate UIListLayout, so we check if its a TextButton
                        game.TweenService:Create(v, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                            BackgroundColor3 = Color3.fromRGB(30, 30, 30) -- We animate other Tab Buttons and making the current one seem Checked
                        }):Play()
                    end
                end
                game.TweenService:Create(tabButton, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                    BackgroundColor3 = Color3.fromRGB(0, 0, 0) -- We animate other Tab Buttons and making the current one seem Checked
                }):Play()
            end
        end
        tabButton.InputBegan:Connect(onInputBegan)




    local PagesHandler = {}

        function PagesHandler:CreateBlankLabel(TextLabelBlankText)
            TextLabelMainText = TextLabelMainText or ""

            local PageBlanklFrame = Instance.new("Frame")
            local BlankFrame = Instance.new("TextLabel")
            local TextLabelCorner_2 = Instance.new("UICorner")


            PageBlanklFrame.Name = "PageBlanklFrame"
            PageBlanklFrame.Parent = newPage
            PageBlanklFrame.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
            PageBlanklFrame.BackgroundTransparency = 1.000
            PageBlanklFrame.BorderSizePixel = 0
            PageBlanklFrame.Position = UDim2.new(0.0211267602, 0, 0.0235245991, 0)
            PageBlanklFrame.Size = UDim2.new(0, 340, 0, 25)

            BlankFrame.Name = "BlankFrame"
            BlankFrame.Parent = PageBlanklFrame
            BlankFrame.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
            BlankFrame.BackgroundTransparency = 1.000
            BlankFrame.BorderSizePixel = 0
            BlankFrame.Size = UDim2.new(0, 340, 0, 25)
            BlankFrame.Font = Enum.Font.Cartoon
            BlankFrame.Text = TextLabelBlankText
            BlankFrame.TextColor3 = Color3.fromRGB(255, 255, 255)
            BlankFrame.TextSize = 15.000
            BlankFrame.TextStrokeTransparency = 0.900
            BlankFrame.TextTransparency = 0.300

            TextLabelCorner_2.Name = "TextLabelCorner"
            TextLabelCorner_2.Parent = BlankFrame
        end


        function PagesHandler:CreateTextLabel(TextLabelMainText, callback)
            TextLabelMainText = TextLabelMainText or "TextLabel"

            local PageTextLabelFrame = Instance.new("Frame")
            local TextLabel = Instance.new("TextLabel")
            local TextLabelCorner = Instance.new("UICorner")

            PageTextLabelFrame.Name = "PageTextLabelFrame"
            PageTextLabelFrame.Parent = newPage
            PageTextLabelFrame.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
            PageTextLabelFrame.BackgroundTransparency = 1.000
            PageTextLabelFrame.BorderSizePixel = 0
            PageTextLabelFrame.Position = UDim2.new(0.0211267602, 0, 0.0235245991, 0)
            PageTextLabelFrame.Size = UDim2.new(0, 340, 0, 25)

            TextLabel.Parent = PageTextLabelFrame
            TextLabel.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
            TextLabel.BorderSizePixel = 0
            TextLabel.Size = UDim2.new(0, 340, 0, 25)
            TextLabel.Font = Enum.Font.Cartoon
            TextLabel.Text = TextLabelMainText
            TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
            TextLabel.TextSize = 15.000
            TextLabel.TextStrokeTransparency = 0.900
            TextLabel.TextTransparency = 0.300

            TextLabelCorner.Name = "PageButtonCorner"
            TextLabelCorner.Parent = TextLabel

        end


        function PagesHandler:CreateSection(SectionMainText)
            SectionMainText = SectionMainText or "Section Text"

            local PageSectionFrame = Instance.new("Frame")
            local SectionText = Instance.new("TextLabel")
            local SectionCorner = Instance.new("UICorner")

            PageSectionFrame.Name = "PageSectionFrame"
            PageSectionFrame.Parent = newPage
            PageSectionFrame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            PageSectionFrame.BackgroundTransparency = 1.000
            PageSectionFrame.Position = UDim2.new(0.0211267602, 0, 0.5, 0)
            PageSectionFrame.Size = UDim2.new(0, 340, 0, 60)
            
            SectionText.Name = "SectionText"
            SectionText.Parent = PageSectionFrame
            SectionText.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
            SectionText.Position = UDim2.new(-0.00294117653, 0, 0.277777761, 0)
            SectionText.Size = UDim2.new(0, 340, 0, 25)
            SectionText.Font = Enum.Font.Cartoon
            SectionText.Text = SectionMainText
            SectionText.TextColor3 = Color3.fromRGB(255, 255, 255)
            SectionText.TextSize = 18.000
            SectionText.TextStrokeTransparency = 0.900
            SectionText.TextTransparency = 0.300
            SectionText.TextWrapped = true
            
            SectionCorner.Name = "SectionCorner"
            SectionCorner.Parent = SectionText

        end


		function PagesHandler:CreateButton(ButtonText, callback)
			ButtonText = ButtonText or "Text Button"
			callback = callback or function() end	


            local PageButtonFrame = Instance.new("Frame")
            local PageButton = Instance.new("TextButton")
            local PageButtonCorner = Instance.new("UICorner")
    
            PageButtonFrame.Name = "PageButtonFrame"
            PageButtonFrame.Parent = newPage
            PageButtonFrame.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
            PageButtonFrame.BackgroundTransparency = 1.000
            PageButtonFrame.BorderSizePixel = 0
            PageButtonFrame.Position = UDim2.new(0.0211267602, 0, 0.0235245991, 0)
            PageButtonFrame.Size = UDim2.new(0, 340, 0, 25)

            PageButton.Name = "PageButton"
            PageButton.Parent = PageButtonFrame
            PageButton.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
            PageButton.BorderSizePixel = 0
            PageButton.Position = UDim2.new(-0.00164741068, 0, 0.00867309608, 0)
            PageButton.Size = UDim2.new(0, 340, 0, 25)
            PageButton.Font = Enum.Font.Cartoon
            PageButton.Text = ButtonText
            PageButton.TextColor3 = Color3.fromRGB(255, 255, 255)
            PageButton.TextSize = 15.000
            PageButton.TextStrokeTransparency = 0.900
            PageButton.TextTransparency = 0.300
            PageButton.TextWrapped = true

            PageButtonCorner.Name = "PageButtonCorner"
            PageButtonCorner.Parent = PageButton
        
            local function onInputBegan(input, gameProcessed)
                if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
                    callback()
                end
            end
            PageButton.InputBegan:Connect(onInputBegan)

        end



        function PagesHandler:CreateToggle(ToggleMainText, callback)
            ToggleMainText = ToggleMainText or "Toggle Text"
            callback = callback or function() end	

            local PageToggleFrame = Instance.new("Frame")
            local ToggleText = Instance.new("TextLabel")
            local ToggleButton = Instance.new("TextButton")
            local ToggleButtonCorner = Instance.new("UICorner")
            local ToggleFrameCorner = Instance.new("UICorner")


            PageToggleFrame.Name = "PageToggleFrame"
            PageToggleFrame.Parent = newPage
            PageToggleFrame.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
            PageToggleFrame.BorderSizePixel = 0
            PageToggleFrame.Position = UDim2.new(0.0211267602, 0, 0.0235245991, 0)
            PageToggleFrame.Size = UDim2.new(0, 340, 0, 25)

            ToggleText.Name = "ToggleText"
            ToggleText.Parent = PageToggleFrame
            ToggleText.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            ToggleText.BackgroundTransparency = 1.000
            ToggleText.BorderSizePixel = 0
            ToggleText.Position = UDim2.new(0.0294117648, 0, 0, 0)
            ToggleText.Size = UDim2.new(0, 300, 0, 25)
            ToggleText.Font = Enum.Font.Cartoon
            ToggleText.Text = ToggleMainText
            ToggleText.TextColor3 = Color3.fromRGB(255, 255, 255)
            ToggleText.TextSize = 15.000
            ToggleText.TextStrokeTransparency = 0.900
            ToggleText.TextTransparency = 0.300
            ToggleText.TextXAlignment = Enum.TextXAlignment.Left

            ToggleButton.Name = "ToggleButton"
            ToggleButton.Parent = PageToggleFrame
            ToggleButton.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
            ToggleButton.Position = UDim2.new(0.911764681, 0, 0.0799999982, 0)
            ToggleButton.Size = UDim2.new(0, 20, 0, 20)
            ToggleButton.Font = Enum.Font.SourceSans
            ToggleButton.Text = ""
            ToggleButton.TextColor3 = Color3.fromRGB(255, 255, 255)
            ToggleButton.TextSize = 15.000

            ToggleButtonCorner.CornerRadius = UDim.new(0, 20)
            ToggleButtonCorner.Name = "ToggleButtonCorner"
            ToggleButtonCorner.Parent = ToggleButton

            ToggleFrameCorner.Name = "ToggleFrameCorner"
            ToggleFrameCorner.Parent = PageToggleFrame

            local tog = false
			
            local function onInputBegan(input, gameProcessed)
                if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
                    tog = not tog
				    callback(tog) -- Callbacks whenever we toggle
                    if tog then 
                        game.TweenService:Create(ToggleButton, TweenInfo.new(0.15, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                            BackgroundColor3 = Color3.fromRGB(0, 0, 0)
                        }):Play()
                        --- We put our animation here when the toggle is on
                    else
                        game.TweenService:Create(ToggleButton, TweenInfo.new(0.15, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                            BackgroundColor3 = Color3.fromRGB(60, 60, 60)
                        }):Play()
                        ---We Put our animation here when the toggle is off
                    end
                end
            end
            ToggleButton.InputBegan:Connect(onInputBegan)

		end



        function PagesHandler:CreateSlider(SliderMainText, options , callback)
            SliderMainText = SliderMainText or "Slider Text"
            callback = callback or function() end	

            local PageSliderFrame = Instance.new("Frame")
            local SliderFrameCorner = Instance.new("UICorner")
            local SiderMainTextButton = Instance.new("TextButton")
            local SliderMainTextButtonCorner = Instance.new("UICorner")
            local SlidingBar = Instance.new("Frame")
            local SlidingBarCorner = Instance.new("UICorner")
            local MainSlidingBar = Instance.new("Frame")
            local MainSlidingBarCorner = Instance.new("UICorner")
            local AmountLabelFrame = Instance.new("Frame")
            local AmountLabelFrameCorner = Instance.new("UICorner")
            local AmountLabel = Instance.new("TextLabel")
            local SliderText = Instance.new("TextLabel")


            PageSliderFrame.Name = "PageSliderFrame"
            PageSliderFrame.Parent = newPage
            PageSliderFrame.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
            PageSliderFrame.BorderSizePixel = 0
            PageSliderFrame.Position = UDim2.new(0.0211267602, 0, 0.027777778, 0)
            PageSliderFrame.Size = UDim2.new(0, 340, 0, 45)

            SliderFrameCorner.Name = "SliderFrameCorner"
            SliderFrameCorner.Parent = PageSliderFrame

            SiderMainTextButton.Name = "SiderMainTextButton"
            SiderMainTextButton.Parent = PageSliderFrame
            SiderMainTextButton.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
            SiderMainTextButton.BackgroundTransparency = 0.500
            SiderMainTextButton.Position = UDim2.new(0.0260000005, 0, 0.600000024, -5)
            SiderMainTextButton.Size = UDim2.new(0, 320, 0, 20)
            SiderMainTextButton.Font = Enum.Font.SourceSans
            SiderMainTextButton.Text = ""
            SiderMainTextButton.TextColor3 = Color3.fromRGB(0, 0, 0)
            SiderMainTextButton.TextSize = 14.000
            SiderMainTextButton.TextTransparency = 1.000

            SliderMainTextButtonCorner.Name = "SliderMainTextButtonCorner"
            SliderMainTextButtonCorner.Parent = SiderMainTextButton

            SlidingBar.Name = "SlidingBar"
            SlidingBar.Parent = SiderMainTextButton
            SlidingBar.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
            SlidingBar.Position = UDim2.new(0.015625, 0, 0.150000006, 0)
            SlidingBar.Size = UDim2.new(0, 310, 0, 13)

            SlidingBarCorner.Name = "SlidingBarCorner"
            SlidingBarCorner.Parent = SlidingBar

            MainSlidingBar.Name = "MainSlidingBar"
            MainSlidingBar.Parent = SlidingBar
            MainSlidingBar.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
            MainSlidingBar.Position = UDim2.new(-0.00050403201, 0, -0.00384615362, 0)
            MainSlidingBar.Size = UDim2.new(0, 155, 0, 13)

            MainSlidingBarCorner.Name = "MainSlidingBarCorner"
            MainSlidingBarCorner.Parent = MainSlidingBar

            AmountLabelFrame.Name = "AmountLabelFrame"
            AmountLabelFrame.Parent = PageSliderFrame
            AmountLabelFrame.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
            AmountLabelFrame.Position = UDim2.new(0.754999995, 0, 0, 3)
            AmountLabelFrame.Size = UDim2.new(0, 80, 0, 15)

            AmountLabelFrameCorner.Name = "AmountLabelFrameCorner"
            AmountLabelFrameCorner.Parent = AmountLabelFrame

            AmountLabel.Name = "AmountLabel"
            AmountLabel.Parent = AmountLabelFrame
            AmountLabel.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
            AmountLabel.BackgroundTransparency = 1.000
            AmountLabel.Position = UDim2.new(0, 0, -0.200000003, 2)
            AmountLabel.Size = UDim2.new(0, 75, 0, 15)
            AmountLabel.Font = Enum.Font.SourceSans
            AmountLabel.Text = "50"
            AmountLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
            AmountLabel.TextSize = 15.000
            AmountLabel.TextStrokeTransparency = 0.900
            AmountLabel.TextTransparency = 0.300
            AmountLabel.TextXAlignment = Enum.TextXAlignment.Right

            SliderText.Name = "SliderText"
            SliderText.Parent = PageSliderFrame
            SliderText.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            SliderText.BackgroundTransparency = 1.000
            SliderText.BorderColor3 = Color3.fromRGB(27, 42, 53)
            SliderText.BorderSizePixel = 0
            SliderText.Position = UDim2.new(0, 8, 0, 3)
            SliderText.Size = UDim2.new(0, 247, 0, 19)
            SliderText.Font = Enum.Font.Cartoon
            SliderText.Text = SliderMainText
            SliderText.TextColor3 = Color3.fromRGB(255, 255, 255)
            SliderText.TextSize = 14.000
            SliderText.TextStrokeTransparency = 0.900
            SliderText.TextTransparency = 0.300
            SliderText.TextWrapped = true
            SliderText.TextXAlignment = Enum.TextXAlignment.Left


            local SMTB = SiderMainTextButton
            local hold = false
            local MSbar = SMTB.SlidingBar.MainSlidingBar
            local amtBox = SMTB.Parent.AmountLabelFrame.AmountLabel
            local Min = options.Min
            local Max = options.Max
            local Default = options.Default or options.Default

            local plr = game.Players.LocalPlayer
            local ms = plr:GetMouse()
            local rlpos
            local rlsiz
            local ap = Vector2.new(SMTB.AbsolutePosition.X, SMTB.AbsolutePosition.Y)
            local as = Vector2.new(SMTB.AbsoluteSize.X, SMTB.AbsoluteSize.Y)

            amtBox.Text = tostring(Default)
            MSbar.Size = UDim2.new(0, (310/Max)*Default, 0, 13)
            

            local function onInputBegan(input, gameProcessed)
                if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
                    hold = true
                end
            end
            SMTB.InputBegan:Connect(onInputBegan)

            game:GetService('UserInputService').InputEnded:Connect(function(input)
                if  input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch  then
                    hold = false
                end
            end)

            game:GetService('RunService').RenderStepped:Connect(function()
                if hold then
                    ap = Vector2.new(SMTB.AbsolutePosition.X, SMTB.AbsolutePosition.Y)
                    as = Vector2.new(SMTB.AbsoluteSize.X, SMTB.AbsoluteSize.Y)

                    rlpos = (ms.X-ap.X)
                    rlsiz = (ms.X-ap.X)
                    local result = math.floor(Max * (rlsiz / 310))
                    if rlpos > 310 then
                        result = Max
                    elseif rlpos < 0 then
                        result = 0
                    end

                    if rlsiz <= 310 and rlsiz >= 0 then
                        amtBox.Text = tostring(result)
                        MSbar.Size = UDim2.new(0, rlsiz, 0, 13)
                        MSbar.Visible = true
                        callback(result)
                    end
                    if rlsiz <= 0 then
                        amtBox.Text = tostring(Min)
                        MSbar.Size = UDim2.new(0, 0, 0, 13)
                        MSbar.Visible = false
                        callback(Min)
                    end
                    if rlsiz >= 310 then
                        amtBox.Text = tostring(Max)
                        MSbar.Size = UDim2.new(0, 310, 0, 13)
                        MSbar.Visible = true
                        callback(Max)
                    end
                    
                end
            end)

        end



        function PagesHandler:CreateDropdown(DropdownMainText, Contents, callback)
            DropdownMainText = DropdownMainText or "Dropdown Text"
            callback = callback or function() end	

            local PageDropdownFrame = Instance.new("Frame")
            local DropdownText = Instance.new("TextLabel")
            local DropdownFrameCorner = Instance.new("UICorner")
            local DropdownArrow = Instance.new("ImageButton")
            local DropdownMainButton = Instance.new("TextButton")

            ----------Dropdown List----------

            local PageDropdownScrollingFrame = Instance.new("ScrollingFrame")
            local DropdownScrollCorner = Instance.new("UICorner")
            local DropdownScrollListLayout = Instance.new("UIListLayout")
            local DropdownScrollPadding = Instance.new("UIPadding")

            ----------Dropdown List----------

            
            PageDropdownFrame.Name = "PageDropdownFrame"
            PageDropdownFrame.Parent = newPage
            PageDropdownFrame.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
            PageDropdownFrame.BorderSizePixel = 0
            PageDropdownFrame.Position = UDim2.new(0.0211267602, 0, 0.0235245991, 0)
            PageDropdownFrame.Size = UDim2.new(0, 340, 0, 25)

            DropdownText.Name = "DropdownText"
            DropdownText.Parent = PageDropdownFrame
            DropdownText.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            DropdownText.BackgroundTransparency = 1.000
            DropdownText.BorderSizePixel = 0
            DropdownText.Position = UDim2.new(0.0294117648, 0, 0, 0)
            DropdownText.Size = UDim2.new(0, 300, 0, 25)
            DropdownText.Font = Enum.Font.Cartoon
            DropdownText.Text = DropdownMainText
            DropdownText.TextColor3 = Color3.fromRGB(255, 255, 255)
            DropdownText.TextSize = 15.000
            DropdownText.TextStrokeTransparency = 0.900
            DropdownText.TextTransparency = 0.300
            DropdownText.TextWrapped = true
            DropdownText.TextXAlignment = Enum.TextXAlignment.Left

            DropdownFrameCorner.Name = "DropdownFrameCorner"
            DropdownFrameCorner.Parent = PageDropdownFrame

            DropdownArrow.Name = "DropdownArrow"
            DropdownArrow.Parent = PageDropdownFrame
            DropdownArrow.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            DropdownArrow.BackgroundTransparency = 1.000
            DropdownArrow.Position = UDim2.new(0.925000012, 0, 0.0799999982, 0)
            DropdownArrow.Rotation = 180
            DropdownArrow.Size = UDim2.new(0, 20, 0, 20)
            DropdownArrow.Image = "http://www.roblox.com/asset/?id=71659683"

            DropdownMainButton.Name = "DropdownMainButton"
            DropdownMainButton.Parent = PageDropdownFrame
            DropdownMainButton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            DropdownMainButton.BackgroundTransparency = 1.000
            DropdownMainButton.BorderSizePixel = 0
            DropdownMainButton.Size = UDim2.new(0, 339, 0, 25)
            DropdownMainButton.Font = Enum.Font.SourceSans
            DropdownMainButton.Text = ""
            DropdownMainButton.TextColor3 = Color3.fromRGB(0, 0, 0)
            DropdownMainButton.TextSize = 14.000


            ----------Dropdown List----------

            PageDropdownScrollingFrame.Name = "PageDropdownScrollingFrame"
            PageDropdownScrollingFrame.Parent = newPage
            PageDropdownScrollingFrame.Active = false
            PageDropdownScrollingFrame.Visible = false
            PageDropdownScrollingFrame.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
            PageDropdownScrollingFrame.BorderSizePixel = 0
            PageDropdownScrollingFrame.Position = UDim2.new(0.0633802786, 0, 0.156156242, 0)
            PageDropdownScrollingFrame.Size = UDim2.new(0, 340, 0, 155)
            PageDropdownScrollingFrame.CanvasSize = UDim2.new(0, 0, 0, 0)
            PageDropdownScrollingFrame.ScrollBarThickness = 7

            DropdownScrollCorner.CornerRadius = UDim.new(0, 5)
            DropdownScrollCorner.Name = "DropdownScrollCorner"
            DropdownScrollCorner.Parent = PageDropdownScrollingFrame

            DropdownScrollListLayout.Name = "DropdownScrollListLayout"
            DropdownScrollListLayout.Parent = PageDropdownScrollingFrame
            DropdownScrollListLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center
            DropdownScrollListLayout.SortOrder = Enum.SortOrder.LayoutOrder
            DropdownScrollListLayout.Padding = UDim.new(0, 5)

            DropdownScrollPadding.Name = "DropdownScrollPadding"
            DropdownScrollPadding.Parent = PageDropdownScrollingFrame
            DropdownScrollPadding.PaddingTop = UDim.new(0, 5)

            ----------Dropdown List----------

            local function TEGYQ_fake_script() -- PageDropdownScrollingFrame.DropdownScrollFixer 
                local script = Instance.new('Script', PageDropdownScrollingFrame)
            
                spawn(function()
                    getgenv().autofixertheui = true
                    while autofixertheui do wait()
                        pcall(function()
                            local function UpdateCanvasSize(Canvas, Constraint)
                                Canvas.CanvasSize = UDim2.new(0, 0, 0, Constraint.AbsoluteContentSize.Y+10)
                            end
                
                
                            wait() --//Idk why add wait LMFAO//
                
                            UpdateCanvasSize(script.Parent, script.Parent.DropdownScrollListLayout)
                        end)
                    end
                end)
            end
            coroutine.wrap(TEGYQ_fake_script)()


            local function onInputBegan(input, gameProcessed)
                if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
                    if DropdownArrow.Rotation == 90 then
                        local TweenService = game:GetService("TweenService")
                        local Object = DropdownArrow -- The object you want to tween.
                        local tweenInfo = TweenInfo.new(
                            0.2, -- The time the tween takes to complete
                            Enum.EasingStyle.Linear, -- The tween style.
                            Enum.EasingDirection.Out, -- EasingDirection
                            .5, -- How many times you want the tween to repeat. If you make it less than 0 it will repeat forever.
                            false, -- Reverse?
                            0 -- Delay
                        )
                        local Tween = TweenService:Create(Object, tweenInfo, {Rotation = 180}) -- Creates the tween with the TweenInfo and what properties you want to change
                        Tween:Play() -- Plays the tween
                        wait(0.2)
                        PageDropdownScrollingFrame.Active = false
                        PageDropdownScrollingFrame.Visible = false
                    elseif DropdownArrow.Rotation == 180.000 then
                        local TweenService = game:GetService("TweenService")
                        local Object = DropdownArrow -- The object you want to tween.
                        local tweenInfo = TweenInfo.new(
                            0.2, -- The time the tween takes to complete
                            Enum.EasingStyle.Linear, -- The tween style.
                            Enum.EasingDirection.Out, -- EasingDirection
                            .5, -- How many times you want the tween to repeat. If you make it less than 0 it will repeat forever.
                            false, -- Reverse?
                            0 -- Delay
                        )
                        local Tween = TweenService:Create(Object, tweenInfo, {Rotation = 90}) -- Creates the tween with the TweenInfo and what properties you want to change
                        Tween:Play() -- Plays the tween
                        wait(0.2)
                        PageDropdownScrollingFrame.Active = true
                        PageDropdownScrollingFrame.Visible = true
                    end 
                end
            end
            DropdownMainButton.InputBegan:Connect(onInputBegan)

            
            local ChangeFunction = callback
            local function CreateContents(List)
                for i,v in ipairs(List) do
                    local DropdownTextButton = Instance.new("TextButton")
                    local DropdownTextButtonCorner = Instance.new("UICorner")

                    DropdownTextButton.Name = v
                    DropdownTextButton.Parent = PageDropdownScrollingFrame
                    DropdownTextButton.BackgroundColor3 = Color3.fromRGB(35, 35, 35)
                    DropdownTextButton.Size = UDim2.new(0, 310, 0, 25)
                    DropdownTextButton.Font = Enum.Font.Cartoon
                    DropdownTextButton.Text = v
                    DropdownTextButton.TextColor3 = Color3.fromRGB(255, 255, 255)
                    DropdownTextButton.TextSize = 15.000
                    DropdownTextButton.TextStrokeTransparency = 0.900
                    DropdownTextButton.TextTransparency = 0.300
                    DropdownTextButton.TextWrapped = true
        
                    DropdownTextButtonCorner.CornerRadius = UDim.new(0, 5)
                    DropdownTextButtonCorner.Name = "DropdownTextButtonCorner"
                    DropdownTextButtonCorner.Parent = DropdownTextButton

                    local function onInputBegan(input, gameProcessed)
                        if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
                            DropdownText.Text = DropdownTextButton.Text
                            coroutine.wrap(ChangeFunction)(DropdownTextButton.Text)
                        end
                    end
                    DropdownTextButton.InputBegan:Connect(onInputBegan)
                end
            end
            
            CreateContents(Contents)

        end

		return PagesHandler

    end

    return TabsHandler

end

------------------------------------------------------------

--return DEVIL_UI_Library_Mobile

------------------------------------------------------------




































local DEVIL_UI_Library_PC = {}

function DEVIL_UI_Library_PC:CreateWindow(GuiName, GameName)
    GuiName = GuiName or "Name"
    GameName = GameName or "Game Name"

    local ScreenGUI = (syn and syn.screengui_gui) or (function() end);
    local ScreenGui = Instance.new("ScreenGui")
    ScreenGUI(ScreenGui)
    local Main = Instance.new("Frame")
    local GameNameFrame = Instance.new("Frame")
    local HubName = Instance.new("TextLabel")
    local Line = Instance.new("Frame")
    local SideBar = Instance.new("Frame")
    local allTabs = Instance.new("ScrollingFrame")
    local TabListLayout = Instance.new("UIListLayout")
    local TabPadding = Instance.new("UIPadding")
    local tabListing = Instance.new("UICorner")
    local allPages = Instance.new("Frame")
    local pagesFolder = Instance.new("Folder")


    ScreenGui.Name = "DEVIL_UI_Lib"
    ScreenGui.Parent = game.CoreGui
    ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
    
    Main.Name = "Main"
    Main.Parent = ScreenGui
    Main.BackgroundColor3 = Color3.fromRGB(40, 40, 40)
    Main.BorderColor3 = Color3.fromRGB(255, 255, 255)
    Main.BorderSizePixel = 2
    Main.Position = UDim2.new(0.5, -250, 0.5, -150)
    Main.Size = UDim2.new(0, 500, 0, 300)
    Main.ZIndex = 999999999
    
    GameNameFrame.Name = "GameNameFrame"
    GameNameFrame.Parent = Main
    GameNameFrame.BackgroundColor3 = Color3.fromRGB(40, 40, 40)
    GameNameFrame.BorderSizePixel = 0
    GameNameFrame.Size = UDim2.new(0, 500, 0, 40)
    GameNameFrame.ZIndex = 999999999
    
    HubName.Name = "HubName"
    HubName.Parent = GameNameFrame
    HubName.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    HubName.BackgroundTransparency = 1.000
    HubName.BorderSizePixel = 0
    HubName.Position = UDim2.new(0.0199999996, 0, 0, 0)
    HubName.Size = UDim2.new(0, 490, 0, 40)
    HubName.Font = Enum.Font.Cartoon
    HubName.Text = GuiName.." : "..GameName
    HubName.TextColor3 = Color3.fromRGB(255, 255, 255)
    HubName.TextSize = 34.000
    HubName.TextWrapped = true
    HubName.TextXAlignment = Enum.TextXAlignment.Left
    
    Line.Name = "Line"
    Line.Parent = GameNameFrame
    Line.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    Line.BorderSizePixel = 0
    Line.Position = UDim2.new(0, 0, 0.824999988, 0)
    Line.Size = UDim2.new(0, 500, 0, 2)
    
    SideBar.Name = "SideBar"
    SideBar.Parent = Main
    SideBar.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    SideBar.BackgroundTransparency = 1.000
    SideBar.BorderSizePixel = 0
    SideBar.Position = UDim2.new(0.0240000002, 0, 0.150000006, 0)
    SideBar.Size = UDim2.new(0, 123, 0, 245)
    
    allTabs.Name = "allTabs"
    allTabs.Parent = SideBar
    allTabs.Active = true
    allTabs.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
    allTabs.BorderSizePixel = 0
    allTabs.Position = UDim2.new(-0.0206504054, 0, -0.0217686985, 0)
    allTabs.Size = UDim2.new(0, 125, 0, 250)
    allTabs.ScrollBarThickness = 5
    allTabs.CanvasSize = UDim2.new(0, 0, 0, 0)
    
    TabListLayout.Name = "TabListLayout"
    TabListLayout.Parent = allTabs
    TabListLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center
    TabListLayout.SortOrder = Enum.SortOrder.LayoutOrder
    TabListLayout.Padding = UDim.new(0, 5)
    
    TabPadding.Name = "TabPadding"
    TabPadding.Parent = allTabs
    TabPadding.PaddingTop = UDim.new(0, 5)
    
    tabListing.CornerRadius = UDim.new(0, 5)
    tabListing.Name = "tabListing"
    tabListing.Parent = allTabs


    local function WCDCV_fake_script()
        local script = Instance.new('Script', Main)

        game:GetService("UserInputService").InputBegan:Connect(function(key)
            if key.KeyCode == Enum.KeyCode[_G.ToggleUI] then
                script.Parent.Parent.Enabled = not script.Parent.Parent.Enabled
            end
        end)
    end
    coroutine.wrap(WCDCV_fake_script)()


    local function LNWIAV_fake_script() -- allTabs.ScrollFrameFixer 
        local script = Instance.new('Script', allTabs)

        spawn(function()
            getgenv().autofixertheui = true
            while autofixertheui do wait()
                pcall(function()
                    local function UpdateCanvasSize(Canvas, Constraint)
                        Canvas.CanvasSize = UDim2.new(0, 0, 0, Constraint.AbsoluteContentSize.Y+15)
                    end
        
                    wait() --//Idk why add wait LMFAO//
        
                    UpdateCanvasSize(script.Parent, script.Parent.TabListLayout)
                end)
            end
        end)
    end
    coroutine.wrap(LNWIAV_fake_script)()



    local TabsHandler = {}

    function TabsHandler:CreateTab(tabname)
        tabname = tabname or "New Tab"
        local tabButton = Instance.new("TextButton")
        local UICorner = Instance.new("UICorner")
        local newPage = Instance.new("ScrollingFrame")
        local newPageCorner = Instance.new("UICorner")
        local NewPageListLayout = Instance.new("UIListLayout")
        local NewPagePadding = Instance.new("UIPadding")

        

        tabButton.Name = "tabButton"
        tabButton.Parent = allTabs
        tabButton.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
        tabButton.BorderSizePixel = 0
        tabButton.Position = UDim2.new(-0.00351155549, 0, 0.134228438, 0)
        tabButton.Size = UDim2.new(0, 120, 0, 25)
        tabButton.Font = Enum.Font.Cartoon
        tabButton.Text = tabname
        tabButton.TextColor3 = Color3.fromRGB(255, 255, 255)
        tabButton.TextSize = 15.000
        tabButton.TextStrokeTransparency = 0.900
        tabButton.TextTransparency = 0.300
        tabButton.TextWrapped = true

        
        UICorner.CornerRadius = UDim.new(0, 5)
        UICorner.Parent = tabButton

        newPage.Name = "newPage"
        newPage.Parent = pagesFolder
        newPage.Active = true
        newPage.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
        newPage.BorderSizePixel = 0
        newPage.Position = UDim2.new(-0.00148277823, 0, -0.0139387827, 0)
        newPage.Size = UDim2.new(0, 348, 0, 250)
        newPage.CanvasPosition = Vector2.new(0, 240)
        newPage.ScrollBarThickness = 5
        newPage.CanvasSize = UDim2.new(0, 0, 0, 0)


        local function DWMOAM_fake_script() -- newPage.ScrollFrameFixer 
            local script = Instance.new('Script', newPage)
    
            spawn(function()
                getgenv().autofixertheui2 = true
                while autofixertheui2 do wait()
                    pcall(function()
                        local function UpdateCanvasSize(Canvas, Constraint)
                            Canvas.CanvasSize = UDim2.new(0, 0, 0, Constraint.AbsoluteContentSize.Y+10)
                        end
            
                        wait() --//Idk why add wait LMFAO//
            
                        UpdateCanvasSize(script.Parent, script.Parent.NewPageListLayout)
                    end)
                end
            end)
        end
        coroutine.wrap(DWMOAM_fake_script)()


        newPageCorner.CornerRadius = UDim.new(0, 5)
        newPageCorner.Name = "newPageCorner"
        newPageCorner.Parent = newPage

        
        NewPageListLayout.Name = "NewPageListLayout"
        NewPageListLayout.Parent = newPage
        NewPageListLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center
        NewPageListLayout.SortOrder = Enum.SortOrder.LayoutOrder
        NewPageListLayout.Padding = UDim.new(0, 5)

    
        NewPagePadding.Name = "NewPagePadding"
        NewPagePadding.Parent = newPage
        NewPagePadding.PaddingTop = UDim.new(0, 5)
    

        allPages.Name = "allPages"
        allPages.Parent = Main
        allPages.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
        allPages.BackgroundTransparency = 1.000
        allPages.BorderSizePixel = 0
        allPages.Position = UDim2.new(0.282000005, 0, 0.146666661, 0)
        allPages.Size = UDim2.new(0, 350, 0, 245)


        pagesFolder.Name = "pagesFolder"
        pagesFolder.Parent = allPages


        for i,v in next, pagesFolder:GetChildren() do -- We get all the pages that we added
            v.Visible = false	-- then we make them invisible 
        end 
        local function onInputBegan(input, gameProcessed)
            if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
                for i,v in next, pagesFolder:GetChildren() do -- We get all the pages that we added
                    v.Visible = false	-- then we make them invisible 
                end 
                newPage.Visible = true	-- We make current page visible but not others
                
                --Animations Below  -- Optional
                for i,v in next, allTabs:GetChildren() do	-- We get all the elements inside the frame
                    if v:IsA("TextButton") then -- We can't animate UIListLayout, so we check if its a TextButton
                        game.TweenService:Create(v, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                            BackgroundColor3 = Color3.fromRGB(30, 30, 30) -- We animate other Tab Buttons and making the current one seem Checked
                        }):Play()
                    end
                end
                game.TweenService:Create(tabButton, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                    BackgroundColor3 = Color3.fromRGB(0, 0, 0) -- We animate other Tab Buttons and making the current one seem Checked
                }):Play()
            end
        end
        tabButton.InputBegan:Connect(onInputBegan)



        local PagesHandler = {}


        function PagesHandler:CreateBlankLabel(TextLabelBlankText)
            TextLabelMainText = TextLabelMainText or ""

            local PageBlanklFrame = Instance.new("Frame")
            local BlankFrame = Instance.new("TextLabel")
            local TextLabelCorner_2 = Instance.new("UICorner")


            PageBlanklFrame.Name = "PageBlanklFrame"
            PageBlanklFrame.Parent = newPage
            PageBlanklFrame.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
            PageBlanklFrame.BackgroundTransparency = 1.000
            PageBlanklFrame.BorderSizePixel = 0
            PageBlanklFrame.Position = UDim2.new(0.0211267602, 0, 0.0235245991, 0)
            PageBlanklFrame.Size = UDim2.new(0, 340, 0, 25)

            BlankFrame.Name = "BlankFrame"
            BlankFrame.Parent = PageBlanklFrame
            BlankFrame.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
            BlankFrame.BackgroundTransparency = 1.000
            BlankFrame.BorderSizePixel = 0
            BlankFrame.Size = UDim2.new(0, 340, 0, 25)
            BlankFrame.Font = Enum.Font.Cartoon
            BlankFrame.Text = TextLabelBlankText
            BlankFrame.TextColor3 = Color3.fromRGB(255, 255, 255)
            BlankFrame.TextSize = 15.000
            BlankFrame.TextStrokeTransparency = 0.900
            BlankFrame.TextTransparency = 0.300

            TextLabelCorner_2.Name = "TextLabelCorner"
            TextLabelCorner_2.Parent = BlankFrame
        end



        function PagesHandler:CreateTextLabel(TextLabelMainText, callback)
            TextLabelMainText = TextLabelMainText or "TextLabel"

            local PageTextLabelFrame = Instance.new("Frame")
            local TextLabel = Instance.new("TextLabel")
            local TextLabelCorner = Instance.new("UICorner")


            PageTextLabelFrame.Name = "PageTextLabelFrame"
            PageTextLabelFrame.Parent = newPage
            PageTextLabelFrame.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
            PageTextLabelFrame.BackgroundTransparency = 1.000
            PageTextLabelFrame.BorderSizePixel = 0
            PageTextLabelFrame.Position = UDim2.new(0.0211267602, 0, 0.0235245991, 0)
            PageTextLabelFrame.Size = UDim2.new(0, 340, 0, 25)
        
            TextLabel.Parent = PageTextLabelFrame
            TextLabel.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
            TextLabel.BorderSizePixel = 0
            TextLabel.Size = UDim2.new(0, 340, 0, 25)
            TextLabel.Font = Enum.Font.Cartoon
            TextLabel.Text = TextLabelMainText
            TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
            TextLabel.TextSize = 15.000
            TextLabel.TextStrokeTransparency = 0.900
            TextLabel.TextTransparency = 0.300
        
            TextLabelCorner.Name = "TextLabelCorner"
            TextLabelCorner.Parent = TextLabel
        end

        function PagesHandler:CreateSection(SectionMainText)
            SectionMainText = SectionMainText or "Section Text"

            local PageSectionFrame = Instance.new("Frame")
            local SectionText = Instance.new("TextLabel")
            local SectionCorner = Instance.new("UICorner")


            PageSectionFrame.Name = "PageSectionFrame"
            PageSectionFrame.Parent = newPage
            PageSectionFrame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            PageSectionFrame.BackgroundTransparency = 1.000
            PageSectionFrame.Position = UDim2.new(0.0211267602, 0, 0.5, 0)
            PageSectionFrame.Size = UDim2.new(0, 340, 0, 60)
        
            SectionText.Name = "SectionText"
            SectionText.Parent = PageSectionFrame
            SectionText.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
            SectionText.Position = UDim2.new(-0.00294117653, 0, 0.277777761, 0)
            SectionText.Size = UDim2.new(0, 340, 0, 25)
            SectionText.Font = Enum.Font.Cartoon
            SectionText.Text = SectionMainText
            SectionText.TextColor3 = Color3.fromRGB(255, 255, 255)
            SectionText.TextSize = 18.000
            SectionText.TextStrokeTransparency = 0.900
            SectionText.TextTransparency = 0.300
            SectionText.TextWrapped = true
        
            SectionCorner.Name = "SectionCorner"
            SectionCorner.Parent = SectionText
        end


        function PagesHandler:CreateButton(ButtonText, callback)
			ButtonText = ButtonText or "Text Button"
			callback = callback or function() end	

            local PageButtonFrame = Instance.new("Frame")
            local PageButton = Instance.new("TextButton")
            local PageButtonCorner = Instance.new("UICorner")


            PageButtonFrame.Name = "PageButtonFrame"
            PageButtonFrame.Parent = newPage
            PageButtonFrame.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
            PageButtonFrame.BackgroundTransparency = 1.000
            PageButtonFrame.BorderSizePixel = 0
            PageButtonFrame.Position = UDim2.new(0.0211267602, 0, 0.0235245991, 0)
            PageButtonFrame.Size = UDim2.new(0, 340, 0, 25)
        
        
            PageButton.Name = "PageButton"
            PageButton.Parent = PageButtonFrame
            PageButton.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
            PageButton.BorderSizePixel = 0
            PageButton.Position = UDim2.new(-0.00164741068, 0, 0.00867309608, 0)
            PageButton.Size = UDim2.new(0, 340, 0, 25)
            PageButton.Font = Enum.Font.Cartoon
            PageButton.Text = ButtonText
            PageButton.TextColor3 = Color3.fromRGB(255, 255, 255)
            PageButton.TextSize = 15.000
            PageButton.TextStrokeTransparency = 0.900
            PageButton.TextTransparency = 0.300
            PageButton.TextWrapped = true
        
            PageButtonCorner.Name = "PageButtonCorner"
            PageButtonCorner.Parent = PageButton


            local function onInputBegan(input, gameProcessed)
                if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
                    callback()
                end
            end
            PageButton.InputBegan:Connect(onInputBegan)

        end

        function PagesHandler:CreateToggle(ToggleMainText, callback)
            ToggleMainText = ToggleMainText or "Toggle Text"
            callback = callback or function() end
        
            local PageToggleFrame = Instance.new("Frame")
            local ToggleText = Instance.new("TextLabel")
            local ToggleButton = Instance.new("TextButton")
            local ToggleButtonCorner = Instance.new("UICorner")
            local ToggleFrameCorner = Instance.new("UICorner")
            
            PageToggleFrame.Name = "PageToggleFrame"
            PageToggleFrame.Parent = newPage
            PageToggleFrame.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
            PageToggleFrame.BorderSizePixel = 0
            PageToggleFrame.Position = UDim2.new(0.0211267602, 0, 0.0235245991, 0)
            PageToggleFrame.Size = UDim2.new(0, 340, 0, 25)

            ToggleText.Name = "ToggleText"
            ToggleText.Parent = PageToggleFrame
            ToggleText.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            ToggleText.BackgroundTransparency = 1.000
            ToggleText.BorderSizePixel = 0
            ToggleText.Position = UDim2.new(0.0294117648, 0, 0, 0)
            ToggleText.Size = UDim2.new(0, 300, 0, 25)
            ToggleText.Font = Enum.Font.Cartoon
            ToggleText.Text = ToggleMainText
            ToggleText.TextColor3 = Color3.fromRGB(255, 255, 255)
            ToggleText.TextSize = 15.000
            ToggleText.TextStrokeTransparency = 0.900
            ToggleText.TextTransparency = 0.300
            ToggleText.TextXAlignment = Enum.TextXAlignment.Left

            ToggleButton.Name = "ToggleButton"
            ToggleButton.Parent = PageToggleFrame
            ToggleButton.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
            ToggleButton.Position = UDim2.new(0.911764681, 0, 0.0799999982, 0)
            ToggleButton.Size = UDim2.new(0, 20, 0, 20)
            ToggleButton.Font = Enum.Font.SourceSans
            ToggleButton.Text = ""
            ToggleButton.TextColor3 = Color3.fromRGB(255, 255, 255)
            ToggleButton.TextSize = 15.000

            ToggleButtonCorner.CornerRadius = UDim.new(0, 20)
            ToggleButtonCorner.Name = "ToggleButtonCorner"
            ToggleButtonCorner.Parent = ToggleButton

            ToggleFrameCorner.Name = "ToggleFrameCorner"
            ToggleFrameCorner.Parent = PageToggleFrame
            

            local function onInputBegan(input, gameProcessed)
                if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
                    tog = not tog
				    callback(tog) -- Callbacks whenever we toggle
                    if tog then 
                        game.TweenService:Create(ToggleButton, TweenInfo.new(0.15, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                            BackgroundColor3 = Color3.fromRGB(0, 0, 0)
                        }):Play()
                        --- We put our animation here when the toggle is on
                    else
                        game.TweenService:Create(ToggleButton, TweenInfo.new(0.15, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                            BackgroundColor3 = Color3.fromRGB(60, 60, 60)
                        }):Play()
                        ---We Put our animation here when the toggle is off
                    end
                end
            end
            ToggleButton.InputBegan:Connect(onInputBegan)

            
        end



        function PagesHandler:CreateSlider(SliderMainText, options , callback)
            SliderMainText = SliderMainText or "Slider Text"
            callback = callback or function() end	


            local PageSliderFrame = Instance.new("Frame")
            local SliderFrameCorner = Instance.new("UICorner")
            local SiderMainTextButton = Instance.new("TextButton")
            local SliderFrameCorner_2 = Instance.new("UICorner")
            local SlidingBar = Instance.new("Frame")
            local SlidingBarCorner = Instance.new("UICorner")
            local MainSlidingBar = Instance.new("Frame")
            local MainSlidingBarCorner = Instance.new("UICorner")
            local SliderText = Instance.new("TextLabel")
            local AmountLabelFrame = Instance.new("Frame")
            local AmountLabel = Instance.new("TextLabel")
            local AmountLabelFrameCorner = Instance.new("UICorner")


            PageSliderFrame.Name = "PageSliderFrame"
            PageSliderFrame.Parent = newPage
            PageSliderFrame.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
            PageSliderFrame.BorderSizePixel = 0
            PageSliderFrame.Position = UDim2.new(0.0211267602, 0, 0.027777778, 0)
            PageSliderFrame.Size = UDim2.new(0, 340, 0, 45)
    
            SliderFrameCorner.Name = "SliderFrameCorner"
            SliderFrameCorner.Parent = PageSliderFrame
    
            SiderMainTextButton.Name = "SiderMainTextButton"
            SiderMainTextButton.Parent = PageSliderFrame
            SiderMainTextButton.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
            SiderMainTextButton.BackgroundTransparency = 0.500
            SiderMainTextButton.Position = UDim2.new(0.0260000005, 0, 0.600000024, -5)
            SiderMainTextButton.Size = UDim2.new(0, 320, 0, 20)
            SiderMainTextButton.Font = Enum.Font.SourceSans
            SiderMainTextButton.Text = ""
            SiderMainTextButton.TextColor3 = Color3.fromRGB(0, 0, 0)
            SiderMainTextButton.TextSize = 14.000
            SiderMainTextButton.TextTransparency = 1.000
    
            SliderFrameCorner_2.Name = "SliderFrameCorner"
            SliderFrameCorner_2.Parent = SiderMainTextButton
    
            SlidingBar.Name = "SlidingBar"
            SlidingBar.Parent = SiderMainTextButton
            SlidingBar.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
            SlidingBar.Position = UDim2.new(0.015625, 0, 0.150000006, 0)
            SlidingBar.Size = UDim2.new(0, 310, 0, 13)
    
            SlidingBarCorner.Name = "SlidingBarCorner"
            SlidingBarCorner.Parent = SlidingBar
    
            MainSlidingBar.Name = "MainSlidingBar"
            MainSlidingBar.Parent = SlidingBar
            MainSlidingBar.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
            MainSlidingBar.Position = UDim2.new(-0.00050403201, 0, -0.00384615362, 0)
            MainSlidingBar.Size = UDim2.new(0, 155, 0, 13)
    
            MainSlidingBarCorner.Name = "MainSlidingBarCorner"
            MainSlidingBarCorner.Parent = MainSlidingBar
    
            SliderText.Name = "SliderText"
            SliderText.Parent = PageSliderFrame
            SliderText.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            SliderText.BackgroundTransparency = 1.000
            SliderText.BorderColor3 = Color3.fromRGB(27, 42, 53)
            SliderText.BorderSizePixel = 0
            SliderText.Position = UDim2.new(0, 8, 0, 3)
            SliderText.Size = UDim2.new(0, 247, 0, 19)
            SliderText.Font = Enum.Font.Cartoon
            SliderText.Text = SliderMainText
            SliderText.TextColor3 = Color3.fromRGB(255, 255, 255)
            SliderText.TextSize = 14.000
            SliderText.TextStrokeTransparency = 0.900
            SliderText.TextTransparency = 0.300
            SliderText.TextWrapped = true
            SliderText.TextXAlignment = Enum.TextXAlignment.Left
    
            AmountLabelFrame.Name = "AmountLabelFrame"
            AmountLabelFrame.Parent = PageSliderFrame
            AmountLabelFrame.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
            AmountLabelFrame.Position = UDim2.new(0.754999995, 0, 0, 3)
            AmountLabelFrame.Size = UDim2.new(0, 80, 0, 15)
    
            AmountLabel.Name = "AmountLabel"
            AmountLabel.Parent = AmountLabelFrame
            AmountLabel.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
            AmountLabel.BackgroundTransparency = 1.000
            AmountLabel.Position = UDim2.new(0, 0, -0.200000003, 2)
            AmountLabel.Size = UDim2.new(0, 75, 0, 15)
            AmountLabel.Font = Enum.Font.SourceSans
            AmountLabel.Text = "50"
            AmountLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
            AmountLabel.TextSize = 15.000
            AmountLabel.TextStrokeTransparency = 0.900
            AmountLabel.TextTransparency = 0.300
            AmountLabel.TextXAlignment = Enum.TextXAlignment.Right
    
            AmountLabelFrameCorner.Name = "AmountLabelFrameCorner"
            AmountLabelFrameCorner.Parent = AmountLabelFrame


            local SMTB = SiderMainTextButton
            local hold = false
            local MSbar = SMTB.SlidingBar.MainSlidingBar
            local amtBox = SMTB.Parent.AmountLabelFrame.AmountLabel
            local Min = options.Min
            local Max = options.Max
            local Default = options.Default or options.Default

            local plr = game.Players.LocalPlayer
            local ms = plr:GetMouse()
            local rlpos
            local rlsiz
            local ap = Vector2.new(SMTB.AbsolutePosition.X, SMTB.AbsolutePosition.Y)
            local as = Vector2.new(SMTB.AbsoluteSize.X, SMTB.AbsoluteSize.Y)

            amtBox.Text = tostring(Default)
            MSbar.Size = UDim2.new(0, (310/Max)*Default, 0, 13)
            

            local function onInputBegan(input, gameProcessed)
                if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
                    hold = true
                end
            end
            SMTB.InputBegan:Connect(onInputBegan)

            game:GetService('UserInputService').InputEnded:Connect(function(input)
                if  input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch  then
                    hold = false
                end
            end)

            game:GetService('RunService').RenderStepped:Connect(function()
                if hold then
                    ap = Vector2.new(SMTB.AbsolutePosition.X, SMTB.AbsolutePosition.Y)
                    as = Vector2.new(SMTB.AbsoluteSize.X, SMTB.AbsoluteSize.Y)

                    rlpos = (ms.X-ap.X)
                    rlsiz = (ms.X-ap.X)
                    local result = math.floor(Max * (rlsiz / 310))
                    if rlpos > 310 then
                        result = Max
                    elseif rlpos < 0 then
                        result = 0
                    end

                    if rlsiz <= 310 and rlsiz >= 0 then
                        amtBox.Text = tostring(result)
                        MSbar.Size = UDim2.new(0, rlsiz, 0, 13)
                        MSbar.Visible = true
                        callback(result)
                    end
                    if rlsiz <= 0 then
                        amtBox.Text = tostring(Min)
                        MSbar.Size = UDim2.new(0, 0, 0, 13)
                        MSbar.Visible = false
                        callback(Min)
                    end
                    if rlsiz >= 310 then
                        amtBox.Text = tostring(Max)
                        MSbar.Size = UDim2.new(0, 310, 0, 13)
                        MSbar.Visible = true
                        callback(Max)
                    end
                    
                end
            end)

        end


	function PagesHandler:CreateDropdown(DropdownMainText, Contents, callback)
	    DropdownMainText = DropdownMainText or "Dropdown Text"
	    callback = callback or function() end	

	    local PageDropdownFrame = Instance.new("Frame")
	    local DropdownText = Instance.new("TextLabel")
	    local DropdownFrameCorner = Instance.new("UICorner")
	    local DropdownArrow = Instance.new("ImageButton")
	    local DropdownMainButton = Instance.new("TextButton")
	    local PageDropdownScrollingFrame = Instance.new("ScrollingFrame")
	    local DropdownTextButton = Instance.new("TextButton")
	    local DropdownTextButtonCorner = Instance.new("UICorner")
	    local DropdownScrollCorner = Instance.new("UICorner")
	    local DropdownScrollListLayout = Instance.new("UIListLayout")
	    local DropdownScrollPadding = Instance.new("UIPadding")


	    PageDropdownFrame.Name = "PageDropdownFrame"
	    PageDropdownFrame.Parent = newPage
	    PageDropdownFrame.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
	    PageDropdownFrame.BorderSizePixel = 0
	    PageDropdownFrame.Position = UDim2.new(0.0211267602, 0, 0.0235245991, 0)
	    PageDropdownFrame.Size = UDim2.new(0, 340, 0, 25)

	    DropdownText.Name = "DropdownText"
	    DropdownText.Parent = PageDropdownFrame
	    DropdownText.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	    DropdownText.BackgroundTransparency = 1.000
	    DropdownText.BorderSizePixel = 0
	    DropdownText.Position = UDim2.new(0.0294117648, 0, 0, 0)
	    DropdownText.Size = UDim2.new(0, 300, 0, 25)
	    DropdownText.Font = Enum.Font.Cartoon
	    DropdownText.Text = "Dropdown"
	    DropdownText.TextColor3 = Color3.fromRGB(255, 255, 255)
	    DropdownText.TextSize = 15.000
	    DropdownText.TextStrokeTransparency = 0.900
	    DropdownText.TextTransparency = 0.300
	    DropdownText.TextWrapped = true
	    DropdownText.TextXAlignment = Enum.TextXAlignment.Left

	    DropdownFrameCorner.Name = "DropdownFrameCorner"
	    DropdownFrameCorner.Parent = PageDropdownFrame

	    DropdownArrow.Name = "DropdownArrow"
	    DropdownArrow.Parent = PageDropdownFrame
	    DropdownArrow.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	    DropdownArrow.BackgroundTransparency = 1.000
	    DropdownArrow.Position = UDim2.new(0.925000012, 0, 0.0799999982, 0)
	    DropdownArrow.Rotation = 180.000
	    DropdownArrow.Size = UDim2.new(0, 20, 0, 20)
	    DropdownArrow.Image = "http://www.roblox.com/asset/?id=71659683"

	    DropdownMainButton.Name = "DropdownMainButton"
	    DropdownMainButton.Parent = PageDropdownFrame
	    DropdownMainButton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	    DropdownMainButton.BackgroundTransparency = 1.000
	    DropdownMainButton.BorderSizePixel = 0
	    DropdownMainButton.Size = UDim2.new(0, 339, 0, 25)
	    DropdownMainButton.Font = Enum.Font.SourceSans
	    DropdownMainButton.Text = ""
	    DropdownMainButton.TextColor3 = Color3.fromRGB(0, 0, 0)
	    DropdownMainButton.TextSize = 14.000

	    PageDropdownScrollingFrame.Name = "PageDropdownScrollingFrame"
	    PageDropdownScrollingFrame.Parent = newPage
	    PageDropdownScrollingFrame.Active = true
	    PageDropdownScrollingFrame.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
	    PageDropdownScrollingFrame.BorderSizePixel = 0
	    PageDropdownScrollingFrame.Position = UDim2.new(0.0633802786, 0, 0.156156242, 0)
	    PageDropdownScrollingFrame.Size = UDim2.new(0, 340, 0, 155)
	    PageDropdownScrollingFrame.CanvasSize = UDim2.new(0, 0, 0, 0)
	    PageDropdownScrollingFrame.ScrollBarThickness = 5

	    DropdownTextButton.Name = "DropdownTextButton"
	    DropdownTextButton.Parent = PageDropdownScrollingFrame
	    DropdownTextButton.BackgroundColor3 = Color3.fromRGB(35, 35, 35)
	    DropdownTextButton.Size = UDim2.new(0, 310, 0, 25)
	    DropdownTextButton.Font = Enum.Font.Cartoon
	    DropdownTextButton.Text = DropdownMainText
	    DropdownTextButton.TextColor3 = Color3.fromRGB(255, 255, 255)
	    DropdownTextButton.TextSize = 15.000
	    DropdownTextButton.TextStrokeTransparency = 0.900
	    DropdownTextButton.TextTransparency = 0.300
	    DropdownTextButton.TextWrapped = true

	    DropdownTextButtonCorner.CornerRadius = UDim.new(0, 5)
	    DropdownTextButtonCorner.Name = "DropdownTextButtonCorner"
	    DropdownTextButtonCorner.Parent = DropdownTextButton

	    DropdownScrollCorner.CornerRadius = UDim.new(0, 5)
	    DropdownScrollCorner.Name = "DropdownScrollCorner"
	    DropdownScrollCorner.Parent = PageDropdownScrollingFrame

	    DropdownScrollListLayout.Name = "DropdownScrollListLayout"
	    DropdownScrollListLayout.Parent = PageDropdownScrollingFrame
	    DropdownScrollListLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center
	    DropdownScrollListLayout.SortOrder = Enum.SortOrder.LayoutOrder
	    DropdownScrollListLayout.Padding = UDim.new(0, 5)

	    DropdownScrollPadding.Name = "DropdownScrollPadding"
	    DropdownScrollPadding.Parent = PageDropdownScrollingFrame
	    DropdownScrollPadding.PaddingTop = UDim.new(0, 5)


	    PageDropdownScrollingFrame.Active = false
	    PageDropdownScrollingFrame.Visible = false

	    local function TEGYQ_fake_script() -- PageDropdownScrollingFrame.DropdownScrollFixer 
		local script = Instance.new('Script', PageDropdownScrollingFrame)

		spawn(function()
		    getgenv().autofixertheui = true
		    while autofixertheui do wait()
			pcall(function()
			    local function UpdateCanvasSize(Canvas, Constraint)
				Canvas.CanvasSize = UDim2.new(0, 0, 0, Constraint.AbsoluteContentSize.Y+15)
			    end

			    wait() --//Idk why add wait LMFAO//

			    UpdateCanvasSize(script.Parent, script.Parent.DropdownScrollListLayout)
			end)
		    end
		end)
	    end
	    coroutine.wrap(TEGYQ_fake_script)()


            local function onInputBegan(input, gameProcessed)
                if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
                    if DropdownArrow.Rotation == 90 then
                        local TweenService = game:GetService("TweenService")
                        local Object = DropdownArrow -- The object you want to tween.
                        local tweenInfo = TweenInfo.new(
                            0.2, -- The time the tween takes to complete
                            Enum.EasingStyle.Linear, -- The tween style.
                            Enum.EasingDirection.Out, -- EasingDirection
                            0.5, -- How many times you want the tween to repeat. If you make it less than 0 it will repeat forever.
                            false, -- Reverse?
                            0 -- Delay
                        )
                        local Tween = TweenService:Create(Object, tweenInfo, {Rotation = 180}) -- Creates the tween with the TweenInfo and what properties you want to change
                        Tween:Play() -- Plays the tween
                        wait(0.2)
                        PageDropdownScrollingFrame.Active = false
                        PageDropdownScrollingFrame.Visible = false
                    elseif DropdownArrow.Rotation == 180.000 then
                        local TweenService = game:GetService("TweenService")
                        local Object = DropdownArrow -- The object you want to tween.
                        local tweenInfo = TweenInfo.new(
                            0.2, -- The time the tween takes to complete
                            Enum.EasingStyle.Linear, -- The tween style.
                            Enum.EasingDirection.Out, -- EasingDirection
                            .5, -- How many times you want the tween to repeat. If you make it less than 0 it will repeat forever.
                            false, -- Reverse?
                            0 -- Delay
                        )
                        local Tween = TweenService:Create(Object, tweenInfo, {Rotation = 90}) -- Creates the tween with the TweenInfo and what properties you want to change
                        Tween:Play() -- Plays the tween
                        wait(0.2)
                        PageDropdownScrollingFrame.Active = true
                        PageDropdownScrollingFrame.Visible = true
                    end 
                end
            end
            DropdownMainButton.InputBegan:Connect(onInputBegan)

            
            local ChangeFunction = callback
            local function CreateContents(List)
                for i,v in ipairs(List) do
                    local DropdownTextButton = Instance.new("TextButton")
                    local DropdownTextButtonCorner = Instance.new("UICorner")

                    DropdownTextButton.Name = v
                    DropdownTextButton.Parent = PageDropdownScrollingFrame
                    DropdownTextButton.BackgroundColor3 = Color3.fromRGB(35, 35, 35)
                    DropdownTextButton.Size = UDim2.new(0, 310, 0, 25)
                    DropdownTextButton.Font = Enum.Font.Cartoon
                    DropdownTextButton.Text = v
                    DropdownTextButton.TextColor3 = Color3.fromRGB(255, 255, 255)
                    DropdownTextButton.TextSize = 15.000
                    DropdownTextButton.TextStrokeTransparency = 0.900
                    DropdownTextButton.TextTransparency = 0.300
                    DropdownTextButton.TextWrapped = true
        
                    DropdownTextButtonCorner.CornerRadius = UDim.new(0, 5)
                    DropdownTextButtonCorner.Name = "DropdownTextButtonCorner"
                    DropdownTextButtonCorner.Parent = DropdownTextButton

                    local function onInputBegan(input, gameProcessed)
                        if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
                            DropdownText.Text = DropdownTextButton.Text
                            coroutine.wrap(ChangeFunction)(DropdownTextButton.Text)
                        end
                    end
                    DropdownTextButton.InputBegan:Connect(onInputBegan)
                end
            end
            
            CreateContents(Contents)
        end






        -- Scripts:

        local function QVUFO_fake_script() -- Main.DraggableScript 
            local script = Instance.new('Script', Main)

            --[[
                    
                Works on mobile to 🥱
                If this dont work then just throw you pc/mobile retard 😂
            
            ]]
            
            
            
            local UserInputService = game:GetService("UserInputService")
            
            local gui = script.Parent
            
            local dragging
            local dragInput
            local dragStart
            local startPos
            
            local function update(input)
                local delta = input.Position - dragStart
                gui.Position = UDim2.new(startPos.X.Scale, startPos.X.Offset + delta.X, startPos.Y.Scale, startPos.Y.Offset + delta.Y)
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
        coroutine.wrap(QVUFO_fake_script)()
        local function FAIHHBB_fake_script() -- Line.Script 
            local script = Instance.new('Script', Line)

            --[[local fakename = script.Parent
            local top = 100
            while true do
                wait()
                for i = 1,top,1 do
                    fakename.BackgroundColor3 = Color3.new(i/top,0/top,0/top)
                    wait()
                end
                for i = 1,top,1 do
                    fakename.BackgroundColor3 = Color3.new(top/top,i/top,0/top)
                    wait()
                end
                for i = 1,top,1 do
                    fakename.BackgroundColor3 = Color3.new(top/top,top/top,i/top)
                    wait()
                end
                for i = top,1,-1 do
                    fakename.BackgroundColor3 = Color3.new(i/top,top/top,top/top)
                    wait()
                end
                for i = top,1,-1 do
                    fakename.BackgroundColor3 = Color3.new(0/top,i/top,top/top)
                    wait()
                end
                for i = top,1,-1 do
                    fakename.BackgroundColor3 = Color3.new(0/top,0/top,i/top)
                    wait()
                end
            end
            ]]
            spawn(function()
                while wait() do
                    pcall(function()
                        local r = (math.sin(workspace.DistributedGameTime/2)/2)+0.5
                        local g = (math.sin(workspace.DistributedGameTime)/2)+0.5
                        local b = (math.sin(workspace.DistributedGameTime*1.5)/2)+0.5
                        local color = Color3.new(r, g, b)
                        script.Parent.BackgroundColor3 = color
                    end)
                end
            end)
        end
        coroutine.wrap(FAIHHBB_fake_script)()
        
        

        local function CAKBVSK_fake_script() -- Main.Script 
            local script = Instance.new('Script', Main)

            --[[local fakename = script.Parent
            local top = 100
            while true do
                wait()
                for i = 1,top,1 do
                    fakename.BorderColor3 = Color3.new(i/top,0/top,0/top)
                    wait()
                end
                for i = 1,top,1 do
                    fakename.BorderColor3 = Color3.new(top/top,i/top,0/top)
                    wait()
                end
                for i = 1,top,1 do
                    fakename.BorderColor3 = Color3.new(top/top,top/top,i/top)
                    wait()
                end
                for i = top,1,-1 do
                    fakename.BorderColor3 = Color3.new(i/top,top/top,top/top)
                    wait()
                end
                for i = top,1,-1 do
                    fakename.BorderColor3 = Color3.new(0/top,i/top,top/top)
                    wait()
                end
                for i = top,1,-1 do
                    fakename.BorderColor3 = Color3.new(0/top,0/top,i/top)
                    wait()
                end
            end]]
            
            spawn(function()
                while wait() do
                    pcall(function()
                        local r = (math.sin(workspace.DistributedGameTime/2)/2)+0.5
                        local g = (math.sin(workspace.DistributedGameTime)/2)+0.5
                        local b = (math.sin(workspace.DistributedGameTime*1.5)/2)+0.5
                        local color = Color3.new(r, g, b)
                        script.Parent.BorderColor3 = color
                    end)
                end
            end)
        end
        coroutine.wrap(CAKBVSK_fake_script)()

        return PagesHandler

    end

    return TabsHandler

end

--return DEVIL_UI_Library_PC



local UserInputService = game:GetService("UserInputService")
if UserInputService.TouchEnabled and not UserInputService.KeyboardEnabled and not UserInputService.MouseEnabled then
    return(DEVIL_UI_Library_Mobile)
elseif not UserInputService.TouchEnabled and UserInputService.KeyboardEnabled and UserInputService.MouseEnabled then
    return(DEVIL_UI_Library_PC)
end

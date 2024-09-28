--[[
 /$$$$$$$                      /$$                 /$$$$$$$$                               
| $$__  $$                    |__/                |__  $$__/                               
| $$  \ $$  /$$$$$$   /$$$$$$$ /$$  /$$$$$$          | $$  /$$$$$$   /$$$$$$  /$$$$$$/$$$$ 
| $$$$$$$/ /$$__  $$ /$$_____/| $$ /$$__  $$         | $$ /$$__  $$ |____  $$| $$_  $$_  $$
| $$__  $$| $$  \ $$|  $$$$$$ | $$| $$$$$$$$         | $$| $$$$$$$$  /$$$$$$$| $$ \ $$ \ $$
| $$  \ $$| $$  | $$ \____  $$| $$| $$_____/         | $$| $$_____/ /$$__  $$| $$ | $$ | $$
| $$  | $$|  $$$$$$/ /$$$$$$$/| $$|  $$$$$$$         | $$|  $$$$$$$|  $$$$$$$| $$ | $$ | $$
|__/  |__/ \______/ |_______/ |__/ \_______/         |__/ \_______/ \_______/|__/ |__/ |__/     

[+] Rosie Team Cảm Ơn Bạn Đã Tin Tưởng Và Sử Dụng Dịch Vụ Của Chúng Tôi, Nếu Thấy Hữu Ít Hãy Chia Sẻ Cho Bạn Bè Của Bạn !!
[+] Không Được Share Hay Crack Mã Nguồn Này Cho Ai! Nếu Không Bạn Sẽ Bị Ban IP Khỏi Website Vĩnh Viễn!
[+] Chúng Tôi Không Nhận Hỗ Trợ Những Mã Nguồn Miễn Phí, Xin Đừng Bảo Vì Sao. Tạo Ticket Hỗ Trợ Của Website Tại: https://rosieteam.net/dash/ticket
[+]  Nếu Bạn Edit Source Và Up Web Share Nhớ Obfuscate Script. Nếu Bạn Có Tiền Thì Sử Dụng: Lura.Ph, Luarmor.Net | Nếu Bạn Không Có Tiền Thì Dùng: luaobfuscate.com, MoonSec, 77Fuscate,... Nhé!
]]

do local GUI = game.CoreGui:FindFirstChild("THUNDERZHUB") if GUI then GUI:Destroy() end end
do local TOGGLE = game.CoreGui:FindFirstChild("ImageButton") if TOGGLE then TOGGLE:Destroy() end end

---[Notify Má»›i LÃ m:))]
local Notif = {}

local CoreGUI = game:GetService("CoreGui")
local TS = game:GetService("TweenService")

local HIDEUI = get_hidden_gui or gethui
if syn and typeof(syn) == "table" and RenderWindow then syn.protect_gui = gethui; end
local function Hide_UI(gui)
    if HIDEUI then
        gui["Parent"] = HIDEUI()
    elseif (not is_sirhurt_closure) and (syn and syn.protect_gui) then
        syn.protect_gui(gui)
        gui["Parent"] = CoreGUI
    elseif CoreGUI:FindFirstChild('RobloxGui') then
        gui["Parent"] = CoreGUI.RobloxGui
    else
        gui["Parent"] = CoreGUI
    end
end

local screen_gui = Instance.new("ScreenGui")
Hide_UI(screen_gui)

local frame = Instance.new("Frame")
frame.AnchorPoint = Vector2.new(0.5, 0.949999988079071)
frame.BackgroundColor3 = Color3.new(1, 1, 1)
frame.BackgroundTransparency = 1
frame.BorderColor3 = Color3.new(0, 0, 0)
frame.BorderSizePixel = 0
frame.Position = UDim2.new(0.5, 0, 0.954999983, 0)
frame.Size = UDim2.new(0, 100, 0, 100)
frame.Visible = true
frame.Parent = screen_gui

local uilist_layout = Instance.new("UIListLayout")
uilist_layout.HorizontalAlignment = Enum.HorizontalAlignment.Center
uilist_layout.SortOrder = Enum.SortOrder.LayoutOrder
uilist_layout.VerticalAlignment = Enum.VerticalAlignment.Bottom
uilist_layout.Parent = frame
	
function Notif.New(text, timee)
    local frame_2 = Instance.new("Frame")
    frame_2.BackgroundColor3 = Color3.new(1, 1, 1)
    frame_2.BorderColor3 = Color3.new(0, 0, 0)
    frame_2.BorderSizePixel = 0
    frame_2.BackgroundTransparency = 1
    frame_2.Size = UDim2.new(0, 100, 0, 0)
    frame_2.Visible = true
    frame_2.Parent = frame
	
    -- Main Notification Frame
    local frame_3 = Instance.new("Frame")
    frame_3.AnchorPoint = Vector2.new(0.5, 1)
    frame_3.AutomaticSize = Enum.AutomaticSize.X
    frame_3.BackgroundColor3 = Color3.new(0.141176, 0.141176, 0.141176)
    frame_3.BackgroundTransparency = 0.20000000298023224
    frame_3.BorderColor3 = Color3.new(0, 0, 0)
    frame_3.Position = UDim2.new(0.5, 0, 1, 60)
    frame_3.Size = UDim2.new(0, 0, 0, 30)
    frame_3.Visible = true
    frame_3.Parent = frame_2

    local uicorner = Instance.new("UICorner")
    uicorner.CornerRadius = UDim.new(0, 6)
    uicorner.Parent = frame_3

    local uipadding = Instance.new("UIPadding")
    uipadding.PaddingBottom = UDim.new(0, 3)
    uipadding.PaddingLeft = UDim.new(0, 3)
    uipadding.PaddingRight = UDim.new(0, 3)
    uipadding.PaddingTop = UDim.new(0, 3)
    uipadding.Parent = frame_3

    local uistroke = Instance.new("UIStroke")
    uistroke.ApplyStrokeMode = Enum.ApplyStrokeMode.Border
    uistroke.Color = Color3.new(0.0313726, 0.0313726, 0.0313726)
    uistroke.Parent = frame_3

    local text_label = Instance.new("TextLabel")
    text_label.Font = Enum.Font.Gotham
    text_label.Text = text
    text_label.TextColor3 = Color3.new(0.784314, 0.784314, 0.784314)
    text_label.TextSize = 14
    text_label.AutomaticSize = Enum.AutomaticSize.X
    text_label.BackgroundColor3 = Color3.new(1, 1, 1)
    text_label.BackgroundTransparency = 1
    text_label.BorderColor3 = Color3.new(0, 0, 0)
    text_label.BorderSizePixel = 0
    text_label.Size = UDim2.new(0, 0, 0, 24)
    text_label.Visible = true
    text_label.Parent = frame_3

    local uipadding_2 = Instance.new("UIPadding")
    uipadding_2.PaddingLeft = UDim.new(0, 5)
    uipadding_2.PaddingRight = UDim.new(0, 30)
    uipadding_2.Parent = text_label

    local text_button = Instance.new("TextButton")
    text_button.Font = Enum.Font.SourceSans
    text_button.Text = ""
    text_button.TextColor3 = Color3.new(0, 0, 0)
    text_button.TextSize = 14
    text_button.AnchorPoint = Vector2.new(1, 0.5)
    text_button.BackgroundColor3 = Color3.new(0, 0, 0)
    text_button.BackgroundTransparency = 1
    text_button.BorderColor3 = Color3.new(0, 0, 0)
    text_button.BorderSizePixel = 0
    text_button.Position = UDim2.new(1, 0, 0.5, 0)
    text_button.Size = UDim2.new(0, 24, 0, 24)
    text_button.Visible = true
    text_button.Parent = frame_3

    local uicorner_2 = Instance.new("UICorner")
    uicorner_2.CornerRadius = UDim.new(0, 5)
    uicorner_2.Parent = text_button

    local image_button = Instance.new("ImageButton")
    image_button.Image = "https://img.chanhtuoi.com/uploads/2023/09/logo-cheems-blox-fruit-dac-biet.jpg"https://img.chanhtuoi.com/uploads/2023/09/logo-cheems-blox-fruit-dac-biet.jpg
    image_button.ImageColor3 = Color3.new(0.784314, 0.784314, 0.784314)
    image_button.ImageRectOffset = Vector2.new(924, 724)
    image_button.ImageRectSize = Vector2.new(36, 36)
    image_button.AnchorPoint = Vector2.new(0.5, 0.5)
    image_button.BackgroundTransparency = 1
    image_button.LayoutOrder = 3
    image_button.Position = UDim2.new(0.5, 0, 0.5, 0)
    image_button.Size = UDim2.new(0, 18, 0, 18)
    image_button.Visible = true
    image_button.ZIndex = 2
    image_button.Parent = text_button

    --Animations
    TS:Create(frame_3, TweenInfo.new(0.2, Enum.EasingStyle.Quint), { Position = UDim2.new(0.5, 0, 1, 0) }):Play()
    TS:Create(frame_2, TweenInfo.new(0.2, Enum.EasingStyle.Quint), { Size = UDim2.new(0, 100, 0, 35) }):Play()

    -- Close Button
    local function close_notif()
        TS:Create(image_button, TweenInfo.new(0.15, Enum.EasingStyle.Quint), { ImageTransparency = 1 }):Play()
        TS:Create(text_button, TweenInfo.new(0.15, Enum.EasingStyle.Quint), { BackgroundTransparency = 1 }):Play()
        TS:Create(text_label, TweenInfo.new(0.15, Enum.EasingStyle.Quint), { TextTransparency = 1 }):Play()
        task.wait(.17)
        TS:Create(frame_3, TweenInfo.new(0.25, Enum.EasingStyle.Quint), { BackgroundTransparency = 1 }):Play()
        TS:Create(uistroke, TweenInfo.new(0.24, Enum.EasingStyle.Quint), { Transparency = 1 }):Play()
        task.wait(.05)
        TS:Create(frame_2, TweenInfo.new(0.2, Enum.EasingStyle.Quint), { Size = UDim2.new(0, 100, 0, 0) }):Play()
        task.wait(.2)
        frame_2:Destroy()
    end
    text_button.MouseEnter:Connect(function()
        TS:Create(text_button, TweenInfo.new(0.25, Enum.EasingStyle.Quint), { BackgroundTransparency = 0.8 }):Play()
        TS:Create(image_button, TweenInfo.new(0.3, Enum.EasingStyle.Quint),
            { ImageColor3 = Color3.new(0.890196, 0.054902, 0.054902) }):Play()
    end)

    text_button.MouseLeave:Connect(function()
        TS:Create(text_button, TweenInfo.new(0.25, Enum.EasingStyle.Quint), { BackgroundTransparency = 1 }):Play()
        TS:Create(image_button, TweenInfo.new(0.3, Enum.EasingStyle.Quint),
            { ImageColor3 = Color3.new(0.784314, 0.784314, 0.784314) }):Play()
    end)

    text_button.MouseButton1Click:Connect(function()
        TS:Create(image_button, TweenInfo.new(0.15, Enum.EasingStyle.Quint), { ImageTransparency = 1 }):Play()
        TS:Create(text_button, TweenInfo.new(0.15, Enum.EasingStyle.Quint), { BackgroundTransparency = 1 }):Play()
        TS:Create(text_label, TweenInfo.new(0.15, Enum.EasingStyle.Quint), { TextTransparency = 1 }):Play()
        task.wait(.17)
        TS:Create(frame_3, TweenInfo.new(0.25, Enum.EasingStyle.Quint), { BackgroundTransparency = 1 }):Play()
        TS:Create(uistroke, TweenInfo.new(0.24, Enum.EasingStyle.Quint), { Transparency = 1 }):Play()
        task.wait(.05)
        TS:Create(frame_2, TweenInfo.new(0.2, Enum.EasingStyle.Quint), { Size = UDim2.new(0, 100, 0, 0) }):Play()
        task.wait(.2)
        frame_2:Destroy()
    end)
    image_button.MouseButton1Click:Connect(close_notif)
    task.delay(tonumber(timee) and timee or 10, close_notif)
end

local ScreenGui1 = Instance.new("ScreenGui")
local ImageButton1 = Instance.new("ImageButton")
local UICorner = Instance.new("UICorner")
local UIGradient = Instance.new("UIGradient")
local UIStroke = Instance.new("UIStroke")
ScreenGui1.Name = "ImageButton"
ScreenGui1.Parent = game.CoreGui
ScreenGui1.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

ImageButton1.Parent = ScreenGui1
ImageButton1.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
ImageButton1.BackgroundTransparency = 1.10
ImageButton1.BorderSizePixel = 0
ImageButton1.Position = UDim2.new(0.120833337, 0, 0.0952890813, 0)
ImageButton1.Size = UDim2.new(0, 70, 0, 70)
ImageButton1.Draggable = true
ImageButton1.Image = "http://www.roblox.com/asset/?id=16373597069"
ImageButton1.MouseButton1Down:connect(function()
  game:GetService("VirtualInputManager"):SendKeyEvent(true,305,false,game)
  game:GetService("VirtualInputManager"):SendKeyEvent(false,305,false,game)
end)

UIGradient.Parent = UIStroke

if game:GetService("CoreGui"):FindFirstChild("AppleHub") then
    game:GetService("CoreGui"):FindFirstChild("AppleHub"):Destroy()
end

repeat wait(1) until game:IsLoaded()
local LocalPlayer = game:GetService("Players").LocalPlayer
local HttpService = game:GetService("HttpService")
local pfp
local user
local tag
local userinfo = {}

pcall(function()
    userinfo = HttpService:JSONDecode(readfile(""));
end)
 
pfp = userinfo["pfp"] or "https://www.roblox.com/headshot-thumbnail/image?userId=".. game.Players.LocalPlayer.UserId .."&width=420&height=420&format=png"
user =  userinfo["user"] or game.Players.LocalPlayer.Name
tag = userinfo["tag"] or tostring(math.random(1,10))

local function SaveInfo()
    userinfo["pfp"] = pfp
    userinfo["user"] = user
    userinfo["tag"] = tag
    writefile("", HttpService:JSONEncode(userinfo));
end


local UserInputService = game:GetService("UserInputService")
local TweenService = game:GetService("TweenService")

local function MakeDraggable(topbarobject, object)
    local Dragging = nil
    local DragInput = nil
    local DragStart = nil
    local StartPosition = nil
    
    local function Update(input)
        local Delta = input.Position - DragStart
        local pos = UDim2.new(StartPosition.X.Scale, StartPosition.X.Offset + Delta.X, StartPosition.Y.Scale, StartPosition.Y.Offset + Delta.Y)
        local Tween = TweenService:Create(object, TweenInfo.new(0.15), {
        Position = pos
        })
        Tween:Play()
    end
    
    topbarobject.InputBegan:Connect(
        function(input)
            if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
                Dragging = true
                DragStart = input.Position
                StartPosition = object.Position
    
                input.Changed:Connect(
                    function()
                        if input.UserInputState == Enum.UserInputState.End then
                            Dragging = false
                        end
                    end
                )
             end
        end
    )
    
    topbarobject.InputChanged:Connect(
        function(input)
            if
                input.UserInputType == Enum.UserInputType.MouseMovement or
                input.UserInputType == Enum.UserInputType.Touch
            then
                DragInput = input
            end
        end
    )
    
    UserInputService.InputChanged:Connect(
        function(input)
            if input == DragInput and Dragging then
                Update(input)
            end
        end
    )
end

local Update = {}
local pfp = "https://www.roblox.com/headshot-thumbnail/image?userId=".. game.Players.LocalPlayer.UserId .."&width=420&height=420&format=png"

function Update:Window(text,logo,keybind)
    local osfunc = {}
    local uihide = false
    local abc = false
    local currentpage = ""
    local keybind = keybind or Enum.KeyCode.RightControl
    local yoo = string.gsub(tostring(keybind),"Enum.KeyCode.","")

    local THUNDERZHUB = Instance.new("ScreenGui")
    THUNDERZHUB.Name = "THUNDERZHUB"
    THUNDERZHUB.Parent = game.CoreGui
    THUNDERZHUB.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

    local Main = Instance.new("Frame")
    Main.Name = "Main"
    Main.Parent = THUNDERZHUB
    Main.ClipsDescendants = true
    Main.AnchorPoint = Vector2.new(0.5,0.5)
    Main.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
    Main.Position = UDim2.new(0.5, 0, 0.5, 0)
    Main.Size = UDim2.new(0, 0, 0, 0)

    Main:TweenSize(UDim2.new(0, 540, 0, 340),"Out","Quad",0.4,true)

    local BtnStroke = Instance.new("UIStroke")

    BtnStroke.Name = "BtnStroke"
    BtnStroke.Parent = Main
    BtnStroke.ApplyStrokeMode = Enum.ApplyStrokeMode.Border
    BtnStroke.Color = Color3.fromRGB(255, 0, 0)
    BtnStroke.LineJoinMode = Enum.LineJoinMode.Round
    BtnStroke.Thickness = 1
    BtnStroke.Transparency = 0
    BtnStroke.Enabled = true
    BtnStroke.Archivable = true

    local MCNR = Instance.new("UICorner")
    MCNR.Name = "MCNR"
    MCNR.Parent = Main

    local Top = Instance.new("Frame")
    Top.Name = "Top"
    Top.Parent = Main
    Top.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
    Top.Size = UDim2.new(0, 556, 0, 30)
    Top.BackgroundTransparency = 1.000
    local TCNR = Instance.new("UICorner")
    TCNR.Name = "TCNR"
    TCNR.Parent = Top
    TCNR.CornerRadius = UDim.new(0,5) 

    local ServerTime = Instance.new("TextLabel")
    ServerTime.Name = "ServerTime"
    ServerTime.Parent = Top
    ServerTime.BackgroundColor3 = Color3.fromRGB(255,255,255)
    ServerTime.BackgroundTransparency = 1.000
    ServerTime.Position = UDim2.new(0.68, 0,0.074, 0)
    ServerTime.Size = UDim2.new(0, 225, 0, 25)
    ServerTime.Font = Enum.Font.GothamSemibold
    ServerTime.Text = ""
    ServerTime.TextSize = 11.000
    ServerTime.TextColor3 = Color3.fromRGB(255,255,255)
    ServerTime.TextXAlignment = Enum.TextXAlignment.Left

    function osfunc:Set(textadd)
        ServerTime.Text = textadd
    end

    local Ping = Instance.new("TextLabel")
    Ping.Name = "Ping"
    Ping.Parent = Top
    Ping.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    Ping.BackgroundTransparency = 1.000
    Ping.Position = UDim2.new(0.28, 0,0.074, 0)
    Ping.Size = UDim2.new(0, 225, 0, 25)
    Ping.Font = Enum.Font.GothamSemibold
    Ping.Text = "ScriptBlox"
    Ping.TextColor3 = Color3.fromRGB(255,255,255)
    Ping.TextSize = 14.000
    Ping.TextXAlignment = Enum.TextXAlignment.Left

    local User = Instance.new("Frame")
    User.Name = "User"
    User.Parent = Top
    User.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    User.BackgroundTransparency = 1.000
    User.Position = UDim2.new(0, 0,0, 25)
    User.Size = UDim2.new(0, 125, 0, 40)
    
    local UserText = Instance.new("TextLabel")
    UserText.Name = "UserText"
    UserText.Parent = User
    UserText.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    UserText.BackgroundTransparency = 1.000
    UserText.Position = UDim2.new(0.3,7 ,0, -18)
    UserText.TextColor3 = Color3.fromRGB(255, 255, 255)
    UserText.Size = UDim2.new(0, 80, 0, 25)
    UserText.Font = Enum.Font.GothamSemibold
    UserText.Text = ","
    UserText.TextScaled = true
    UserText.TextSize = 17.000
    UserText.TextWrapped = true
    UserText.TextXAlignment = Enum.TextXAlignment.Left
    
    local UITextSizeConstraint = Instance.new("UITextSizeConstraint")
    UITextSizeConstraint.Parent = UserText
    UITextSizeConstraint.MaxTextSize = 17

    local UserImage = Instance.new("ImageLabel")
    UserImage.Name = "UserImage"
    UserImage.Parent = User
    UserImage.BackgroundTransparency = 0
    UserImage.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
    UserImage.Position = UDim2.new(0, 10, 0, -15)
    UserImage.Size = UDim2.new(0, 25, 0, 25)
    UserImage.Image = ""
    local UserImageCorner = Instance.new("UICorner")
    UserImageCorner.CornerRadius = UDim.new(0, 100)
    UserImageCorner.Name = "UserImageCorner"
    UserImageCorner.Parent = UserImage


    local Logo = Instance.new("ImageLabel")
	Logo.Name = "Logo"
	Logo.Parent = Main
	Logo.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Logo.BackgroundTransparency = 1.000
	Logo.Position = UDim2.new(0, -5, 0, -5)
	Logo.Size = UDim2.new(0, 135, 0, 135)
	Logo.Image = "rbxassetid://16373597069"
    local Tab = Instance.new("Frame")
    Tab.Name = "Tab"
    Tab.Parent = Main
    Tab.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
    Tab.Position = UDim2.new(0, 5, 0, 135)
    Tab.Size = UDim2.new(0, 0, 0, 0)

    local TabCorner = Instance.new("UIListLayout")
    TabCorner.Name = "TabCorner"
    TabCorner.Parent = Tab
    TabCorner.SortOrder = Enum.SortOrder.LayoutOrder
    TabCorner.Padding = UDim.new(0,15)
    local BtnStroke = Instance.new("UIStroke")
    local ScrollTab = Instance.new("ScrollingFrame")
    local Crner = Instance.new("UICorner")
    ScrollTab.Name = "ScrollTab"
    ScrollTab.Parent = Tab
    ScrollTab.Active = true
    ScrollTab.BackgroundColor3 = Color3.fromRGB(0, 0, 128)
    ScrollTab.BackgroundTransparency = 1.000
    ScrollTab.Size = UDim2.new(0, 133, 0, 203)
    ScrollTab.CanvasSize = UDim2.new(0, 0, 0, 0)
    ScrollTab.ScrollBarThickness = 0

    local PLL = Instance.new("UIListLayout")
    PLL.Name = "PLL"
    PLL.Parent = ScrollTab
    PLL.SortOrder = Enum.SortOrder.LayoutOrder
    PLL.Padding = UDim.new(0, 15)

    local PPD = Instance.new("UIPadding")
    PPD.Name = "PPD"
    PPD.Parent = ScrollTab
    PPD.PaddingLeft = UDim.new(0, 9)
    PPD.PaddingTop = UDim.new(0, 2)
    local BtnStroke = Instance.new("UIStroke")
    local Page = Instance.new("Frame")
    Page.Name = "Page"
    Page.Parent = Main
    Page.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
    Page.Position = UDim2.new(0.255426834, 0, 0.086000003, 0)
    Page.Size = UDim2.new(0, 410, 0, 308)

    local PCNR = Instance.new("UICorner")
    PCNR.Parent = Page
    PCNR.CornerRadius = UDim.new(0,3)

local Page = Instance.new("ImageLabel")
Page.Name = "Page"
Page.Parent = Main
Page.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
Page.BackgroundTransparency = 1.10
Page.Position = UDim2.new(0.265426834, 0, 0.075000003, 0)
Page.Size = UDim2.new(0, 400, 0, 400)
Page.Image = ""

    local MainPage = Instance.new("Frame")
    MainPage.Name = "MainPage"
    MainPage.Parent = Page
    MainPage.ClipsDescendants = true
    MainPage.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    MainPage.BackgroundTransparency = 1.000
    MainPage.Size = UDim2.new(0, 410, 0, 308)

    local PageList = Instance.new("Folder")
    PageList.Name = "PageList"
    PageList.Parent = MainPage

    local UIPageLayout = Instance.new("UIPageLayout")

    UIPageLayout.Parent = PageList
    UIPageLayout.SortOrder = Enum.SortOrder.LayoutOrder
    UIPageLayout.EasingDirection = Enum.EasingDirection.InOut
    UIPageLayout.EasingStyle = Enum.EasingStyle.Quad
    UIPageLayout.FillDirection = Enum.FillDirection.Vertical
    UIPageL

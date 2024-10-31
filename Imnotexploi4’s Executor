local player = game.Players.LocalPlayer
local playerGui = player:WaitForChild("PlayerGui")

-- Function to initialize the GUI
local function initializeGui()
-- Clear previous GUI if exists
if playerGui:FindFirstChild("ExecutorGui") then
playerGui.ExecutorGui:Destroy()
end

local screenGui = Instance.new("ScreenGui")
screenGui.Name = "ExecutorGui"
screenGui.Parent = playerGui

-- Toggle Button
local toggleButton = Instance.new("TextButton", screenGui)
toggleButton.Size = UDim2.new(0.1, 0, 0.1, 0)
toggleButton.Position = UDim2.new(0, 10, 0, 10)
toggleButton.Text = "Toggle GUI"
toggleButton.BackgroundColor3 = Color3.fromRGB(255, 0, 0)
toggleButton.TextScaled = true

-- Executor Frame
local executorFrame = Instance.new("Frame", screenGui)
executorFrame.Size = UDim2.new(0.5, 0, 0.5, 0)
executorFrame.Position = UDim2.new(0.25, 0, 0.25, 0)
executorFrame.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
executorFrame.Visible = true
executorFrame.Active = true
executorFrame.Draggable = true

-- Title Label
local titleLabel = Instance.new("TextLabel", executorFrame)
titleLabel.Size = UDim2.new(1, 0, 0.1, 0)
titleLabel.Position = UDim2.new(0, 0, 0, 0)
titleLabel.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
titleLabel.Text = "Imnotexploi4's Executor"
titleLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
titleLabel.TextScaled = true

-- Pages Frame
local pages = Instance.new("Frame", executorFrame)
pages.Size = UDim2.new(1, 0, 0.1, 0)
pages.Position = UDim2.new(0, 0, 0.1, 0)
pages.BackgroundColor3 = Color3.fromRGB(60, 60, 60)

local page1Button = Instance.new("TextButton", pages)
page1Button.Size = UDim2.new(0.5, 0, 1, 0)
page1Button.Position = UDim2.new(0, 0, 0, 0)
page1Button.Text = "Page 1"
page1Button.BackgroundColor3 = Color3.fromRGB(70, 70, 70)
page1Button.TextScaled = true

local page2Button = Instance.new("TextButton", pages)
page2Button.Size = UDim2.new(0.5, 0, 1, 0)
page2Button.Position = UDim2.new(0.5, 0, 0, 0)
page2Button.Text = "Page 2"page2Button.BackgroundColor3 = Color3.fromRGB(70, 70, 70)
page2Button.TextScaled = true

-- Page 1 Content
local page1 = Instance.new("Frame", executorFrame)
page1.Size = UDim2.new(1, 0, 0.8, 0)
page1.Position = UDim2.new(0, 0, 0.2, 0)
page1.BackgroundColor3 = Color3.fromRGB(50, 50, 50)

local codeBox1 = Instance.new("TextBox", page1)
codeBox1.Size = UDim2.new(0.9, 0, 0.7, 0)
codeBox1.Position = UDim2.new(0.05, 0, 0.05, 0)
codeBox1.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
codeBox1.TextColor3 = Color3.fromRGB(255, 255, 255)
codeBox1.TextScaled = true
codeBox1.Text = "Enter your script here"
codeBox1.ClearTextOnFocus = true
codeBox1.MultiLine = true

local executeButton1 = Instance.new("TextButton", page1)
executeButton1.Size = UDim2.new(0.4, 0, 0.1, 0)
executeButton1.Position = UDim2.new(0.3, 0, 0.8, 0)
executeButton1.Text = "Execute"
executeButton1.BackgroundColor3 = Color3.fromRGB(0, 255, 0)
executeButton1.TextScaled = true

local function executeScript1()
local script = codeBox1.Text
local success, errorMessage = pcall(function()
loadstring(script)()
end)

if not success then
warn("Error executing script:", errorMessage)
else
print("Script executed successfully")
end
end

executeButton1.MouseButton1Click:Connect(executeScript1)

-- Page 2 Content
local page2 = Instance.new("Frame", executorFrame)
page2.Size = UDim2.new(1, 0, 0.8, 0)
page2.Position = UDim2.new(0, 0, 0.2, 0)
page2.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
page2.Visible = false

local codeBox2 = Instance.new("TextBox", page2)
codeBox2.Size = UDim2.new(0.9, 0, 0.7, 0)
codeBox2.Position = UDim2.new(0.05, 0, 0.05, 0)
codeBox2.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
codeBox2.TextColor3 = Color3.fromRGB(255, 255, 255)
codeBox2.TextScaled = true
codeBox2.Text = "Enter your script here"
codeBox2.ClearTextOnFocus = true
codeBox2.MultiLine = true

local executeButton2 = Instance.new("TextButton", page2)
executeButton2.Size = UDim2.new(0.4, 0, 0.1, 0)
executeButton2.Position = UDim2.new(0.3, 0, 0.8, 0)
executeButton2.Text = "Execute"
executeButton2.BackgroundColor3 = Color3.fromRGB(0, 255, 0)
executeButton2.TextScaled = true

local function executeScript2()
local script = codeBox2.Text
local success, errorMessage = pcall(function()
loadstring(script)()
end)

if not success then
warn("Error executing script:", errorMessage)
else
print("Script executed successfully")
end
end

executeButton2.MouseButton1Click:Connect(executeScript2)

-- Toggle GUI Visibility
local function toggleGui()
executorFrame.Visible = not executorFrame.Visible
end

toggleButton.MouseButton1Click:Connect(toggleGui)

-- Page Switching
local function switchToPage1()
page1.Visible = true
page2.Visible = false
end

local function switchToPage2()
page1.Visible = false
page2.Visible = true
end

page1Button.MouseButton1Click:Connect(switchToPage1)
page2Button.MouseButton1Click:Connect(switchToPage2)

-- Print welcome message
print("Hello, " .. player.Name .. ", Welcome to Imnotexploi4's Executor!")
end

-- Initialize the GUI when the script runs
initializeGui()

-- Reinitialize the GUI when the player respawns
player.CharacterAdded:Connect(function()
wait(1) -- Wait a moment to ensure the character is fully loaded
initializeGui()
end)

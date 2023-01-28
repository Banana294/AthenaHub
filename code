--Booting Rayfield Library
local Rayfield = loadstring(game:HttpGet('https://raw.githubusercontent.com/shlexware/Rayfield/main/source'))()

--Creating a window
local Window = Rayfield:CreateWindow({
   Name = "Athena Hub",
   LoadingTitle = "Athena Hub",
   LoadingSubtitle = "by Banana",
   ConfigurationSaving = {
      Enabled = true,
      FolderName = AthenaHub, -- Create a custom folder for your hub/game
      FileName = "Athena Hub"
   },
   Discord = {
      Enabled = false,
      Invite = "ABCD", -- The Discord invite code, do not include discord.gg/
      RememberJoins = true -- Set this to false to make them join the discord every time they load it up
   },
   KeySystem = true, -- Set this to true to use our key system
   KeySettings = {
      Title = "Athena Hub",
      Subtitle = "Key System",
      Note = "Join the Discord to get the key!",
      FileName = "SiriusKey",
      SaveKey = true,
      GrabKeyFromSite = false, -- If this is true, set Key below to the RAW site you would like Rayfield to get the key from
      Key = "Hello"
   }
})

--LocalPlayer
local LocalPlayer = Window:CreateTab("Player Configuration", 3605022185) -- Title, Image
--Walkspeed
local Walkspeed = LocalPlayer:CreateSection("Walkspeed Configuration")
local SpeedSlider = LocalPlayer:CreateSlider({ --Walkspeed
   Name = "Walkspeed Slider",
   Range = {1, 100},
   Increment = 5,
   Suffix = "walkspeed",
   CurrentValue = 16,
   Flag = "SpeedSlider", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
   game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = Value
   end,
})

local SpeedInput = LocalPlayer:CreateInput({
   Name = "Walkspeed",
   PlaceholderText = "16",
   RemoveTextAfterFocusLost = true,
   Callback = function(Text)
   game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = Text
   SpeedSlider:Set(Text)
   end,
})

local SpeedReset = LocalPlayer:CreateButton({ --Reset speed
   Name = "Reset Speed",
   Callback = function()
   game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 16
   SpeedSlider:Set(16)
   end,
})

--JumpPower
local JumpPower = LocalPlayer:CreateSection("Jump Configuration")
local JumpSlider = LocalPlayer:CreateSlider({ --Jump power
   Name = "Jump Power Slider",
   Range = {16, 500},
   Increment = 1,
   Suffix = "jump power",
   CurrentValue = 50,
   Flag = "JumpSlider", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
   game.Players.LocalPlayer.Character.Humanoid.JumpPower = Value
   end,
})

local JumpInput = LocalPlayer:CreateInput({
   Name = "Jump Power",
   PlaceholderText = "50",
   RemoveTextAfterFocusLost = true,
   Callback = function(Text)
   game.Players.LocalPlayer.Character.Humanoid.JumpPower = Text
   SpeedSlider:Set(Text)
   end,
})

local JumpReset = LocalPlayer:CreateButton({ --Reset jump
   Name = "Reset Jump",
   Callback = function()
   game.Players.LocalPlayer.Character.Humanoid.JumpPower = 50
   SpeedSlider:Set(50)
   end,
})

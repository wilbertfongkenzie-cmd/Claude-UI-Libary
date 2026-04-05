# ClaudeUI - Keybind Edition

UI Library for Roblox scripts with **Keybind System** added.

## ✨ Features
- Modern and clean UI design
- Acrylic blur effect support
- Tabs, Buttons, Toggles, Sliders, Dropdowns, Inputs
- **NEW: Keybind System** (`AddKeybind`, `AddKeybindToggle`)

## 🚀 Usage

```lua
local ClaudeUI = loadstring(game:HttpGet("raw-url-github-kamu"))()

local ui = ClaudeUI.new({
    Title = "My Script",
    Width = 700,
    Height = 500,
})

local mainTab = ui:CreateTab({ Title = "Main", Icon = "settings" })

-- Keybind biasa
mainTab:AddKeybind("Teleport Key", "T", function(key)
    print("Pressed:", key)
    -- your code here
end)

-- Keybind + Toggle (switch)
local aimbot = mainTab:AddKeybindToggle("Aimbot", "X", false, function(enabled, key)
    if enabled then
        print("Aimbot ON - Press", key, "to toggle")
    else
        print("Aimbot OFF")
    end
end)

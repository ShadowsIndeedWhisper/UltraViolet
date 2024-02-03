# UltraVoilet UI Library Setup

UltraVoilet is a powerful UI library for Roblox based on the principles of React and Redux. Before you start, it is recommended that you have a basic understanding of Luau/Lua programming language.

## Prerequisites

Make sure you have Lua or Luau scripting knowledge before attempting to use UltraVoilet. If you're new to Lua, consider learning the basics before diving into the library.

## Installation

Follow these steps to install UltraVoilet:

1. **Download the Module:**
   - Visit the [UltraVoilet GitHub repository](https://github.com/UltraVoilet/UltraVoilet).
   - Click on the "Code" button and select "Download ZIP" to download the library as a zip file.
   - Extract the contents of the zip file to a location of your choice.

2. **Integrate with Your Project:**
   - Open Roblox Studio and navigate to the Explorer window.
   - Right-click on "ServerScriptService" or "StarterPlayer" (or any other suitable location for your project) and choose "Insert Object."
   - Select "ModuleScript" and name it "UltraVoilet."

3. **Copy Library Files:**
   - Copy the contents of the extracted UltraVoilet folder into the "UltraVoilet" ModuleScript you created.

## Usage

Now that UltraVoilet is integrated into your project, you can start building user interfaces using its React-like components and Redux state management.

```lua
-- Example usage of UltraVoilet components
local Roact = require(game.ReplicatedStorage.UltraVoilet.Roact)
local UltraVoilet = require(game.ReplicatedStorage.UltraVoilet.UltraVoilet)

-- Define a simple component
local MyComponent = Roact.Component:extend("MyComponent")

function MyComponent:render()
    return UltraVoilet.createElement("TextLabel", {
        Text = "Hello, UltraVoilet!",
        Size = UDim2.new(0, 200, 0, 50),
    })
end

-- Mount the component to the player's PlayerGui
local myElement = UltraVoilet.createElement(MyComponent)
Roact.mount(myElement, game.Players.LocalPlayer.PlayerGui)

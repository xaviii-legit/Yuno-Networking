# Network Manager Module

## Roblox-Specific Documentation

### Overview
This document provides detailed information about the Network Manager module as used specifically in Roblox games.

### Features
- **Remote Event Management**: Easily send and receive events between the server and client.
- **Connection Handling**: Automatically manage player connections and disconnections.

### Usage
1. **Initial Setup**:
   Make sure the Network Manager module is instantiated in your game’s starter or services directory.

2. **Sending Events**:
   ```lua
   NetworkManager:FireEvent('EventName', data)
   ```

3. **Receiving Events**:
   ```lua
   NetworkManager.OnEventReceived:Connect(function(eventName, data)
       -- Handle the event here
   end)
   ```

### Best Practices
- Always disconnect player events when they leave to prevent memory leaks.
- Use descriptive names for your events to ensure clarity.

### Example
```lua
local NetworkManager = require(game.ServerScriptService.NetworkManager)

NetworkManager.OnEventReceived:Connect(function(eventName, data)
    print('Event:', eventName, 'Data:', data)
end)

NetworkManager:FireEvent('PlayerConnected', playerName)
```
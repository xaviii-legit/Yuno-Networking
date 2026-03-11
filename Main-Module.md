# Network Manager Module

## Roblox-Specific Documentation

### Overview
This document provides detailed information about the networking module as used specifically in Roblox games.

### Features
- **Remote Event Management**: Easily send and receive events between the server and client.
- **Bindable Events And Functions Support**: Easily create bindable events and functions with just a few configurations.

### Usage
1. **Initial Setup**:
   Make sure the Network Manager module is instantiated in your game’s starter or services directory.
   ```lua
      local NetworkManager = require(game.ReplicatedStorage.Network)
   ```
2. **Setting Net Type**
   Net types are useful in cases of quickly changing configurations of a packet(see later documentation for more info). Net type is set to "Default" automatically.

3. **Obtaining A Connection**
   ```lua
      local remotePacket = NetworkManager:Get("packetnamehere")
   ```
   ```lua :Get() ``` is case sensitive. Ensure the packet name matches the one mentioned inside the packet database.

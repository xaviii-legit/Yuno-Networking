# Network Manager Module

## Roblox-Specific Documentation

### Overview
This section will cover the middleware folder along with its modules.
```lua
  path.to.Network.Middleware
```

Middleware is run **BEFORE** the callback for an event/connection is run.

### Usage
The middleware folder contains 2 base modules: Ratelimit and Types.

Ratelimit prevents spam

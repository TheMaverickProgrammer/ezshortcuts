# Installation
Put contents of `ezshortcuts/scripts/` into your `scripts/ezlibs-custom/` folder.
Put contents of `ezshortcuts/assets/` into your `assets/` folder.

This lib requires EzMemory to be available.

## To install with EzLibs
Add to your custom.lua like so:
```lua
local CustPlugin = {}

-- local playerNaviCache = require('scripts/ezlibs-custom/player_navi_cache')
-- other plugins ... 
local ezshortcuts = helpers.safe_require('scripts/ezlibs-custom/ezshortcuts')

return CustPlugin
```

# API
After installing the lib into EzLibs custom.lua, the script will run whenever a player connects.
If the player has a checkpoint, it will transfer them to that area and xyz position for you.
You don't have to do anything else.

### Create Checkpoint
`ezshortcuts.create_checkpoint(player_id,x,y,z,show_checkpoint?)`

If show_checkpoint is true, a bot that is exclusive to the owning player is spawned with an animation to help see the point.

### Remove Checkpoint
`ezshortcuts.remove_checkpoint(player_id)`

If this player has a checkpoint, it will remove it from EzMemory and will remove the bot (if it exists)

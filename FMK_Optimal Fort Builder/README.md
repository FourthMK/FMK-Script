# Universal Construction Hotspot Follower

 ⚒️ **Automatically finds, follows, and interacts with optimal construction hotspots in RuneScape 3, with XP detection and retry mechanisms.**

## Features

- **Hotspot Detection**: Scans for construction hotspots using configurable IDs (e.g., 125061, 125065).
- **Optimal Targeting**: Moves to and interacts with the closest hotspot.
- **XP Monitoring**: Detects Construction XP gains to confirm successful actions.
- **Retry System**: Retries interactions up to 3 times if no XP is detected, then stops safely.
- **Configurable Options**: Adjust search distance, hotspot IDs, debug logging, and more.
- **Safe Stopping**: Automatically stops if no hotspots are found or after failed retries.

## How to Use

1. **Prerequisites**:
   - api.lua
   - Place the script in your scripts folder.

2. **Setup**:
   - Manually select or create your building of choice.
   - be near the hotspots
   - Start the script.

3. **Operation**:
   - The script will scan for hotspots within the search distance.
   - It interacts with the closest hotspot and waits for XP gain.
   - If XP is gained, it continues; otherwise, it retries.
   - Stops after 3 failed retries or if no hotspots are detected.

4. **Stopping**:
   - The script stops automatically based on XP detection or lack of hotspots.
   - You can manually stop via injector.

## Configuration

Edit the config section at the top of the script:

```lua
local HOTSPOT_IDS = {125061, 125065}  -- Add more IDs if needed
local SEARCH_DISTANCE = 60             -- Distance to scan for hotspots
local DEBUG = true                    -- Enable debug logging

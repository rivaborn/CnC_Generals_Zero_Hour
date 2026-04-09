# GeneralsMD/Code/GameEngine/Include/GameClient/MapUtil.h

## Purpose
Header for map utility functions and classes in the SAGE engine, handling map metadata, caching, and UI integration.

## Responsibilities
- Define data structures for map metadata and caching
- Declare functions for map validation, preview, and list population
- Manage waypoints, supply/tech positions, and map file handling
- Provide access to default and official maps

## Key Types
- **MapMetaData (Class)**: Stores metadata for a map (name, extent, player count, waypoints, etc.)
- **MapCache (Class)**: Manages cached map data and updates from filesystem
- **WaypointMap (Class)**: Maps waypoint names to 3D coordinates
- **TechAndSupplyImages (Class)**: Stores positions for tech/supply images
- **WinTimeStamp (Struct)**: Windows file timestamp (low/high parts)
- **SUPPLY_TECH_SIZE (Enum)**: Constant for supply/tech image size

## Key Functions
### populateMapListbox
- Purpose: Populate a listbox with available maps.
- Calls: Not inferable (implementation in .cpp)

### isValidMap
- Purpose: Validate if a map exists and is suitable for gameplay.
- Calls: Not inferable

### getMapPreviewImage
- Purpose: Retrieve the preview image for a map.
- Calls: Not inferable

### parseMapPreviewChunk
- Purpose: Parse preview data from a map file chunk.
- Calls: Not inferable

### WouldMapTransfer
- Purpose: Check if a map would be transferred in multiplayer.
- Calls: Not inferable

## Globals
- **TheMapCache (MapCache*)**: Singleton for global map cache access.
- **TheSupplyAndTechImageLocations (TechAndSupplyImages)**: Stores UI positions for supply/tech images.

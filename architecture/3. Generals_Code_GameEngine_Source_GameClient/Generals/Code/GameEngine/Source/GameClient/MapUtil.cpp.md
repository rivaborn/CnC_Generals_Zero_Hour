# Generals/Code/GameEngine/Source/GameClient/MapUtil.cpp

## Purpose
Handles map loading, parsing, validation, and preview rendering in the game client.

## Responsibilities
- Load and parse map files (height data, objects, waypoints)
- Manage map metadata and caching
- Validate and select default maps
- Generate map preview images
- Populate UI listboxes with available maps

## Key Types
- **MapCache (Class)**: Manages cached map metadata and INI file operations
- **MapMetaData (Struct)**: Stores map properties (name, size, player count, etc.)
- **WaypointMap (Class)**: Tracks waypoint positions in a map
- **None**: No other significant classes/structs/enums

## Key Functions
### calcCRC
- Purpose: Computes CRC checksum for a map file.
- Calls: `TheFileSystem->openFile`, `fp->read`, `theCRC.computeCRC`

### loadMap
- Purpose: Loads and parses a map file into memory.
- Calls: `fileStrm.open`, `file.registerParser`, `file.parse`

### populateMapListboxNoReset
- Purpose: Populates a listbox with available maps, including preview images.
- Calls: `GadgetListBoxReset`, `GadgetListBoxAddEntryImage`, `GadgetListBoxSetItemData`

### getMapPreviewImage
- Purpose: Retrieves or generates a preview image for a map.
- Calls: `TheMappedImageCollection->findImageByName`, `copyFromBigToDir`

### isValidMap
- Purpose: Checks if a map is valid for single/multiplayer.
- Calls: `TheMapCache->updateCache`, `TheMapCache->find`

## Globals
- **mapExtension (char*)**: Stores the ".map" file extension.
- **m_width/m_height/m_borderSize (Int)**: Map dimensions and border size.
- **m_data (UnsignedByte*)**: Height map data array.
- **worldDict (Dict)**: Stores world metadata from the map.
- **TheMapCache (MapCache*)**: Global map cache instance.

## Dependencies
- **Common/CRC.h**, **Common/FileSystem.h**, **Common/DataChunk.h**
- **GameClient/Image.h**, **GameClient/GadgetListBox.h**
- **GameLogic/GameLogic.h**, **GameNetwork/GameInfo.h**
- Uses `TheFileSystem`, `TheThingFactory`, `TheMappedImageCollection` globals.

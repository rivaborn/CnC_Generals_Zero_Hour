# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/RadiusDecalUpdate.cpp

## Purpose
Manages creation, update, and cleanup of radius decals for game objects.

## Responsibilities
- Creates and manages radius decals based on templates
- Handles decal lifecycle (creation, update, destruction)
- Controls decal visibility based on object attack status
- Serializes decal state for save/load

## Key Types
- **RadiusDecalUpdate (Class)**: Manages radius decal updates for a game object
- **RadiusDecalTemplate (Type)**: Template for creating radius decals (external)

## Key Functions
### `createRadiusDecal`
- Purpose: Creates a new radius decal at specified position with given radius
- Calls: `RadiusDecalTemplate::createRadiusDecal`, `setWakeFrame`

### `killRadiusDecal`
- Purpose: Destroys the current radius decal
- Calls: `clear()` on decal container

### `update`
- Purpose: Updates decal state each frame and checks attack status
- Calls: `m_deliveryDecal.update()`, `getObject()->testStatus()`

### `xfer`
- Purpose: Serializes/deserializes decal state for save/load
- Calls: `UpdateModule::xfer()`, `m_deliveryDecal.xferRadiusDecal()`

## Globals
- None

## Dependencies
- `UpdateModule` (base class)
- `Thing` (associated game object)
- `Xfer` (serialization)
- `RadiusDecalTemplate` (decal creation)
- `Common/RandomValue.h`, `Common/Xfer.h`, `GameLogic/GameLogic.h`

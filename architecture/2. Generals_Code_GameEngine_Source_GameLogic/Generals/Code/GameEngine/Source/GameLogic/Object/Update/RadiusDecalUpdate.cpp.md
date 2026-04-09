# Generals/Code/GameEngine/Source/GameLogic/Object/Update/RadiusDecalUpdate.cpp

## Purpose
This file contains the implementation of the `RadiusDecalUpdate` class, which manages radius decals for game objects in Command & Conquer Generals.

## Responsibilities
- Manages the creation and destruction of radius decals.
- Updates the state of the decal based on object status.
- Handles serialization and deserialization of decal data.

## Key Types
- `RadiusDecalUpdate` (Class): Manages radius decals for game objects.
- `RadiusDecalTemplate` (Struct): Template for creating radius decals.
- `Coord3D` (Struct): Represents a 3D coordinate in the game world.

## Key Functions
### RadiusDecalUpdate::createRadiusDecal
- Purpose: Creates a radius decal at a specified position with a given template and radius.
- Calls:
  - `tmpl.createRadiusDecal`
  - `setWakeFrame`

### RadiusDecalUpdate::killRadiusDecal
- Purpose: Clears the radius decal associated with the object.
- Calls:
  - `m_deliveryDecal.clear`
  - `setWakeFrame`

### RadiusDecalUpdate::update
- Purpose: Updates the state of the radius decal based on whether the object is attacking.
- Calls:
  - `getObject()->testStatus`
  - `m_deliveryDecal.update`
  - `setWakeFrame`

## Globals
None

## Dependencies
- Includes:
  - "PreRTS.h"
  - "Common/RandomValue.h"
  - "Common/Xfer.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Module/RadiusDecalUpdate.h"
  - "GameLogic/Object.h"

- External symbols used but not defined here:
  - `Thing`
  - `ModuleData`
  - `UpdateModule`
  - `Real`
  -

# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DOverlordAircraftDraw.cpp

## Purpose
Handles drawing logic for aircraft units that contain portable structure upgrades (e.g., Helix, SpectreGunship).

## Responsibilities
- Draws the aircraft and its rider (turret/upgrade)
- Manages visibility of the rider
- Handles color tinting for the rider
- Provides serialization (Xfer) and CRC support

## Key Types
- `W3DOverlordAircraftDrawModuleData` (Class): Module data container
- `W3DOverlordAircraftDraw` (Class): Draw module for overlord aircraft

## Key Functions
### `doDrawModule`
- Purpose: Draws the aircraft and its rider
- Calls: `W3DModelDraw::doDrawModule`, `Drawable::setColorTintEnvelope`, `Drawable::notifyDrawableDependencyCleared`, `Drawable::draw`

### `setHidden`
- Purpose: Hides/shows the aircraft and its rider
- Calls: `W3DModelDraw::setHidden`, `Drawable::setDrawableHidden`

### `crc`
- Purpose: Serialization CRC calculation
- Calls: `W3DModelDraw::crc`

### `xfer`
- Purpose: Serialization/deserialization
- Calls: `W3DModelDraw::xfer`

### `loadPostProcess`
- Purpose: Post-load processing
- Calls: `W3DModelDraw::loadPostProcess`

## Globals
- None

## Dependencies
- `Common/Xfer.h`
- `GameClient/Drawable.h`
- `GameLogic/Object.h`
- `GameLogic/Module/ContainModule.h`
- `W3DDevice/GameClient/Module/W3DOverlordAircraftDraw.h

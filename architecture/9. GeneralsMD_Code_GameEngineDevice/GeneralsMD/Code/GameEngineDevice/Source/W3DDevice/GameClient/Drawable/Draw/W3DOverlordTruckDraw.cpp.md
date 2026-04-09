# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DOverlordTruckDraw.cpp

## Purpose
Handles special drawing logic for the Overlord truck, ensuring its rider (turret) is rendered after the truck itself.

## Responsibilities
- Overrides drawing behavior to render the Overlord's turret after the truck
- Manages visibility synchronization between the truck and its turret
- Provides access to the turret through the Overlord's containment system
- Implements serialization (Xfer) and CRC for save/load functionality

## Key Types
- **W3DOverlordTruckDrawModuleData (Class)**: Module data container (empty implementation)
- **W3DOverlordTruckDraw (Class)**: Specialized draw module for Overlord trucks

## Key Functions
### `doDrawModule`
- Purpose: Renders the Overlord truck and its turret in the correct order
- Calls: `W3DTruckDraw::doDrawModule`, `setColorTintEnvelope`, `notifyDrawableDependencyCleared`, `draw`

### `setHidden`
- Purpose: Synchronizes visibility between the truck and its turret
- Calls: `W3DTruckDraw::setHidden`, `setDrawableHidden`

### `crc`
- Purpose: Serialization checksum for save/load
- Calls: `W3DTruckDraw::crc`

### `xfer`
- Purpose: Serialization/deserialization for save/load
- Calls: `W3DTruckDraw::xfer`

### `loadPostProcess`
- Purpose: Post-load initialization
- Calls: `W3DTruckDraw::loadPostProcess`

## Globals
None

## Dependencies
- `Common/Xfer.h` (Xfer, XferVersion)
- `GameClient/Drawable.h` (Drawable)
- `GameLogic/

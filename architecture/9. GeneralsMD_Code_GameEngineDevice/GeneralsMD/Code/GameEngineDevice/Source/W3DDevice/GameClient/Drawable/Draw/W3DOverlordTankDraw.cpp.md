# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DOverlordTankDraw.cpp

## Purpose
Handles special rendering logic for the Overlord tank, ensuring its rider (turret) is drawn after the tank itself.

## Responsibilities
- Extends `W3DTankDraw` to add Overlord-specific rendering behavior
- Manages rider visibility in sync with the tank
- Ensures rider uses the same color tint as the tank
- Handles serialization (CRC, Xfer) for module data

## Key Types
- `W3DOverlordTankDrawModuleData` (Class): Module data container (empty implementation)
- `W3DOverlordTankDraw` (Class): Specialized draw module for Overlord tank

## Key Functions
### `doDrawModule`
- Purpose: Renders the tank and its rider in correct order
- Calls: `W3DTankDraw::doDrawModule`, `setColorTintEnvelope`, `notifyDrawableDependencyCleared`, `draw`

### `setHidden`
- Purpose: Synchronizes visibility between tank and rider
- Calls: `W3DTankDraw::setHidden`, `setDrawableHidden`

### `crc`
- Purpose: Serialization CRC calculation
- Calls: `W3DTankDraw::crc`

### `xfer`
- Purpose: Serialization/deserialization
- Calls: `W3DTankDraw::xfer`

### `loadPostProcess`
- Purpose: Post-load initialization
- Calls: `W3DTankDraw::loadPostProcess`

## Globals
None

## Dependencies
- `Common/Xfer.h` (Xfer)
- `GameClient/Drawable.h` (Drawable)
- `GameLogic/Object.h` (Object)
- `GameLogic/Module/ContainModule.h`

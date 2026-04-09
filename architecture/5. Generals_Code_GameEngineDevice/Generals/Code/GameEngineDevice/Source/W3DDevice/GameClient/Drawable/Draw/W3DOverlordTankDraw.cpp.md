# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DOverlordTankDraw.cpp

## Purpose
Handles special drawing logic for the Overlord tank, ensuring its rider (turret) is rendered after the tank itself.

## Responsibilities
- Extends `W3DTankDraw` to customize drawing behavior for the Overlord tank.
- Manages the rider's visibility state to match the tank's hidden state.
- Ensures the rider's color tint matches the tank's.
- Handles serialization (CRC, Xfer) and loading.

## Key Types
- `W3DOverlordTankDrawModuleData` (Class): Module data container (empty implementation).
- `W3DOverlordTankDraw` (Class): Custom draw module for the Overlord tank.

## Key Functions
### `doDrawModule`
- Purpose: Draws the tank and its rider in the correct order.
- Calls: `W3DTankDraw::doDrawModule`, `setColorTintEnvelope`, `notifyDrawableDependencyCleared`, `draw`.

### `setHidden`
- Purpose: Hides/shows the tank and its rider together.
- Calls: `W3DTankDraw::setHidden`, `setDrawableHidden`.

### `crc`
- Purpose: Serialization CRC calculation.
- Calls: `W3DTankDraw::crc`.

### `xfer`
- Purpose: Serialization/deserialization.
- Calls: `W3DTankDraw::xfer`.

### `loadPostProcess`
- Purpose: Post-load initialization.
- Calls: `W3DTankDraw::loadPostProcess`.

## Globals
None.

## Dependencies
- `Common/Xfer.h`, `GameClient/Drawable.h`, `GameLogic/Object.h`, `GameLogic/Module/ContainModule.h`, `W3D

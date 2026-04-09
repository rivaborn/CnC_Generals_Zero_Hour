# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DDependencyModelDraw.cpp

## Purpose
Handles conditional drawing of 3D models that depend on another object finishing its draw first, with optional bone attachment.

## Responsibilities
- Manages dependency-cleared state for draw ordering
- Adjusts transform matrix based on container bone attachment
- Synchronizes stealth appearance with container
- Serializes/deserializes module state

## Key Types
- `W3DDependencyModelDrawModuleData` (Class): Stores module configuration including bone attachment name
- `W3DDependencyModelDraw` (Class): Main draw module implementing dependency logic

## Key Functions
### `doDrawModule`
- Purpose: Conditionally renders model only after dependency is cleared
- Calls: `W3DModelDraw::doDrawModule`, `getDrawable`, `getObject`, `getContainedBy`, `getContain`, `isEnclosingContainerFor`, `getDrawable`, `imitateStealthLook`, `getCurrentWorldspaceClientBonePositions`, `getTransformMatrix`

### `notifyDrawModuleDependencyCleared`
- Purpose: Signals that dependent object has finished drawing
- Calls: None

### `adjustTransformMtx`
- Purpose: Modifies transform matrix for bone attachment to container
- Calls: `W3DModelDraw::adjustTransformMtx`, `getDrawable`, `getObject`, `getContainedBy`, `getContain`, `isEnclosingContainerFor`, `getDrawable`, `getCurrentWorldspaceClientBonePositions`, `getTransformMatrix`

### `crc`
- Purpose: Generates CRC checksum for module data
- Calls: `W3DModelDraw::crc`

### `xfer`
- Purpose: Serializes/deserializes module state
- Calls: `W3DModelDraw::xfer`, `xferVersion`, `xferBool`

## Globals
- None

## Dependencies
- `Common/Xfer.h` (Xfer)
- `GameClient/Drawable.h` (Drawable)
- `GameLogic/Object.h` (Object)
- `GameLogic/Module/ContainModule.h` (ContainModule)
- `W3DDevice/GameClient/Module/W3DDependencyModelDraw.h` (W3DDependencyModelDrawModuleData, W3DModelDraw)

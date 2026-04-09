# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DDependencyModelDraw.cpp

## Purpose
Handles conditional drawing of 3D models based on external dependencies, primarily for attached objects like transports.

## Responsibilities
- Manages draw dependency state (`m_dependencyCleared`)
- Adjusts transform matrix for bone attachment in containers
- Extends `W3DModelDraw` with dependency-aware drawing logic
- Serializes/deserializes dependency state via Xfer

## Key Types
- `W3DDependencyModelDrawModuleData` (Class): Stores module configuration (e.g., bone attachment name)
- `W3DDependencyModelDraw` (Class): Dependency-aware draw module implementation

## Key Functions
### `doDrawModule`
- Purpose: Conditionally draws the model only if dependency is cleared.
- Calls: `W3DModelDraw::doDrawModule`

### `notifyDrawModuleDependencyCleared`
- Purpose: Signals that the dependency has been resolved, allowing drawing.
- Calls: None

### `adjustTransformMtx`
- Purpose: Adjusts the transform matrix for bone attachment in containers.
- Calls: `W3DModelDraw::adjustTransformMtx`, `getCurrentWorldspaceClientBonePositions`

### `xfer`
- Purpose: Serializes/deserializes the module's state.
- Calls: `W3DModelDraw::xfer`, `Xfer::xferBool`

## Globals
- None

## Dependencies
- `W3DDependencyModelDraw.h`, `W3DModelDraw.h`
- `Drawable.h`, `Object.h`, `ContainModule.h`
- `Xfer.h` (for serialization)

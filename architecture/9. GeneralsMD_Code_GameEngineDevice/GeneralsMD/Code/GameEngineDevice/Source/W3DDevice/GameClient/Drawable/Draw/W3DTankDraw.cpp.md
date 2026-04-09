# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DTankDraw.cpp

## Purpose
Handles rendering of turreted tanks, including tread animation and debris effects.

## Responsibilities
- Manages tank tread animation via UV scrolling
- Controls debris particle systems for moving tanks
- Handles tank turning and movement visualization
- Manages W3D render object lifecycle

## Key Types
- `W3DTankDrawModuleData` (Class): Stores tank-specific draw module configuration
- `W3DTankDraw` (Class): Main tank draw module implementation
- `TreadObjectInfo` (Struct): Tracks individual tread render objects and their settings
- `Matrix3D` (Class): 3D transformation matrix (external)

## Key Functions
### `updateTreadPositions`
- Purpose: Updates UV coordinates for tread scrolling animation
- Calls: `WWMath::Floor`

### `updateTreadObjects`
- Purpose: Identifies and caches tread sub-meshes from the render object
- Calls: `RenderObjClass` methods, `MaterialInfoClass` methods

### `doDrawModule`
- Purpose: Main draw routine that handles tread animation and debris effects
- Calls: `startMoveDebris`, `stopMoveDebris`, `updateTreadPositions`, `W3DModelDraw::doDrawModule`

### `createEmitters`
- Purpose: Creates particle systems for tread debris
- Calls: `TheParticleSystemManager` methods

## Globals
- `TheParticleSystemManager` (Global): Particle system manager instance
- `TheTacticalView` (Global): Tactical view manager
- `TheScriptEngine` (Global): Script engine instance

## Dependencies
- `W3DModelDraw.h` (base class)
- `ParticleSys.h` (particle systems)
- `Thing.h`, `ThingTemplate.h` (game entity system)
- `PhysicsUpdate.h`, `BodyModule.h` (physics)
- `AIUpdate.h` (AI behavior)
- `GameAudio.h` (audio)
- `Xfer.h` (serialization)
- WW3D2 rendering API (`RenderObjClass`, `MaterialInfoClass`, etc.)

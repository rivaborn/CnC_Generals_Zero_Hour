# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DTankDraw.cpp

## Purpose
Handles rendering of turreted tanks in the game, including tread animation and debris effects.

## Responsibilities
- Manages tank tread animation and debris particle systems
- Updates UV coordinates for tread scrolling based on movement
- Controls debris emission based on tank velocity and turning state
- Handles tank rendering with special effects for movement

## Key Types
- **Matrix3D (Class)**: 3D transformation matrix (external)
- **W3DTankDrawModuleData (Class)**: Stores tank-specific rendering data (tread debris names, animation rates)
- **W3DTankDraw (Class)**: Main tank drawing module handling tread animation and debris
- **TreadObjectInfo (Struct)**: Tracks individual tread objects and their material settings

## Key Functions
### `updateTreadPositions`
- Purpose: Updates UV coordinates for tread scrolling animation
- Calls: `WWMath::Floor`

### `updateTreadObjects`
- Purpose: Identifies and stores references to tread sub-meshes in the tank model
- Calls: `RenderObjClass` methods, `MaterialInfoClass` methods

### `doDrawModule`
- Purpose: Main rendering function that handles tank drawing, tread animation, and debris effects
- Calls: `W3DModelDraw::doDrawModule`, `startMoveDebris`, `stopMoveDebris`, `updateTreadPositions`

### `startMoveDebris` / `stopMoveDebris`
- Purpose: Controls debris particle system emission based on tank movement state
- Calls: `ParticleSystem` methods

## Globals
- **TheParticleSystemManager (Global)**: Manages particle system templates and instances
- **TheTacticalView (Global)**: Provides view state information
- **TheScriptEngine (Global)**: Handles scripted game events

## Dependencies
- Key includes: `Common/Thing.h`, `GameLogic/Weapon.h`, `GameClient/Drawable.h`, `W3DDevice/GameClient/Module/W3DTankDraw.h`
- External symbols: `RenderObjClass`, `MaterialInfoClass`, `ParticleSystem`, `PhysicsBehavior`, `AIUpdateInterface`

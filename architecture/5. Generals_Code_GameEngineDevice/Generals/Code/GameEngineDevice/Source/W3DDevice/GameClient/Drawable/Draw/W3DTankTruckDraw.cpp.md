# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DTankTruckDraw.cpp

## Purpose
Handles rendering of tank and truck vehicles, including wheel/tread animation, particle effects, and sound management.

## Responsibilities
- Manages visual effects (dust, dirt, powerslide) for vehicles
- Animates wheels and treads based on movement
- Handles particle systems for debris and effects
- Manages sound events for vehicle actions
- Updates bone transformations for vehicle parts

## Key Types
- `W3DTankTruckDrawModuleData` (Class): Stores configuration for tank/truck rendering
- `W3DTankTruckDraw` (Class): Main draw module for tank/truck vehicles
- `TreadObjectInfo` (Struct): Tracks tread mesh and material settings
- `TreadType` (Enum): Identifies tread types (left/right/middle)

## Key Functions
### `createEmitters`
- Purpose: Creates particle emitters for dust, dirt, and powerslide effects
- Calls: `TheParticleSystemManager->findTemplate`, `TheParticleSystemManager->createParticleSystem`

### `doDrawModule`
- Purpose: Main rendering function that handles wheel/tread animation and effects
- Calls: `W3DModelDraw::doDrawModule`, `getRenderObject()->Control_Bone`, `enableEmitters`

### `updateTreadPositions`
- Purpose: Updates UV coordinates for tread scrolling animation
- Calls: `WWMath::Floor`

### `updateBones`
- Purpose: Updates bone indices for wheel/tread bones
- Calls: `getRenderObject()->Get_Bone_Index`

## Globals
- `TheParticleSystemManager` (Global): Particle system manager instance
- `TheGlobalData` (Global): Game global data
- `TheTacticalView` (Global): Tactical view manager
- `TheScriptEngine` (Global): Script engine instance
- `TheAudio` (Global): Audio system

## Dependencies
- Common game systems (Thing, GameAudio, GlobalData)
- Game logic (Weapon, GameLogic, PhysicsUpdate)
- W3D rendering system (W3DGameClient, W3DTankTruckDraw)
- Particle system management
- WW3D2 math utilities

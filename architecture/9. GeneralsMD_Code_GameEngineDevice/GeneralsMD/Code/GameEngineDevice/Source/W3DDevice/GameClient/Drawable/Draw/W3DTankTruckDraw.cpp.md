# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DTankTruckDraw.cpp

## Purpose
Handles rendering of tank and truck vehicles, including wheel/tread animation, particle effects, and sound management.

## Responsibilities
- Manages visual effects (dust, dirt, powerslide particles)
- Animates wheels and treads based on vehicle movement
- Handles sound effects for landing and powersliding
- Updates bone transformations for vehicle parts
- Manages particle system debris for tank treads

## Key Types
- `W3DTankTruckDrawModuleData` (Class): Stores configuration for tank/truck rendering (tread debris names, animation rates, etc.)
- `W3DTankTruckDraw` (Class): Main drawable module for tanks and trucks
- `TreadObjectInfo` (Struct): Tracks tread sub-mesh and material settings
- `TreadType` (Enum): Defines tread types (left, right, middle)

## Key Functions
### `createEmitters`
- Purpose: Creates particle emitters for dust, dirt, and powerslide effects
- Calls: `TheParticleSystemManager->findTemplate`, `TheParticleSystemManager->createParticleSystem`

### `updateBones`
- Purpose: Updates bone indices for wheel/tire bones from module data
- Calls: `getRenderObject()->Get_Bone_Index`

### `doDrawModule`
- Purpose: Main rendering function that handles wheel rotation, particle effects, and tread animation
- Calls: `W3DModelDraw::doDrawModule`, `enableEmitters`, `updateTreadPositions`, `TheAudio->addAudioEvent`

### `updateTreadPositions`
- Purpose: Updates UV coordinates for tread scrolling animation
- Calls: None (direct math operations)

## Globals
- `TheParticleSystemManager` (External): Manages particle systems
- `TheGlobalData` (External): Global game data
- `TheTacticalView` (External): Tactical view state
- `TheScriptEngine` (External): Script engine
- `TheAudio` (External): Audio system

## Dependencies
- Common game systems: `Thing`, `ThingTemplate`, `GameAudio`
- Game logic: `PhysicsBehavior`, `AIUpdateInterface`
- Rendering: `W3DModelDraw`, `RenderObjClass`
- Particle systems: `ParticleSystemTemplate`, `ParticleSystem`
- Math: `Matrix3D`, `Coord3D`

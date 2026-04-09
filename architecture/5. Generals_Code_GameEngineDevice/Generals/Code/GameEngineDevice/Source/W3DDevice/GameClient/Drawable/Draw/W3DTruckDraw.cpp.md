# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DTruckDraw.cpp

## Purpose
Handles rendering and animation of truck-like vehicles (e.g., rocket buggies) in the game, including wheel rotation, particle effects, and physics-based visuals.

## Responsibilities
- Manages visual effects (dust, dirt spray, powerslide effects) for trucks
- Animates wheels and vehicle components based on physics state
- Handles bone manipulation for tire and cab rotation
- Manages particle emitters for ground effects
- Plays sound effects for landing and powersliding

## Key Types
- **W3DTruckDrawModuleData (Class)**: Stores configuration data for truck drawing (bone names, effect names, rotation factors)
- **W3DTruckDraw (Class)**: Main drawable module for trucks, inherits from W3DModelDraw
- **TWheelInfo (Struct)**: Contains wheel position and angle data (external)

## Key Functions
### `createEmitters`
- Purpose: Creates particle emitters for dust, dirt, and powerslide effects
- Calls: `TheParticleSystemManager->findTemplate`, `TheParticleSystemManager->createParticleSystem`

### `doDrawModule`
- Purpose: Renders the truck with animated wheels and effects based on physics state
- Calls: `W3DModelDraw::doDrawModule`, `getRenderObject()->Control_Bone`, `enableEmitters`, `TheAudio->addAudioEvent`

### `updateBones`
- Purpose: Updates bone indices for tires and vehicle components
- Calls: `getRenderObject()->Get_Bone_Index`

### `enableEmitters`
- Purpose: Starts/stops particle emitters based on vehicle state
- Calls: `createEmitters`, `m_dustEffect->start/stop`, etc.

## Globals
- **TheParticleSystemManager (External)**: Manages particle systems
- **TheAudio (External)**: Handles sound playback
- **TheGlobalData (External)**: Contains game global settings
- **TheTacticalView (External)**: Provides view state information
- **TheScriptEngine (External)**: Script execution interface
- **ThePartitionManager (External)**: Spatial partitioning manager

## Dependencies
- Common headers: `Thing.h`, `ThingFactory.h`, `GameAudio.h`, `GlobalData.h`
- GameClient headers: `Drawable.h`, `ParticleSys.h`
- GameLogic headers: `AIPathfind.h`, `Weapon.h`, `GameLogic.h`, `PartitionManager.h`, `Locomotor.h`
- W3DDevice headers: `W3DGameClient.h`, `W3DTruckDraw.h`
- Standard libraries: `stdlib.h`, `math.h`

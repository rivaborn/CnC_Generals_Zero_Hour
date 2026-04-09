# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DTruckDraw.cpp

## Purpose
Handles rendering and animation of truck-like vehicles (e.g., rocket buggies) in the game, including wheel rotation, particle effects, and physics-based visuals.

## Responsibilities
- Manages visual effects (dust, dirt spray, powerslide effects)
- Animates vehicle wheels and cab based on physics state
- Handles particle emitter creation/destruction
- Processes bone transformations for vehicle parts
- Manages sound effects for landing and powersliding

## Key Types
- **W3DTruckDrawModuleData (Class)**: Stores configuration data for truck drawing (bone names, effect names, rotation factors)
- **W3DTruckDraw (Class)**: Main drawable module for trucks, extends W3DModelDraw
- **TWheelInfo (Struct)**: Contains wheel position/rotation data (external)
- **AudioEventRTS (Class)**: Sound event data (external)

## Key Functions
### `createEmitters`
- Purpose: Creates particle emitters for dust, dirt, and powerslide effects
- Calls: `TheParticleSystemManager->findTemplate`, `TheParticleSystemManager->createParticleSystem`

### `doDrawModule`
- Purpose: Handles per-frame drawing and animation of truck components
- Calls: `W3DModelDraw::doDrawModule`, `getRenderObject()->Control_Bone`, `enableEmitters`, `TheAudio->addAudioEvent`

### `updateBones`
- Purpose: Updates bone indices for truck model components
- Calls: `getRenderObject()->Get_Bone_Index`

### `enableEmitters`
- Purpose: Starts/stops particle emitters based on vehicle state
- Calls: `createEmitters`, `m_dustEffect->start/stop`, etc.

## Globals
- **TheParticleSystemManager (Global)**: Manages particle systems
- **TheGlobalData (Global)**: Contains game-wide settings
- **TheTacticalView (Global)**: Provides view/camera state
- **TheScriptEngine (Global)**: Handles script execution
- **ThePartitionManager (Global)**: Manages spatial partitioning
- **TheAudio (Global)**: Handles sound playback

## Dependencies
- Common game systems: `Thing`, `ThingTemplate`, `GameAudio`
- Rendering: `W3DModelDraw`, `W3DRenderObject`
- Physics: `PhysicsBehavior`, `Locomotor`
- AI: `AIUpdateInterface`
- Particle effects: `ParticleSystemTemplate`, `ParticleSystemManager`
- Scripting: `ScriptEngine`
- Networking: `Xfer` for serialization

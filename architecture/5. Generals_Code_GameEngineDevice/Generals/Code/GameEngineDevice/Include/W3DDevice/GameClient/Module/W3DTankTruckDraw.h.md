# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/Module/W3DTankTruckDraw.h

## Purpose
Defines classes for rendering vehicles with treads and wheels in the SAGE engine.

## Responsibilities
- Manages vehicle wheel/tread animation and rendering
- Handles particle effects for dust, dirt, and powersliding
- Controls tank-specific debris emitters
- Updates bone transformations for vehicle parts

## Key Types
- **W3DTankTruckDrawModuleData (Class)**: Stores configuration data for vehicle rendering (effect names, bone names, animation rates)
- **W3DTankTruckDraw (Class)**: Main vehicle rendering module handling wheels, treads, and effects
- **TreadObjectInfo (Struct)**: Contains render object and material settings for treads
- **TreadType (Enum)**: Defines tread types (left, right, middle)
- **MAX_TREADS_PER_TANK (Enum)**: Constant for maximum tread count (4)

## Key Functions
### createEmitters
- Purpose: Creates particle effects for the vehicle
- Calls: Not inferable

### enableEmitters
- Purpose: Enables/disables debris emitters
- Calls: Not inferable

### updateTreadObjects
- Purpose: Updates pointers to sub-objects like treads
- Calls: Not inferable

### updateTreadPositions
- Purpose: Updates UV coordinates on each tread
- Calls: Not inferable

## Globals
- None

## Dependencies
- `DrawModule.h`, `AudioEventRTS.h`, `ParticleSys.h`, `W3DModelDraw.h`, `HAnim.h`, `RendObj.h`, `Part_Emt.h`
- `W3DModelDrawModuleData`, `ParticleSystem`, `RenderObjClass`, `AudioEventRTS`, `Matrix3D`

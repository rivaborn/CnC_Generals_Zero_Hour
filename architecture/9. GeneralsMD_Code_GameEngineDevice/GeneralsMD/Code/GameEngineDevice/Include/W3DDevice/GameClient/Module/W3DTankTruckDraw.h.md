# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/Module/W3DTankTruckDraw.h

## Purpose
Defines classes for rendering vehicles with treads and wheels in the W3D engine.

## Responsibilities
- Manages vehicle tread and wheel animation
- Handles particle effects for dust, dirt, and powersliding
- Controls tank-specific debris emitters
- Updates bone transformations for vehicle parts

## Key Types
- **W3DTankTruckDrawModuleData (Class)**: Stores configuration data for tank/truck rendering
- **W3DTankTruckDraw (Class)**: Main class handling vehicle rendering and effects
- **TreadType (Enum)**: Defines tread types (left, right, middle)
- **TreadObjectInfo (Struct)**: Contains tread rendering information

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
- Common/DrawModule.h
- Common/AudioEventRTS.h
- GameClient/ParticleSys.h
- W3DDevice/GameClient/Module/W3DModelDraw.h
- WW3D2/HAnim.h
- WW3D2/RendObj.h
- WW3D2/Part_Emt.h

# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/Module/W3DTankDraw.h

## Purpose
Defines classes for rendering tank models with animated treads and debris effects in the SAGE engine.

## Responsibilities
- Manages tank-specific rendering modules
- Handles tread animation and debris particle effects
- Provides module data for tank visual properties
- Updates tread positions and UV coordinates during movement

## Key Types
- **W3DTankDrawModuleData (Class)**: Stores tank-specific visual parameters (tread debris names, animation rates)
- **W3DTankDraw (Class)**: Main tank rendering module handling treads and debris
- **TreadObjectInfo (Struct)**: Contains tread sub-object and material override data
- **TreadType (Enum)**: Identifies left/right/middle tread types
- **MAX_TREADS_PER_TANK (Enum)**: Constant for maximum tread count (4)

## Key Functions
### W3DTankDraw::doDrawModule
- Purpose: Renders the tank with tread animations
- Calls: updateTreadObjects, updateTreadPositions, startMoveDebris, stopMoveDebris

### W3DTankDraw::updateTreadPositions
- Purpose: Updates UV coordinates for tread scrolling animation
- Calls: Not inferable

### W3DTankDraw::createEmitters
- Purpose: Initializes particle systems for tread debris
- Calls: Not inferable

## Globals
- None

## Dependencies
- Common/DrawModule.h
- GameClient/ParticleSys.h
- W3DDevice/GameClient/Module/W3DModelDraw.h
- WW3D2/HAnim.h
- WW3D2/RendObj.h
- WW3D2/Part_Emt.h

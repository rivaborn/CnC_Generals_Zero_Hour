# GeneralsMD/Code/GameEngine/Source/GameClient/FXList.cpp

## Purpose
Defines various visual/audio effect classes and their parsing logic for the SAGE game engine.

## Responsibilities
- Implements concrete FXNugget subclasses for different effect types
- Provides INI parsing for effect definitions
- Manages FXList and FXListStore classes for effect storage/retrieval
- Handles spatial calculations for effect positioning

## Key Types
- **SoundFXNugget (Class)**: Plays sound effects at object positions
- **TracerFXNugget (Class)**: Creates tracer visuals between two points
- **RayEffectFXNugget (Class)**: Renders ray effects between objects
- **LightPulseFXNugget (Class)**: Creates light pulses around objects
- **ViewShakeFXNugget (Class)**: Triggers screen shake effects
- **TerrainScorchFXNugget (Class)**: Applies scorch marks to terrain
- **ParticleSystemFXNugget (Class)**: Spawns particle systems
- **FXListAtBonePosFXNugget (Class)**: Applies effects at object bone positions
- **FXList (Class)**: Container for multiple FXNuggets
- **FXListStore (Class)**: Global store for named FXLists

## Key Functions
### adjustVector
- Purpose: Transforms a vector through a matrix
- Calls: Matrix3D::Rotate_Vector

### calcDist
- Purpose: Calculates 3D distance between two points
- Calls: None

### FXList::doFXPos
- Purpose: Executes all effects in the list at a position
- Calls: FXNugget::doFXPos, ThePartitionManager checks

### FXList::doFXObj
- Purpose: Executes all effects in the list on an object
- Calls: FXNugget::doFXObj, shroud status checks

## Globals
- **TheFXListStore (FXListStore*)**: Global FXList store instance
- **TheFXListFieldParse (FieldParse[])**: Field parsing definitions for FXLists

## Dependencies
- GameClient/FXList.h
- Common/DrawModule.h
- Common/GameAudio.h
- Common/INI.h
- Common/Player.h
- Common/PlayerList.h
- Common/RandomValue.h
- Common/ThingTemplate.h
- Common/ThingFactory.h
- GameLogic/Object.h
- GameLogic/GameLogic.h
- GameLogic/TerrainLogic.h
- GameClient/Display.h
- GameClient/GameClient.h
- GameClient/Drawable.h
- GameClient/ParticleSys.h
- GameLogic/PartitionManager.h

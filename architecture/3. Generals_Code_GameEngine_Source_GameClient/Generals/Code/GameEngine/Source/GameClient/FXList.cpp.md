# Generals/Code/GameEngine/Source/GameClient/FXList.cpp

## Purpose
Implements visual and audio effects (FX) for the game, including particle systems, tracers, sounds, and terrain modifications.

## Responsibilities
- Defines various FX nugget classes (Sound, Tracer, RayEffect, etc.)
- Parses FX definitions from INI files
- Manages FX execution based on object positions or world coordinates
- Handles shroud/fog visibility checks before applying effects

## Key Types
- **FXNugget (Class)**: Base class for all FX types
- **SoundFXNugget (Class)**: Plays sound effects at specified positions
- **TracerFXNugget (Class)**: Creates tracer visuals between two points
- **RayEffectFXNugget (Class)**: Renders ray effects between objects
- **LightPulseFXNugget (Class)**: Creates light pulses around objects
- **ViewShakeFXNugget (Class)**: Triggers screen shake effects
- **TerrainScorchFXNugget (Class)**: Applies scorch marks to terrain
- **ParticleSystemFXNugget (Class)**: Spawns particle systems
- **FXListAtBonePosFXNugget (Class)**: Applies FX at specific bone positions
- **FXList (Class)**: Container for multiple FX nuggets
- **FXListStore (Class)**: Manages named collections of FX lists

## Key Functions
### adjustVector
- Purpose: Adjusts a vector by a transformation matrix
- Calls: Matrix3D::Rotate_Vector

### calcDist
- Purpose: Calculates distance between two 3D coordinates
- Calls: None

### FXList::doFXPos
- Purpose: Executes all FX in the list at a world position
- Calls: FXNugget::doFXPos, ThePartitionManager checks

### FXList::doFXObj
- Purpose: Executes all FX in the list attached to an object
- Calls: FXNugget::doFXObj, shroud status checks

### FXListStore::parseFXListDefinition
- Purpose: Parses FX list definitions from INI files
- Calls: INI::initFromINI, TheNameKeyGenerator

## Globals
- **TheFXListStore (FXListStore*)**: Global store for FX list definitions
- **TheFXListFieldParse (FieldParse[])**: Field parsing definitions for FX lists

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

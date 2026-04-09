# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/CrushDie.h

## Purpose
Defines the CrushDie module for handling crush-related death logic and audio events in the game.

## Responsibilities
- Manages crush-related death behavior for game objects
- Plays crush sound effects based on damage type
- Configures crush sound probabilities via module data
- Inherits from DieModule to extend death handling

## Key Types
- **CrushEnum (Enum)**: Defines types of crush damage (TOTAL_CRUSH, BACK_END_CRUSH, FRONT_END_CRUSH, NO_CRUSH)
- **CrushDieModuleData (Class)**: Contains audio events and probability settings for crush sounds
- **CrushDie (Class)**: Main module class implementing crush death logic
- **Thing (Class)**: Forward reference to game object class

## Key Functions
### CrushDieModuleData::buildFieldParse
- Purpose: Registers INI field parsers for crush sound configurations
- Calls: DieModuleData::buildFieldParse, INI::parseAudioEventRTS, INI::parseInt

### CrushDie::onDie
- Purpose: Handles crush death logic and plays appropriate sound effects
- Calls: Not inferable from header

## Globals
None

## Dependencies
- Common/AudioEventRTS.h
- Common/INI.h
- GameLogic/Module/DieModule.h
- Memory pool and module macro utilities (MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE, MAKE_STANDARD_MODULE_MACRO_WITH_MODULE_DATA)

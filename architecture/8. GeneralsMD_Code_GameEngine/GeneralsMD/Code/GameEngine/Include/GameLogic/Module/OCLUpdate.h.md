# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/OCLUpdate.h

## Purpose
Defines the OCLUpdate module for managing timed object creation lists in the game.

## Responsibilities
- Manages timed creation of object lists (OCLs)
- Handles faction-specific OCL triggers
- Provides countdown feedback and timer control
- Supports module data configuration and parsing

## Key Types
- **OCLUpdateModuleData (Class)**: Module configuration data for OCL updates
- **FactionOCLInfo (Struct)**: Stores faction name and associated OCL
- **FactionOCLList (Type)**: List of FactionOCLInfo entries
- **OCLUpdate (Class)**: Main update module class handling timed OCL creation
- **OCLUpdateMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **OCLUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### OCLUpdateModuleData::buildFieldParse
- Purpose: Parses module data fields from configuration
- Calls: Not inferable

### OCLUpdate::update
- Purpose: Updates the module's timer and triggers OCL creation when ready
- Calls: shouldCreate(), setNextCreationFrame()

### OCLUpdate::shouldCreate
- Purpose: Determines if OCL should be created based on timer and conditions
- Calls: Not inferable

### OCLUpdate::setNextCreationFrame
- Purpose: Calculates and sets the next frame for OCL creation
- Calls: Not inferable

### OCLUpdate::getCountdownPercent
- Purpose: Returns current countdown percentage (0-100%)
- Calls: Not inferable

### OCLUpdate::getRemainingFrames
- Purpose: Returns remaining frames until next OCL creation
- Calls: Not inferable

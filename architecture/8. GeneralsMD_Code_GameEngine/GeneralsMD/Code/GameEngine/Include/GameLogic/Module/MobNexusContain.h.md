# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/MobNexusContain.h

## Purpose
Defines the MobNexusContain module for handling container logic in mobile units, acting as a proxy for UI and AI interactions.

## Responsibilities
- Manages containment of objects within mobile units
- Handles unit entry/exit logic and capacity checks
- Provides transport passenger interface functionality
- Manages door reservations for unit exits
- Handles evacuation of contained units

## Key Types
- **MobNexusContainModuleData (Class)**: Contains configuration data for the containment module
- **InitialPayload (Struct)**: Stores initial payload name and count data
- **MobNexusContain (Class)**: Implements the containment logic for mobile units
- **MobNexusContainMagicEnum (Enum)**: Not inferable (empty enum)
- **MobNexusContain_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (empty enum)

## Key Functions
### MobNexusContainModuleData::buildFieldParse
- Purpose: Registers INI field parsing for module data
- Calls: Not inferable

### MobNexusContainModuleData::parseInitialPayload
- Purpose: Parses initial payload data from INI files
- Calls: Not inferable

### MobNexusContain::isValidContainerFor
- Purpose: Checks if an object can be contained
- Calls: Not inferable

### MobNexusContain::onContaining
- Purpose: Handles object containment events
- Calls: Not inferable

### MobNexusContain::onRemoving
- Purpose: Handles object removal events
- Calls: Not inferable

### MobNexusContain::update
- Purpose: Per-frame update for containment logic
- Calls: Not inferable

###

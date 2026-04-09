# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ParachuteContain.h

## Purpose
Defines the parachute containment module for transport units in Command & Conquer Generals Zero Hour.

## Responsibilities
- Manages parachute deployment and behavior for contained objects
- Handles object containment logic specific to parachute drops
- Controls visual and physical positioning of contained objects
- Manages collision and damage responses during parachute operations

## Key Types
- **ParachuteContainModuleData (Class)**: Contains configuration data for parachute behavior (pitch/roll rates, damage thresholds, etc.)
- **ParachuteContain (Class)**: Implements the parachute containment logic for transport units
- **ParachuteContainMagicEnum (Enum)**: Not inferable (empty enum)
- **ParachuteContain_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (empty enum)

## Key Functions
### ParachuteContain::update
- Purpose: Updates parachute state once per frame
- Calls: Not inferable (implementation not shown)

### ParachuteContain::onCollide
- Purpose: Handles collision events during parachute operations
- Calls: Not inferable

### ParachuteContain::onDie
- Purpose: Processes death/damage events for the container
- Calls: Not inferable

### ParachuteContain::setOverrideDestination
- Purpose: Sets a specific landing destination override
- Calls: Not inferable

## Globals
- None

## Dependencies
- `GameLogic/Module/OpenContain.h` (base class)
- `MultiIniFieldParse` (for configuration parsing)
- `AudioEventRTS` (for sound events)
- Memory pool and module macro utilities (SAGE engine internals)

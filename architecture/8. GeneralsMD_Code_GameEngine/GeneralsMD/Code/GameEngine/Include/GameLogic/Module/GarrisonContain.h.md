# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/GarrisonContain.h

## Purpose
Defines the `GarrisonContain` module for structures that can be garrisoned, managing unit containment, positioning, and behavior.

## Responsibilities
- Manages garrisoned units within a structure
- Handles unit positioning at garrison points
- Controls unit healing and damage responses
- Manages exit rally points and unit deployment

## Key Types
- **GarrisonContainModuleData (Class)**: Module data for garrison containment settings
- **InitialRoster (Class)**: Stores initial garrison unit template and count
- **GarrisonContain (Class)**: Core garrison containment logic
- **GarrisonPointData (Class)**: Data for individual garrison points
- **StationPointData (Class)**: Data for pre-assigned station points
- **GARRISON_INDEX_INVALID (Enum)**: Invalid garrison point index
- **MAX_GARRISON_POINTS (Enum)**: Maximum garrison points (40)

## Key Functions
### update
- Purpose: Called once per frame to update garrison logic
- Calls: Not inferable

### isValidContainerFor
- Purpose: Checks if object can be contained, forbidding containment if structure is really damaged
- Calls: Not inferable

### onBodyDamageStateChange
- Purpose: Handles state changes when structure is damaged
- Calls: Not inferable

### healObjects
- Purpose: Heals all objects within the garrison
- Calls: Not inferable

### redeployOccupants
- Purpose: Redeploys occupants at available garrison points
- Calls: Not inferable

## Globals
- None

## Dependencies
- `GameLogic/Module/OpenContain.h`
- `Common/ModelState.h`
- INI parsing utilities
- Memory pool and module macros

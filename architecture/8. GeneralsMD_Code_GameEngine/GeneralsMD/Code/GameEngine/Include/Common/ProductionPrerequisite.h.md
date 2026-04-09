# GeneralsMD/Code/GameEngine/Include/Common/ProductionPrerequisite.h

## Purpose
Defines the `ProductionPrerequisite` class for managing production requirements in the game, including science and unit prerequisites.

## Responsibilities
- Manage science and unit prerequisites for production.
- Resolve prerequisite names after template loading.
- Check if a player satisfies all prerequisites.
- Provide build facility template information.

## Key Types
- **ProductionPrerequisite (Class)**: Manages production prerequisites.
- **PrereqUnitRec (Struct)**: Stores unit prerequisite data (template, flags, name).
- **(anonymous enum)**: Flags for unit prerequisite logic (e.g., `UNIT_OR_WITH_PREV`).
- **MAX_PREREQ (Enum)**: Maximum number of prerequisites (32).

## Key Functions
### `addUnitPrereq`
- Purpose: Adds a unit prerequisite with optional "OR" logic.
- Calls: None visible.

### `resolveNames`
- Purpose: Resolves prerequisite names after template loading.
- Calls: None visible.

### `isSatisfied`
- Purpose: Checks if a player meets all prerequisites.
- Calls: `calcNumPrereqUnitsOwned`.

### `getExistingBuildFacilityTemplate`
- Purpose: Returns the build facility template if required and available.
- Calls: None visible.

## Globals
- None.

## Dependencies
- `ThingTemplate`, `Player` (forward declarations).
- `ScienceType`, `ScienceVec` (from `Science.h`).
- `AsciiString`, `UnicodeString` (from `GameCommon.h`).
- `std::vector`.

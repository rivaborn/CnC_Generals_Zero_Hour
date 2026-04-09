# GeneralsMD/Code/GameEngine/Include/GameClient/Module/SwayClientUpdate.h

## Purpose
Defines the `SwayClientUpdate` module for handling tree swaying effects in the game client.

## Responsibilities
- Manages tree swaying physics and rendering updates
- Handles client-side animation of swaying objects
- Provides module interface for tree sway behavior
- Implements memory pooling for performance

## Key Types
- **SwayClientUpdate (Class)**: Tree sway client update module
- **SwayClientUpdateMagicEnum (Enum)**: Not inferable
- **SwayClientUpdate_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### SwayClientUpdate::clientUpdate
- Purpose: Main client update callback for sway logic
- Calls: updateSway

### SwayClientUpdate::updateSway
- Purpose: Updates sway physics calculations
- Calls: Not inferable

### SwayClientUpdate::stopSway
- Purpose: Stops the swaying animation
- Calls: None

## Globals
- None

## Dependencies
- `Common/ClientUpdateModule.h`
- `Thing` (forward declared)
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`)
- Module macros (`MAKE_STANDARD_MODULE_MACRO`)

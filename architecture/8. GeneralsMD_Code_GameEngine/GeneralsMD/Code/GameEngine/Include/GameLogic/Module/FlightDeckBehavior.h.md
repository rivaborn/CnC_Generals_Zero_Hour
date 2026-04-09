# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/FlightDeckBehavior.h

## Purpose
Defines the flight deck behavior module for aircraft carriers, handling aircraft movement, parking, and launch/landing mechanics.

## Responsibilities
- Manages aircraft parking, takeoff, and landing on carrier runways
- Handles healing and defecting of parked units
- Controls ramp and catapult animations/effects
- Provides AI command processing for flight deck operations
- Maintains runway and parking space reservations

## Key Types
- **RunwayDefinition (Struct)**: Contains bone names and particle system for runway configuration
- **FlightDeckBehaviorModuleData (Class)**: Module data containing runway info, timing parameters, and healing values
- **FlightDeckBehavior (Class)**: Main behavior class implementing parking, exit, and die interfaces
- **FlightDeckInfo (Struct)**: Tracks parked aircraft position and orientation
- **RunwayInfo (Struct)**: Stores runway start/end points, taxi/creation locations, and reservation status
- **HealingInfo (Struct)**: Tracks healing progress for parked units

## Key Functions
### `reserveDoorForExit`
- Purpose: Reserves an exit door for an aircraft taking off
- Calls: Not inferable

### `exitObjectViaDoor`
- Purpose: Handles aircraft exiting via a runway
- Calls: Not inferable

### `update`
- Purpose: Updates flight deck state and aircraft positions
- Calls: `purgeDead`, `validateAssignments`, `propagateOrdersToPlanes`

### `onDie`
- Purpose: Handles carrier destruction cleanup
- Calls: `killAllParkedUnits`

### `aiDoCommand`
- Purpose: Processes AI commands for the flight deck
- Calls: Not inferable

## Globals
- **MAX_RUNWAYS (const)**: Maximum number of runways (2)

## Dependencies
- `BehaviorModule.h`, `DieModule.h`, `AIUpdate.h`
- `MultiIniFieldParse`, `INI`, `ThingTemplate`, `Object`, `Team`, `ParticleSystemTemplate`
- Memory pool and module macro definitions

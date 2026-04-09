# GeneralsMD/Code/GameEngine/Include/Common/Radar.h

## Purpose
Defines the radar subsystem for the game, including radar events, object visibility, and coordinate conversions.

## Responsibilities
- Manages radar object visibility and priorities
- Handles radar events (construction, attacks, etc.)
- Provides coordinate conversion between world and radar space
- Maintains shroud/fog of war state
- Controls radar display options (hidden/forced on)

## Key Types
- **RadarObject (Class)**: Represents objects displayed on the radar
- **RadarEventType (Enum)**: Types of radar events (construction, attack, etc.)
- **RadarPriorityType (Enum)**: Priority levels for radar object visibility
- **Radar (Class)**: Main radar subsystem interface
- **RadarEvent (Struct)**: Stores information about active radar events

## Key Functions
### `createEvent`
- Purpose: Creates a radar event at a world location
- Calls: `internalCreateEvent`

### `worldToRadar`
- Purpose: Converts world coordinates to radar coordinates
- Calls: None visible

### `addObject`
- Purpose: Adds an object to the radar display
- Calls: None visible

### `draw`
- Purpose: Renders the radar (pure virtual)
- Calls: None visible

## Globals
- **TheRadar (Radar*)**: Singleton instance of the radar subsystem

## Dependencies
- `GameWindow`, `Object`, `Player`, `TerrainLogic` (forward declarations)
- `Xfer`, `Snapshot`, `SubsystemInterface` (base classes)
- `Coord3D`, `ICoord2D`, `Color`, `RGBAColorInt` (types)
- `MemoryPoolObject` (base class for `RadarObject`)

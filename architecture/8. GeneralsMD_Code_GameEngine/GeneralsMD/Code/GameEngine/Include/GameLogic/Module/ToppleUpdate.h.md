# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ToppleUpdate.h

## Purpose
Defines the ToppleUpdate module for handling object toppling physics and collision behavior in the game.

## Responsibilities
- Manages toppling state (upright, falling, down)
- Applies toppling forces with configurable options
- Handles collision events during toppling
- Controls visual effects (FX) for toppling/bouncing
- Generates stump objects when toppled

## Key Types
- **ToppleUpdateModuleData (Class)**: Contains configuration data for toppling behavior (FX lists, velocities, kill flags).
- **ToppleState (Enum)**: Represents the three states of toppling (upright, falling, down).
- **ToppleUpdate (Class)**: Implements the toppling logic and collision interface.
- **FXList (Class)**: Reference to toppling/bounce effects (defined elsewhere).

## Key Functions
### `applyTopplingForce`
- Purpose: Initiates toppling with specified direction, speed, and options.
- Calls: Not inferable.

### `update`
- Purpose: Updates toppling state and physics each frame.
- Calls: Not inferable.

### `onCollide`
- Purpose: Handles collision events during toppling.
- Calls: Not inferable.

## Globals
- **TOPPLE_OPTIONS_NONE (Enum)**: No special options.
- **TOPPLE_OPTIONS_NO_BOUNCE (Enum)**: Disables bouncing on ground impact.
- **TOPPLE_OPTIONS_NO_FX (Enum)**: Disables visual effects.

## Dependencies
- `BehaviorModule.h`, `CollideModule.h`, `UpdateModule.h`
- `MultiIniFieldParse`, `AsciiString`, `Coord3D`, `ObjectID`, `Thing`, `Object` (external types).

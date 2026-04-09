# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Die/CrushDie.cpp - Enhanced Analysis

## Architectural Role
This file implements the crush damage system, bridging physics collision detection with visual/audio feedback. It's part of the damage/destruction pipeline, handling post-collision effects when objects are crushed by vehicles.

## Cross-References
### Incoming
- Called by damage system when crush damage is applied
- Used by physics collision resolution code

### Outgoing
- Calls `BodyModule` to update crushed state
- Uses `Drawable` to update model conditions
- Accesses `TheAudio` for sound effects
- Queries `GameLogic` for object references

## Design Patterns
- **Strategy Pattern**: `CrushDie` extends `DieModule` as a specific damage strategy
- **State Pattern**: Updates object state via `BodyModule` and `Drawable`
- **Factory Pattern**: Relies on `ThingFactory` for object creation (inferred from dependencies)

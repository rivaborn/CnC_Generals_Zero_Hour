# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/MinefieldBehavior.h

## Purpose
Defines the minefield behavior module for the game, handling minefield logic, collisions, damage, and detonation.

## Responsibilities
- Manages minefield behavior including detonation, regeneration, and immunity tracking
- Handles collisions with objects and determines detonation conditions
- Implements damage and healing logic for minefields
- Controls minefield movement and scooting behavior
- Manages virtual mines and creator death checks

## Key Types
- **MinefieldBehaviorModuleData (Class)**: Configuration data for minefield behavior
- **MinefieldBehavior (Class)**: Main minefield behavior module implementing multiple interfaces
- **MinefieldBehaviorMagicEnum (Enum)**: Not inferable
- **MinefieldBehavior_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable
- **ImmuneInfo (Struct)**: Tracks objects immune to minefield detonation
- **DetonatorInfo (Struct)**: Stores information about detonators

## Key Functions
### MinefieldBehavior::onDamage
- Purpose: Handles damage events for the minefield
- Calls: Not inferable

### MinefieldBehavior::onDie
- Purpose: Handles minefield destruction events
- Calls: Not inferable

### MinefieldBehavior::update
- Purpose: Updates minefield state each frame
- Calls: Not inferable

### MinefieldBehavior::onCollide
- Purpose: Handles collision events with other objects
- Calls: Not inferable

### MinefieldBehavior::detonateOnce
- Purpose: Triggers a single minefield detonation
- Calls: Not inferable

## Globals
- None

## Dependencies
- GameLogic/Module/BehaviorModule.h
- GameLogic/Module/CollideModule.h
- GameLogic/Module/UpdateModule.h
- GameLogic/Module/Damage

# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/PropagandaCenterBehavior.h

## Purpose
Defines the PropagandaCenterBehavior class, which handles brainwashing mechanics for a propaganda center in the game.

## Responsibilities
- Manages brainwashing duration and tracking of brainwashed units
- Handles updates and removal of brainwashed objects
- Extends PrisonBehavior functionality for propaganda-specific behavior

## Key Types
- **PropagandaCenterBehaviorModuleData (Class)**: Module data for propaganda center, including brainwash duration
- **PropagandaCenterBehavior (Class)**: Behavior class for propaganda center, managing brainwashing logic
- **BrainwashedIDList (Typedef)**: List of ObjectIDs representing brainwashed units

## Key Functions
### PropagandaCenterBehavior::update
- Purpose: Updates brainwashing state and manages brainwashed units
- Calls: Not inferable

### PropagandaCenterBehavior::onRemoving
- Purpose: Handles removal of brainwashed objects
- Calls: Not inferable

## Globals
- None

## Dependencies
- PrisonBehavior.h (inheritance)
- MultiIniFieldParse (for field parsing)
- std::list (for BrainwashedIDList)
- ObjectID (game object identifier)
- UnsignedInt (for duration tracking)

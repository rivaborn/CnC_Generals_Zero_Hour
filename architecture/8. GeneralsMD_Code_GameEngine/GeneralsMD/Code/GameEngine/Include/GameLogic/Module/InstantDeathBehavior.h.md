# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/InstantDeathBehavior.h

## Purpose
Defines the `InstantDeathBehavior` module for handling instant death effects in the game.

## Responsibilities
- Manages instant death behavior for game objects
- Handles death effects (FX, object creation, weapons)
- Integrates with the game's module system
- Provides data structure for death behavior configuration

## Key Types
- `InstantDeathBehaviorModuleData` (Class): Stores death behavior configuration (FX, OCLs, weapons)
- `InstantDeathBehavior` (Class): Implements the instant death behavior module
- `FXListVec` (Class): Vector of FXList pointers
- `OCLVec` (Class): Vector of ObjectCreationList pointers
- `WeaponTemplateVec` (Class): Vector of WeaponTemplate pointers

## Key Functions
### `InstantDeathBehavior::onDie`
- Purpose: Handles death behavior when an object dies
- Calls: Not inferable (implementation in .cpp)

## Globals
- None

## Dependencies
- `DieModule.h` (include)
- `FXList`, `ObjectCreationList`, `WeaponTemplate`, `DamageInfo` (external classes)
- `std::vector` (STL)
- `MultiIniFieldParse` (for field parsing)

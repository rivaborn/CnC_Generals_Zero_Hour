# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/BunkerBusterBehavior.h

## Purpose
Defines the BunkerBusterBehavior module, which handles bunker destruction logic and damage to garrisoned units.

## Responsibilities
- Manages bunker destruction behavior
- Applies damage to garrisoned units
- Handles detonation effects and shockwaves
- Updates and responds to object death events

## Key Types
- **BunkerBusterBehaviorModuleData (Class)**: Contains configuration data for the bunker buster behavior
- **BunkerBusterBehavior (Class)**: Implements the bunker destruction behavior module
- **BunkerBusterBehaviorMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **FXList (Class)**: Reference to explosion/effect list (external)
- **UpgradeTemplate (Class)**: Reference to upgrade requirements (external)

## Key Functions
### BunkerBusterBehavior::update
- Purpose: Updates the bunker buster behavior state
- Calls: Not inferable

### BunkerBusterBehavior::onDie
- Purpose: Handles object death and triggers bunker destruction
- Calls: bustTheBunker

### BunkerBusterBehavior::bustTheBunker
- Purpose: Executes the bunker destruction logic and damage application
- Calls: Not inferable

## Globals
- None

## Dependencies
- BehaviorModule.h, UpdateModule.h, DieModule.h
- FXList.h (external)
- MultiIniFieldParse (external)
- AsciiString, UnsignedInt, Real, WeaponTemplate, ObjectID (external types)

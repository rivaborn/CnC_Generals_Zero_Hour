# GeneralsMD/Code/GameEngine/Include/GameLogic/Object.h

## Purpose
Defines the core `Object` class, representing game entities like units, buildings, and projectiles in the SAGE engine.

## Responsibilities
- Manages object state, team affiliation, and relationships
- Handles damage, healing, and special abilities
- Provides interfaces for modules (behavior, physics, etc.)
- Tracks experience, veterancy, and command sets
- Manages weapon systems and targeting logic

## Key Types
- **Object (Class)**: Core game entity class
- **TTriggerInfo (Struct)**: Tracks trigger area interactions
- **CrushSquishTestType (Enum)**: Defines crush/squish test modes
- **ObjectPrivateStatusBits (Enum)**: Internal object status flags
- **CommandSourceType (Enum)**: Source of commands (player/AI)
- **SpecialPowerType (Enum)**: Types of special abilities
- **WeaponSetType (Enum)**: Weapon set configuration flags
- **ArmorSetType (Enum)**: Armor set configuration flags
- **WeaponStatus (Enum)**: Weapon operational states
- **RadarPriorityType (Enum)**: Radar display priorities
- **CanAttackResult (Enum)**: Attack capability results

## Key Functions
### `attemptDamage`
- Purpose: Applies damage to the object
- Calls: Damage module handlers

### `doSpecialPower`
- Purpose: Executes a special ability
- Calls: Special power module interfaces

### `chooseBestWeaponForTarget`
- Purpose: Selects optimal weapon for a target
- Calls: Weapon evaluation logic

### `setTeam`
- Purpose: Changes object team affiliation
- Calls: Team management and relationship updates

### `getAbleToAttackSpecificObject`
- Purpose: Determines if object can attack target
- Calls: Weapon and targeting checks

## Globals
- **TheObjectIDToDebug (ObjectID)**: Debugging identifier (debug builds only)

## Dependencies
- **Common/Geometry.h**: Geometry utilities
- **Common/Snapshot.h**: Snapshot serialization
- **GameLogic/Damage.h**: Damage handling
- **GameLogic/WeaponSet.h**: Weapon management
- **GameClient/Color.h**: Color definitions
- **GameLogic/Module/StealthUpdate.h**: Stealth behavior
- Forward declarations for module interfaces (AI, physics, etc.)

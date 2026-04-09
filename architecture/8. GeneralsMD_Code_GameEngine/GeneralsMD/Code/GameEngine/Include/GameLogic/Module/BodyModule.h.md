# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/BodyModule.h

## Purpose
Defines the BodyModule system for handling object health, damage, and damage states in the SAGE engine.

## Responsibilities
- Manages object health, damage, and healing mechanics
- Handles damage states (pristine, damaged, destroyed)
- Provides damage estimation for AI targeting
- Tracks damage history and visual conditions

## Key Types
- **WeaponTemplate (Class)**: Not inferable (forward declaration)
- **BodyDamageType (Enum)**: Damage state enumeration (pristine, damaged, destroyed, rubble)
- **MaxHealthChangeType (Enum)**: Health modification types (preserve ratio, absolute change)
- **BodyModuleData (Class)**: Module data container
- **BodyModuleInterface (Class)**: Pure virtual interface for body module functionality
- **BodyModule (Class)**: Base implementation of body module with health management

## Key Functions
### attemptDamage
- Purpose: Applies damage to object considering armor and damage effects
- Calls: Not inferable (pure virtual)

### attemptHealing
- Purpose: Applies healing to object
- Calls: Not inferable (pure virtual)

### estimateDamage
- Purpose: Calculates potential damage without applying it (for AI targeting)
- Calls: Not inferable (pure virtual)

### internalChangeHealth
- Purpose: Directly modifies health bypassing armor/damage effects
- Calls: Not inferable (pure virtual)

## Globals
- **TheBodyDamageTypeNames (const char**)**: String names for damage states
- **TheMaxHealthChangeTypeNames (const char**)**: String names for health change types

## Dependencies
- Common/Module.h
- GameLogic/Damage.h
- GameLogic/ArmorSet.h
- GameLogic/Module/BehaviorModule.h

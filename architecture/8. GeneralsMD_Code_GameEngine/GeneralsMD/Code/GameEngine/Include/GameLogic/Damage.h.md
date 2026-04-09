# GeneralsMD/Code/GameEngine/Include/GameLogic/Damage.h

## Purpose
Defines damage and death types, flags, and data structures for damage calculation in the game engine.

## Responsibilities
- Declares damage and death type enums
- Provides bit flag manipulation utilities for damage types
- Defines input/output structures for damage calculation
- Establishes damage info container class

## Key Types
- DamageType (Enum): enumerates all possible damage types (explosion, crush, radiation, etc.)
- DeathType (Enum): enumerates all possible death types (normal, burned, exploded, etc.)
- DamageTypeFlags (Class): bit flag wrapper for damage types
- DeathTypeFlags (Class): bit flag wrapper for death types
- DamageInfoInput (Class): input parameters for damage calculation
- DamageInfoOutput (Class): output results from damage calculation
- DamageInfo (Class): container combining input and output damage data

## Key Functions
### getDamageTypeFlag
- Purpose: checks if a damage type flag is set
- Calls: BitFlags::test

### setDamageTypeFlag
- Purpose: sets a damage type flag
- Calls: BitFlags::set

### clearDamageTypeFlag
- Purpose: clears a damage type flag
- Calls: BitFlags::set

### IsSubdualDamage
- Purpose: checks if damage type is a subdual type
- Calls: None

### IsHealthDamagingDamage
- Purpose: checks if damage type affects health
- Calls: None

### initDamageTypeFlags
- Purpose: initializes global damage type flags
- Calls: None

### getDeathTypeFlag
- Purpose: checks if a death type flag is set
- Calls: None

### setDeathTypeFlag
- Purpose: sets a death type flag
- Calls: None

### clearDeathTypeFlag
- Purpose: clears a death type flag
- Calls: None

## Globals
- DAMAGE_TYPE_FLAGS_NONE (DamageTypeFlags): flag with no bits set
- DAMAGE_TYPE_FLAGS_ALL (DamageTypeFlags): flag with all bits set
- DEATH_TYPE_FLAGS_ALL (DeathTypeFlags): flag with all death bits set
- DEATH_TYPE_FLAGS_NONE (DeathTypeFlags): flag with no death bits set
- HUGE_DAMAGE_AMOUNT (Real): constant for large damage value

## Dependencies
- Common/BitFlags.h
- Common/GameType.h
- Common/ObjectStatusTypes.h
- Common/Snapshot.h
- Object, INI, ThingTemplate (forward declarations)

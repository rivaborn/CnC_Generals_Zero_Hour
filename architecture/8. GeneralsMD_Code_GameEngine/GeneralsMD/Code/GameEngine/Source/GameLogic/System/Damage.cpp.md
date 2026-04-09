# GeneralsMD/Code/GameEngine/Source/GameLogic/System/Damage.cpp

## Purpose
Handles damage-related structures and serialization for the game's damage system.

## Responsibilities
- Defines damage type flags and their serialization
- Implements Xfer methods for damage-related classes
- Initializes global damage type flag constants

## Key Types
- **DamageTypeFlags (struct)**: Bitmask for damage types (e.g., EXPLOSION, CRUSH)
- **DamageInfo (struct)**: Container for damage input/output data
- **DamageInfoInput (struct)**: Input parameters for damage (source, type, amount)
- **DamageInfoOutput (struct)**: Output results of damage application

## Key Functions
### `initDamageTypeFlags()`
- Purpose: Initializes global damage type flags to all bits set
- Calls: `SET_ALL_DAMAGE_TYPE_BITS()`

### `DamageInfo::xfer()`
- Purpose: Serializes DamageInfo structure
- Calls: `xferSnapshot()`

### `DamageInfoInput::xfer()`
- Purpose: Serializes damage input parameters
- Calls: `xferObjectID()`, `xferUser()`, `xferReal()`, `xferBool()`, `xferCoord3D()`, `xferAsciiString()`

### `DamageInfoOutput::xfer()`
- Purpose: Serializes damage output results
- Calls: `xferReal()`, `xferBool()`

## Globals
- **DAMAGE_TYPE_FLAGS_NONE (DamageTypeFlags)**: Zero-initialized flags
- **DAMAGE_TYPE_FLAGS_ALL (DamageTypeFlags)**: All bits set (initialized by `initDamageTypeFlags()`)

## Dependencies
- `Xfer.h`, `Damage.h`, `BitFlagsIO.h`, `ThingFactory.h`, `ThingTemplate.h`
- `TheThingFactory` (global ThingFactory instance)

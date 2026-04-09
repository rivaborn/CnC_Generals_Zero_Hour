# GeneralsMD/Code/GameEngine/Include/GameClient/FXList.h

## Purpose
Defines the FXList system for managing audio/video effects in the game.

## Responsibilities
- Declares `FXNugget` (effect components) and `FXList` (effect collections)
- Provides `FXListStore` for global FXList management
- Defines interfaces for playing effects at positions or on objects

## Key Types
- **FXNugget (Class)**: Abstract base class for individual effects (sound/video)
- **FXList (Class)**: Container for multiple FXNuggets representing a complete effect
- **FXListStore (Class)**: Global store/manager for all FXLists
- **FXNuggetMagicEnum (Enum)**: Not inferable (likely internal implementation detail)
- **FXNuggetList (Class)**: Typedef for `std::list<FXNugget*>` (internal storage)

## Key Functions
### FXNugget::doFXPos
- Purpose: Play effect at a 3D position
- Calls: None (pure virtual)

### FXNugget::doFXObj
- Purpose: Play effect on an object (defaults to position-based)
- Calls: `doFXPos`

### FXList::doFXPos
- Purpose: Execute all nuggets' position-based effects
- Calls: Each nugget's `doFXPos`

### FXList::doFXObj
- Purpose: Execute all nuggets' object-based effects
- Calls: Each nugget's `doFXObj`

### FXListStore::findFXList
- Purpose: Retrieve an FXList by name
- Calls: None

### FXListStore::parseFXListDefinition
- Purpose: Load FXList definitions from INI files
- Calls: None

## Globals
- **TheFXListStore (FXListStore*)**: Global instance of the FXList store

## Dependencies
- `Common/GameMemory.h`, `Common/NameKeyGenerator.h`, `Common/STLTypedefs.h`
- `std::list`, `std::hash_map` (STL)
- Forward references: `INI`, `Object`, `Matrix3D`

# GeneralsMD/Code/GameEngine/Source/Common/System/Xfer.cpp

## Purpose
Implements the Xfer system for serializing/deserializing data blocks, supporting file I/O, CRC computation, and versioning.

## Responsibilities
- Provides low-level data transfer methods for primitive types and game-specific structures
- Handles versioning and compatibility checks for saved/loaded data
- Supports different transfer modes (save, load, CRC)
- Manages complex data types like vectors, lists, and bitmasks
- Converts between internal and portable map paths

## Key Types
- `Xfer` (Class): Base class for data transfer operations
- `XferVersion` (Type): Version identifier for serialized data
- `XferMode` (Enum): Transfer operation mode (save/load/CRC)

## Key Functions
### `xferImplementation`
- Purpose: Abstract method for actual data transfer implementation
- Calls: None (pure virtual)

### `xferVersion`
- Purpose: Transfers version data with validation
- Calls: `xferImplementation`

### `xferMapName`
- Purpose: Handles map path conversion during transfer
- Calls: `xferAsciiString`, `TheGameState->realMapPathToPortableMapPath`, `TheGameState->portableMapPathToRealMapPath`

### `xferScienceType`
- Purpose: Serializes ScienceType using string names
- Calls: `xferAsciiString`, `TheScienceStore->getInternalNameForScience`, `TheScienceStore->getScienceFromInternalName`

### `xferUpgradeMask`
- Purpose: Transfers upgrade bitmasks using upgrade names
- Calls: `xferAsciiString`, `TheUpgradeCenter->firstUpgradeTemplate`, `TheUpgradeCenter->findUpgrade`

## Globals
- `TheGameState` (GameState*): Global game state reference
- `TheScienceStore` (ScienceStore*): Global science store reference
- `TheUpgradeCenter` (UpgradeCenter*): Global upgrade center reference

## Dependencies
- `Common/Xfer.h`, `Common/GameState.h`, `Common/Upgrade.h`, `Common/BitFlagsIO.h`
- `PreRTS.h` (engine precompiled header)
- STL containers (`vector`, `list`)
- Game-specific types (`ScienceType`, `UpgradeMaskType`, `KindOfType`)

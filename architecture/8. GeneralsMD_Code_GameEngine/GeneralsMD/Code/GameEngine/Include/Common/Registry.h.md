# GeneralsMD/Code/GameEngine/Include/Common/Registry.h

## Purpose
Header file defining an interface for reading registry values in the SAGE engine.

## Responsibilities
- Declares functions for retrieving string and unsigned integer values from the Windows registry.
- Provides convenience functions for common registry keys (language, game name, version, map pack version).
- Supports both Generals and Zero Hour registry paths.

## Key Types
None

## Key Functions
### GetStringFromGeneralsRegistry
- Purpose: Retrieves a string value from the original Generals registry.
- Calls: Not inferable

### GetStringFromRegistry
- Purpose: Retrieves a string value from the registry.
- Calls: Not inferable

### GetUnsignedIntFromRegistry
- Purpose: Retrieves an unsigned integer value from the registry.
- Calls: Not inferable

### GetRegistryLanguage
- Purpose: Convenience function to get the language setting from the registry.
- Calls: Not inferable

### GetRegistryGameName
- Purpose: Convenience function to get the game name from the registry.
- Calls: Not inferable

### GetRegistryVersion
- Purpose: Convenience function to get the game version from the registry.
- Calls: Not inferable

### GetRegistryMapPackVersion
- Purpose: Convenience function to get the map pack version from the registry.
- Calls: Not inferable

## Globals
None

## Dependencies
- `Common/AsciiString.h`: For string handling.
- `Bool`, `UnsignedInt`: Basic types likely from engine headers.

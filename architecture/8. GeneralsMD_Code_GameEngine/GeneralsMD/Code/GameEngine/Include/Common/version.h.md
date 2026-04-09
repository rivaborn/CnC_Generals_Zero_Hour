# GeneralsMD/Code/GameEngine/Include/Common/version.h

## Purpose
Defines the `Version` class for managing and retrieving game version information.

## Responsibilities
- Stores version components (major, minor, build numbers)
- Provides formatted version strings (ASCII/Unicode)
- Tracks build metadata (time, location, user)
- Manages display preferences for version info

## Key Types
- **Version (Class)**: Encapsulates game version and build metadata.

## Key Functions
### `Version()`
- Purpose: Default constructor.
- Calls: Not inferable.

### `getVersionNumber()`
- Purpose: Returns a 4-byte integer for WOLAPI compatibility.
- Calls: Not inferable.

### `getAsciiVersion()`, `getUnicodeVersion()`, `getFullUnicodeVersion()`
- Purpose: Returns human-readable version strings in different formats.
- Calls: Not inferable.

### `getAsciiBuildTime()`, `getUnicodeBuildTime()`, `getAsciiBuildLocation()`, `getUnicodeBuildLocation()`, `getAsciiBuildUser()`, `getUnicodeBuildUser()`
- Purpose: Retrieves formatted build metadata strings.
- Calls: Not inferable.

### `setVersion()`
- Purpose: Initializes version and build metadata.
- Calls: Not inferable.

## Globals
- **TheVersion (Version*)**: Singleton instance of the `Version` class.

## Dependencies
- `UnsignedInt`, `AsciiString`, `UnicodeString`, `Bool`, `Int` (external types)
- No external symbols defined here.

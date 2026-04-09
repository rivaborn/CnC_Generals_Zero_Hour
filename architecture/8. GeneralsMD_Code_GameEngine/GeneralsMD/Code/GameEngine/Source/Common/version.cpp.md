# GeneralsMD/Code/GameEngine/Source/Common/version.cpp

## Purpose
Manages game version information, including build metadata and localization.

## Responsibilities
- Stores version numbers (major, minor, build, local build)
- Provides formatted version strings (ASCII/Unicode)
- Handles build metadata (user, location, time/date)
- Supports debug/internal build flags

## Key Types
- **Version (Class)**: Central version information container
- **TheVersion (Version*)**: Global singleton instance

## Key Functions
### `setVersion`
- Purpose: Initializes version fields with build metadata
- Calls: None

### `getVersionNumber`
- Purpose: Returns packed major/minor version as 32-bit integer
- Calls: None

### `getAsciiVersion`
- Purpose: Formats version string for ASCII output
- Calls: `format` (AsciiString)

### `getUnicodeVersion`
- Purpose: Formats localized Unicode version string
- Calls: `TheGameText->fetch`, `format` (UnicodeString)

### `getFullUnicodeVersion`
- Purpose: Returns extended Unicode version with build details
- Calls: `TheGameText->fetch`, `format` (UnicodeString)

### `getAsciiBuildTime`
- Purpose: Combines build date/time into ASCII string
- Calls: `format` (AsciiString)

### `getUnicodeBuildTime`
- Purpose: Returns localized Unicode build time string
- Calls: `translate` (UnicodeString), `TheGameText->fetch`, `format`

## Globals
- **TheVersion (Version*)**: Global singleton instance

## Dependencies
- `PreRTS.h`, `GameText.h`, `Version.h`
- `AsciiString`, `UnicodeString` classes
- `TheGameText` (GameText singleton)

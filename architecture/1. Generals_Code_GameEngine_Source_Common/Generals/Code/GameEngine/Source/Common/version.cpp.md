# Generals/Code/GameEngine/Source/Common/version.cpp

## Purpose
This file contains the implementation of the `Version` class, which manages version information for the Command & Conquer Generals game.

## Responsibilities
- Manages and stores version details such as major, minor, build number, and local build number.
- Provides methods to set and retrieve version information in both ASCII and Unicode formats.
- Includes debug and internal build information based on compilation flags.

## Key Types
- `Version` (Class): Stores and manages version information for the game.

## Key Functions
### Version::setVersion
- Purpose: Sets the version details including major, minor, build number, local build number, user, location, build time, and build date.
- Calls: None

### Version::getAsciiVersion
- Purpose: Returns the version as an ASCII string in a formatted manner based on debug or internal flags.
- Calls: `AsciiString::format`

### Version::getUnicodeVersion
- Purpose: Returns the version as a Unicode string with additional debug and internal information if applicable.
- Calls: `TheGameText->fetch`, `UnicodeString::format`, `UnicodeString::concat`

### Version::getFullUnicodeVersion
- Purpose: Returns the full version as a Unicode string without any conditional formatting.
- Calls: `TheGameText->fetch`, `UnicodeString::format`, `UnicodeString::concat`

### Version::getAsciiBuildTime
- Purpose: Returns the build time and date as an ASCII string.
- Calls: `AsciiString::format`

### Version::getUnicodeBuildTime
- Purpose: Returns the build time and date as a Unicode string.
- Calls: `TheGameText->fetch`, `AsciiString::translate`, `UnicodeString::format`

### Version::getAsciiBuildLocation
- Purpose: Returns the build location as an ASCII string.
- Calls: None

### Version::getUnicodeBuildLocation
- Purpose

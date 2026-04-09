# GeneralsMD/Code/GameEngine/Source/Common/INI/INI.cpp

## Purpose
Handles parsing of INI configuration files for the game, including game data, assets, and settings.

## Responsibilities
- Parses INI blocks and fields using a type registry
- Loads INI files from directories (recursively if needed)
- Validates INI file names and content
- Provides utility functions for scanning INI values (ints, reals, etc.)

## Key Types
- **BlockParse (struct)**: Maps INI block tokens to their parsing functions
- **INI (class)**: Main INI parser class (defined elsewhere)

## Key Functions
### `findBlockParse`
- Purpose: Looks up the parsing function for a given INI block token
- Calls: None (direct)

### `findFieldParse`
- Purpose: Looks up the parsing function for a given INI field token
- Calls: None (direct)

### `parseGameClientRandomVariable`
- Purpose: Parses random variable definitions (low/high values and distribution)
- Calls: `INI::scanReal`, `INI::scanIndexList`

### `parseDurationReal`
- Purpose: Parses duration values in milliseconds and converts to frames
- Calls: `ConvertDurationFromMsecsToFrames`

### `parseVeterancyLevelFlags`
- Purpose: Parses veterancy level flag definitions
- Calls: `INI::scanIndexList`, `setVeterancyLevelFlag`, `clearVeterancyLevelFlag`

## Globals
- **s_xfer (Xfer*)**: Global transfer object for INI loading
- **theTypeTable (BlockParse[])**: Registry of INI block types and their parsers

## Dependencies
- Key includes: `INI.h`, `INIException.h`, `File.h`, `FileSystem.h`, `Xfer.h`
- External symbols: `TheFileSystem`, `TheVeterancyNames`, `TheDeathNames`, `ConvertDurationFromMsecsToFrames`, etc.

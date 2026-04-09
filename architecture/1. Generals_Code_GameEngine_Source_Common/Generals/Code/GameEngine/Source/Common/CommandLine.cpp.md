# Generals/Code/GameEngine/Source/Common/CommandLine.cpp

## Purpose
This file handles parsing command-line arguments for the Command & Conquer Generals game, setting various configuration options based on user input.

## Responsibilities
- Parsing command-line parameters.
- Setting global flags and configurations.
- Handling debug and non-debug specific options.
- Loading mods based on command-line arguments.

## Key Types
- **FuncPtr (Class)**: Function pointer type for handling different command-line parameters.
- **CommandLineParam (Class)**: Structure to map command-line parameter names to their corresponding handler functions.

## Key Functions
### parseCommandLine
- Purpose: Parses command-line arguments and sets global configurations accordingly.
- Calls:
  - `params[param].func(argv+arg, argc-arg)`

### ConvertShortMapPathToLongMapPath
- Purpose: Converts a short map path to a long map path by appending directory names until a valid `.map` file is found.
- Calls: None

## Globals
- **TheDebugIgnoreSyncErrors (Bool)**: Flag to ignore sync errors during debugging.
- **DX8Wrapper_PreserveFPU (Int)**: External variable related to FPU preservation.
- **F_NOCASE (UnsignedByte)**: Constant for case-insensitive string comparison.
- **params (CommandLineParam[])**: Array of command-line parameter mappings.

## Dependencies
- Key includes:
  - "Common/ArchiveFileSystem.h"
  - "Common/CommandLine.h"
  - "Common/CRCDebug.h"
  - "Common/LocalFileSystem.h"
  - "Common/Version.h"
  - "GameClient/TerrainVisual.h"
  - "GameClient/GameText.h"

- External symbols used:
  - `TheWritableGlobalData`
  - `TheVersion`
  - `TheLocalFileSystem`
  - `TheArchiveFileSystem`

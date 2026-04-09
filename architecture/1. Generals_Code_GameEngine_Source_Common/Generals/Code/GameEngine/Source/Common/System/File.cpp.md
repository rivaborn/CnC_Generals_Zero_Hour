# Generals/Code/GameEngine/Source/Common/System/File.cpp

## Purpose
This file contains the implementation of a basic file handling class, `File`, which provides methods for opening, closing, reading, writing, and managing file operations in the Command & Conquer Generals game engine.

## Responsibilities
- Manage file open/close states.
- Handle file access modes (read, write, append).
- Provide methods to read/write data and determine file size.
- Support text and binary file formats.

## Key Types
- `File` (Class): Manages file operations such as opening, closing, reading, writing, and determining file size.

## Key Functions
### File::open
- Purpose: Opens a file with specified access modes.
- Calls: None

### File::close
- Purpose: Closes the file and resets internal state.
- Calls: None

### File::size
- Purpose: Returns the size of the file.
- Calls: `seek`

### File::position
- Purpose: Returns the current position in the file.
- Calls: `seek`

### File::print
- Purpose: Writes formatted text to the file.
- Calls: `vsprintf`, `write`

## Globals
None

## Dependencies
- Key includes:
  - `<assert.h>`
  - `<string.h>`
  - `<stdarg.h>`
  - `<stdio.h>`
  - `"Common/File.h"`

- External symbols used but not defined here:
  - `Char`
  - `Int`
  - `Bool`
  - `NONE`
  - `STREAMING`
  - `WRITE`
  - `TEXT`
  - `BINARY`
  - `READ`
  - `APPEND`
  - `TRUNCATE`

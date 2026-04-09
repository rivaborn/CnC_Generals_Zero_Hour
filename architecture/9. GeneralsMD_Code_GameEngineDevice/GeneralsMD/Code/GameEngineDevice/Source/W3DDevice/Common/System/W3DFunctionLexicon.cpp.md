# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/Common/System/W3DFunctionLexicon.cpp

## Purpose
Defines function lexicon for W3D-specific function pointers, registering draw and init callbacks for game UI elements.

## Responsibilities
- Registers W3D-specific draw functions for UI gadgets and menus
- Registers W3D-specific layout initialization functions
- Extends base FunctionLexicon with W3D-specific entries
- Provides init/reset/update lifecycle methods

## Key Types
- `W3DFunctionLexicon` (Class): Manages W3D function registrations
- `TableEntry` (Struct): Function name-pointer mapping
- `gameWinDrawTable` (Array): Draw function registrations
- `layoutInitTable` (Array): Init function registrations

## Key Functions
### `W3DFunctionLexicon::init`
- Purpose: Initializes W3D-specific function tables
- Calls: `FunctionLexicon::init`, `loadTable`

### `W3DFunctionLexicon::reset`
- Purpose: Resets W3D function registrations
- Calls: `FunctionLexicon::reset`

### `W3DFunctionLexicon::update`
- Purpose: Updates W3D function registrations
- Calls: `FunctionLexicon::update`

## Globals
- `gameWinDrawTable` (TableEntry[]): Draw function mappings
- `layoutInitTable` (TableEntry[]): Init function mappings

## Dependencies
- `FunctionLexicon` (base class)
- `GameWinDefaultDraw`, `W3DGameWinDefaultDraw`, etc. (draw functions)
- `W3DMainMenuInit` (init function)
- `NAMEKEY_INVALID` (constant)

# Generals/Code/GameEngineDevice/Source/W3DDevice/Common/System/W3DFunctionLexicon.cpp

## Purpose
Defines function lexicon for W3D-specific function pointers, including UI drawing and layout initialization methods.

## Responsibilities
- Registers W3D-specific function tables
- Manages game window draw methods
- Manages layout initialization methods
- Extends base FunctionLexicon functionality

## Key Types
- `W3DFunctionLexicon` (Class): Manages W3D function lexicon
- `TableEntry` (Struct): Function pointer entry (from FunctionLexicon)

## Key Functions
### `W3DFunctionLexicon::init`
- Purpose: Initializes W3D-specific function tables
- Calls: `FunctionLexicon::init`, `loadTable`

### `W3DFunctionLexicon::reset`
- Purpose: Resets function lexicon state
- Calls: `FunctionLexicon::reset`

### `W3DFunctionLexicon::update`
- Purpose: Updates function lexicon state
- Calls: `FunctionLexicon::update`

## Globals
- `gameWinDrawTable` (TableEntry[]): UI drawing function pointers
- `layoutInitTable` (TableEntry[]): Layout initialization function pointers

## Dependencies
- `FunctionLexicon` (base class)
- `GameWindow.h`, `W3DFunctionLexicon.h`, `W3DGUICallbacks.h`, `W3DGameWindow.h`, `W3DGadget.h`

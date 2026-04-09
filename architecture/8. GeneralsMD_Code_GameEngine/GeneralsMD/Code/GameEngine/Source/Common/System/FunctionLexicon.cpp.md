# GeneralsMD/Code/GameEngine/Source/Common/System/FunctionLexicon.cpp

## Purpose
Manages a dictionary of function pointers for UI callbacks and game window operations in the SAGE engine.

## Responsibilities
- Registers and validates function pointers for UI components
- Provides lookup methods to retrieve functions by name key
- Maintains tables for different UI operation types (draw, system, input, etc.)

## Key Types
- FunctionLexicon (Class): Main class managing function pointer tables
- TableEntry (Struct): Entry in function tables containing name, key, and function pointer

## Key Functions
### FunctionLexicon::init
- Purpose: Initializes all function tables and validates entries
- Calls: loadTable, validate

### FunctionLexicon::findFunction
- Purpose: Searches tables for a function matching the given key
- Calls: keyToFunc

### FunctionLexicon::validate
- Purpose: Checks for duplicate function addresses in tables
- Calls: None

### gameWinDrawFunc
- Purpose: Retrieves draw function by key
- Calls: findFunction

### winLayoutInitFunc
- Purpose: Retrieves layout init function by key
- Calls: findFunction

## Globals
- TheFunctionLexicon (FunctionLexicon*): Global instance of the function lexicon
- gameWinDrawTable (TableEntry[]): Table of draw functions
- gameWinSystemTable (TableEntry[]): Table of system message handlers
- gameWinInputTable (TableEntry[]): Table of input handlers
- gameWinTooltipTable (TableEntry[]): Table of tooltip handlers
- winLayoutInitTable (TableEntry[]): Table of layout initialization functions
- winLayoutUpdateTable (TableEntry[]): Table of layout update functions
- winLayoutShutdownTable (TableEntry[]): Table of layout shutdown functions

## Dependencies
- FunctionLexicon.h (header)
- GameWindow.h, GameWindowManager.h, GUICallbacks.h, Gadget.h (UI components)
- PreRTS.h (engine precompiled header)
- NameKeyGenerator (external symbol for name key generation)

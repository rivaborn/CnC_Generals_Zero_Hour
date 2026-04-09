# GeneralsMD/Code/GameEngine/Include/GameClient/Shell.h

## Purpose
Manages the shell menu system, including screen layouts, animations, and stack-based navigation.

## Responsibilities
- Manages a stack of window layouts for menu screens
- Handles push/pop operations with shutdown/initialization callbacks
- Controls shell animations and transitions
- Maintains menu schemes and special layouts (options, save/load)

## Key Types
- **Shell (Class)**: Main shell manager handling menu navigation and layout stack
- **WindowLayout (Class)**: Represents individual menu screens (forward reference)
- **AnimateWindowManager (Class)**: Manages window animations (forward reference)
- **ShellMenuSchemeManager (Class)**: Handles menu color schemes (forward reference)
- **AnimTypes (Enum)**: Animation types for windows

## Key Functions
### Shell::push
- Purpose: Load a new screen layout onto the stack
- Calls: doPush, shutdownComplete

### Shell::pop
- Purpose: Remove the top layout from the stack
- Calls: doPop, shutdownComplete

### Shell::shutdownComplete
- Purpose: Notify shell that a layout has finished shutting down
- Calls: doPush, doPop

### Shell::update
- Purpose: Update all layouts in the stack
- Calls: WindowLayout::update (inferred)

## Globals
- **TheShell (Shell*)**: Global shell interface instance

## Dependencies
- SubsystemInterface (inheritance)
- WindowLayout, AnimateWindowManager, GameWindow, ShellMenuSchemeManager (forward references)
- AsciiString, Bool, Int, UnsignedInt (types)

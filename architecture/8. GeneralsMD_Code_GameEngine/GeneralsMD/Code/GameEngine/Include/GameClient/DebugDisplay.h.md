# GeneralsMD/Code/GameEngine/Include/GameClient/DebugDisplay.h

## Purpose
Defines interfaces and classes for in-game debug text display functionality.

## Responsibilities
- Declares `DebugDisplayInterface` abstract base class for debug rendering
- Implements `DebugDisplay` concrete class for debug text display
- Defines color enumeration for text rendering
- Provides methods for cursor positioning, text formatting, and display margins
- Exposes debug display functionality for audio diagnostics in debug builds

## Key Types
- **DebugDisplayInterface (Class)**: Abstract interface for debug text rendering
- **Color (Enum)**: Text color options (WHITE, BLACK, YELLOW, RED, GREEN, BLUE)
- **DebugDisplay (Class)**: Concrete implementation of debug display functionality

## Key Functions
### DebugDisplayInterface::printf
- Purpose: Print formatted text at current cursor position
- Calls: Not inferable (pure virtual)

### DebugDisplay::printf
- Purpose: Print formatted text at current cursor position
- Calls: Not inferable (implementation not shown)

### DebugDisplay::drawText
- Purpose: Render null-terminated string at specified position
- Calls: Not inferable (protected pure virtual)

## Globals
- **AudioDebugDisplay (Function)**: Audio diagnostics display function (debug builds only)

## Dependencies
- `Lib/BaseType.h` (for basic types)
- `<stdio.h>` (for printf functionality)
- Uses `Char` and `Int` types from BaseType.h

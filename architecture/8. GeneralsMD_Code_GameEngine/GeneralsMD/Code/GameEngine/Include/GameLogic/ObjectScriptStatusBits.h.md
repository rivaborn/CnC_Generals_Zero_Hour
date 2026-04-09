# GeneralsMD/Code/GameEngine/Include/GameLogic/ObjectScriptStatusBits.h

## Purpose
Defines an enum for object script status bits used in the game engine.

## Responsibilities
- Declares `ObjectScriptStatusBit` enum with bit flags for object states
- Provides constants for script-controlled object properties
- Supports header detangling (modular include system)

## Key Types
- **ObjectScriptStatusBit (Enum)**: Bit flags for object script status states
- **OBJECT_STATUS_SCRIPT_DISABLED (Enum)**: Object disabled via script
- **OBJECT_STATUS_SCRIPT_UNPOWERED (Enum)**: Object unpowered via script
- **OBJECT_STATUS_SCRIPT_UNSELLABLE (Enum)**: Object cannot be sold
- **OBJECT_STATUS_SCRIPT_UNSTEALTHED (Enum)**: Object cannot stealth
- **OBJECT_STATUS_SCRIPT_TARGETABLE (Enum)**: Object can be targeted but not auto-acquired

## Key Functions
None

## Globals
None

## Dependencies
- None (standalone header)

# GeneralsMD/Code/GameEngine/Include/GameClient/KeyDefs.h

## Purpose
Defines keyboard key codes and state flags for input handling in the game engine.

## Responsibilities
- Maps DirectInput key codes to game-specific key definitions
- Defines keyboard state flags for modifier keys
- Provides key constants for all standard and special keys
- Includes platform-specific DirectInput headers

## Key Types
- **KeyDefType (Enum)**: Enumeration of all keyboard keys (letters, numbers, function keys, etc.)
- **KeyStateType (Enum)**: Flags representing keyboard modifier states (shift, control, alt, etc.)

## Key Functions
None

## Globals
None

## Dependencies
- `<stdlib.h>`
- `<dinput.h>` (DirectInput headers)
- DirectInput key constants (DIK_*)

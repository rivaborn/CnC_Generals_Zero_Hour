# GeneralsMD/Code/GameEngine/Include/GameClient/Keyboard.h

## Purpose
Defines the `Keyboard` class and related structures for handling keyboard input in the game engine.

## Responsibilities
- Manages keyboard state and input events
- Provides methods to check modifier keys (Shift, Ctrl, Alt)
- Handles key repeat and translation to printable characters
- Maintains a singleton instance for global keyboard access

## Key Types
- `KeyboardIO` (struct): Holds a single keyboard event with key data, status, state, and sequence info
- `StatusType` (enum): Defines key status flags (`STATUS_UNUSED`, `STATUS_USED`)
- `Keyboard` (class): Singleton class for keyboard input management
- `m_keyNames` (struct): Maps keys to their standard, shifted, and shifted2 characters

## Key Functions
### `init()`
- Purpose: Initialize the keyboard system
- Calls: `initKeyNames()`

### `update()`
- Purpose: Gather current state of all keys
- Calls: `updateKeys()`, `checkKeyRepeat()`

### `getKey()`
- Purpose: Get key data for a single key (pure virtual)
- Calls: None (must be implemented by derived class)

### `translateKey()`
- Purpose: Translate key code to printable Unicode character
- Calls: None

### `getPrintableKey()`
- Purpose: Get printable character for a key based on its state
- Calls: None

## Globals
- `TheKeyboard` (Keyboard*): Global singleton instance of the Keyboard class

## Dependencies
- `SubsystemInterface.h`: Base class for subsystem interfaces
- `KeyDefs.h`: Defines key states and related constants
- `BaseType.h`: Basic type definitions (e.g., `UnsignedByte`, `WideChar`)

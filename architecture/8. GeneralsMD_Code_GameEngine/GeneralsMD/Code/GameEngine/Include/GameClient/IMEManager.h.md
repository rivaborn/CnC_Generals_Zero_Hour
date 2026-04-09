# GeneralsMD/Code/GameEngine/Include/GameClient/IMEManager.h

## Purpose
Defines the IME (Input Method Editor) manager interface for handling text input in non-Latin scripts.

## Responsibilities
- Declares the `IMEManagerInterface` abstract class for IME operations
- Provides global accessor for the IME manager singleton
- Defines factory function for creating the IME manager
- Specifies methods for IME state management and candidate list handling

## Key Types
- `IMEManagerInterface` (Class): Abstract interface for IME functionality
- `GameWindow` (Class): Forward reference to window class
- `UnicodeString` (Class): Forward reference to Unicode string class

## Key Functions
### `CreateIMEManagerInterface`
- Purpose: Factory function to create the IME manager instance
- Calls: None

## Globals
- `TheIMEManager` (IMEManagerInterface*): Global pointer to the IME manager instance

## Dependencies
- `Lib/BaseType.h` (for Bool, Int, UnsignedInt)
- `Common/SubsystemInterface.h` (base class)
- `Common/UnicodeString.h` (for UnicodeString)

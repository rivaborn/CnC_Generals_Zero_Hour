# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/trackwin.h - Enhanced Analysis

## Architectural Role
This header defines a utility class for managing sub-window tracking within a larger window, likely used in the UI or rendering subsystems to handle viewport clipping or dynamic window resizing. The `NEVER` preprocessor guard suggests this class was deprecated or experimental in the final engine.

## Cross-References
### Incoming
- Not inferable (no usage examples in provided context).

### Outgoing
- Depends on `Rect` type from `trect.h` (included conditionally).

## Design Patterns
- **Wrapper Facade**: Encapsulates sub-window logic behind a simple interface.
- **State Preservation**: Maintains full-window dimensions for reset/clip operations.
- **Conditional Compilation**: Uses `#ifdef NEVER` to disable the class, indicating legacy or unused code.

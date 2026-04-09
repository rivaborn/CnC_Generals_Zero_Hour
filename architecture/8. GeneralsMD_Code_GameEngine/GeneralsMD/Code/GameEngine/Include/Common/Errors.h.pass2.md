# GeneralsMD/Code/GameEngine/Include/Common/Errors.h - Enhanced Analysis

## Architectural Role
This header defines the standardized error codes used across the SAGE engine for exception handling. It serves as the central contract for error reporting, ensuring consistency in how failures (memory, file corruption, invalid arguments) are communicated between subsystems.

## Cross-References
### Incoming
- **Game Logic**: Uses `ERROR_INVALID_FILE_VERSION` and `ERROR_CORRUPT_FILE_FORMAT` for mission/asset loading failures.
- **W3D**: References `ERROR_INVALID_D3D` for Direct3D initialization errors.
- **Networking**: Likely uses `ERROR_BAD_ARG` for packet validation.
- **Modding**: Relies on `ERROR_BAD_INI` for script/config parsing.

### Outgoing
- None (header-only, no direct calls).

## Design Patterns
- **Enum as Contract**: The `ErrorCode` enum acts as a shared contract for error handling, promoting consistency.
- **Magic Number Avoidance**: Uses `ERROR_BASE` (0xdead0001) to prevent collisions with other numeric codes.
- **Documentation-Driven**: Each error code includes inline comments, serving as both API docs and runtime debugging aids.

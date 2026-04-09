# Generals/Code/Libraries/Source/WWVegas/WWLib/WWCOMUtil.h - Enhanced Analysis

## Architectural Role
This header provides low-level COM interop utilities, bridging the game engine with external COM components (e.g., DirectX, scripting hosts). It abstracts IDispatch calls and COM server management, likely used for dynamic runtime integration (e.g., UI scripting, audio middleware).

## Cross-References
### Incoming
- **UI System**: Likely calls `Dispatch_*` for scriptable UI components (e.g., Flash-based menus).
- **Audio Subsystem**: May use COM for DirectSound or EAX integration.
- **Modding Framework**: Could leverage `RegisterCOMServer` for custom DLL loading.

### Outgoing
- **COM Runtime**: Directly interacts with `IDispatch` and COM registration APIs.
- **WWLib Core**: May depend on WWLibâs error handling or logging utilities.

## Design Patterns
- **Facade Pattern**: Wraps complex COM IDispatch calls into simpler functions.
- **Utility Class**: Static-like functions (no instances) for COM operations.
- **Not inferable**: No clear dependency injection or factory patterns visible.

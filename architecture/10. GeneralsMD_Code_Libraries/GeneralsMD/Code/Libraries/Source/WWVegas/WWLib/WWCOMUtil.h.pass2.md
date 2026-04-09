# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/WWCOMUtil.h - Enhanced Analysis

## Architectural Role
This header provides COM interop utilities, bridging the game engine with external COM components (e.g., DirectX, scripting engines). It abstracts IDispatch calls and COM server registration, likely used for dynamic runtime behavior (e.g., UI scripting or modding hooks).

## Cross-References
### Incoming
- **UI System**: Likely calls `Dispatch_*` for scriptable UI elements (e.g., Flash-based menus).
- **Modding Framework**: Uses `RegisterCOMServer`/`UnregisterCOMServer` for plugin DLLs.
- **Audio/Video Subsystems**: May invoke COM objects (e.g., DirectShow filters).

### Outgoing
- **COM Runtime**: Directly interacts with `IDispatch`, `DISPPARAMS`, etc.
- **Windows API**: Uses `HRESULT` and COM registration functions.

## Design Patterns
- **Facade Pattern**: Hides COM complexity behind simple functions (e.g., `Dispatch_GetProperty`).
- **Dependency Injection**: Assumes COM objects are passed in (e.g., `IDispatch* object`), enabling runtime flexibility.
- **Not inferable**: No clear use of other patterns (e.g., no factories or observers visible).

*Token count: 198*

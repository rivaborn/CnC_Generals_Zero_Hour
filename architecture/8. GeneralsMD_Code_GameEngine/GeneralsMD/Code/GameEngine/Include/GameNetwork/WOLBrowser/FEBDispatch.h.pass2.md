# GeneralsMD/Code/GameEngine/Include/GameNetwork/WOLBrowser/FEBDispatch.h - Enhanced Analysis

## Architectural Role
This file provides the COM dispatch infrastructure for the game's embedded browser (WOLBrowser), enabling scripting/automation support via IDispatch. It bridges the game's C++ code with the browser's COM-based scripting engine.

## Cross-References
### Incoming
- Likely called by browser-related classes (e.g., `WOLBrowser` itself) to expose game functionality to JavaScript/VBScript.
- May be referenced by UI systems needing embedded web content (e.g., in-game browsers for WOL features).

### Outgoing
- Relies on ATL (`CComObjectRootEx`, `CComCoClass`) for COM object management.
- Uses COM runtime (`ITypeLib`, `ITypeInfo`, `CreateStdDispatch`) for type library binding.
- Depends on `_Module` (global ATL module) for COM initialization.

## Design Patterns
- **Template Method**: The template class `FEBDispatch` defines a skeleton for COM dispatch implementation, leaving concrete behavior to derived classes.
- **Adapter**: Acts as an adapter between the game's C++ objects and COM's IDispatch interface, enabling scripting access.
- **Resource Management**: Uses RAII for COM object lifecycle (AddRef/Release in constructor/destructor).

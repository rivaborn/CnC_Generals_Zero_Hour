# Generals/Code/Libraries/Source/WWVegas/WWLib/WWCOMUtil.cpp - Enhanced Analysis

## Architectural Role
This file serves as a thin abstraction layer for COM interoperability within the SAGE engine, bridging the game's native C++ code with external COM components (likely used for scripting or plugin support). It centralizes COM-related operations to ensure consistent error handling and resource management.

## Cross-References
### Incoming
- Likely called by scripting systems (e.g., WWScript) or plugin managers that need to interact with COM objects.
- May be referenced by UI components that use COM for dynamic property binding.

### Outgoing
- Directly invokes COM APIs (`IDispatch`, `LoadLibrary`, etc.).
- Relies on Windows COM infrastructure for method/property access and DLL registration.

## Design Patterns
- **Facade Pattern**: Wraps complex COM operations behind simpler interfaces (`Dispatch_GetProperty`, etc.).
- **Resource Management**: Uses RAII-like patterns for library handles (`LoadLibrary`/`FreeLibrary` pairs).
- **Error Handling**: Propagates HRESULT values directly, deferring interpretation to callers.

*Not inferable*: No clear use of other patterns (e.g., no factories, observers, or singletons visible).

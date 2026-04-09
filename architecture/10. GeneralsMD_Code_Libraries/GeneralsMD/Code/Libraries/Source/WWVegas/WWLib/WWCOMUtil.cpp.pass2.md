# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/WWCOMUtil.cpp - Enhanced Analysis

## Architectural Role
This file serves as a thin abstraction layer for COM interoperability within the SAGE engine, bridging Windows COM APIs with internal game systems. It likely supports scripting or external tool integration (e.g., modding utilities) by providing safe wrappers around IDispatch operations.

## Cross-References
### Incoming
- **Scripting/Modding Subsystem**: Likely called by Lua or other scripting interfaces to interact with COM objects (e.g., DirectX components or external tools).
- **Installer/Update System**: `RegisterCOMServer`/`UnregisterCOMServer` are probably invoked during game installation or patching to manage COM dependencies.

### Outgoing
- **Windows COM API**: Directly calls `IDispatch` methods (`GetIDsOfNames`, `Invoke`) and COM registration functions (`DllRegisterServer`).
- **Windows DLL Loading**: Uses `LoadLibrary`/`FreeLibrary` for dynamic COM server management.

## Design Patterns
- **Facade Pattern**: Wraps complex COM operations (property access, method invocation) behind simpler interfaces.
- **Error Handling via HRESULT**: Propagates COM errors directly, adhering to Windows conventions.
- **Resource Management**: Explicit `LoadLibrary`/`FreeLibrary` pairing ensures DLL handles are released.

*Not inferable*: No clear use of Singleton, Observer, or other patterns.

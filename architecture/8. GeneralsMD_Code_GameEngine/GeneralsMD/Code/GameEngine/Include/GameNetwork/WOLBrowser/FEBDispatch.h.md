# GeneralsMD/Code/GameEngine/Include/GameNetwork/WOLBrowser/FEBDispatch.h

## Purpose
Template class for implementing IDispatch interface for COM objects with type libraries, used for the game's embedded browser.

## Responsibilities
- Manages COM object dispatch interface creation
- Handles type library loading and type info retrieval
- Provides COM interface mapping for derived classes

## Key Types
- **FEBDispatch (Class)**: Template class for COM dispatch implementation
- **_ComMapClass (Class)**: COM interface mapping helper (ATL internal)

## Key Functions
### FEBDispatch()
- Purpose: Initializes COM dispatch interface and loads type library
- Calls: `GetModuleFileName`, `LoadTypeLib`, `GetTypeInfoOfGuid`, `CreateStdDispatch`

### ~FEBDispatch()
- Purpose: Cleans up COM resources
- Calls: `Release` on `m_ptinfo` and `m_dispatch`

## Globals
- **_Module (CComModule)**: ATL module instance for COM initialization

## Dependencies
- `<atlbase.h>`, `<atlcom.h>`, `<comutil.h>`
- `CComObjectRootEx`, `CComCoClass` (ATL classes)
- `ITypeLib`, `ITypeInfo`, `IDispatch` (COM interfaces)
- `CreateStdDispatch` (COM helper function)

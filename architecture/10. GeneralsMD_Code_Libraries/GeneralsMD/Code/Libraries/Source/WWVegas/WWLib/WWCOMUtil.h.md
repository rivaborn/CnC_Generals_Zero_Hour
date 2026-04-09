# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/WWCOMUtil.h

## Purpose
Header file declaring COM utility functions and macros for IDispatch interface interaction and COM server registration.

## Responsibilities
- Declares functions for IDispatch property/method invocation
- Provides COM server registration/unregistration utilities
- Exposes COM-related helper macros (not shown in snippet)

## Key Types
None

## Key Functions
### Dispatch_GetProperty
- Purpose: Invokes PropertyGet on an IDispatch interface.
- Calls: None (declaration only)

### Dispatch_PutProperty
- Purpose: Invokes PropertyPut on an IDispatch interface.
- Calls: None (declaration only)

### Dispatch_InvokeMethod
- Purpose: Invokes a method on an IDispatch interface.
- Calls: None (declaration only)

### RegisterCOMServer
- Purpose: Registers a COM in-process DLL server.
- Calls: None (declaration only)

### UnregisterCOMServer
- Purpose: Unregisters a COM in-process DLL server.
- Calls: None (declaration only)

## Globals
None

## Dependencies
- `<oaidl.h>` (for COM/IDispatch types)
- External symbols: `HRESULT`, `STDMETHODCALLTYPE`, `IDispatch`, `OLECHAR`, `VARIANT`, `DISPPARAMS` (from Windows COM SDK)

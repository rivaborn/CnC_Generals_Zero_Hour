# Generals/Code/Libraries/Source/WWVegas/WWLib/WWCOMUtil.cpp

## Purpose
Provides utility functions for COM (Component Object Model) operations, including property access, method invocation, and server registration.

## Responsibilities
- Wraps IDispatch interface calls for property get/put and method invocation
- Handles COM server DLL registration/unregistration
- Manages HRESULT error handling for COM operations

## Key Types
None

## Key Functions
### Dispatch_GetProperty
- Purpose: Retrieves a property value from an IDispatch object
- Calls: IDispatch::GetIDsOfNames, IDispatch::Invoke

### Dispatch_PutProperty
- Purpose: Sets a property value on an IDispatch object
- Calls: IDispatch::GetIDsOfNames, IDispatch::Invoke

### Dispatch_InvokeMethod
- Purpose: Invokes a method on an IDispatch object
- Calls: IDispatch::GetIDsOfNames, IDispatch::Invoke

### RegisterCOMServer
- Purpose: Registers an in-process COM server DLL
- Calls: LoadLibrary, GetProcAddress, DllRegisterServer

### UnregisterCOMServer
- Purpose: Unregisters an in-process COM server DLL
- Calls: LoadLibrary, GetProcAddress, DllUnregisterServer

## Globals
None

## Dependencies
- Key includes: WWCOMUtil.h, COM headers (IDispatch, DISPPARAMS, etc.)
- External symbols: LoadLibrary, GetProcAddress, FreeLibrary, DllRegisterServer, DllUnregisterServer

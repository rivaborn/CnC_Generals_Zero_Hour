# Generals/Code/Libraries/Source/WWVegas/WWLib/WWCOMUtil.h

## Purpose
Header file declaring COM utility functions and macros for IDispatch interface interaction and COM server registration.

## Responsibilities
- Declares functions for IDispatch property/method invocation
- Provides COM server registration/unregistration utilities
- Exposes COM-related helper functions for use in the game engine

## Key Types
None

## Key Functions
### Dispatch_GetProperty
- Purpose: Invokes PropertyGet on an IDispatch interface.
- Calls: None

### Dispatch_PutProperty
- Purpose: Invokes PropertyPut on an IDispatch interface.
- Calls: None

### Dispatch_InvokeMethod
- Purpose: Invokes a method on an IDispatch interface.
- Calls: None

### RegisterCOMServer
- Purpose: Registers a COM in-process DLL server.
- Calls: None

### UnregisterCOMServer
- Purpose: Unregisters a COM in-process DLL server.
- Calls: None

## Globals
None

## Dependencies
- `<oaidl.h>`: For COM-related types (IDispatch, OLECHAR, VARIANT, DISPPARAMS)

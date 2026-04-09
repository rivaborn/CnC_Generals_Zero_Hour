# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/refcount.h

## Purpose
Implements a reference counting mechanism for managing object lifetimes in the SAGE engine.

## Responsibilities
- Provides reference counting via `Add_Ref()`/`Release_Ref()`
- Tracks active references in debug builds
- Manages global reference count statistics
- Defines macros for safe pointer assignment (`REF_PTR_SET`, `REF_PTR_RELEASE`)

## Key Types
- **RefCountClass (Class)**: Base class for reference-counted objects
- **ActiveRefStruct (Struct)**: Stores file/line info for debug tracking (debug builds only)
- **RefCountNodeClass (Class)**: List node for active references (debug builds only)
- **RefCountListClass (Class)**: List of active references (debug builds only)

## Key Functions
### `Add_Ref()`
- Purpose: Increments reference count for an object
- Calls: `Inc_Total_Refs()` (debug builds only)

### `Release_Ref()`
- Purpose: Decrements reference count and deletes object if count reaches zero
- Calls: `Dec_Total_Refs()` (debug builds only), `Delete_This()`

### `Delete_This()`
- Purpose: Virtual method to delete the object (default: `delete this`)
- Calls: None

### `Add_Active_Ref()`
- Purpose: Adds object to active reference list (debug builds only)
- Calls: None

### `Remove_Active_Ref()`
- Purpose: Removes object from active reference list (debug builds only)
- Calls: None

## Globals
- **TotalRefs (int)**: Tracks total reference count across all objects
- **ActiveRefList (RefCountListClass)**: List of actively referenced objects (debug builds only)

## Dependencies
- `always.h`, `listnode.h`
- `W3DNEW` (memory allocation)
- `assert()` (debug checks)

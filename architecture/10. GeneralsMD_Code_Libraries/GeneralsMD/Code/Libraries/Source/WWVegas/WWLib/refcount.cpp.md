# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/refcount.cpp

## Purpose
Implements reference counting for object tracking in debug builds.

## Responsibilities
- Manages active reference list
- Tracks total reference counts
- Provides debug validation for references
- Supports breakpoints for debugging

## Key Types
- `RefCountClass`: Base class for reference-counted objects
- `RefCountListClass`: List of active references
- `RefCountNodeClass`: Node in active reference list

## Key Functions
### `Add_Active_Ref`
- Purpose: Adds an object to the active reference list
- Calls: `ActiveRefList.Add_Head`

### `Set_Ref_Owner`
- Purpose: Sets debug info (file/line) for a reference
- Calls: None

### `Remove_Active_Ref`
- Purpose: Removes an object from the active reference list
- Calls: `ActiveRefNode.Unlink`

### `Validate_Active_Ref`
- Purpose: Checks if an object exists in the active reference list
- Calls: `ActiveRefList.First`, `Next`

### `Inc_Total_Refs`
- Purpose: Increments the global reference counter
- Calls: None

### `Dec_Total_Refs`
- Purpose: Decrements the global reference counter
- Calls: None

### `Add_Ref`
- Purpose: Increments object's reference count and global counter
- Calls: `Inc_Total_Refs`

## Globals
- `TotalRefs` (int): Tracks total active references
- `ActiveRefList` (RefCountListClass): List of all active references
- `BreakOnReference` (RefCountClass*): Debug breakpoint trigger

## Dependencies
- `refcount.h`
- `<windows.h>`
- `assert` (for debug validation)

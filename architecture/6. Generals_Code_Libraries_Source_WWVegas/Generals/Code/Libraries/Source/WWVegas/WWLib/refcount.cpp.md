# Generals/Code/Libraries/Source/WWVegas/WWLib/refcount.cpp

## Purpose
Implements reference counting for object lifetime management in debug builds.

## Responsibilities
- Manages active reference list for tracked objects
- Provides reference counting utilities (increment/decrement)
- Supports debug breakpoints for memory leak detection
- Validates reference integrity in paranoid mode

## Key Types
- **RefCountClass**: Base class for reference-counted objects
- **RefCountListClass**: Container for active reference nodes
- **RefCountNodeClass**: Node in the active reference list

## Key Functions
### Add_Active_Ref
- Purpose: Adds an object to the active reference tracking list
- Calls: ActiveRefList.Add_Head

### Set_Ref_Owner
- Purpose: Records file/line information for reference debugging
- Calls: None

### Remove_Active_Ref
- Purpose: Removes an object from active reference tracking
- Calls: ActiveRefNode.Unlink

### Validate_Active_Ref
- Purpose: Verifies an object exists in the active reference list
- Calls: ActiveRefList.First, node->Next

### Inc_Total_Refs
- Purpose: Increments global reference counter
- Calls: None

### Dec_Total_Refs
- Purpose: Decrements global reference counter
- Calls: None

## Globals
- **TotalRefs** (int): Tracks total active references
- **ActiveRefList** (RefCountListClass): List of all active references
- **BreakOnReference** (RefCountClass*): Debug breakpoint trigger

## Dependencies
- `refcount.h` (header)
- `windows.h` (for DebugBreak)
- `assert` (for validation checks)

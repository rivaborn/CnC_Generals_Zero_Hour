# Generals/Code/Tools/WW3D/max2w3d/namedsel.cpp

## Purpose
Manages named selection sets for 3D modeling tools, allowing named groups of objects to be saved/loaded.

## Responsibilities
- Maintains a list of named selection sets (BitArray + name pairs)
- Provides CRUD operations for sets
- Handles serialization/deserialization of sets
- Ensures consistency between set and name counts

## Key Types
- **NamedSelSetList (Class)**: Container for named selection sets with management methods
- **BitArray (External)**: Bit array representing object selection state
- **TSTR (External)**: String type for set names

## Key Functions
### `Append_Set`
- Purpose: Adds a new named selection set to the list
- Calls: `BitArray` constructor, `TSTR` constructor, `Append` on `Sets` and `Names`

### `Delete_Set`
- Purpose: Removes a selection set by index or name
- Calls: `delete` on set/name, `Delete` on `Sets`/`Names`

### `Save`/`Load`
- Purpose: Serializes/deserializes the entire set list
- Calls: `ISave`/`ILoad` methods, `Save`/`Load` on `BitArray`

### `Load_Set`
- Purpose: Loads a single set from chunk data
- Calls: `BitArray::Load`, `ILoad::ReadWStringChunk`

## Globals
None

## Dependencies
- `namedsel.h` (header)
- `BitArray` (external)
- `TSTR` (external)
- `ISave`/`ILoad` (serialization interfaces)
- `IOResult` (status codes)

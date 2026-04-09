# Generals/Code/Tools/WW3D/max2w3d/namedsel.h

## Purpose
Manages named selection sets for 3D models, storing bit arrays and associated names.

## Responsibilities
- Stores dynamic arrays of bit arrays and strings for named selections
- Provides methods to manipulate, load, and save selection sets
- Supports finding, deleting, and appending selection sets
- Handles serialization via chunk-based I/O

## Key Types
- **NamedSelSetList (Class)**: Container for named selection sets with bit arrays and names
- **(anonymous enum) (Enum)**: Chunk ID constants for serialization
- **NAMED_SEL_SET_CHUNK (Enum)**: Chunk ID for set data
- **NAMED_SEL_BITS_CHUNK (Enum)**: Chunk ID for bit array data
- **NAMED_SEL_NAME_CHUNK (Enum)**: Chunk ID for name data

## Key Functions
### `operator[]`
- Purpose: Accesses a named selection set by index
- Calls: None

### `Find_Set`
- Purpose: Finds a named selection set by name
- Calls: None

### `Delete_Set`
- Purpose: Removes a named selection set by index or name
- Calls: None

### `Append_Set`
- Purpose: Adds a new named selection set
- Calls: None

### `Load` / `Save` / `Load_Set`
- Purpose: Serializes named selection sets to/from disk
- Calls: None

### `Set_Size`
- Purpose: Resizes the container
- Calls: None

## Globals
- None

## Dependencies
- `Max.h` (3DS Max SDK)
- `Tab` (template container)
- `BitArray` (bit array class)
- `TSTR` (string class)
- `ILoad` /

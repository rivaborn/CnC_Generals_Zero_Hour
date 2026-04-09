# Generals/Code/Tools/Launcher/Toolkit/Support/RefCounted.h

## Purpose
Base class for reference-counted objects, enabling shared ownership via `RefPtr` smart pointers.

## Responsibilities
- Manages reference counting for object lifetime.
- Provides thread-unsafe reference acquisition/release.
- Supports virtual `Release()` for derived classes.
- Prevents copying/assignment by default.
- Asserts zero refcount on destruction.

## Key Types
- **RefCounted (Class)**: Base class for reference-counted objects.

## Key Functions
### `RefCounted()`
- Purpose: Default constructor initializing `mRefCount` to 0.
- Calls: None.

### `RefCounted(const RefCounted&)`
- Purpose: Copy constructor initializing `mRefCount` to 0.
- Calls: None.

### `operator=(const RefCounted&)`
- Purpose: Disables assignment by returning a dummy reference.
- Calls: None.

### `~RefCounted()`
- Purpose: Virtual destructor asserting `mRefCount` is 0.
- Calls: `assert(mRefCount == 0)`.

### `AddReference()`
- Purpose: Increments the reference count.
- Calls: None.

### `Release()`
- Purpose: Decrements the reference count and deletes the object if zero.
- Calls: `delete this` (when `mRefCount` reaches 0).

### `ReferenceCount()`
- Purpose: Returns the current reference count.
- Calls: None.

### `operator==(const RefCounted&)`
- Purpose: Disables equality comparison by default.
- Calls: None.

### `operator!=(const RefCounted&)`
- Purpose: Disables inequality comparison by default.
- Calls: None.

## Globals
- **mRefCount (unsigned int)**: Tracks the number of active

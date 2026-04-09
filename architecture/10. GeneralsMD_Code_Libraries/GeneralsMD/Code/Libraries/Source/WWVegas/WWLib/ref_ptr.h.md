# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/ref_ptr.h

## Purpose
Implements a smart pointer (`RefCountPtr`) for reference-counted objects, managing automatic reference counting.

## Responsibilities
- Manages reference counting for objects implementing `Add_Ref()`/`Release_Ref()`.
- Provides safe pointer operations (dereferencing, assignment, comparison).
- Supports type-safe conversions between related types.
- Handles object lifetime via automatic reference management.

## Key Types
- **DummyPtrType (Class)**: Dummy type for null comparisons.
- **RefCountPtr (Class)**: Smart pointer wrapper for reference-counted objects.
- **ReferenceHandling (Enum)**: Flags for `GET`/`PEEK` reference handling modes.

## Key Functions
### `operator==` (template)
- Purpose: Compares two `RefCountPtr` instances for equality.
- Calls: `Peek()` on both operands.

### `operator<` (template)
- Purpose: Less-than comparison for `RefCountPtr`.
- Calls: `Peek()` on both operands.

### `Static_Cast` (template)
- Purpose: Safely casts a base `RefCountPtr` to a derived type.
- Calls: `Create_Peek()` with a C-style cast.

## Globals
- **None**

## Dependencies
- `always.h`, `wwdebug.h`
- Assumes objects implement `Add_Ref()`/`Release_Ref()`.
- Uses `NEW` macro for object creation.

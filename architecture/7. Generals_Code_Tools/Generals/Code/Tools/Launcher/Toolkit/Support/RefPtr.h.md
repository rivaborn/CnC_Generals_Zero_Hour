# Generals/Code/Tools/Launcher/Toolkit/Support/RefPtr.h

## Purpose
Implements `RefPtr` and `RefPtrConst` smart pointers for reference-counted objects derived from `RefCounted`.

## Responsibilities
- Manages reference counting for pointed-to objects
- Provides const-friendly polymorphic pointer semantics
- Supports dynamic, reinterpret, and const casting
- Handles object lifetime via automatic reference management

## Key Types
- **RefPtrBase (Class)**: Base class for reference-counted pointer operations
- **RefPtr (Class)**: Non-const smart pointer template
- **RefPtrConst (Class)**: Const smart pointer template

## Key Functions
### `Dynamic_Cast`
- Purpose: Performs dynamic casting between `RefPtr` types
- Calls: `Attach`, `GetRefObject`

### `Reinterpret_Cast`
- Purpose: Performs reinterpret casting between `RefPtr` types
- Calls: `Attach`, `GetRefObject`

### `Const_Cast`
- Purpose: Converts `RefPtrConst` to `RefPtr`
- Calls: `Attach`, `ReferencedObject`

## Globals
- None

## Dependencies
- `RefCounted.h` (base class for reference-counted objects)
- `VisualC.h` (platform-specific headers)
- `<stddef.h>`, `<assert.h>` (standard C headers)

# GeneralsMD/Code/GameEngine/Include/Common/Override.h

## Purpose
Provides a template class `OVERRIDE<T>` for managing object overrides in the game engine, enabling runtime replacement of object pointers while maintaining compatibility with pointer operations.

## Responsibilities
- Wraps a pointer to an `Overridable`-derived object
- Provides pointer-like operations (`->`, `*`, casting) that resolve to the final override
- Ensures proper memory management when overriding objects
- Maintains backward compatibility with existing pointer-based code

## Key Types
- `OVERRIDE<T>` (Class): A smart pointer wrapper for overriding objects of type `T`

## Key Functions
### `OVERRIDE<T>::operator->()`
- Purpose: Dereferences the override chain to return the final overridden object.
- Calls: `m_overridable->getFinalOverride()`

### `OVERRIDE<T>::operator*()`
- Purpose: Dereferences the override chain to return the final overridden object.
- Calls: `m_overridable->getFinalOverride()`

### `OVERRIDE<T>::getNonOverloadedPointer()`
- Purpose: Returns the raw pointer without resolving overrides.
- Calls: None

### `OVERRIDE<T>::operator const T*()`
- Purpose: Allows implicit casting to `const T*`.
- Calls: `operator*()`

## Globals
- None

## Dependencies
- `Common/Overridable.h` (for `Overridable` base class and `getFinalOverride()`)
- Uses template parameter `T` (must derive from `Overridable`)

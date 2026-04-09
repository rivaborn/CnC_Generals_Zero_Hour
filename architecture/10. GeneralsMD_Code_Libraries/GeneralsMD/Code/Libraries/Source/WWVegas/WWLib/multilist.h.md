# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/multilist.h

## Purpose
Defines a multi-list data structure allowing objects to belong to multiple lists simultaneously.

## Responsibilities
- Provides `MultiListObjectClass` base for objects in multiple lists
- Implements `GenericMultiListClass` core list functionality
- Offers typed wrappers (`MultiListClass`, `RefMultiListClass`)
- Supports iteration via `MultiListIterator` and variants
- Manages reference counting for ref-counted objects

## Key Types
- **MultiListObjectClass (Class)**: Base class for objects that can be in multiple lists
- **MultiListNodeClass (Class)**: Internal node linking objects to lists
- **GenericMultiListClass (Class)**: Core untyped list implementation
- **MultiListClass (Template)**: Typed list wrapper
- **RefMultiListClass (Template)**: Typed list with reference counting
- **MultiListIterator (Template)**: List iterator
- **PriorityMultiListIterator (Template)**: Priority queue iterator

## Key Functions
### `Internal_Add`
- Purpose: Adds object to list internally
- Calls: None visible

### `Internal_Remove`
- Purpose: Removes object from list internally
- Calls: None visible

### `Process_Head`
- Purpose: Processes head node in priority queue
- Calls: `Remove_Current_Object`, `Add_Tail`

## Globals
- None

## Dependencies
- `always.h`, `mempool.h`, `<assert.h>`
- `AutoPoolClass`, `RefCountClass` (external)

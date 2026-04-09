# Generals/Code/Libraries/Source/WWVegas/WWLib/multilist.h

## Purpose
Defines a multi-list data structure allowing objects to belong to multiple lists simultaneously.

## Responsibilities
- Provides `MultiListObjectClass` base for objects in multi-lists
- Implements `GenericMultiListClass` core list logic
- Offers typed wrappers (`MultiListClass`, `RefMultiListClass`)
- Supports iteration via `MultiListIterator` and variants
- Manages reference counting for ref-counted objects

## Key Types
- **MultiListObjectClass (Class)**: Base class for objects that can be in multiple lists
- **MultiListNodeClass (Class)**: Internal node linking objects to lists
- **GenericMultiListClass (Class)**: Core untyped list implementation
- **MultiListClass (Template)**: Typed list wrapper
- **RefMultiListClass (Template)**: Typed list with reference counting
- **MultiListIterator (Template)**: Iterator for typed lists
- **PriorityMultiListIterator (Template)**: Priority-queue iterator

## Key Functions
### `MultiListObjectClass::~MultiListObjectClass`
- Purpose: Automatically removes object from all lists on destruction
- Calls: `Internal_Remove` (via `ListNode`)

### `GenericMultiListClass::Internal_Add`
- Purpose: Adds object to list (with optional uniqueness check)
- Calls: None (direct list manipulation)

### `RefMultiListClass::Add`
- Purpose: Adds object with reference counting
- Calls: `Internal_Add`, `obj->Add_Ref()`

### `PriorityMultiListIterator::Process_Head`
- Purpose: Moves head to tail (priority queue behavior)
- Calls: `Remove_Current_Object`, `Add_Tail`

## Globals
- None

## Dependencies
- `always.h`, `mempool.h`, `<assert.h>`
- `AutoPoolClass` (memory management)
- `RefCountClass` (reference counting)

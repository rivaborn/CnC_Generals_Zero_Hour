# GeneralsMD/Code/GameEngine/Include/GameClient/SelectionInfo.h

## Purpose
Defines structures and functions for managing game object selection context, including selection counts and pick types.

## Responsibilities
- Define `SelectionInfo` struct for tracking selection counts
- Define `PickDrawableStruct` for drawable list management
- Declare functions for context-sensitive selection handling
- Provide translation between pick types and object kinds

## Key Types
- **SelectionInfo (struct)**: Tracks counts of selected objects (enemies, civilians, mines, etc.)
- **PickDrawableStruct (struct)**: Manages drawable lists with filtering options
- **None**: No enums/classes beyond these structs

## Key Functions
### `contextCommandForNewSelection`
- Purpose: Determines context commands for new selection based on current/new selections
- Calls: Not inferable (implementation in another file)

### `getPickTypesForContext`
- Purpose: Returns pick types based on context (e.g., attack mode)
- Calls: Not inferable

### `getPickTypesForCurrentSelection`
- Purpose: Returns pick types based on current selection
- Calls: Not inferable

### `translatePickTypesToKindof`
- Purpose: Converts pick types to a kind-of mask
- Calls: Not inferable

### `addDrawableToList`
- Purpose: Adds a drawable to a list (callback for region iteration)
- Calls: Not inferable

## Globals
- **None**: No global/static variables declared

## Dependencies
- `GameClient/InGameUI.h`
- `DrawableList`, `Drawable`, `KindOfMaskType` (external types)
- `Int`, `Bool`, `UnsignedInt` (primitive types)

# GeneralsMD/Code/GameEngine/Include/Common/ThingSort.h - Enhanced Analysis

## Architectural Role
This header defines the categorization system for game objects in the editor, serving as a foundational type for object organization in the World Builder tool. It bridges the gap between the editor UI and the game's object hierarchy.

## Cross-References
### Incoming
- Editor UI components (e.g., object browser panels) that filter/sort objects by `EditorSortingType`
- Object loading/registration systems that assign sorting categories to game entities

### Outgoing
- None (header-only, no direct calls)

## Design Patterns
- **Enumeration as Type System**: Uses an enum to create a closed set of categories for type-safe object classification
- **Conditional Definition**: `EditorSortingNames` array is only defined when `DEFINE_EDITOR_SORTING_NAMES` is set, enabling selective compilation for editor vs runtime builds
- **Not inferable**: No other patterns evident from this header alone

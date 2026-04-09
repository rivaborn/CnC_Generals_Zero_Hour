# GeneralsMD/Code/GameEngine/Include/Common/ThingSort.h

## Purpose
Defines an enumeration for categorizing game objects in the editor for sorting purposes.

## Responsibilities
- Declares `EditorSortingType` enum for object categorization
- Provides string names for each sorting type (conditionally)
- Supports editor functionality for organizing objects

## Key Types
- **EditorSortingType (Enum)**: Categories for sorting game objects in the editor (e.g., structures, infantry, vehicles).

## Key Functions
None.

## Globals
- **EditorSortingNames (char\*[])**: Array of string names for each sorting type (defined only if `DEFINE_EDITOR_SORTING_NAMES` is set).

## Dependencies
- None (header-only file).

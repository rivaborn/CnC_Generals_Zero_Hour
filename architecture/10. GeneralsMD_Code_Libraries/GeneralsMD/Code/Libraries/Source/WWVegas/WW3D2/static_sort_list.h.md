# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/static_sort_list.h

## Purpose
Defines abstract and concrete classes for managing render objects sorted by depth level in the WW3D rendering pipeline.

## Responsibilities
- Declares abstract `StaticSortListClass` interface for render object sorting.
- Implements `DefaultStaticSortListClass` to manage objects by sort level.
- Provides methods to add objects, render them, and control sort level ranges.

## Key Types
- **RenderInfoClass (Class)**: Not defined here; used for rendering context.
- **StaticSortListClass (Class)**: Abstract base class defining render object sorting interface.
- **DefaultStaticSortListClass (Class)**: Concrete implementation of `StaticSortListClass` with sort level management.

## Key Functions
### `StaticSortListClass::Add_To_List`
- Purpose: Adds a render object to the sort list at a specified level.
- Calls: None (pure virtual).

### `StaticSortListClass::Render_And_Clear`
- Purpose: Renders all objects in the list and clears it.
- Calls: None (pure virtual).

### `DefaultStaticSortListClass::Add_To_List`
- Purpose: Adds a render object to the appropriate sort level list.
- Calls: None (implementation not shown).

### `DefaultStaticSortListClass::Render_And_Clear`
- Purpose: Renders objects within the configured sort level range and clears the lists.
- Calls: None (implementation not shown).

### `DefaultStaticSortListClass::Get_Min_Sort`
- Purpose: Returns the minimum sort level.
- Calls: None.

### `DefaultStaticSortListClass::Get_Max_Sort`
- Purpose: Returns the maximum sort level.
- Calls: None.

### `DefaultStaticSortListClass::Set_Min_Sort`
- Purpose: Sets

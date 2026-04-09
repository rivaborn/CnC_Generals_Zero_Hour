# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/static_sort_list.cpp

## Purpose
Implements a default static sort list for managing render objects with different sort levels.

## Responsibilities
- Manages render objects in sort lists
- Adds objects to appropriate sort levels
- Renders objects in correct order and clears lists

## Key Types
- DefaultStaticSortListClass (Class): Default implementation of static sort list
- RenderObjClass (Class): Render object base class
- RenderInfoClass (Class): Rendering information structure

## Key Functions
### DefaultStaticSortListClass::Add_To_List
- Purpose: Adds a render object to the appropriate sort list
- Calls: WWASSERT

### DefaultStaticSortListClass::Render_And_Clear
- Purpose: Renders all objects in sort lists and clears them
- Calls: RenderObjClass::Get_Render_Hook, RenderObjClass::Render, TheDX8MeshRenderer.Flush

## Globals
- None

## Dependencies
- static_sort_list.h
- rendobj.h
- dx8renderer.h

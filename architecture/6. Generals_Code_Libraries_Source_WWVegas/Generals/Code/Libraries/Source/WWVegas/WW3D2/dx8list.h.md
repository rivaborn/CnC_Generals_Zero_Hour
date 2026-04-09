# Generals/Code/Libraries/Source/WWVegas/WW3D2/dx8list.h

## Purpose
Defines typedefs for specialized multi-list containers used in the DirectX 8 rendering subsystem.

## Responsibilities
- Provides type aliases for texture, FVF (Flexible Vertex Format), polygon renderer, and texture tracker lists.
- Uses `MultiListClass` template to manage collections of specific DirectX 8 related classes.
- Ensures consistent list types across the rendering system.

## Key Types
- `DX8TextureCategoryClass` (Class): Base class for texture categories.
- `TextureCategoryList` (Class): List of texture categories.
- `TextureCategoryListIterator` (Class): Iterator for texture category lists.
- `DX8FVFCategoryContainer` (Class): Container for FVF categories.
- `FVFCategoryList` (Class): List of FVF categories.
- `FVFCategoryListIterator` (Class): Iterator for FVF category lists.
- `DX8PolygonRendererClass` (Class): Base class for polygon renderers.
- `DX8PolygonRendererList` (Class): List of polygon renderers.
- `DX8PolygonRendererListIterator` (Class): Iterator for polygon renderer lists.
- `DX8TextureTrackerClass` (Class): Base class for texture trackers.
- `DX8TextureTrackerList` (Class): List of texture trackers.
- `DX8TextureTrackerListIterator` (Class): Iterator for texture tracker lists.

## Key Functions
None (header-only file with no function definitions).

## Globals
None.

## Dependencies
- `always.h`: Likely contains common macros or assertions.
- `multilist.h`: Defines the `MultiListClass` and `MultiListIterator` templates used here.

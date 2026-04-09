# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/dx8list.h

## Purpose
Defines typedefs for specialized multi-list containers used in the DirectX 8 rendering subsystem.

## Responsibilities
- Typedefs for texture category lists
- Typedefs for FVF (Flexible Vertex Format) category lists
- Typedefs for polygon renderer lists
- Typedefs for texture tracker lists

## Key Types
- DX8TextureCategoryClass (Class): Base class for texture categories
- TextureCategoryList (Class): Multi-list container for texture categories
- TextureCategoryListIterator (Class): Iterator for texture category lists
- DX8FVFCategoryContainer (Class): Base class for FVF categories
- FVFCategoryList (Class): Multi-list container for FVF categories
- FVFCategoryListIterator (Class): Iterator for FVF category lists
- DX8PolygonRendererClass (Class): Base class for polygon renderers
- DX8PolygonRendererList (Class): Multi-list container for polygon renderers
- DX8PolygonRendererListIterator (Class): Iterator for polygon renderer lists
- TextureTrackerClass (Class): Base class for texture trackers
- TextureTrackerList (Class): Multi-list container for texture trackers
- TextureTrackerListIterator (Class): Iterator for texture tracker lists

## Key Functions
None

## Globals
None

## Dependencies
- "always.h": Header for common macros
- "multilist.h": Template-based multi-list container implementation

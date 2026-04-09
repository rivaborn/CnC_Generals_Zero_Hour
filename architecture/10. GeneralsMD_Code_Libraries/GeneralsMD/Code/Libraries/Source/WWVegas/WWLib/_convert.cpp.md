# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/_convert.cpp

## Purpose
Declares global pointers for various drawing classes used in the game's rendering system.

## Responsibilities
- Defines global pointers for different drawer classes (voxel, unit, terrain, animation, normal, isometric).
- Provides a central registry for rendering components.

## Key Types
None

## Key Functions
None

## Globals
- VoxelDrawer (ConvertClass*): Pointer to voxel drawer instance.
- UnitDrawer (ConvertClass*): Pointer to unit drawer instance.
- TerrainDrawer (ConvertClass*): Pointer to terrain drawer instance.
- AnimDrawer (ConvertClass*): Pointer to animation drawer instance.
- NormalDrawer (ConvertClass*): Pointer to normal drawer instance.
- IsometricDrawer (ConvertClass*): Pointer to isometric drawer instance.

## Dependencies
- `_convert.h`: Header for ConvertClass declaration.
- `always.h`: Likely contains common includes or macros.

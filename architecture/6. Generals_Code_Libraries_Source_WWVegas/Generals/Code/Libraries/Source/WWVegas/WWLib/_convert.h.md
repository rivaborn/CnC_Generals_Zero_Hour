# Generals/Code/Libraries/Source/WWVegas/WWLib/_convert.h

## Purpose
Header file declaring global instances of ConvertClass for different rendering modes.

## Responsibilities
- Declares global ConvertClass pointers for voxel, unit, terrain, animation, normal, and isometric rendering.
- Provides external linkage for these converters.
- Includes the base convert.h header.

## Key Types
None

## Key Functions
None

## Globals
- VoxelDrawer (ConvertClass*): Voxel rendering converter instance
- UnitDrawer (ConvertClass*): Unit rendering converter instance
- TerrainDrawer (ConvertClass*): Terrain rendering converter instance
- AnimDrawer (ConvertClass*): Animation rendering converter instance
- NormalDrawer (ConvertClass*): Normal rendering converter instance
- IsometricDrawer (ConvertClass*): Isometric rendering converter instance

## Dependencies
- convert.h (included)

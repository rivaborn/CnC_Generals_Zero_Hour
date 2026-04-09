# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/_convert.h

## Purpose
Header file declaring global instances of ConvertClass for various rendering types.

## Responsibilities
- Declares global ConvertClass instances for different drawers
- Provides external references for voxel, unit, terrain, animation, normal, and isometric rendering
- Includes the base convert.h header

## Key Types
None

## Key Functions
None

## Globals
- VoxelDrawer (ConvertClass*): Global instance for voxel rendering conversion
- UnitDrawer (ConvertClass*): Global instance for unit rendering conversion
- TerrainDrawer (ConvertClass*): Global instance for terrain rendering conversion
- AnimDrawer (ConvertClass*): Global instance for animation rendering conversion
- NormalDrawer (ConvertClass*): Global instance for normal rendering conversion
- IsometricDrawer (ConvertClass*): Global instance for isometric rendering conversion

## Dependencies
- convert.h (included header)
- ConvertClass (external class definition)

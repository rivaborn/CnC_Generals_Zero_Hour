# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/hanim.h

## Purpose
Defines the core animation classes and interfaces for the W3D engine, including hierarchical animation, pivot mapping, and animation blending.

## Responsibilities
- Declares base animation class (`HAnimClass`) with virtual interface
- Defines pivot mapping classes for per-bone weight control
- Implements animation combo system for blending/mixing animations
- Provides memory management via reference counting and auto-pooling

## Key Types
- **HAnimClass (Class)**: Base animation interface with frame/transform access
- **PivotMapClass (Class)**: Base class for pivot weight maps
- **NamedPivotMapClass (Class)**: Named pivot map with update capability
- **HAnimComboDataClass (Class)**: Animation data container with weight/frame info
- **HAnimComboClass (Class)**: Animation blending system with multiple channels
- **WeightInfoStruct (Struct)**: Stores name/weight pairs for named pivot maps

## Key Functions
### `Get_Transform`
- Purpose: Retrieves transformation matrix for a pivot at a given frame
- Calls: None visible in header

### `Build_Active_Pivot_Map`
- Purpose: Constructs active pivot map from named weights
- Calls: Not visible in header

### `Normalize_Weights`
- Purpose: Normalizes all animation weights in the combo
- Calls: Not visible in header

## Globals
- **EMBEDDED_SOUND_BONE_INDEX_NOT_SET (const int)**: Default value for sound bone index

## Dependencies
- `quat.h`, `refcount.h`, `w3d_file.h`, `hash.h`, `mempool.h`
- `DynamicVectorClass`, `RefCountClass`, `HashableClass`
- `Vector3`, `Quaternion`, `Matrix3D`

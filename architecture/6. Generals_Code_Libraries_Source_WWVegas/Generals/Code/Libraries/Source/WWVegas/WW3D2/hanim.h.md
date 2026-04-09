# Generals/Code/Libraries/Source/WWVegas/WW3D2/hanim.h

## Purpose
Defines the core animation system classes for the W3D engine, including base animation interface and animation blending/combo functionality.

## Responsibilities
- Declares base `HAnimClass` interface for all animation formats
- Defines animation combo system for blending/mixing animations
- Provides pivot mapping for per-bone weight control
- Manages animation data sharing and reference counting
- Supports both named and unnamed pivot weight maps

## Key Types
- `HAnimClass` (Class): Base interface for all animation formats
- `HAnimComboDataClass` (Class): Individual animation entry with frame/weight/pivot map
- `HAnimComboClass` (Class): Collection of animations for blending
- `PivotMapClass` (Class): Base class for pivot weight maps
- `NamedPivotMapClass` (Class): Pivot map with named bone references
- `WeightInfoStruct` (Struct): Stores name/weight pairs for named pivot maps

## Key Functions
### `HAnimClass::Get_Transform`
- Purpose: Retrieves transformation matrix for a pivot at a specific frame
- Calls: None visible

### `NamedPivotMapClass::Update_Pivot_Map`
- Purpose: Configures pivot map using an HTree
- Calls: None visible

### `HAnimComboClass::Normalize_Weights`
- Purpose: Normalizes all animation weights in the combo
- Calls: None visible

## Globals
- None

## Dependencies
- `quat.h`, `refcount.h`, `w3d_file.h`, `hash.h`, `mempool.h`
- `DynamicVectorClass`, `RefCountClass`, `HashableClass`
- `Vector3`, `Quaternion`, `Matrix3D`

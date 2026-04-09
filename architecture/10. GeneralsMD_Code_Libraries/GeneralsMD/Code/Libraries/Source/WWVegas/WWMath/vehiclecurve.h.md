# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/vehiclecurve.h

## Purpose
Defines a `VehicleCurveClass` for modeling vehicle movement paths with turn arcs based on a given radius.

## Responsibilities
- Manages vehicle path curves with turn arcs
- Provides evaluation and key manipulation for the curve
- Handles serialization (save/load) for persistence
- Tracks curve sharpness and evaluation time

## Key Types
- **VehicleCurveClass (Class)**: Represents a vehicle's movement path with turn arcs.
- **_ArcInfoStruct (Struct)**: Stores arc geometry data (center, points, angles, radius).
- **ArcInfoStruct (Type alias)**: Alias for `_ArcInfoStruct`.
- **ARC_LIST (Type alias)**: Dynamic vector of `ArcInfoStruct` for arc storage.

## Key Functions
### `VehicleCurveClass::Evaluate`
- Purpose: Computes the vehicle's position at a given time on the curve.
- Calls: Not inferable (implementation in `.cpp`).

### `VehicleCurveClass::Initialize_Arc`
- Purpose: Initializes the curve with a specified turn radius.
- Calls: Not inferable.

### `VehicleCurveClass::Update_Arc_List`
- Purpose: Recalculates arc data when the curve is modified.
- Calls: Not inferable.

### `VehicleCurveClass::Save` / `Load`
- Purpose: Serializes/deserializes the curve data.
- Calls: `ChunkSaveClass`/`ChunkLoadClass` methods.

## Globals
- **None**

## Dependencies
- `curve.h` (base `Curve3DClass`)
- `vector.h` (for `Vector3`)
- `ChunkSaveClass`/`ChunkLoadClass` (for serialization)

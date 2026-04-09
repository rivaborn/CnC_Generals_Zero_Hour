# Generals/Code/Libraries/Source/WWVegas/WWMath/vehiclecurve.h

## Purpose
Defines a `VehicleCurveClass` for modeling vehicle paths through turn arcs based on a turn radius.

## Responsibilities
- Manages vehicle path curves with turn arcs
- Handles key point manipulation (add/remove/set/clear)
- Evaluates curve positions at given times
- Tracks sharpness and last evaluation time
- Supports serialization via `Save`/`Load`

## Key Types
- **VehicleCurveClass (Class)**: Represents a vehicle's path curve with turn arcs.
- **_ArcInfoStruct (Struct)**: Stores arc geometry (center, points, angles, radius).
- **ArcInfoStruct (Type alias)**: Alias for `_ArcInfoStruct`.
- **ARC_LIST (Type alias)**: Dynamic vector of `ArcInfoStruct`.

## Key Functions
### `VehicleCurveClass::Evaluate`
- Purpose: Computes the curve position at a given time.
- Calls: `Update_Arc_List` (indirectly via `m_IsDirty` check).

### `VehicleCurveClass::Initialize_Arc`
- Purpose: Initializes the curve with a turn radius.
- Calls: None (directly).

### `VehicleCurveClass::Update_Arc_List`
- Purpose: Recalculates arc geometry when keys change.
- Calls: Not inferable (implementation in `.cpp`).

### `VehicleCurveClass::Save`/`Load`
- Purpose: Serializes/deserializes curve data.
- Calls: `Load_Variables` (in `Load`).

## Globals
- None.

## Dependencies
- **Includes**: `curve.h`, `vector.h`
- **Externals**: `Curve3DClass`, `PersistFactoryClass`, `ChunkSaveClass`, `ChunkLoadClass`, `DynamicVectorClass`

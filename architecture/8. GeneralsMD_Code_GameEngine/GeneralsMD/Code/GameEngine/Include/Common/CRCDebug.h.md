# GeneralsMD/Code/GameEngine/Include/Common/CRCDebug.h

## Purpose
Header for CRC debugging utilities in the SAGE engine, enabling logging and verification of game state for sync error tracking.

## Responsibilities
- Defines macros for dumping math types (vectors, matrices, coords)
- Provides logging functions for CRC verification
- Declares CRC verification classes and globals
- Conditionally enables/disables debug features

## Key Types
- `CRCVerification` (Class): RAII wrapper for CRC verification blocks
- `Vector3` (Type): 3D vector (external)
- `Coord3D` (Type): 3D coordinate (external)
- `Matrix3D` (Type): 3D transformation matrix (external)

## Key Functions
### `dumpVector3`
- Purpose: Logs a Vector3's components with metadata
- Calls: None visible

### `dumpCoord3D`
- Purpose: Logs a Coord3D's components with metadata
- Calls: None visible

### `dumpMatrix3D`
- Purpose: Logs a Matrix3D's components with metadata
- Calls: None visible

### `dumpReal`
- Purpose: Logs a floating-point value with metadata
- Calls: None visible

### `outputCRCDebugLines`
- Purpose: Outputs accumulated CRC debug lines
- Calls: None visible

### `outputCRCDumpLines`
- Purpose: Outputs accumulated CRC dump lines
- Calls: None visible

### `addCRCDebugLine`
- Purpose: Adds a formatted line to CRC debug output
- Calls: None visible

### `addCRCDumpLine`
- Purpose: Adds a formatted line to CRC dump output
- Calls: None visible

### `addCRCGenLine`
- Purpose: Adds a formatted line to CRC generation output
- Calls: None

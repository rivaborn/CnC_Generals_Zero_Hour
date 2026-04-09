# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/Module/W3DDependencyModelDraw.h

## Purpose
Defines a draw module that depends on another object's draw completion before rendering.

## Responsibilities
- Manages dependency-based drawing order
- Handles bone attachment for dependent models
- Adjusts transformation matrices for proper rendering
- Notifies when dependencies are cleared

## Key Types
- **W3DDependencyModelDrawModuleData (Class)**: Stores module configuration including bone attachment name
- **W3DDependencyModelDraw (Class)**: Main dependency-aware draw module class
- **W3DDependencyModelDrawMagicEnum (Enum)**: Not inferable (empty)
- **W3DDependencyModelDraw_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (empty)

## Key Functions
### W3DDependencyModelDraw::doDrawModule
- Purpose: Handles the actual drawing when dependencies are cleared
- Calls: Not inferable

### W3DDependencyModelDraw::notifyDrawModuleDependencyCleared
- Purpose: Signals that dependent objects have finished drawing
- Calls: Not inferable

### W3DDependencyModelDraw::adjustTransformMtx
- Purpose: Adjusts transformation matrix for proper rendering
- Calls: Not inferable

## Globals
- None

## Dependencies
- W3DModelDraw.h (inheritance)
- MultiIniFieldParse (for field parsing)
- Standard module macros (memory pool, module creation)
- Matrix3D (for transformation)

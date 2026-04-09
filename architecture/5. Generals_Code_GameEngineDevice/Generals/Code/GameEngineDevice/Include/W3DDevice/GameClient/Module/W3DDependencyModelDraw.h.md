# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/Module/W3DDependencyModelDraw.h

## Purpose
Defines a draw module that depends on another object's draw completion before rendering.

## Responsibilities
- Manages dependency-based drawing order
- Adjusts transform matrices for dependent rendering
- Provides notification when dependencies are cleared

## Key Types
- **W3DDependencyModelDrawModuleData (Class)**: Module data containing bone attachment reference
- **W3DDependencyModelDraw (Class)**: Main dependency-aware draw module
- **W3DDependencyModelDrawMagicEnum (Enum)**: Not inferable
- **W3DDependencyModelDraw_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### W3DDependencyModelDraw::doDrawModule
- Purpose: Handles the actual drawing when dependencies are cleared
- Calls: Not inferable

### W3DDependencyModelDraw::notifyDrawModuleDependencyCleared
- Purpose: Notifies module that dependencies are ready
- Calls: Not inferable

### W3DDependencyModelDraw::adjustTransformMtx
- Purpose: Adjusts transform matrix for dependent rendering
- Calls: Not inferable

## Globals
- None

## Dependencies
- W3DModelDraw.h
- MultiIniFieldParse (used in buildFieldParse)
- Matrix3D (used in transform operations)
- Thing (base class reference)
- ModuleData (base class reference)

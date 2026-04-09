# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/Module/W3DTreeDraw.h

## Purpose
Defines the W3DTreeDraw module for rendering 3D tree models in the game.

## Responsibilities
- Manages tree model rendering with customizable parameters
- Handles tree toppling effects and shadow rendering
- Provides module data parsing for tree configuration
- Implements draw module interface for tree objects

## Key Types
- **W3DTreeDrawModuleData (Class)**: Contains tree rendering parameters (model, texture, toppling effects, shadows)
- **W3DTreeDraw (Class)**: Draw module implementation for tree rendering
- **W3DTreeDrawMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **W3DTreeDraw_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely internal macro enum)

## Key Functions
### W3DTreeDrawModuleData::buildFieldParse
- Purpose: Parses tree module data from configuration files
- Calls: MultiIniFieldParse methods

### W3DTreeDraw::doDrawModule
- Purpose: Renders the tree model with current transform
- Calls: Not specified in header

### W3DTreeDraw::reactToTransformChange
- Purpose: Handles updates when tree transform changes
- Calls: Not specified in header

## Globals
- None

## Dependencies
- Common/DrawModule.h
- WW3D2/Line3D.h
- ModuleData, MultiIniFieldParse, AsciiString, FXList, Matrix3D, Coord3D classes
- Memory pool and module macro definitions

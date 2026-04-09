# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/Module/W3DPropDraw.h

## Purpose
Defines a module for drawing 3D props in the W3D rendering system.

## Responsibilities
- Manages 3D prop rendering via `DrawModule`
- Handles prop-specific drawing logic
- Supports shadow and shroud state management
- Provides module data for prop configuration

## Key Types
- **W3DPropDrawModuleData (Class)**: Stores prop model name and parsing logic
- **W3DPropDraw (Class)**: Main prop drawing module with rendering and state callbacks
- **W3DPropDrawMagicEnum (Enum)**: Not inferable (empty)
- **W3DPropDraw_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (empty)

## Key Functions
### W3DPropDraw::doDrawModule
- Purpose: Renders the prop using the given transform matrix
- Calls: Not inferable (implementation not shown)

### W3DPropDraw::reactToTransformChange
- Purpose: Handles updates when the prop's transform changes
- Calls: Not inferable

## Globals
- None

## Dependencies
- `Common/DrawModule.h`
- `WW3D2/Line3D.h`
- `ModuleData`, `MultiIniFieldParse`, `AsciiString`, `Thing`, `Matrix3D`, `Coord3D`, `Bool`, `Real`

# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/Common/Thing/W3DModuleFactory.cpp

## Purpose
Initializes and registers W3D-specific rendering modules for the game engine.

## Responsibilities
- Extends base `ModuleFactory` initialization
- Registers W3D draw modules (e.g., models, debris, lasers)
- Provides factory pattern for W3D rendering components

## Key Types
- `W3DModuleFactory` (Class): Factory for W3D rendering modules

## Key Functions
### `init()`
- Purpose: Registers all W3D-specific draw modules
- Calls: `ModuleFactory::init()`, `addModule()` for each module type

## Globals
None

## Dependencies
- `W3DModuleFactory.h`
- Multiple W3D draw module headers (e.g., `W3DModelDraw.h`, `W3DLaserDraw.h`)
- `ModuleFactory` base class

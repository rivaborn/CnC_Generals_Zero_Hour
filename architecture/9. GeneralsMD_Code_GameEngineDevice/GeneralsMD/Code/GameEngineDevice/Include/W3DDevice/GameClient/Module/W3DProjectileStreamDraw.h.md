# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/Module/W3DProjectileStreamDraw.h

## Purpose
Defines a draw module for rendering textured lines between projectiles in the game.

## Responsibilities
- Manages rendering of segmented lines between projectiles
- Handles texture tiling and scrolling for projectile streams
- Maintains line geometry across frames
- Provides module data for configuration

## Key Types
- **W3DProjectileStreamDrawModuleData (Class)**: Stores module configuration (texture, width, tiling, etc.)
- **W3DProjectileStreamDraw (Class)**: Draw module implementation for projectile streams
- **SegmentedLineClass (Class)**: External line rendering class
- **TextureClass (Class)**: External texture class
- **Vector3 (Class)**: External 3D vector class
- **W3DProjectileStreamDrawMagicEnum (Enum)**: Not inferable
- **W3DProjectileStreamDraw_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable

## Key Functions
### W3DProjectileStreamDraw::doDrawModule
- Purpose: Renders the projectile stream using the current transform
- Calls: makeOrUpdateLine

### W3DProjectileStreamDraw::makeOrUpdateLine
- Purpose: Creates or updates a segmented line between projectile points
- Calls: Not inferable

### W3DProjectileStreamDrawModuleData::buildFieldParse
- Purpose: Parses module data from configuration files
- Calls: Not inferable

## Globals
- None

## Dependencies
- `Common/DrawModule.h`
- `GameLogic/Module/ProjectileStreamUpdate.h`
- `SegmentedLineClass`
- `TextureClass`
- `Vector3`
- `ModuleData`
- `AsciiString`
- `Real`
- `Int`
- `Un

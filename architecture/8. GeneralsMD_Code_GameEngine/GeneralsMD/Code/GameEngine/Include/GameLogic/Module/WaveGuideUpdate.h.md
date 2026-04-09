# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/WaveGuideUpdate.h

## Purpose
Defines the WaveGuideUpdate module for handling water wave effects in the game.

## Responsibilities
- Manages wave propagation logic for water-based effects
- Handles wave shape computation and transformation
- Applies wave effects (motion, shore effects, damage)
- Manages particle systems and audio events for wave effects

## Key Types
- **WaveGuideUpdateModuleData (Class)**: Contains configuration data for wave behavior (timing, size, effects)
- **WaveGuideUpdate (Class)**: Main update module handling wave simulation and effects
- **WaveGuideUpdateMagicEnum (Enum)**: Not inferable (likely internal macro enum)
- **MAX_WAVEGUIDE_SHAPE_POINTS (Enum)**: Constant for maximum wave shape points (64)
- **MAX_SHAPE_EFFECTS (Enum)**: Constant for maximum shape effects per point (3)

## Key Functions
### WaveGuideUpdate::update
- Purpose: Main update loop for wave propagation
- Calls: initWaveGuide, startMoving, computeWaveShapePoints, transformWaveShape, doShapeEffects, doWaterMotion, doShoreEffects, doDamage

### WaveGuideUpdate::initWaveGuide
- Purpose: Initializes the waveguide when motion starts
- Calls: Not inferable

### WaveGuideUpdate::computeWaveShapePoints
- Purpose: Calculates the wave shape points
- Calls: Not inferable

### WaveGuideUpdate::doDamage
- Purpose: Applies damage to objects in the wave path
- Calls: Not inferable

## Globals
- None

## Dependencies
- UpdateModule.h (base class)
- FieldParse (forward reference)
- MultiIniFieldParse (for configuration parsing)
- AudioEventRTS, ParticleSystemTemplate (audio/visual effects)
- Coord3D

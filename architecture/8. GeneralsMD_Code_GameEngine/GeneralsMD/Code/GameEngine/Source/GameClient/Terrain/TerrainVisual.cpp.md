# GeneralsMD/Code/GameEngine/Source/GameClient/Terrain/TerrainVisual.cpp

## Purpose
Handles the visual representation of terrain in the game client, including loading and managing terrain data.

## Responsibilities
- Manages terrain visual state (loading, resetting, updating)
- Stores terrain filename and basic metadata
- Provides interface for terrain serialization (Xfer/CRC)
- Implements seismic simulation effects (dome-style explosions)

## Key Types
- **TerrainVisual (Class)**: Base class for terrain visual representation
- **SeismicSimulationFilterBase (Class)**: Base class for seismic simulation filters
- **DomeStyleSeismicFilter (Class)**: Implements dome-style explosion effects on terrain

## Key Functions
### TerrainVisual::load
- Purpose: Loads terrain from a file and stores the filename
- Calls: None

### DomeStyleSeismicFilter::filterCallback
- Purpose: Applies dome-style seismic effects to terrain heightmap
- Calls: `heightMap->getBilinearSampleSeismicZVelocity`, `heightMap->setSeismicZVelocity`

### DomeStyleSeismicFilter::applyGravityCallback
- Purpose: Applies gravity effect to seismic velocity
- Calls: None

## Globals
- **TheTerrainVisual (TerrainVisual*)**: Global pointer to the terrain visual instance

## Dependencies
- `PreRTS.h`, `Common/Xfer.h`, `GameClient/TerrainVisual.h`
- `Xfer` class for serialization
- `WorldHeightMapInterfaceClass` for terrain heightmap access

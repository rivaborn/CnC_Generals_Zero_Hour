# GeneralsMD/Code/GameEngine/Include/GameClient/TerrainVisual.h

## Purpose
Defines the `TerrainVisual` class and related structures for terrain rendering and simulation in the SAGE engine.

## Responsibilities
- Manages terrain visual representation (textures, water, LOD)
- Handles seismic simulations (earthquake effects)
- Provides terrain querying (colors, tiles, intersections)
- Controls water grid properties and transformations
- Maintains skybox textures

## Key Types
- `SeismicSimulationNode` (struct): Represents an earthquake simulation node with position, radius, and magnitude.
- `SeismicSimulationFilterBase` (class): Abstract base for seismic simulation filters.
- `TerrainLOD` (enum): Defines terrain detail levels (min, max, automatic, etc.).
- `TerrainVisual` (class): Main terrain rendering and simulation interface.
- `DomeStyleSeismicFilter` (class): Concrete seismic filter implementation.

## Key Functions
### `SeismicSimulationNode::handleFilterCallback`
- Purpose: Applies seismic filter to heightmap.
- Calls: `callbackFilter->filterCallback`

### `TerrainVisual::intersectTerrain`
- Purpose: Ray-terrain intersection test.
- Calls: None (pure virtual).

### `TerrainVisual::updateSeismicSimulations`
- Purpose: Updates all active seismic simulations.
- Calls: None (pure virtual).

## Globals
- `TheTerrainVisual` (TerrainVisual*): Singleton instance of the terrain visual system.

## Dependencies
- `Common/Terrain.h`, `Common/Snapshot.h`, `Common/MapObject.h`
- `WorldHeightMapInterfaceClass`, `ThingTemplate`, `Xfer` (external)

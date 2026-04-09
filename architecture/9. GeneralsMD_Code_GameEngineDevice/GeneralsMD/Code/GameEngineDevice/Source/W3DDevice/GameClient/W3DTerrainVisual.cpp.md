# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DTerrainVisual.cpp

## Purpose
Handles W3D implementation details for terrain visual aspects, including terrain rendering, water effects, seismic simulations, and terrain modifications.

## Responsibilities
- Manages terrain and water render objects
- Handles seismic simulations and terrain deformation
- Controls terrain modifications (bibs, props, tracks)
- Manages skybox textures and water grid rendering
- Serializes terrain state via Xfer system

## Key Types
- **TestSeismicFilter (Class)**: Implements seismic simulation filtering with gravity application
- **W3DTerrainVisual (Class)**: Main terrain visual management class (inherits from TerrainVisual)

## Key Functions
### TestSeismicFilter::filterCallback
- Purpose: Applies seismic simulation effects to heightmap based on explosion parameters
- Calls: heightMap->getBilinearSampleSeismicZVelocity, heightMap->setSeismicZVelocity

### TestSeismicFilter::applyGravityCallback
- Purpose: Applies gravity to seismic velocities
- Calls: None

### W3DTerrainVisual::init
- Purpose: Initializes terrain visual components including render objects and systems
- Calls: TerrainVisual::init, NEW_REF, NEW, TheTerrainTracksRenderObjClassSystem->init, TheW3DShadowManager->init, TheSmudgeManager->init

### W3DTerrainVisual::update
- Purpose: Updates terrain visual state including seismic simulations and water
- Calls: TerrainVisual::update, handleSeismicSimulations, m_waterRenderObject->update

### W3DTerrainVisual::addSeismicSimulation
- Purpose: Adds a seismic simulation node to the processing queue
- Calls: m_seismicSimulationList.push_back

### W3DTerrainVisual::handleSeismicSimulations
- Purpose: Processes all pending seismic simulations
- Calls: m_clientHeightMap->clearSeismicUpdateFlags, testSeismicFilter.filterCallback, testSeismicFilter.applyGravityCallback

## Globals
- **testSeismicFilter (TestSeismicFilter)**: Static instance for seismic filtering

## Dependencies
- Common headers: GameState, GlobalData, PerfTimer, MapReaderWriterInfo, ThingTemplate, WellKnownKeys, TerrainTypes, Xfer, UnitTimings, QuickTrig
- GameClient headers: Drawable, ClientRandomValue
- GameLogic headers: Object, GameLogic
- W3DDevice headers: W3DScene, W3DTerrainVisual, WorldHeightMap, W3DWater, W3DDisplay, W3DDebugIcons, W3DTerrainTracks, W3DGranny, W3DShadow, heightmap, FlatHeightmap, W3DSmudge, W3DModelDraw
- WW3D2 headers: Light, RendObj, ColType, ColTest, assetmgr

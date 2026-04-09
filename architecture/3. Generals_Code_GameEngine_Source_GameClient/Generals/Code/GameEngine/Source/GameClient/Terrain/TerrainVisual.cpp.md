# Generals/Code/GameEngine/Source/GameClient/Terrain/TerrainVisual.cpp

## Purpose
Base class for terrain visual representation in the game client.

## Responsibilities
- Manages terrain visual state
- Handles terrain loading and initialization
- Provides interface for terrain serialization (Xfer/CRC)
- Maintains filename reference for terrain data

## Key Types
- `TerrainVisual` (Class): Base class for terrain visual representation

## Key Functions
### `TerrainVisual::TerrainVisual()`
- Purpose: Default constructor
- Calls: None

### `TerrainVisual::~TerrainVisual()`
- Purpose: Destructor
- Calls: None

### `TerrainVisual::init()`
- Purpose: Initializes device-independent terrain functionality
- Calls: None

### `TerrainVisual::reset()`
- Purpose: Resets terrain visual state
- Calls: None

### `TerrainVisual::update()`
- Purpose: Updates terrain visual state
- Calls: None

### `TerrainVisual::load(AsciiString filename)`
- Purpose: Loads terrain from specified filename
- Calls: None

### `TerrainVisual::crc(Xfer *xfer)`
- Purpose: Generates CRC checksum for serialization
- Calls: None

### `TerrainVisual::xfer(Xfer *xfer)`
- Purpose: Serializes/deserializes terrain data
- Calls: `xfer->xferVersion()`

### `TerrainVisual::loadPostProcess()`
- Purpose: Handles post-processing after terrain load
- Calls: None

## Globals
- `TheTerrainVisual` (TerrainVisual*): Global instance pointer

## Dependencies
- `PreRTS.h`, `Common/Xfer.h`, `GameClient/TerrainVisual.h`
- `Xfer` class for serialization
- `Ascii

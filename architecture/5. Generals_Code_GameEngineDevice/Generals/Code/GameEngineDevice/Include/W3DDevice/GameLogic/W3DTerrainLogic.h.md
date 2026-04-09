# Generals/Code/GameEngineDevice/Include/W3DDevice/GameLogic/W3DTerrainLogic.h

## Purpose
Defines the W3D-specific implementation of logical terrain functionality for the SAGE engine.

## Responsibilities
- Provides terrain height queries and collision detection
- Manages terrain extent and pathfinding boundaries
- Handles map loading and initialization
- Implements line-of-sight calculations
- Supports serialization via CRC and Xfer

## Key Types
- W3DTerrainLogic (Class): W3D-specific terrain logic implementation

## Key Functions
### W3DTerrainLogic()
- Purpose: Constructor for W3DTerrainLogic
- Calls: None

### ~W3DTerrainLogic()
- Purpose: Destructor for W3DTerrainLogic
- Calls: None

### init()
- Purpose: Initializes the terrain logic
- Calls: None

### reset()
- Purpose: Resets the terrain logic state
- Calls: None

### update()
- Purpose: Updates terrain logic state
- Calls: None

### loadMap()
- Purpose: Loads terrain height data from file
- Calls: None

### newMap()
- Purpose: Initializes logic for a new map
- Calls: None

### getGroundHeight()
- Purpose: Returns terrain height at given coordinates
- Calls: None

### isCliffCell()
- Purpose: Checks if a cell is a cliff
- Calls: None

### getLayerHeight()
- Purpose: Returns height at a specific pathfinding layer
- Calls: None

### isClearLineOfSight()
- Purpose: Checks line-of-sight between two points
- Calls: None

### crc()
- Purpose: Generates CRC checksum for serialization
- Calls: None

### xfer()
- Purpose: Serializes/deserializes terrain

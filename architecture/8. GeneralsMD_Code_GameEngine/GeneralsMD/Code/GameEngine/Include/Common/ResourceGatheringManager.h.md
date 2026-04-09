# GeneralsMD/Code/GameEngine/Include/Common/ResourceGatheringManager.h

## Purpose
Manages resource gathering logic for a player, tracking supply centers and warehouses and making decisions for resource transport.

## Responsibilities
- Tracks supply centers and warehouses
- Finds optimal supply centers/warehouses for resource transport
- Manages addition/removal of supply points
- Supports game state serialization (snapshot)

## Key Types
- **ResourceGatheringManager (Class)**: Manages resource gathering decisions
- **objectIDList (Class)**: Typedef for list of ObjectID (std::list<ObjectID>)
- **iterator (Class)**: Typedef for objectIDList iterator (std::list<ObjectID>::iterator)

## Key Functions
### ResourceGatheringManager()
- Purpose: Constructor for ResourceGatheringManager
- Calls: Not inferable

### findBestSupplyWarehouse()
- Purpose: Determines optimal warehouse for a truck to visit
- Calls: Not inferable

### findBestSupplyCenter()
- Purpose: Determines optimal supply center for a truck to return to
- Calls: Not inferable

### addSupplyCenter()
- Purpose: Registers a new supply center
- Calls: Not inferable

### removeSupplyCenter()
- Purpose: Removes a supply center from tracking
- Calls: Not inferable

### addSupplyWarehouse()
- Purpose: Registers a new supply warehouse
- Calls: Not inferable

### removeSupplyWarehouse()
- Purpose: Removes a supply warehouse from tracking
- Calls: Not inferable

### crc()
- Purpose: Generates CRC for snapshot serialization
- Calls: Not inferable

### xfer()
- Purpose: Handles data transfer for snapshot
- Calls: Not inferable

### loadPostProcess()
- Purpose: Post-processing after loading snapshot
- Calls:

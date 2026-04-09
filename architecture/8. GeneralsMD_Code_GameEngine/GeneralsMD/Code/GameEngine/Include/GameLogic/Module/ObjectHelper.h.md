# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ObjectHelper.h

## Purpose
Defines the ObjectHelper class, a base class for game objects that need periodic updates.

## Responsibilities
- Provides memory management via MEMORY_POOL_GLUE_ABC
- Implements snapshot methods (crc, xfer, loadPostProcess) for save/load
- Manages update scheduling via UpdateModule
- Offers sleepUntil() for delayed execution

## Key Types
- ObjectHelper (Class): Base class for updatable game objects
- ObjectHelperMagicEnum (Enum): Not inferable (placeholder)
- ObjectHelper_GLUE_NOT_IMPLEMENTED (Enum): Not inferable (placeholder)

## Key Functions
### ObjectHelper()
- Purpose: Constructor initializing UpdateModule and setting initial sleep state
- Calls: UpdateModule constructor, setWakeFrame

### sleepUntil()
- Purpose: Pauses object updates until specified frame
- Calls: setWakeFrame

### crc()
- Purpose: Generates CRC checksum for object state
- Calls: Not inferable

### xfer()
- Purpose: Serializes/deserializes object state
- Calls: Not inferable

### loadPostProcess()
- Purpose: Post-processing after loading
- Calls: Not inferable

## Globals
None

## Dependencies
- UpdateModule.h (inheritance)
- Xfer (snapshot system)
- Thing (game object base)
- ModuleData (module configuration)
- MEMORY_POOL_GLUE_ABC (memory management macro)

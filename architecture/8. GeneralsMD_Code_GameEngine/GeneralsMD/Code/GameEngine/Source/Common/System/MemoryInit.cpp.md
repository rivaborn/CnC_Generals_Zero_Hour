# GeneralsMD/Code/GameEngine/Source/Common/System/MemoryInit.cpp

## Purpose
Initializes memory pools for the game engine, including DMA pools and object-specific allocations.

## Responsibilities
- Defines default DMA pool parameters
- Configures object pool sizes via `PoolSizeRec` array
- Adjusts pool sizes based on INI file overrides
- Initializes memory manager pools at startup

## Key Types
- **PoolSizeRec (struct)**: Stores initial and overflow counts for object pools
- **PoolInitRec (struct)**: DMA pool configuration (external)

## Key Functions
### userMemoryManagerGetDmaParms
- Purpose: Returns default DMA pool configuration
- Calls: None

### userMemoryAdjustPoolSize
- Purpose: Adjusts pool sizes based on configuration
- Calls: `strcmp`, `DEBUG_CRASH`

### roundUpMemBound
- Purpose: Aligns memory bounds to 4-byte boundary
- Calls: None

### userMemoryManagerInitPools
- Purpose: Initializes memory pools from INI file
- Calls: `fopen`, `fgets`, `sscanf`, `stricmp`, `roundUpMemBound`

## Globals
- **sizes (PoolSizeRec[])**: Array of pool size configurations

## Dependencies
- `GameMemory.h` (external)
- `BaseType.h` (external)
- Standard C library functions (`fopen`, `fgets`, etc.)

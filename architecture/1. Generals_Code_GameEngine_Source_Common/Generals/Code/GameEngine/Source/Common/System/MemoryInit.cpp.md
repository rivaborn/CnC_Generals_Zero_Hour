# Generals/Code/GameEngine/Source/Common/System/MemoryInit.cpp

## Purpose
This file manages memory initialization and pool sizes for the game engine, including DMA parameters and custom pool adjustments.

## Responsibilities
- Initialize DMA parameters with predefined pool sizes.
- Adjust pool sizes based on configuration files.
- Round up memory bounds to alignment requirements.
- Load and apply custom memory pool settings from an INI file.

## Key Types
- **PoolSizeRec (Class)**: Stores initial and overflow allocation counts for different memory pools.

## Key Functions
### userMemoryManagerGetDmaParms
- Purpose: Provides default DMA parameters for memory management.
- Calls: None

### userMemoryAdjustPoolSize
- Purpose: Adjusts the initial and overflow allocation counts for a specified pool.
- Calls: roundUpMemBound

### roundUpMemBound
- Purpose: Rounds up an integer to the nearest multiple of 4.
- Calls: None

### userMemoryManagerInitPools
- Purpose: Initializes memory pools by loading settings from an INI file.
- Calls: fopen, fgets, sscanf, fclose, roundUpMemBound

## Globals
- **sizes (PoolSizeRec[])**: Array of pool size records with initial and overflow counts.

## Dependencies
- Key includes:
  - "Lib/BaseType.h"
  - "Common/GameMemory.h"
- External symbols used but not defined here:
  - Int (likely a typedef for int)
  - PoolInitRec (defined elsewhere)
  - DEBUG_CRASH (defined elsewhere)

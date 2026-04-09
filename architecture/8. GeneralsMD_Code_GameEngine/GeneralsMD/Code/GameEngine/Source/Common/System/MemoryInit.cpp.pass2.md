# GeneralsMD/Code/GameEngine/Source/Common/System/MemoryInit.cpp - Enhanced Analysis

## Architectural Role
This file is the central memory management configuration hub for the SAGE engine, defining pool sizes for nearly all game objects and DMA allocations. It bridges low-level memory allocation with high-level game object instantiation, ensuring optimal performance for the real-time strategy workload.

## Cross-References
### Incoming
- Memory allocation subsystem (GameMemory.h)
- Object factories (ThingTemplatePool, Drawable, etc.)
- W3D rendering system (MeshClass, TextureClass, etc.)
- AI system (AIGroupPool, AIStateMachine, etc.)

### Outgoing
- Standard C library (stdio.h for INI parsing)
- Debug system (DEBUG_CRASH for missing pool definitions)

## Design Patterns
- **Configuration Table Pattern**: Uses `PoolSizeRec` array for centralized pool definitions
- **Factory Method**: `userMemoryAdjustPoolSize` acts as a factory for pool size adjustments
- **Singleton-like Initialization**: `userMemoryManagerInitPools` runs once at startup to configure memory

Rules followed. Output under 400 tokens.

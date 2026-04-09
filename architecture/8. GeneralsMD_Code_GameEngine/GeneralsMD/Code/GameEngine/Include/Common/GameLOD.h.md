# GeneralsMD/Code/GameEngine/Include/Common/GameLOD.h

## Purpose
Defines the Level of Detail (LOD) management system for the game, including static and dynamic LOD levels, hardware detection, and rendering optimization.

## Responsibilities
- Define enums for CPU types, chipset types, and LOD levels
- Declare classes for LOD info, presets, and benchmarks
- Provide the `GameLODManager` class to control and query LOD settings
- Manage particle and debris rendering based on performance

## Key Types
- **ParticlePriorityType (Enum)**: Not inferable.
- **StaticGameLODLevel (Enum)**: Static LOD levels (unknown, low, medium, high, custom).
- **DynamicGameLODLevel (Enum)**: Dynamic LOD levels (unknown, low, medium, high, very high).
- **CpuType (Enum)**: CPU types (unknown, P3, P4, K7).
- **ChipsetType (Enum)**: Graphics chipset types (various GPUs and pixel shader versions).
- **StaticGameLODInfo (Class)**: Stores static LOD settings (FPS, particle limits, texture reduction, etc.).
- **DynamicGameLODInfo (Class)**: Stores dynamic LOD settings (FPS, particle/debris skip masks, slow death scale).
- **LODPresetInfo (Class)**: Hardware configuration preset (CPU, MHz, video type, memory).
- **BenchProfile (Class)**: Benchmark profile (CPU type, MHz, integer/float/memory benchmarks).
- **GameLODManager (Class)**: Manages LOD levels, hardware detection, and rendering optimizations.

## Key Functions
### `GameLODManager::findStaticLODLevel`
- Purpose: Calculate the optimal static LOD level for the system.
- Calls: Not inferable.

### `GameLODManager::setStaticLODLevel`
- Purpose: Set the current static LOD level.
- Calls: Not inferable.

### `GameLODManager::findDynamicLODLevel`
- Purpose: Given an average FPS, return the optimal dynamic LOD.
- Calls: Not inferable.

### `GameLODManager::setDynamicLODLevel`
- Purpose: Set the current dynamic LOD level.
- Calls: Not inferable.

### `GameLODManager::isParticleSkipped`
- Purpose: Check if a particle should be skipped based on dynamic LOD.
- Calls: Not inferable.

### `GameLODManager::isDebrisSkipped`
- Purpose: Check if debris should be skipped based on dynamic LOD.
- Calls: Not inferable.

### `GameLODManager::getSlowDeathScale`
- Purpose: Get the slow death scale for dynamic LOD.
- Calls: Not inferable.

### `

# GeneralsMD/Code/GameEngine/Source/Common/GameLOD.cpp

## Purpose
Manages Level of Detail (LOD) settings for game graphics and performance based on hardware capabilities and user preferences.

## Responsibilities
- Loads and applies LOD presets from INI files
- Determines optimal LOD levels based on hardware benchmarks
- Applies LOD settings to game systems (particles, shadows, textures, etc.)
- Handles dynamic LOD adjustments during gameplay
- Manages custom LOD configurations

## Key Types
- **GameLODManager (Class)**: Central manager for LOD settings
- **StaticGameLODInfo (Struct)**: Stores static LOD settings (particle counts, shadow types, etc.)
- **DynamicGameLODInfo (Struct)**: Stores dynamic LOD settings (particle skip masks, FPS thresholds)
- **LODPresetInfo (Struct)**: Hardware configuration presets for LOD levels
- **BenchProfile (Struct)**: Hardware benchmark profiles

## Key Functions
### `init`
- Purpose: Initializes LOD manager, loads presets, and determines optimal settings
- Calls: `testMinimumRequirements`, `refreshCustomStaticLODLevel`, `setStaticLODLevel`

### `findStaticLODLevel`
- Purpose: Determines the recommended static LOD level based on hardware
- Calls: `testMinimumRequirements`

### `applyStaticLODLevel`
- Purpose: Applies static LOD settings to game systems
- Calls: `refreshCustomStaticLODLevel`, `TheGameClient->adjustLOD`, `TheGameClient->releaseShadows`, `TheGameClient->allocateShadows`, `TheTerrainVisual->setShoreLineDetail`, `TheTerrainVisual->setTerrainTracksDetail`

### `findDynamicLODLevel`
- Purpose: Determines dynamic LOD level based on current FPS
- Calls: None

### `applyDynamicLODLevel`
- Purpose: Applies dynamic LOD settings
- Calls: None

## Globals
- **TheGameLODManager (GameLODManager*)**: Singleton instance of the LOD manager
- **TheStaticGameLODFieldParseTable (FieldParse[])**: Parse table for static LOD settings
- **StaticGameLODNames (const char*[])**: Array of static LOD level names
- **TheDynamicGameLODFieldParseTable (FieldParse[])**: Parse table for dynamic LOD settings
- **DynamicGameLODNames (const char*[])**: Array of dynamic LOD level names
- **CPUNames (char*[])**: Array of CPU type names
- **VideoNames (char*[])**: Array of video chip type names

## Dependencies
- Key includes: `GameLOD.h`, `TerrainVisual.h`, `GameClient.h`, `UserPreferences.h`, `ParticleSys.h`
- External symbols: `testMinimumRequirements`, `TheGlobalData`, `TheWritableGlobalData`, `TheGameClient`, `TheTerrainVisual`

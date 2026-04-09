# Generals/Code/GameEngine/Source/Common/GameLOD.cpp

## Purpose
This file manages game LOD (Level of Detail) settings, including static and dynamic LOD levels, parsing configuration files, and applying settings based on hardware capabilities.

## Responsibilities
- Manage static and dynamic LOD levels.
- Parse configuration files for LOD settings.
- Apply LOD settings to game systems based on hardware capabilities.
- Determine ideal LOD level based on benchmarking and user preferences.

## Key Types
- `GameLODManager` (Class): Manages LOD settings and applies them to the game.
- `StaticGameLODInfo` (Struct): Stores static LOD configuration information.
- `DynamicGameLODInfo` (Struct): Stores dynamic LOD configuration information.
- `BenchProfile` (Struct): Stores benchmark profile data.

## Key Functions
### testMinimumRequirements
- Purpose: Tests minimum hardware requirements.
- Calls: Not inferable.

### parseReallyLowMHz
- Purpose: Parses and sets the really low MHz value from an INI file.
- Calls: `TheGameLODManager->setReallyLowMHz(mhz)`

### INI::parseBenchProfile
- Purpose: Parses benchmark profile data from an INI file.
- Calls: `TheGameLODManager->newBenchProfile()`, `INI::parseInt`, `INI::parseReal`, `INI::parseIndexList`

### INI::parseLODPreset
- Purpose: Parses LOD preset data from an INI file.
- Calls: `TheGameLODManager->getStaticGameLODIndex(name)`, `TheGameLODManager->newLODPreset(index)`, `INI::parseInt`, `INI::parseIndexList`

### GameLODManager::init
- Purpose: Initializes the LOD manager by loading configuration files and setting initial LOD levels.
- Calls: `INI::load`, `OptionPreferences::getStaticGameDetail`, `OptionPreferences::getIdealStaticGameDetail`, `testMinimumRequirements`, `refreshCustomStaticLODLevel`

### GameLODManager::findStaticLODLevel
- Purpose: Determines the ideal static LOD level based on hardware capabilities.
- Calls: `testMinimumRequirements`, `INI::parseIndexList`, `OptionPreferences::write`

### GameLODManager::setStaticLODLevel
- Purpose: Sets the current static LOD level and applies settings.
- Calls: `applyStaticLODLevel(level)`

### GameLODManager::applyStaticLODLevel
- Purpose: Applies static LOD settings to game systems.
- Calls: `refreshCustomStaticLODLevel`, `TheGameClient->adjustLOD(0)`, `TheGameClient->releaseShadows()`, `TheGameClient->allocateShadows()`, `TheTerrainVisual->setShoreLineDetail()`, `TheTerrainVisual->setTerrainTracksDetail()`

### GameLODManager::findDynamicLODLevel
- Purpose: Determines the optimal dynamic LOD level based on average FPS.
- Calls: None

### GameLODManager::setDynamicLODLevel
- Purpose: Sets the current dynamic LOD level and applies settings.
- Calls: `applyDynamicLODLevel(level)`

### GameLODManager::applyDynamicLODLevel
- Purpose: Applies dynamic LOD settings to game systems.
- Calls: None

## Globals
- `TheGameLODManager` (GameLODManager*): Global instance of the LOD manager.
- `TheStaticGameLODFieldParseTable` (const FieldParse[]): Table for parsing static LOD fields.
- `StaticGameLODNames` (const char*[]): Array of static LOD names.
- `TheDynamicGameLODFieldParseTable` (const FieldParse[]): Table for parsing dynamic LOD fields.
- `DynamicGameLODNames` (const char*[]): Array of dynamic LOD names.
- `CP

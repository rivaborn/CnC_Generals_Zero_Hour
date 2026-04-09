# Generals/Code/Libraries/Source/WWVegas/WW3D2/dazzle.cpp

## Purpose
Manages dazzle (light effects) rendering, configuration, and persistence in the SAGE engine.

## Responsibilities
- Loads and initializes dazzle types from INI files
- Handles dazzle rendering with shaders and visibility checks
- Manages lens flare effects
- Provides persistence support for dazzle objects
- Maintains global dazzle state and layer management

## Key Types
- **DazzleINIClass (Class)**: Extended INI parser for vector types
- **DazzlePersistFactoryClass (Class)**: Handles dazzle object serialization
- **(anonymous enum) (Enum)**: Chunk IDs for persistence
- **DAZZLEFACTORY_CHUNKID_VARIABLES (Enum)**: Persistence chunk identifier
- **DAZZLEFACTORY_VARIABLE_OBJPOINTER (Enum)**: Object pointer micro-chunk ID
- **OBSOLETE_DAZZLEFACTORY_VARIABLE_TYPE (Enum)**: Obsolete type variable
- **DAZZLEFACTORY_VARIABLE_TRANSFORM (Enum)**: Transform variable
- **DAZZLEFACTORY_VARIABLE_TYPENAME (Enum)**: Type name variable

## Key Functions
### Init_Shaders
- Purpose: Configures default shaders for dazzle rendering
- Calls: ShaderClass methods (Set_Cull_Mode, Set_Depth_Mask, etc.)

## Globals
- **DAZZLE_LIST_STRING (const char*)**: INI section name for dazzle types
- **HALO_INTENSITY_POW_STRING (const char*)**: Halo intensity power parameter
- **HALO_SIZE_POW_STRING (const char*)**: Halo size power parameter
- **DAZZLE_INTENSITY_POW_STRING (const char*)**: Dazzle intensity power parameter
- **DAZZLE_SIZE_POW_STRING (const char*)**: Dazzle size power parameter
- **HALO_AREA_STRING (const char*)**: Halo area parameter
- **DAZZLE_AREA_STRING (const char*)**: Dazzle area parameter
- **HALO_SCALE_X_STRING (const char*)**: Halo X scale parameter
- **HALO_SCALE_Y_STRING (const char*)**: Halo Y scale parameter
- **DAZZLE_SCALE_X_STRING (const char*)**: Dazzle X scale parameter
- **DAZZLE_SCALE_Y_STRING (const char*)**: Dazzle Y scale parameter
- **HALO_INTENSITY_STRING (const char*)**: Halo intensity parameter
- **DAZZLE_INTENSITY_STRING (const char*)**: Dazzle intensity parameter
- **DAZZLE_DIRECTION_AREA_STRING (const char*)**: Dazzle direction area parameter
- **DAZZLE_DIRECTION_STRING (const char*)**: Dazzle direction parameter
- **FADEOUT_START_STRING (const char*)**: Fadeout start distance parameter
- **FADEOUT_END_STRING (const char*)**: Fadeout end distance parameter
- **SIZE_OPTIMIZATION_LIMIT_STRING (const char*)**: Size optimization limit parameter
- **HISTORY_WEIGHT_STRING (const char*)**: History weight parameter
- **DAZZLE_TEXTURE_STRING (const char*)**: Dazzle texture name parameter
- **HALO_TEXTURE_STRING (const char*)**: Halo texture name parameter
- **USE_CAMERA_TRANSLATION (const char*)**: Camera translation flag parameter
- **HALO_COLOR_STRING (const char*)**: Halo color parameter
- **DAZZLE_COLOR_STRING (const char*)**: Dazzle color parameter

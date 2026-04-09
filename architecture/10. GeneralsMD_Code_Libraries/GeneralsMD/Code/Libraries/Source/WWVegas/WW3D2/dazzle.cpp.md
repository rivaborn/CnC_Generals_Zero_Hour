# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/dazzle.cpp

## Purpose
Implements dazzle and lens flare rendering effects for the WW3D engine, including loading from INI files and persistence support.

## Responsibilities
- Loads and manages dazzle and lens flare types from INI files
- Renders dazzle effects (halos and lens flares) in the scene
- Provides persistence support for dazzle objects in save/load
- Handles visibility calculations for dazzle effects
- Manages dazzle layers and visibility lists

## Key Types
- **DazzleINIClass (Class)**: Extended INI parser supporting Vector2/3/4 types
- **DazzlePersistFactoryClass (Class)**: Handles save/load of dazzle objects
- **(anonymous enum) (Enum)**: Defines chunk IDs for persistence
- **DAZZLEFACTORY_CHUNKID_VARIABLES (Enum)**: Persistence chunk ID
- **DAZZLEFACTORY_VARIABLE_OBJPOINTER (Enum)**: Persistence variable type
- **OBSOLETE_DAZZLEFACTORY_VARIABLE_TYPE (Enum)**: Obsolete persistence variable
- **DAZZLEFACTORY_VARIABLE_TRANSFORM (Enum)**: Persistence variable for transform
- **DAZZLEFACTORY_VARIABLE_TYPENAME (Enum)**: Persistence variable for type name

## Key Functions
### Init_Shaders
- Purpose: Initializes shader states for dazzle rendering
- Calls: ShaderClass methods (Set_Cull_Mode, Set_Depth_Mask, etc.)

## Globals
- **DAZZLE_LIST_STRING (const char*)**: INI section name for dazzle list
- **DAZZLE_INTENSITY_POW_STRING (const char*)**: INI key for dazzle intensity power
- **DAZZLE_SIZE_POW_STRING (const char*)**: INI key for dazzle size power
- **DAZZLE_AREA_STRING (const char*)**: INI key for dazzle area
- **HALO_INTENSITY_POW (const char*)**: INI key for halo intensity power
- **_DazzleLoader (DazzleLoaderClass)**: Global dazzle loader instance
- **types (DazzleTypeClass**)**: Array of dazzle types
- **type_count (unsigned)**: Count of dazzle types
- **current_dazzle_layer (DazzleLayerClass**)**: Current active dazzle layer
- **lensflares (LensflareTypeClass**)**: Array of lens flare types
- **lensflare_count (unsigned)**: Count of lens flare types
- **default_dazzle_shader (ShaderClass)**: Default shader for dazzle
- **default_halo_shader (ShaderClass)**: Default shader for halo
- **vis_shader (ShaderClass)**: Visibility shader
- **debug_shader (ShaderClass)**: Debug shader
- **_DefaultVisibilityHandler (DazzleVisibilityClass)**: Default visibility handler
- **_VisibilityHandler (const DazzleVisibilityClass**)**: Current visibility handler
- **_DazzleFactory (DazzlePersistFactoryClass)**: Persistence factory instance

## Dependencies
- dazzle.h, simplevec.h, vector2.h, camera.h, ww3d.h, wwstring.h, wwdebug.h, assetmgr.h, vector3i.h, quat.h, ini.h, point.h, rinfo.h, vertmaterial.h, chunkio.h, wwfile.h, inisup.h, persistfactory.h, ww3dids.h, dx8wrapper.h, dx

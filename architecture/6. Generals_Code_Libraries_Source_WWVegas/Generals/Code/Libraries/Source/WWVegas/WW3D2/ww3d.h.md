# Generals/Code/Libraries/Source/WWVegas/WW3D2/ww3d.h

## Purpose
Header file defining the WW3D rendering engine's core interface, including scene management, rendering, and device control.

## Responsibilities
- Declares the WW3D class and its rendering-related enums
- Defines global rendering settings and statistics structures
- Provides forward declarations for key rendering classes
- Exposes rendering device management and configuration functions

## Key Types
- WW3D (Class): Main rendering engine interface
- PrelitModeEnum (Enum): Pre-lit rendering modes (vertex/lightmap)
- MeshDrawModeEnum (Enum): Mesh rendering modes (debug/normal)
- TextureThumbnailModeEnum (Enum): Texture thumbnail display modes
- TextureCompressionModeEnum (Enum): Texture compression settings
- NPatchesGapFillingModeEnum (Enum): N-patch gap filling options
- RenderStatistics (Struct): Performance metrics container

## Key Functions
### Init
- Purpose: Initialize the WW3D rendering system
- Calls: Not inferable

### Render
- Purpose: Render scenes or layers
- Calls: Not inferable

### Begin_Render/End_Render
- Purpose: Frame bracketing for rendering operations
- Calls: Not inferable

### Set_Render_Device
- Purpose: Configure rendering device and resolution
- Calls: Not inferable

### Sync
- Purpose: Advance engine timing for animations
- Calls: Not inferable

## Globals
- SyncTime (unsigned int): Current synchronized frame time
- PreviousSyncTime (unsigned int): Previous frame time for interval calculation
- IsInitted (bool): Engine initialization state
- DefaultStaticSortLists (RefRenderObjListClass*): Default static sort lists
- UserStat0/1/2 (long): User-controllable performance counters

## Dependencies
- "always.h", "vector3.h", "layer.h", "w3derr.h", "robjlist.h"
- SceneClass, CameraClass, ShaderClass, DX8Wrapper (forward declarations)
- Vector3, LayerListClass, LayerClass, RenderObjClass, RenderInfoClass (usage)

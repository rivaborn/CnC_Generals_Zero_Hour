# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/ww3d.h

## Purpose
Header file defining the WW3D rendering engine's core interface, including scene management, rendering, and device control.

## Responsibilities
- Declares WW3D class with rendering and device management functions
- Defines enums for rendering modes and configurations
- Declares supporting classes for materials, shaders, and rendering statistics
- Provides timing and performance measurement utilities

## Key Types
- WW3D (Class): Main rendering engine interface
- PrelitModeEnum (Enum): Pre-lit rendering modes
- MeshDrawModeEnum (Enum): Mesh drawing modes
- NPatchesGapFillingModeEnum (Enum): N-patches gap filling modes
- ScreenShotFormatEnum (Enum): Screenshot formats
- RenderStatistics (Struct): Performance statistics container

## Key Functions
### Init
- Purpose: Initialize the WW3D rendering system
- Calls: Not inferable

### Begin_Render
- Purpose: Start a rendering frame
- Calls: Not inferable

### Render
- Purpose: Render scenes or layers
- Calls: Not inferable

### End_Render
- Purpose: End a rendering frame
- Calls: Not inferable

### Make_Screen_Shot
- Purpose: Capture a screenshot
- Calls: Not inferable

### Sync
- Purpose: Update engine timing
- Calls: Not inferable

## Globals
- IsInitted (bool): Tracks initialization state
- SyncTime (unsigned int): Current sync time
- FrameCount (int): Frame counter
- DefaultNativeScreenSize (float): Default screen size for assets
- UserStat0/1/2 (long): User-defined statistics

## Dependencies
- "always.h", "vector3.h", "layer.h", "w3derr.h", "robjlist.h"
- SceneClass, CameraClass, ShaderClass, DX8Wrapper (forward declarations)
- Vector3 (used in function parameters)

# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/statistics.h

## Purpose
Header for texture memory tracking and rendering statistics in the WW3D2 subsystem.

## Responsibilities
- Declares texture recording and statistics tracking functions
- Defines macros for statistics recording
- Exposes counters for textures, polygons, vertices, and draw calls

## Key Types
- TextureClass (Class): texture resource handle
- StringClass (Class): string container
- ShaderClass (Class): shader resource handle
- RecordTextureMode (Enum): texture recording verbosity level

## Key Functions
### Record_Texture_Mode
- Purpose: Set texture recording mode
- Calls: None

### Get_Record_Texture_Mode
- Purpose: Get current texture recording mode
- Calls: None

### Record_Texture
- Purpose: Record a texture for statistics
- Calls: None

### Get_Record_Texture_Size
- Purpose: Get total texture size in bytes
- Calls: None

### Get_DX8_Polygons
- Purpose: Get polygon count
- Calls: None

### Begin_Statistics / End_Statistics / Shutdown_Statistics
- Purpose: Frame statistics lifecycle management
- Calls: None

## Globals
None

## Dependencies
- "always.h" (header guard utilities)
- TextureClass, StringClass, ShaderClass (forward declarations)

# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/statistics.cpp

## Purpose
Manages rendering statistics tracking for the SAGE engine, including texture usage, draw calls, and polygon/vertex counts.

## Responsibilities
- Tracks texture memory usage and changes per frame
- Records DirectX 8 skin/polygon/vertex statistics
- Manages frame-based statistics collection and reporting
- Generates human-readable texture statistics reports

## Key Types
- **TextureStatisticsStruct (struct)**: Stores per-texture usage and change counts
- **Debug_Statistics::RecordTextureMode (enum)**: Controls texture recording detail level

## Key Functions
### Record_Texture_Begin
- Purpose: Resets all texture tracking counters at frame start
- Calls: None

### Record_Texture_End
- Purpose: Finalizes texture statistics and generates report string
- Calls: None

### Debug_Statistics::Record_Texture
- Purpose: Records usage of a specific texture
- Calls: Find_Record_Texture, Add_Record_Texture

### Debug_Statistics::Record_DX8_Skin_Polys_And_Vertices
- Purpose: Tracks skin-rendered polygons and vertices
- Calls: None

### Debug_Statistics::Record_DX8_Polys_And_Vertices
- Purpose: Tracks general polygon/vertex counts with NPatch scaling
- Calls: DX8Wrapper::Get_Current_Caps(), WW3D::Get_NPatches_Level()

### Debug_Statistics::Begin_Statistics
- Purpose: Initializes all statistics counters at frame start
- Calls: Record_Texture_Begin, DX8Wrapper::Begin_Statistics()

### Debug_Statistics::End_Statistics
- Purpose: Finalizes all statistics at frame end
- Calls: Record_Texture_End, DX8Wrapper::End_Statistics()

## Globals
- **texture_memory (int)**: Current frame's total texture memory usage
- **texture_count (int)**: Number of unique textures used
- **lightmap_texture_memory (int)**: Memory used by lightmap textures
- **procedural_texture_memory (int)**: Memory used by procedural textures
- **record_texture_mode (Debug_Statistics::RecordTextureMode)**: Controls texture recording detail
- **texture_statistics (SimpleDynVecClass<TextureStatisticsStruct>)**: Tracks per-texture statistics
- **dx8_skin_renders (int)**: Count of skin-rendered draw calls
- **dx8_polygons (int)**: Total polygons rendered
- **draw_calls (int)**: Total draw calls this frame

## Dependencies
- **statistics.h**: Header for Debug_Statistics class
- **wwstring.h**: StringClass usage
- **simplevec.h**: SimpleDynVecClass for texture statistics
- **dx

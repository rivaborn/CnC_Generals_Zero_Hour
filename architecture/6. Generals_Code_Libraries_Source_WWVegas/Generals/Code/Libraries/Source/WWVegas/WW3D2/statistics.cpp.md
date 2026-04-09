# Generals/Code/Libraries/Source/WWVegas/WW3D2/statistics.cpp

## Purpose
Manages rendering statistics tracking for texture usage, draw calls, and polygon/vertex counts in the SAGE engine.

## Responsibilities
- Tracks texture memory usage and changes per frame
- Records DirectX 8 skin/polygon/vertex statistics
- Maintains frame-to-frame statistics for debugging
- Generates human-readable texture statistics reports
- Manages statistics collection lifecycle (begin/end/shutdown)

## Key Types
- **TextureStatisticsStruct (struct)**: Stores per-texture usage and change counts
- **Debug_Statistics (class)**: Main statistics collection interface (defined elsewhere)
- **RecordTextureMode (enum)**: Controls texture recording detail level (defined elsewhere)

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
- Calls: DX8Caps::Support_NPatches(), WW3D::Get_NPatches_Level()

### Debug_Statistics::Begin_Statistics
- Purpose: Initializes all statistics counters at frame start
- Calls: Record_Texture_Begin, DX8Wrapper::Begin_Statistics

### Debug_Statistics::End_Statistics
- Purpose: Finalizes all statistics at frame end
- Calls: Record_Texture_End, DX8Wrapper::End_Statistics

## Globals
- **texture_memory (int)**: Current frame's total texture memory usage
- **texture_count (int)**: Number of unique textures used this frame
- **lightmap_texture_memory (int)**: Memory used by lightmap textures
- **procedural_texture_memory (int)**: Memory used by procedural textures
- **record_texture_mode (Debug_Statistics::RecordTextureMode)**: Controls texture recording detail
- **texture_statistics (SimpleDynVecClass<TextureStatisticsStruct>)**: Per-texture statistics storage
- **dx8_skin_renders (int)**: Count of skin-rendered draw calls
- **dx8_polygons (int)**: Total polygons rendered
- **sorting_polygons (int)**: Polygons in sorting phase
- **draw_calls (int)**: Total draw calls this frame

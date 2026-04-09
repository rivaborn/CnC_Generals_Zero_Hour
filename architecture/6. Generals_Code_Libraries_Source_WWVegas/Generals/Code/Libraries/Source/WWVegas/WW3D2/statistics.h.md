# Generals/Code/Libraries/Source/WWVegas/WW3D2/statistics.h

## Purpose
Header file defining the Debug_Statistics namespace for tracking rendering performance metrics in the SAGE engine.

## Responsibilities
- Declares texture memory tracking functions
- Provides rendering statistics collection (polygons, vertices, draw calls)
- Defines texture recording modes and macros for statistics collection

## Key Types
- TextureClass (Class): texture resource handle
- StringClass (Class): string container
- ShaderClass (Class): shader resource handle
- RecordTextureMode (Enum): texture recording mode options

## Key Functions
### Record_Texture_Mode
- Purpose: Sets the texture recording mode
- Calls: None

### Get_Record_Texture_Mode
- Purpose: Retrieves current texture recording mode
- Calls: None

### Record_Texture
- Purpose: Records texture usage statistics
- Calls: None

### Get_Record_Texture_Size
- Purpose: Returns total texture size used in latest frame
- Calls: None

### Get_DX8_Polygons
- Purpose: Returns total polygons rendered
- Calls: None

### Begin_Statistics / End_Statistics / Shutdown_Statistics
- Purpose: Manages statistics collection lifecycle
- Calls: None

## Globals
- None

## Dependencies
- "always.h" (header guard utilities)
- TextureClass, StringClass, ShaderClass (forward declarations)
- Uses Debug_Statistics namespace for all symbols

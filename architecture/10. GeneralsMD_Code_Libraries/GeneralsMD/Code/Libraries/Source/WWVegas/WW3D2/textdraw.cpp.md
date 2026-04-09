# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/textdraw.cpp

## Purpose
Implements 3D text rendering functionality for the SAGE engine, handling character drawing, text measurement, and coordinate transformations.

## Responsibilities
- Manages dynamic mesh for text rendering
- Handles coordinate transformations and scaling
- Provides text measurement utilities (width/height)
- Renders individual characters and strings
- Supports debug font visualization

## Key Types
- **TextDrawClass (Class)**: Main text rendering class that extends DynamicMeshClass
- **VertexMaterialClass (Class)**: Material for vertex rendering (external)
- **ShaderClass (Class)**: Shader configuration for text rendering (external)
- **Font3DInstanceClass (Class)**: Font data provider (external)
- **Vector2 (Struct)**: 2D vector for coordinate storage
- **RectClass (Struct)**: Rectangle definition for UV coordinates

## Key Functions
### TextDrawClass::TextDrawClass(int max_chars)
- Purpose: Constructor that initializes text rendering resources
- Calls: NEW_REF, Set_Vertex_Material, Set_Shader, Enable_Sort, Set_Coordinate_Ranges

### TextDrawClass::Reset()
- Purpose: Resets the mesh and reinstalls default rendering settings
- Calls: Reset_Flags, Reset_Mesh_Counters, Enable_Sort, Set_Vertex_Material, Set_Shader

### TextDrawClass::Quad(float x0, float y0, float x1, float y1, float u0, float v0, float u1, float v1)
- Purpose: Draws a textured quad with specified coordinates
- Calls: Begin_Tri_Strip, Vertex, End_Tri_Strip

### TextDrawClass::Print(Font3DInstanceClass *font, char ch, float screen_x, float screen_y)
- Purpose: Renders a single character at specified screen coordinates
- Calls: Char_Width, Char_Spacing, Char_Height, Char_UV, Peek_Texture, Set_Texture, Quad

### TextDrawClass::Print(Font3DInstanceClass *font, const char *message, float screen_x, float screen_y)
- Purpose: Renders a complete string of text
- Calls: Print (character version)

## Globals
- **TextColor (Vector3)**: Stores the current text color (1.0f, 1.0f, 1.0f by default)
- **DefaultVertexMaterial (VertexMaterialClass)**: Default material for text rendering
- **DefaultShader (ShaderClass)**: Default shader configuration
- **TranslateScale (Vector2)**: Scale factors for coordinate transformation
- **TranslateOffset (Vector2)**: Offset values for coordinate transformation
- **PixelSize (Vector2)**: Size of a pixel in normalized coordinates

##

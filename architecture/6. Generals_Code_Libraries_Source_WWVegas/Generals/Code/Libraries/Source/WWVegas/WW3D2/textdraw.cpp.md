# Generals/Code/Libraries/Source/WWVegas/WW3D2/textdraw.cpp

## Purpose
Handles 3D text rendering in the SAGE engine, managing dynamic meshes and font display.

## Responsibilities
- Manages text drawing via dynamic mesh rendering
- Handles coordinate transformations for text placement
- Provides font measurement utilities (width/height)
- Supports basic 2D primitives (quads, lines) for text rendering
- Maintains texture and shader state for text rendering

## Key Types
- **TextDrawClass (Class)**: Main text rendering class that extends DynamicMeshClass
- **VertexMaterialClass (Type)**: Material used for text vertices
- **ShaderClass (Type)**: Shader configuration for text rendering
- **Font3DInstanceClass (Type)**: Font resource used for text drawing

## Key Functions
### TextDrawClass::Print(Font3DInstanceClass*, char, float, float)
- Purpose: Renders a single character at specified screen coordinates
- Calls: Font3DInstanceClass methods (Char_Width, Char_Spacing, Char_UV, Peek_Texture), Quad()

### TextDrawClass::Print(Font3DInstanceClass*, const char*, float, float)
- Purpose: Renders a complete string at specified screen coordinates
- Calls: Print(Font3DInstanceClass*, char, float, float)

### TextDrawClass::Quad(float, float, float, float, float, float, float, float)
- Purpose: Draws a textured quad with specified screen and texture coordinates
- Calls: Begin_Tri_Strip(), Vertex(), End_Tri_Strip()

### TextDrawClass::Get_Width(Font3DInstanceClass*, const char*)
- Purpose: Calculates the width of a string in normalized screen units
- Calls: Font3DInstanceClass::Char_Spacing()

## Globals
- **TextColor (Vector3)**: Default text color (white)
- **DefaultVertexMaterial (VertexMaterialClass)**: Preconfigured vertex material
- **DefaultShader (ShaderClass)**: Preconfigured shader for text rendering
- **TranslateScale/TranslateOffset/PixelSize (Vector2)**: Coordinate transformation parameters

## Dependencies
- textdraw.h, font3d.h, simplevec.h
- DynamicMeshClass, VertexMaterialClass, ShaderClass, Font3DInstanceClass, RectClass, Vector2
- WWMath, WW3D namespaces

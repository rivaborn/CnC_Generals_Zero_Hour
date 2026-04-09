# Generals/Code/Libraries/Source/WWVegas/WW3D2/txt2d.cpp

## Purpose
Handles rendering of 2D text in the game using DirectX 8.

## Responsibilities
- Constructs and renders 2D text objects
- Manages text positioning, centering, and clamping
- Handles texture generation for text rendering
- Calculates screen coordinates and texture coordinates

## Key Types
- Text2DObjClass (Class): Manages 2D text rendering with font, position, and styling
- TextTexture (Not inferable): Static texture used for rendering text

## Key Functions
### Text2DObjClass::Text2DObjClass
- Purpose: Constructor for 2D text objects with variable arguments
- Calls: Set_Text, vsprintf, va_start, va_end

### Text2DObjClass::Set_Text
- Purpose: Sets the text content and rendering parameters for a 2D text object
- Calls: WW3D::Get_Device_Resolution, TextTexture.Build_Texture, TextTexture.Get_Texture, TextTexture.Get_Texture_Size, font.String_Pixel_Width, font.Get_Height, Resize, Set_Texture, Set_Shader, Enable_Sort, Begin_Tri_Strip, Vertex, End_Tri_Strip, WW3D::Get_Pixel_Center, Set_Position, Set_Dirty

## Globals
- Text2DObjClass::_LastWidth (float): Stores the last calculated text width
- Text2DObjClass::_LastHeight (float): Stores the last calculated text height

## Dependencies
- txt2d.h, font.h, assetmgr.h, ww3d.h, pot.h, bsurface.h, texture.h
- <stdio.h>, <stdarg.h>
- WW3D, FontClass, ConvertClass, DynamicScreenMeshClass, ShaderClass, Vector3
- DirectX 8 specific headers (srTextureMap.hpp)

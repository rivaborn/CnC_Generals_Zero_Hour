# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/txt2d.h

## Purpose
Header file declaring the Text2DObjClass for rendering 2D text in the SAGE engine.

## Responsibilities
- Declares the Text2DObjClass for 2D text rendering.
- Defines interface for text positioning, coloring, and alignment.
- Manages text texture generation via DynamicScreenMeshClass.
- Provides static members for tracking last rendered text dimensions.

## Key Types
- Text2DObjClass (Class): 2D text rendering object using DynamicScreenMeshClass.
- FontClass (Class): Reference to font data (forward declared).
- ConvertClass (Class): Reference to text conversion utilities (forward declared).

## Key Functions
### Text2DObjClass constructor
- Purpose: Initializes a 2D text object with font, text, position, colors, and alignment.
- Calls: Not inferable (implementation in .cpp).

### Set_Text
- Purpose: Updates the text content and properties of an existing Text2DObjClass instance.
- Calls: Not inferable (implementation in .cpp).

## Globals
- _LastWidth (float): Tracks width of last rendered text.
- _LastHeight (float): Tracks height of last rendered text.

## Dependencies
- dynamesh.h: For DynamicScreenMeshClass inheritance.
- txt.h: For text-related utilities.
- WW3D_DX8: Conditional compilation for DirectX 8 support.

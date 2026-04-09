# Generals/Code/Libraries/Source/WWVegas/WW3D2/txt2d.h

## Purpose
Header file declaring the Text2DObjClass for rendering 2D text in the SAGE engine.

## Responsibilities
- Declares Text2DObjClass for 2D text rendering
- Defines interface for text positioning, coloring, and formatting
- Manages text texture generation
- Provides class ID for render object identification

## Key Types
- FontClass (Class): Font resource reference
- ConvertClass (Class): Text conversion utility
- Text2DObjClass (Class): 2D text render object (DX8 only)
- TextTextureClass (Class): Internal text texture storage

## Key Functions
### Text2DObjClass constructor
- Purpose: Creates a 2D text object with specified font, text, position, and formatting
- Calls: Not inferable (implementation in .cpp)

### Set_Text
- Purpose: Updates the text content and properties of an existing Text2DObjClass
- Calls: Not inferable (implementation in .cpp)

## Globals
- _LastWidth (float): Stores width of last rendered text
- _LastHeight (float): Stores height of last rendered text

## Dependencies
- dynamesh.h: For DynamicScreenMeshClass inheritance
- txt.h: For text handling utilities
- CLASSID_TEXT2D: Render object class identifier
- WW3D_DX8: Conditional compilation flag

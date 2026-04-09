# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DDebugDisplay.h

## Purpose
Header for the W3DDebugDisplay class, which handles debug text rendering in the W3D (W3D) device context.

## Responsibilities
- Manages debug text display using a GameFont
- Provides font configuration (width/height)
- Implements text rendering via drawText
- Inherits from DebugDisplay base class

## Key Types
- **W3DDebugDisplay (Class)**: Debug text rendering interface for W3D device
- **GameFont (Class)**: Font used for rendering (forward reference)
- **DisplayString (Class)**: Internal display string handler (forward reference)

## Key Functions
### W3DDebugDisplay()
- Purpose: Default constructor
- Calls: None

### ~W3DDebugDisplay()
- Purpose: Destructor
- Calls: None

### init()
- Purpose: Initializes the debug display
- Calls: None

### setFont()
- Purpose: Sets the font for text rendering
- Calls: None

### setFontWidth()
- Purpose: Sets the font width
- Calls: None

### setFontHeight()
- Purpose: Sets the font height
- Calls: None

### drawText()
- Purpose: Renders text at specified coordinates
- Calls: None

## Globals
- None

## Dependencies
- **DebugDisplay.h**: Base class header
- **GameFont**: Forward-declared font class
- **DisplayString**: Forward-declared string class

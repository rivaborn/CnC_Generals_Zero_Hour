# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/MONO.H

## Purpose
Defines a monochrome text display class for console-like output in the game engine.

## Responsibilities
- Manages monochrome text rendering and attributes
- Handles text output, formatting, and display
- Provides windowing and scrolling capabilities
- Controls visibility and attribute settings

## Key Types
- MonoClass (Class): Main monochrome display manager
- MonoAttribute (Enum): Text display attributes (INVISIBLE, UNDERLINE, BLINKING, NORMAL, INVERSE)

## Key Functions
### Enable
- Purpose: Enables monochrome output
- Calls: None

### Disable
- Purpose: Disables monochrome output
- Calls: None

### Is_Enabled
- Purpose: Checks if monochrome output is enabled
- Calls: None

### Sub_Window
- Purpose: Creates a sub-window for text display
- Calls: None

### Fill_Attrib
- Purpose: Fills a rectangular area with a specific attribute
- Calls: None

### Print
- Purpose: Outputs text to the monochrome display
- Calls: None

### Printf
- Purpose: Formatted text output to the monochrome display
- Calls: None

### Text_Print
- Purpose: Prints text at specific coordinates with attributes
- Calls: None

### View
- Purpose: Refreshes the display
- Calls: None

### Scroll
- Purpose: Scrolls the display vertically
- Calls: None

### Pan
- Purpose: Scrolls the display horizontally
- Calls: None

### Set_Default_Attribute
- Purpose: Sets the default text attribute
- Calls: None

## Globals
- Current (MonoClass*): Pointer to

# Generals/Code/Libraries/Source/WWVegas/WWLib/MONO.H

## Purpose
Defines a monochrome text display class for console-like output in the game engine.

## Responsibilities
- Manages monochrome text rendering and attributes
- Handles console-style operations (scrolling, panning, cursor positioning)
- Provides formatted text output with attributes (color, underline, etc.)
- Controls visibility of monochrome output via enable/disable

## Key Types
- MonoClass (Class): Main class for monochrome text display management
- MonoAttribute (Enum): Text display attributes (INVISIBLE, UNDERLINE, BLINKING, NORMAL, INVERSE)

## Key Functions
### Enable
- Purpose: Enables monochrome output globally
- Calls: None

### Disable
- Purpose: Disables monochrome output globally
- Calls: None

### Is_Enabled
- Purpose: Checks if monochrome output is enabled
- Calls: None

### Sub_Window
- Purpose: Creates a sub-window within the monochrome display
- Calls: None

### Fill_Attrib
- Purpose: Fills a rectangular area with a specific attribute
- Calls: None

### Print/Printf
- Purpose: Outputs text with optional formatting
- Calls: None

### Text_Print
- Purpose: Renders text at specific coordinates with attributes
- Calls: None

### View
- Purpose: Updates the display to show current content
- Calls: None

### Scroll/Pan
- Purpose: Moves the display content vertically/horizontally
- Calls: None

## Globals
- Current (MonoClass*): Pointer to the current active monochrome display instance
- Enabled (bool): Static flag indicating if monochrome output is enabled

## Dependencies

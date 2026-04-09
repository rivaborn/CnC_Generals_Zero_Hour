# Generals/Code/Tools/GUIEdit/Source/GUIEditDisplay.cpp

## Purpose
Implements the GUIEditDisplay class, providing drawing operations for the GUI editor tool.

## Responsibilities
- Delegates drawing operations to TheEditWindow
- Provides methods for drawing lines, rectangles, and images
- Manages clipping regions for 2D drawing

## Key Types
- GUIEditDisplay (Class): wrapper for GUI editor display operations

## Key Functions
### GUIEditDisplay::drawLine
- Purpose: Draws a line on the display with specified color and width
- Calls: TheEditWindow->drawLine

### GUIEditDisplay::drawOpenRect
- Purpose: Draws a rectangular border with specified color and line width
- Calls: TheEditWindow->drawOpenRect

### GUIEditDisplay::drawFillRect
- Purpose: Draws a filled rectangle with specified color
- Calls: TheEditWindow->drawFillRect

### GUIEditDisplay::drawImage
- Purpose: Draws an image within specified screen coordinates
- Calls: TheEditWindow->drawImage

### GUIEditDisplay::setClipRegion
- Purpose: Sets the clipping region for 2D drawing operations
- Calls: TheEditWindow->setClipRegion

### GUIEditDisplay::isClippingEnabled
- Purpose: Returns whether clipping is currently enabled
- Calls: TheEditWindow->isClippingEnabled

### GUIEditDisplay::enableClipping
- Purpose: Enables or disables clipping for 2D drawing
- Calls: TheEditWindow->enableClipping

## Globals
- TheEditWindow (EditWindow*): global reference to the editor window

## Dependencies
- "GUIEditDisplay.h"
- "EditWindow.h"
- Image, IRegion2D, Color, DrawImageMode (external types)

# Generals/Code/Tools/WorldBuilder/include/brushoptions.h

## Purpose
Defines the BrushOptions dialog class for configuring brush width, feather, and height in WorldBuilder.

## Responsibilities
- Manages brush tool parameters via a modeless dialog
- Handles UI updates for brush width, feather, and height sliders
- Provides static methods to update brush settings externally
- Implements PopupSliderOwner interface for slider behavior

## Key Types
- BrushOptions (Class): Modeless dialog for brush tool settings
- (anonymous enum): Constants for brush size/feather ranges and slider ticks
- WBPopupSliderButton (Type): UI slider button for brush parameters

## Key Functions
### BrushOptions::setWidth
- Purpose: Updates the current brush width and UI
- Calls: Not inferable

### BrushOptions::setFeather
- Purpose: Updates the current feather width and UI
- Calls: Not inferable

### BrushOptions::setHeight
- Purpose: Updates the current brush height and UI
- Calls: Not inferable

### BrushOptions::GetPopSliderInfo
- Purpose: Provides slider configuration for brush parameters
- Calls: Not inferable

### BrushOptions::PopSliderChanged
- Purpose: Handles real-time slider value changes
- Calls: Not inferable

### BrushOptions::PopSliderFinished
- Purpose: Processes finalized slider values
- Calls: Not inferable

## Globals
- m_staticThis (BrushOptions*): Singleton reference to the dialog
- m_currentWidth (Int): Current brush width value
- m_currentFeather (Int): Current feather width value
- m_currentHeight (Int): Current brush height value

## Dependencies
- WBPopupSlider.h: Popup slider UI components
- OptionsPanel.h: Base class for options panels
- MFC classes (CWnd, COptionsPanel, etc.)

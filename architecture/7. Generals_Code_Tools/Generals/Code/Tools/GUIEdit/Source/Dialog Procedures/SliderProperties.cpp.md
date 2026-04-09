# Generals/Code/Tools/GUIEdit/Source/Dialog Procedures/SliderProperties.cpp

## Purpose
Handles the slider properties dialog in the GUI editor, allowing users to configure slider appearance and behavior.

## Responsibilities
- Manages slider properties dialog creation and interaction
- Handles image/color assignments for slider states
- Validates and saves slider min/max values
- Coordinates with common dialog message handlers

## Key Types
- **ImageAndColorInfo (struct)**: Stores image, color, and border color data for slider states
- **SliderData (struct)**: Contains slider min/max values (Not inferable)
- **GameWindow (class)**: Represents a window/gadget in the GUI system

## Key Functions
### sliderPropertiesCallback
- Purpose: Processes dialog messages for slider properties
- Calls: HandleCommonDialogMessages, StoreColor, GetStateInfo, SaveCommonDialogProperties, GadgetSliderSet* functions, GetDlgItemInt, MessageBox, DestroyWindow, SwitchToState

### InitSliderPropertiesDialog
- Purpose: Initializes and displays the slider properties dialog
- Calls: CreateDialog, CommonDialogInitialize, GadgetSliderGet* functions, StoreImageAndColor, SetDlgItemInt, SwitchToState

## Globals
- None

## Dependencies
- GUIEdit.h, Properties.h, Resource.h
- GameClient/GadgetSlider.h, GameClient/Gadget.h
- External symbols: TheEditor, HandleCommonDialogMessages, SaveCommonDialogProperties, StoreColor, GetStateInfo, StoreImageAndColor, SwitchToState, GadgetSlider* functions

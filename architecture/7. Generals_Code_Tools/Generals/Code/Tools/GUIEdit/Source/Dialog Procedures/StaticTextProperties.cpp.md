# Generals/Code/Tools/GUIEdit/Source/Dialog Procedures/StaticTextProperties.cpp

## Purpose
Handles the properties dialog for static text gadgets in the GUI editor.

## Responsibilities
- Manages the static text properties dialog callback
- Saves/loads static text properties (images, colors, centering)
- Initializes dialog with current gadget properties

## Key Types
- **None**

## Key Functions
### staticTextPropertiesCallback
- Purpose: Handles dialog messages for static text properties
- Calls: `HandleCommonDialogMessages`, `SaveCommonDialogProperties`, `GadgetStaticTextSetEnabledImage`, `GadgetStaticTextSetEnabledColor`, `GadgetStaticTextSetEnabledBorderColor`, `GadgetStaticTextSetDisabledImage`, `GadgetStaticTextSetDisabledColor`, `GadgetStaticTextSetDisabledBorderColor`, `GadgetStaticTextSetHiliteImage`, `GadgetStaticTextSetHiliteColor`, `GadgetStaticTextSetHiliteBorderColor`, `GetStateInfo`, `StoreImageAndColor`, `SwitchToState`

### InitStaticTextPropertiesDialog
- Purpose: Creates and initializes the static text properties dialog
- Calls: `CreateDialog`, `CommonDialogInitialize`, `GadgetStaticTextGetEnabledImage`, `GadgetStaticTextGetEnabledColor`, `GadgetStaticTextGetEnabledBorderColor`, `GadgetStaticTextGetDisabledImage`, `GadgetStaticTextGetDisabledColor`, `GadgetStaticTextGetDisabledBorderColor`, `GadgetStaticTextGetHiliteImage`, `GadgetStaticTextGetHiliteColor`, `GadgetStaticTextGetHiliteBorderColor`, `StoreImageAndColor`, `SwitchToState`

## Globals
- **currCentered (Bool)**: Tracks the centered state of static text

## Dependencies
- `GUIEdit.h`, `Properties.h`, `Resource.h`, `GameClient/GadgetStaticText.h`, `GameClient/Gadget.h`
- `HandleCommonDialogMessages`, `SaveCommonDialogProperties`, `GetStateInfo`, `StoreImageAndColor`, `SwitchToState`

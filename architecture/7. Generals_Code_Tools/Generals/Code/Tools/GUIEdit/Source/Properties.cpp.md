# Generals/Code/Tools/GUIEdit/Source/Properties.cpp

## Purpose
Manages property dialogs for GUI elements in the GUIEdit tool, handling initialization, state management, and color/image properties.

## Responsibilities
- Initialize and populate property dialogs for various UI controls
- Manage state transitions and property storage for UI elements
- Handle color and image selection for UI states
- Validate and adjust gadget drawing methods
- Process common dialog messages for all property dialogs

## Key Types
- `TextDrawData` (struct): Stores text drawing properties (color, border color, etc.)
- `ColorControl` (struct): Maps control IDs to color values
- `ImageAndColorInfo` (struct): Associates UI states with images and colors
- `StateIdentifier` (enum): Identifies different UI states (enabled, disabled, hilite, etc.)

## Key Functions
### `InitPropertiesDialog`
- Purpose: Initializes the appropriate property dialog for a given window
- Calls: `CommonDialogInitialize`, `LoadFontCombo`, `LoadTextStateCombo`, etc.

### `CommonDialogInitialize`
- Purpose: Sets up common dialog elements and loads initial properties
- Calls: `LoadImageListComboBox`, `LoadHeaderTemplateListComboBox`, `LoadStateCombo`

### `HandleCommonDialogMessages`
- Purpose: Processes common messages for all property dialogs
- Calls: `GetCurrentStateInfo`, `SwitchToState`, `ComboBoxSelectionToImage`, `SelectColor`

### `SwitchToState`
- Purpose: Updates the dialog to reflect the selected UI state
- Calls: `GetStateInfo`, `StoreImageAndColor`

### `StoreImageAndColor`
- Purpose: Stores image and color data for a specific UI state
- Calls: None

## Globals
- `textDrawData` (TextDrawData[3]): Stores text drawing properties for enabled/disabled/hilite states
- `currTextIndex` (Int): Tracks current text state selection
- `enabledTextIndex`, `disabledTextIndex`, `hiliteTextIndex` (Int): Indices for text states
- `colorControlTable` (ColorControl[]): Maps control IDs to default colors
- `imageAndColorTable` (ImageAndColorInfo[]): Maps UI states to images and colors

## Dependencies
- Key includes: `Common/Debug.h`, `GameClient/Gadget.h`, `GUIEdit.h`, `Properties.h`
- External symbols: `GameWindow`, `Image`, `StateIdentifier`, `GameMakeColor`, `SelectColor`

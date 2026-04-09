# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/OptionsMenu.cpp

## Purpose
Handles the options menu UI in Command & Conquer Generals Zero Hour, managing game settings and preferences.

## Responsibilities
- Manages game options UI (video, audio, controls, network settings)
- Handles preference loading/saving
- Controls advanced display options
- Manages resolution changes and confirmation dialogs
- Handles keyboard/mouse input for the options menu

## Key Types
- **Detail (Enum)**: Graphics detail levels (High/Medium/Low/Custom)
- **OptionPreferences (Class)**: Manages game preferences and settings

## Key Functions
### OptionsMenuInit
- Purpose: Initializes the options menu UI and loads current settings
- Calls: GadgetCheckBoxSetChecked, GadgetSliderSetPosition, TheWindowManager->winSetModal

### saveOptions
- Purpose: Saves user-selected options to preferences
- Calls: pref->write(), TheWritableGlobalData modifications, various Gadget functions

### OptionsMenuSystem
- Purpose: Handles system messages for the options menu
- Calls: TheShell->push/pop, GameSpyCloseOverlay, DestroyOptionsLayout, DoResolutionDialog

### setDefaults
- Purpose: Resets options to default values
- Calls: Various preference setting functions

### showAdvancedOptions/acceptAdvancedOptions/cancelAdvancedOptions
- Purpose: Manages advanced display options submenu
- Calls: WindowLayout functions, preference updates

## Globals
- **pref (OptionPreferences*)**: Current preferences object
- **OptionsLayout (WindowLayout*)**: Main options menu layout
- **dispChanged (Bool)**: Tracks if display settings changed
- **oldDispSettings/newDispSettings (DisplaySettings)**: Stores display settings before/after changes
- **timer (Int)**: Timer for resolution change dialog

## Dependencies
- GameClient headers (WindowLayout, Gadget*, Shell, etc.)
- Common headers (UserPreferences, AudioSettings, etc.)
- GameNetwork headers (FirewallHelper, IPEnumeration)
- GameLogic headers (GameLogic, ScriptEngine)

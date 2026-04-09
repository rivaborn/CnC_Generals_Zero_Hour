# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/OptionsMenu.cpp

## Purpose
Handles the options menu UI in Command & Conquer Generals, managing game settings and preferences.

## Responsibilities
- Manages game options UI (video, audio, controls, network settings)
- Handles preference loading/saving
- Controls advanced graphics options
- Manages resolution changes and firewall settings
- Handles keyboard/mouse input for the options menu

## Key Types
- **Detail (Enum)**: Graphics detail levels (HIGHDETAIL, MEDIUMDETAIL, LOWDETAIL, CUSTOMDETAIL)
- **OptionPreferences (Class)**: Manages game preferences and settings

## Key Functions
### setDefaults
- Purpose: Resets all options to default values
- Calls: Various preference setting functions

### saveOptions
- Purpose: Saves current options to preferences file
- Calls: pref->write(), various preference setting functions

### OptionsMenuInit
- Purpose: Initializes the options menu UI
- Calls: Gadget*Set* functions, preference loading functions

### OptionsMenuSystem
- Purpose: Handles system messages for the options menu
- Calls: saveOptions(), setDefaults(), showAdvancedOptions(), etc.

## Globals
- **pref (OptionPreferences*)**: Current preferences object
- **OptionsLayout (WindowLayout*)**: The options menu layout
- **comboBox* (GameWindow*)**: Various UI control pointers
- **check* (GameWindow*)**: Checkbox control pointers
- **slider* (GameWindow*)**: Slider control pointers
- **oldDispSettings/newDispSettings (DisplaySettings)**: For resolution change tracking

## Dependencies
- GameClient headers (WindowLayout, Gadget*, Shell)
- Common headers (UserPreferences, AudioSettings)
- GameNetwork headers (FirewallHelper, IPEnumeration)
- GameLogic headers (GameLogic, ScriptEngine)

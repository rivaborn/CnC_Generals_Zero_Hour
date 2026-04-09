# GeneralsMD/Code/GameEngine/Source/Common/INI/INICommandButton.cpp

## Purpose
Parses command button definitions from INI files for the game's control bar UI.

## Responsibilities
- Parses command button definitions from INI files
- Manages creation and override of command buttons
- Validates special power template consistency with button options

## Key Types
- `CommandButton` (Class): Represents a button in the control bar UI
- `SpecialPowerTemplate` (Class): Template for special power associated with a button

## Key Functions
### `INI::parseCommandButtonDefinition`
- Purpose: Entry point for parsing command button definitions
- Calls: `ControlBar::parseCommandButtonDefinition`

### `ControlBar::parseCommandButtonDefinition`
- Purpose: Parses command button definition from INI and creates/updates button
- Calls: `TheControlBar->findNonConstCommandButton`, `TheControlBar->newCommandButton`, `TheControlBar->newCommandButtonOverride`, `ini->initFromINI`, `button->getFieldParse`, `button->getSpecialPowerTemplate`, `BitTest`

## Globals
- `TheControlBar` (ControlBar*): Global control bar instance

## Dependencies
- `PreRTS.h`, `Common/INI.h`, `Common/SpecialPower.h`, `GameClient/ControlBar.h`
- `AsciiString`, `Bool`, `DEBUG_CRASH` macros

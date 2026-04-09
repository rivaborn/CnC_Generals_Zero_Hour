# GeneralsMD/Code/GameEngine/Include/GameClient/GUICommandTranslator.h

## Purpose
Header for a class that translates GUI-initiated game commands requiring world interaction (e.g., targeting).

## Responsibilities
- Translates GUI commands into game messages
- Handles special unit actions needing additional world clicks
- Manages command flow between UI and game logic

## Key Types
- GUICommandTranslator (Class): Translates GUI commands into game messages for world interaction.

## Key Functions
### GUICommandTranslator()
- Purpose: Constructor for GUICommandTranslator.
- Calls: None.

### ~GUICommandTranslator()
- Purpose: Destructor for GUICommandTranslator.
- Calls: None.

### translateGameMessage()
- Purpose: Translates a game message into an appropriate action.
- Calls: None (implementation not shown).

## Globals
- None.

## Dependencies
- `GameClient/InGameUI.h` (for `GameMessageTranslator` base class)
- `GameMessage` (external type)
- `GameMessageDisposition` (external type)

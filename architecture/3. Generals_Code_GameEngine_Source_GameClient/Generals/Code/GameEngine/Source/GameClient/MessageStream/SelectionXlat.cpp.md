# Generals/Code/GameEngine/Source/GameClient/MessageStream/SelectionXlat.cpp

## Purpose
Handles unit selection logic, including click/drag selection, group management, and input translation for the game client.

## Responsibilities
- Processes mouse/keyboard input for selection
- Manages selection state and feedback
- Handles group selection/hotkeys
- Validates selectable objects
- Translates game messages into selection actions

## Key Types
- **SelectionTranslator (Class)**: Main selection handler
- **SFWRec (Struct)**: Wrapper data for selection callbacks
- **GameMessageDisposition (Enum)**: Message processing result

## Key Functions
### `CanSelectDrawable`
- Purpose: Determines if a drawable can be selected
- Calls: `isEffectivelyDead`, `isKindOf`, `isDrawableEffectivelyHidden`, `isLocallyControlled`, `isSelectable`

### `translateGameMessage`
- Purpose: Processes game messages for selection actions
- Calls: `deselectAll`, `TheMessageStream->appendMessage`, `TheInGameUI->selectDrawable`

### `selectFriends`
- Purpose: Selects friendly units
- Calls: `CanSelectDrawable`, `TheInGameUI->selectDrawable`

### `killThemKillThemAll`
- Purpose: Handles "kill all" selection mode
- Calls: None directly (uses message stream)

## Globals
- **TheSelectionTranslator (SelectionTranslator*)**: Singleton instance
- **TheHurtSelectionMode (Bool)**: Debug selection flag
- **TheHandOfGodSelectionMode (Bool)**: Debug selection flag
- **TheDebugSelectionMode (Bool)**: Debug selection flag

## Dependencies
- GameClient headers: `ControlBar.h`, `Display.h`, `Drawable.h`, `GameClient.h`
- GameLogic headers: `Damage.h`, `GameLogic.h`, `Object.h`
- Common headers: `ActionManager.h`, `GameAudio.h`, `MessageStream.h`
- Internal: `PreRTS.h`, `GameText.h`, `Keyboard.h`, `SelectionInfo.h`

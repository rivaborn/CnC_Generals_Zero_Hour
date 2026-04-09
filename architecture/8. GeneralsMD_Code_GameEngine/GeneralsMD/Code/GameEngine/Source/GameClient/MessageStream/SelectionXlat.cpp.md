# GeneralsMD/Code/GameEngine/Source/GameClient/MessageStream/SelectionXlat.cpp

## Purpose
Handles unit selection logic and message translation for the game client.

## Responsibilities
- Manages selection/deselection of game objects
- Processes mouse input for selection operations
- Handles team/group selection commands
- Implements drag selection behavior
- Manages selection feedback and constraints

## Key Types
- **SelectionTranslator (Class)**: Main selection handler class
- **SFWRec (Struct)**: Helper struct for selection callbacks
- **TheSelectionTranslator (Global)**: Singleton instance of SelectionTranslator

## Key Functions
### `CanSelectDrawable`
- Purpose: Determines if a drawable can be selected under current rules
- Calls: `isEffectivelyDead`, `isKindOf`, `isDrawableEffectivelyHidden`, `isLocallyControlled`, `isSelectable`

### `selectFriends`
- Purpose: Selects friendly drawables and adds them to a team message
- Calls: `CanSelectDrawable`, `selectDrawable`, `appendObjectIDArgument`

### `translateGameMessage`
- Purpose: Processes game messages related to selection
- Calls: `deselectAll`, `selectDrawable`, `appendMessage`, `getHotkeySquad`, `lookAt`

### `deselectAll`
- Purpose: Deselects all drawables and emits a team destroy message
- Calls: `deselectAllDrawables`, `appendMessage`

## Globals
- **TheSelectionTranslator (SelectionTranslator*)**: Global instance of the selection translator

## Dependencies
- Common: ActionManager, GameAudio, MessageStream, Player, PlayerList, ThingTemplate
- GameLogic: Damage, GameLogic, Object, Squad, BodyModule, ContainModule, UpdateModule
- GameClient: ControlBar, Display, Drawable, GameClient, GameText, GameWindowManager, Keyboard, SelectionInfo, TerrainVisual

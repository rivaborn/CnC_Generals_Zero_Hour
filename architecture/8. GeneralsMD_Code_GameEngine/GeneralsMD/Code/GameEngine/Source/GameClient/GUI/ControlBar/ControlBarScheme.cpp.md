# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarScheme.cpp

## Purpose
Manages the visual scheme and animations for the game's control bar (HUD).

## Responsibilities
- Parses control bar scheme definitions from INI files
- Manages control bar animations (e.g., sliding effects)
- Handles resolution scaling for different screen sizes
- Preloads control bar assets
- Provides scheme selection based on player side/template

## Key Types
- ControlBarScheme (Class): Contains all visual elements and animations for a control bar scheme
- ControlBarSchemeImage (Class): Represents a single image in the control bar
- ControlBarSchemeAnimation (Class): Handles animated elements in the control bar
- ControlBarSchemeManager (Class): Manages multiple control bar schemes and current selection

## Key Functions
### parseImagePart
- Purpose: Parses static image definitions from INI
- Calls: INI::parseICoord2D, INI::parseMappedImage, INI::parseInt

### parseAnimatingPart
- Purpose: Parses animated element definitions from INI
- Calls: parseAnimatingPartImage, INI::parseLookupList, INI::parseDurationUnsignedInt

### animSlideRight
- Purpose: Updates slide-right animation frame
- Calls: None (directly manipulates animation state)

### setControlBarSchemeByPlayer
- Purpose: Selects appropriate control bar scheme based on player side
- Calls: findControlBarScheme, TheDisplay->getWidth/Height

## Globals
- AnimTypeNames (LookupListRec[]): Maps animation type names to enum values
- ControlBarSchemeManager::m_controlBarSchemeFieldParseTable (FieldParse[]): INI parsing rules for control bar schemes

## Dependencies
- Common/Player.h, Common/PlayerTemplate.h, GameClient/ControlBar.h
- GameClient/Image.h, GameClient/GameWindowManager.h
- INI parsing utilities (INI::parse* functions)
- Display and WindowManager singletons (TheDisplay, TheWindowManager)

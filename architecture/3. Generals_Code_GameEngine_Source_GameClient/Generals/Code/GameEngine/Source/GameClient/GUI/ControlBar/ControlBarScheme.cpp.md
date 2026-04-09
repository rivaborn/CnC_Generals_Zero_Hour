# Generals/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarScheme.cpp

## Purpose
Manages the visual scheme and animations for the in-game control bar (command bar) UI element.

## Responsibilities
- Parses control bar scheme definitions from INI files
- Manages control bar animations (e.g., sliding effects)
- Handles resolution scaling for different screen sizes
- Provides methods to find and set active control bar schemes
- Preloads texture assets for control bar elements

## Key Types
- ControlBarScheme (Class): Contains all visual elements and animations for a control bar scheme
- ControlBarSchemeImage (Class): Represents a single image element in the control bar
- ControlBarSchemeAnimation (Class): Handles animated elements in the control bar
- (anonymous enum): Contains animation type constants
- COMMAND_BAR_SIZE_OFFSET (Enum): Size offset constant

## Key Functions
### parseImagePart
- Purpose: Parses image part definitions from INI files
- Calls: INI::parseICoord2D, INI::parseMappedImage, INI::parseInt

### parseAnimatingPart
- Purpose: Parses animated part definitions from INI files
- Calls: parseAnimatingPartImage, INI::parseAsciiString, INI::parseLookupList, INI::parseDurationUnsignedInt, INI::parseICoord2D

### animSlideRight
- Purpose: Handles the slide-right animation logic for control bar elements
- Calls: None (direct calls)

### setControlBarSchemeByPlayer
- Purpose: Sets the appropriate control bar scheme based on player side
- Calls: findControlBarScheme, TheWindowManager->winGetWindowFromId, TheControlBar->setControlCommand, TheControlBar->findCommandButton

## Globals
- AnimTypeNames (LookupListRec[]): Maps animation type names to constants
- m_controlBarSchemeFieldParseTable (FieldParse[]): Field parsing table for control bar schemes

## Dependencies
- PreRTS.h, Common/Player.h, Common/PlayerTemplate.h, Common/Recorder.h
- GameClient/ControlBarScheme.h, GameClient/Display.h, GameClient/ControlBar.h
- GameClient/Image.h, GameClient/GameWindowManager.h, GameClient/GadgetPushButton.h
- INI class, TheDisplay, TheMappedImageCollection, TheWindowManager, TheControlBar, TheRecorder

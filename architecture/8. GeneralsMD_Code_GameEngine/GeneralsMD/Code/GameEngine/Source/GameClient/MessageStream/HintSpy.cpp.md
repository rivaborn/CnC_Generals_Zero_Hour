# GeneralsMD/Code/GameEngine/Source/GameClient/MessageStream/HintSpy.cpp

## Purpose
Handles game messages to generate visual UI hints (e.g., drag selection rectangles, command previews).

## Responsibilities
- Intercepts specific game messages
- Delegates hint creation to the in-game UI system
- Manages message disposal (destroy/keep) based on hint requirements

## Key Types
- **HintSpyTranslator (Class)**: Message translator for generating UI hints
- **GameMessageDisposition (Enum)**: Message handling disposition (KEEP_MESSAGE/DESTROY_MESSAGE)

## Key Functions
### translateGameMessage
- Purpose: Processes game messages to generate appropriate UI hints
- Calls: TheInGameUI->createMouseoverHint, TheInGameUI->createCommandHint, TheInGameUI->beginAreaSelectHint, TheInGameUI->endAreaSelectHint, TheInGameUI->createMoveHint, TheInGameUI->createAttackHint, TheInGameUI->createForceAttackHint, TheInGameUI->createGarrisonHint

## Globals
- **TheInGameUI (GameWindowManager)**: Global UI manager instance

## Dependencies
- Common/MessageStream.h
- GameClient/HintSpy.h
- GameClient/GameWindowManager.h
- GameClient/GameWindow.h
- GameClient/GameClient.h
- GameClient/Drawable.h

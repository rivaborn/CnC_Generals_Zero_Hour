# Generals/Code/GameEngine/Source/GameClient/MessageStream/HintSpy.cpp

## Purpose
Handles game messages to generate visual UI hints (e.g., drag selection rectangles, command indicators).

## Responsibilities
- Intercepts specific game messages
- Delegates hint creation to UI system
- Manages message disposal (destroy/keep)

## Key Types
- **HintSpyTranslator (Class)**: Message translator for UI hints

## Key Functions
### `translateGameMessage`
- Purpose: Processes game messages to generate appropriate UI hints
- Calls: `TheInGameUI->createMouseoverHint`, `TheInGameUI->createCommandHint`, `TheInGameUI->beginAreaSelectHint`, `TheInGameUI->endAreaSelectHint`, `TheInGameUI->createMoveHint`, `TheInGameUI->createAttackHint`, `TheInGameUI->createForceAttackHint`, `TheInGameUI->createGarrisonHint`

## Globals
- **TheInGameUI (GameWindowManager)**: Global UI manager instance

## Dependencies
- `MessageStream.h`, `HintSpy.h`, `GameWindowManager.h`, `GameWindow.h`, `GameClient.h`, `Drawable.h`
- `GameMessage` class (message types)

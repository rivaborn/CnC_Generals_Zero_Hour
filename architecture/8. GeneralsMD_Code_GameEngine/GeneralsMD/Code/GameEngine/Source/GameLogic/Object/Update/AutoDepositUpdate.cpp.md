# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/AutoDepositUpdate.cpp

## Purpose
Handles automatic money deposits for game objects (e.g., resource generators) and upgrade-based supply boosts.

## Responsibilities
- Manages periodic money deposits for objects
- Applies upgrade-based supply boosts
- Displays floating money text for visual feedback
- Handles initial capture bonuses
- Serializes/deserializes module state

## Key Types
- `AutoDepositUpdate` (Class): Manages auto-deposit logic for game objects
- `upgradePair` (Struct): Stores upgrade type and associated supply boost amount

## Key Functions
### `parseUpgradePair`
- Purpose: Parses upgrade pair data from INI files
- Calls: `INI::scanInt`, `ini->getNextToken`, `ini->getSepsColon`

### `awardInitialCaptureBonus`
- Purpose: Awards initial capture bonus to player
- Calls: `Player::getMoney()->deposit`, `Player::getScoreKeeper()->addMoneyEarned`, `TheInGameUI->addFloatingText`

### `update`
- Purpose: Handles periodic money deposits and visual feedback
- Calls: `TheGameLogic->getFrame`, `getObject()->getControllingPlayer()`, `TheInGameUI->addFloatingText`, `getUpgradedSupplyBoost`

### `getUpgradedSupplyBoost`
- Purpose: Calculates supply boost from player upgrades
- Calls: `TheUpgradeCenter->findUpgrade`, `Player::hasUpgradeComplete`

### `xfer`
- Purpose: Serializes/deserializes module state
- Calls: `UpdateModule::xfer`, `xfer->xferVersion`, `xfer->xferUnsignedInt`, `xfer->xferBool`

## Globals
- `TheGameLogic` (GameLogic*): Access to game logic system
- `TheUpgradeCenter` (UpgradeCenter*): Access to upgrade system
- `TheInGameUI` (InGameUI*): Access to in-game UI for floating text
- `TheGameText` (GameText*): Access to game text resources

## Dependencies
- Common headers: `BuildAssistant.h`, `Thing.h`, `ThingTemplate.h`, `INI.h`, `RandomValue.h`, `Player.h`, `Xfer.h`
- GameLogic headers: `GameLogic.h`, `Module/AutoDepositUpdate.h`, `Module/AIUpdate.h`, `Object.h`
- GameClient headers: `InGameUI.h`, `Color.h`, `GameText.h`

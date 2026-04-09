# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/SpecialPower/CashHackSpecialPower.cpp - Enhanced Analysis

## Architectural Role
This file implements the Cash Hack special power, a game mechanic that allows players to steal money from enemies. It extends the `SpecialPowerModule` base class, integrating with the player economy system and UI feedback mechanisms.

## Cross-References
### Incoming
- **GameLogic/Object/SpecialPower/SpecialPowerModule.cpp**: Calls `SpecialPowerModule::doSpecialPowerAtObject` as part of the base class extension.
- **GameClient/InGameUI.cpp**: Uses `TheInGameUI->addFloatingText` for visual feedback.
- **Common/Player.cpp**: Interacts with `Player::getMoney()` and `Player::getScoreKeeper()` for money transfer and scoring.

### Outgoing
- **GameLogic/Module/CashHackSpecialPower.h**: Defines the module data structure and upgrade parsing.
- **Common/Xfer.h**: Handles serialization via `Xfer` for network sync.
- **GameClient/GameText.h**: Retrieves localized strings for floating text.

## Design Patterns
- **Template Method**: Extends `SpecialPowerModule` with `doSpecialPowerAtObject`, adhering to the base class contract.
- **Strategy**: Encapsulates money theft logic as a modular special power, allowing for easy swapping with other abilities.
- **Observer**: Indirectly notifies UI via `TheInGameUI` for visual feedback (floating text).

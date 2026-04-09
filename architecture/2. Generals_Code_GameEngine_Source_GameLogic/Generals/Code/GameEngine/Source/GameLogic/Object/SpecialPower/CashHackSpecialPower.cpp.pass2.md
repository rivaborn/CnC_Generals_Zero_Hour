# Generals/Code/GameEngine/Source/GameLogic/Object/SpecialPower/CashHackSpecialPower.cpp - Enhanced Analysis

## Architectural Role
This file is integral to the game logic, specifically handling a special power called "Cash Hack." It manages the configuration parsing, execution, and UI feedback for this power, interacting with various subsystems like player management, money handling, and user interface updates.

## Cross-References
### Incoming
- Not inferable.

### Outgoing
- `Common/Player.h`
- `Common/Xfer.h`
- `GameClient/GameText.h`
- `GameLogic/Object.h`
- `GameLogic/Module/CashHackSpecialPower.h`
- `GameClient/InGameUI.h`

## Design Patterns
- **Builder Pattern**: Used in `buildFieldParse` to construct field parsing for Cash Hack module data, extending the functionality of a base class.
- **Strategy Pattern**: The `findAmountToSteal` method uses different strategies based on player science upgrades to determine the amount of money to steal.
- **Observer Pattern**: The UI updates (`addFloatingText`) act as observers to notify players about money transactions.

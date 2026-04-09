# GeneralsMD/Code/GameEngine/Source/Common/RTS/Money.cpp

## Purpose
Handles money management for players in the game, including deposits, withdrawals, and serialization.

## Responsibilities
- Manages player money balance
- Handles money deposit/withdrawal with optional sound effects
- Serializes money data for save/load
- Parses money values from configuration files

## Key Types
- **Money (Class)**: Manages player money balance and operations

## Key Functions
### `withdraw`
- Purpose: Deducts money from player balance with optional sound
- Calls: `TheAudio->getMiscAudio()`, `TheAudio->addAudioEvent()`

### `deposit`
- Purpose: Adds money to player balance with optional sound and stats tracking
- Calls: `TheAudio->getMiscAudio()`, `TheAudio->addAudioEvent()`, `ThePlayerList->getNthPlayer()`, `player->getAcademyStats()->recordIncome()`

### `xfer`
- Purpose: Serializes money data for save/load operations
- Calls: `xfer->xferVersion()`, `xfer->xferUnsignedInt()`

### `parseMoneyAmount`
- Purpose: Parses money values from configuration files
- Calls: `INI::parseUnsignedInt()`

## Globals
- None

## Dependencies
- `Common/Money.h`
- `Common/GameAudio.h`
- `Common/MiscAudio.h`
- `Common/Player.h`
- `Common/PlayerList.h`
- `Common/Xfer.h`
- `PreRTS.h`

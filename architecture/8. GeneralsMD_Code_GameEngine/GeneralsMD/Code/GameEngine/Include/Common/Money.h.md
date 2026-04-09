# GeneralsMD/Code/GameEngine/Include/Common/Money.h

## Purpose
Encapsulates player resource (money) management with basic operations like deposit/withdraw.

## Responsibilities
- Tracks player resource amount
- Handles deposits/withdrawals with sound feedback
- Supports serialization via Snapshot interface
- Provides comparison and parsing utilities

## Key Types
- **Money (Class)**: Manages player resource amount and player index.

## Key Functions
### Money::withdraw
- Purpose: Deducts specified amount from money, returns actual amount withdrawn.
- Calls: Not inferable.

### Money::deposit
- Purpose: Adds specified amount to money.
- Calls: Not inferable.

### Money::parseMoneyAmount
- Purpose: Parses money amount from INI file.
- Calls: Not inferable.

### Money::crc
- Purpose: Generates CRC for snapshot serialization.
- Calls: Not inferable.

### Money::xfer
- Purpose: Serializes/deserializes money data.
- Calls: Not inferable.

### Money::loadPostProcess
- Purpose: Post-processing after loading.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- `Lib/BaseType.h` (UnsignedInt, Int, Bool)
- `Common/Debug.h`
- `Common/Snapshot.h` (Snapshot, Xfer)
- `INI` class (external)

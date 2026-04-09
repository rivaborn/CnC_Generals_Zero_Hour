# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Body/HighlanderBody.cpp

## Purpose
Implements a body type that resists damage, preventing death unless hit by unresistable damage.

## Responsibilities
- Overrides damage logic to cap damage at current health - 1
- Handles serialization (Xfer) and CRC for network sync
- Extends ActiveBody functionality

## Key Types
- HighlanderBody (Class): damage-resistant body that can't die from normal damage

## Key Functions
### HighlanderBody::HighlanderBody
- Purpose: Constructor that initializes base ActiveBody
- Calls: ActiveBody constructor

### HighlanderBody::~HighlanderBody
- Purpose: Destructor (empty implementation)
- Calls: None

### HighlanderBody::attemptDamage
- Purpose: Modifies damage to prevent death unless damage is unresistable
- Calls: ActiveBody::attemptDamage

### HighlanderBody::crc
- Purpose: Serialization CRC calculation
- Calls: ActiveBody::crc

### HighlanderBody::xfer
- Purpose: Serialization/deserialization handler
- Calls: ActiveBody::xfer, Xfer::xferVersion

### HighlanderBody::loadPostProcess
- Purpose: Post-load initialization
- Calls: ActiveBody::loadPostProcess

## Globals
- None

## Dependencies
- PreRTS.h, Common/Xfer.h, GameLogic/Module/HighlanderBody.h
- ActiveBody (base class), DamageInfo, Xfer, XferVersion, DAMAGE_UNRESISTABLE

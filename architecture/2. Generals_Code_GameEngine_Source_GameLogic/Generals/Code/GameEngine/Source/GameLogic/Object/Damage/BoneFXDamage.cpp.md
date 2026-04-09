# Generals/Code/GameEngine/Source/GameLogic/Object/Damage/BoneFXDamage.cpp

## Purpose
This file implements the `BoneFXDamage` class, a damage module that interacts with the `BoneFXUpdate` module to handle bone-based effects and damage states in game objects.

## Responsibilities
- Manages damage state changes for game objects.
- Ensures the presence of the `BoneFXUpdate` module.
- Handles CRC (Cyclic Redundancy Check) and Xfer (transfer) operations for data serialization.

## Key Types
- BoneFXDamage (Class): Damage module that handles bone-based effects and damage states.
- None

## Key Functions
### BoneFXDamage::onObjectCreated
- Purpose: Ensures the presence of the `BoneFXUpdate` module in the game object.
- Calls: getObject()->findUpdateModule

### BoneFXDamage::onBodyDamageStateChange
- Purpose: Switches damage states by notifying the `BoneFXUpdate` module.
- Calls: changeBodyDamageState

### BoneFXDamage::crc
- Purpose: Extends base class CRC handling.
- Calls: DamageModule::crc

### BoneFXDamage::xfer
- Purpose: Handles data serialization with versioning.
- Calls: xferVersion, DamageModule::xfer

### BoneFXDamage::loadPostProcess
- Purpose: Extends base class post-load processing.
- Calls: DamageModule::loadPostProcess

## Globals
- None

## Dependencies
- Key includes:
  - "Common/Xfer.h"
  - "GameClient/Drawable.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"
  - "GameLogic/Module/BoneFXDamage.h"
  - "GameLogic/Module/BoneFXUpdate.h"

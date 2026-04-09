# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Damage/BoneFXDamage.cpp

## Purpose
Handles damage-related effects tied to bone animations in game objects.

## Responsibilities
- Manages damage state transitions for objects with bone animations
- Coordinates with BoneFXUpdate module for visual damage effects
- Implements serialization (Xfer) and CRC for network sync
- Validates module dependencies during object creation

## Key Types
- **BoneFXDamage (Class)**: Damage module that integrates with bone-based visual effects
- **BoneFXUpdate (Class)**: External module for handling bone animation updates (referenced but not defined here)

## Key Functions
### BoneFXDamage::BoneFXDamage
- Purpose: Constructor that initializes the damage module
- Calls: DamageModule constructor

### BoneFXDamage::onObjectCreated
- Purpose: Validates presence of required BoneFXUpdate module
- Calls: getObject(), findUpdateModule()

### BoneFXDamage::onBodyDamageStateChange
- Purpose: Notifies BoneFXUpdate when object's damage state changes
- Calls: getObject(), findUpdateModule(), BoneFXUpdate::changeBodyDamageState()

### BoneFXDamage::crc
- Purpose: Generates CRC checksum for network synchronization
- Calls: DamageModule::crc()

### BoneFXDamage::xfer
- Purpose: Serializes/deserializes module state for network play
- Calls: Xfer::xferVersion(), DamageModule::xfer()

### BoneFXDamage::loadPostProcess
- Purpose: Handles post-processing after module loading
- Calls: DamageModule::loadPostProcess()

## Globals
- **key_BoneFXUpdate (NameKeyType)**: Static name key for locating BoneFXUpdate module

## Dependencies
- **PreRTS.h**: Game engine precompiled header
- **Common/Xfer.h**: Network serialization utilities

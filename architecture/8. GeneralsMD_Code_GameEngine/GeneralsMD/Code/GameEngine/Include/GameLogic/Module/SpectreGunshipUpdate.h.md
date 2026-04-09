# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SpectreGunshipUpdate.h

## Purpose
Defines the Spectre Gunship update module for handling the weapon firing logic of the Spectre Gunship special power in Command & Conquer Generals.

## Responsibilities
- Manages the Spectre Gunship's orbital behavior and weapon firing
- Handles state transitions (inserting, orbiting, departing, idle)
- Controls visual/audio effects and decals for targeting
- Processes termination conditions for the special power

## Key Types
- **SpectreGunshipUpdateModuleData (Class)**: Module data containing templates and parameters for the gunship behavior
- **GunshipStatus (Enum)**: Represents the gunship's operational states (inserting, orbiting, departing, idle)
- **SpectreGunshipUpdate (Class)**: Main update module implementing SpecialPowerUpdateModule interface

## Key Functions
### SpectreGunshipUpdate::initiateIntentToDoSpecialPower
- Purpose: Initiates the special power action for the gunship
- Calls: Not inferable

### SpectreGunshipUpdate::update
- Purpose: Handles the periodic update logic for the gunship's behavior
- Calls: Not inferable

### SpectreGunshipUpdate::setSpecialPowerOverridableDestination
- Purpose: Sets an override destination for the gunship's targeting
- Calls: Not inferable

## Globals
- None

## Dependencies
- SpecialPowerUpdateModule.h
- Common/KindOf.h
- Forward references: SpecialPowerModule, ParticleSystem, FXList, AudioEventRTS, ParticleSystemID

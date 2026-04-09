# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SpectreGunshipDeploymentUpdate.h

## Purpose
Defines the SpectreGunshipDeploymentUpdate module for handling the deployment of the Spectre Gunship special power in Command & Conquer Generals Zero Hour.

## Responsibilities
- Manages the deployment logic for the Spectre Gunship special power
- Handles the gunship's lifecycle (inserting, orbiting, departing, idle)
- Provides interface for special power updates
- Manages module data and configuration

## Key Types
- **SpectreGunshipDeploymentUpdateModuleData (Class)**: Holds configuration data for the gunship deployment
- **GunshipDeployStatus (Enum)**: Tracks the current state of the gunship deployment
- **GunshipCreateLocType (Enum)**: Defines where the gunship should be created relative to the source/target

## Key Functions
### SpectreGunshipDeploymentUpdate::initiateIntentToDoSpecialPower
- Purpose: Initiates the special power deployment
- Calls: Not inferable

### SpectreGunshipDeploymentUpdate::update
- Purpose: Updates the gunship deployment state
- Calls: Not inferable

### SpectreGunshipDeploymentUpdate::cleanUp
- Purpose: Cleans up resources when the deployment is complete
- Calls: Not inferable

## Globals
- None

## Dependencies
- SpecialPowerUpdateModule.h
- Common/KindOf.h
- Forward references to SpecialPowerModule, ParticleSystem, FXList, AudioEventRTS classes
- Enums: ParticleSystemID, ScienceType

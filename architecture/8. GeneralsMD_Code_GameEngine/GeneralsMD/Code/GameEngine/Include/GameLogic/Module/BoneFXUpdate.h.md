# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/BoneFXUpdate.h

## Purpose
Defines the BoneFXUpdate module for managing bone-attached visual effects in the SAGE engine.

## Responsibilities
- Manages FX lists, object creation lists, and particle systems attached to skeletal bones
- Handles effect playback based on body damage states
- Updates and resolves bone locations for effect positioning
- Tracks and kills running particle systems

## Key Types
- **BoneLocInfo (struct)**: Stores bone name for effect positioning
- **BaseBoneListInfo (struct)**: Base class for bone-attached effect info with timing and playback flags
- **BoneFXListInfo (class)**: FX list attachment info inheriting from BaseBoneListInfo
- **BoneOCLInfo (class)**: Object creation list attachment info
- **BoneParticleSystemInfo (class)**: Particle system attachment info
- **BoneFXUpdateModuleData (class)**: Module data containing effect configurations per body state
- **BoneFXUpdate (class)**: Main update module class managing bone-attached effects

## Key Functions
### BoneFXUpdateModuleData::buildFieldParse
- Purpose: Registers INI field parsers for module data
- Calls: UpdateModuleData::buildFieldParse

### BoneFXUpdate::update
- Purpose: Updates all bone-attached effects based on current state
- Calls: doFXListAtBone, doOCLAtBone, doParticleSystemAtBone, killRunningParticleSystems

### BoneFXUpdate::changeBodyDamageState
- Purpose: Handles transitions between body damage states
- Calls: Not inferable

### BoneFXUpdate::resolveBoneLocations
- Purpose: Resolves bone positions for effect placement
- Calls: Not inferable

## Globals
- **BONE_FX_MAX_BONES (enum)**: Maximum number of effects per body state (8)

## Dependencies
- GameClient/ParticleSys.h
- GameLogic/Module/UpdateModule.h
- DamageInfo (forward declaration)
- Thing (forward declaration)
- FXList (forward declaration)
- ObjectCreationList (forward declaration)
- ParticleSystemTemplate (forward declaration)

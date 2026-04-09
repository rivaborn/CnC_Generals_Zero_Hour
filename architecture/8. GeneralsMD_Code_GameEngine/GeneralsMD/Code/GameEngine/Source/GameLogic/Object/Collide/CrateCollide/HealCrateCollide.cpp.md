# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Collide/CrateCollide/HealCrateCollide.cpp

## Purpose
Implements the healing crate behavior in the game, which heals all objects owned by the player who collides with it.

## Responsibilities
- Heals all objects owned by the colliding player
- Plays a sound effect when the crate is picked up
- Handles serialization (CRC, Xfer) for save/load functionality
- Manages post-load processing

## Key Types
- **HealCrateCollide (Class)**: Handles healing crate collision logic
- **CrateCollide (Class)**: Base class for crate collision behavior

## Key Functions
### HealCrateCollide::executeCrateBehavior
- Purpose: Heals all objects owned by the colliding player and plays a sound effect
- Calls: `Player::healAllObjects`, `AudioEventRTS::setPosition`, `TheAudio->addAudioEvent`

### HealCrateCollide::crc
- Purpose: Serializes class data for CRC calculation
- Calls: `CrateCollide::crc`

### HealCrateCollide::xfer
- Purpose: Handles serialization for save/load functionality
- Calls: `Xfer::xferVersion`, `CrateCollide::xfer`

### HealCrateCollide::loadPostProcess
- Purpose: Performs post-load initialization
- Calls: `CrateCollide::loadPostProcess`

## Globals
- **TheAudio (AudioSystem)**: Global audio system reference

## Dependencies
- `PreRTS.h`, `Common/AudioEventRTS.h`, `Common/MiscAudio.h`, `Common/Player.h`, `Common/Xfer.h`, `GameLogic/Object.h`, `GameLogic/Module/HealCrateCollide.h`

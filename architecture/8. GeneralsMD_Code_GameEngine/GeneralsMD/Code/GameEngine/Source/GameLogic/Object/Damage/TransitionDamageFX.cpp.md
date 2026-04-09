# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Damage/TransitionDamageFX.cpp

## Purpose
Handles visual effects (FX, particle systems, object creation lists) triggered by damage state transitions in game objects.

## Responsibilities
- Parses damage effect configuration from INI files
- Manages FX, particle systems, and object creation lists tied to damage states
- Triggers effects when an object's damage state worsens
- Cleans up particle systems when damage states change

## Key Types
- `TransitionDamageFXModuleData` (Class): Stores damage effect configurations (FX lists, OCLs, particle systems)
- `FXLocInfo` (Struct): Describes effect location (bone or coordinate)
- `TransitionDamageFX` (Class): Damage module that handles effect transitions

## Key Functions
### `parseFXLocInfo`
- Purpose: Parses bone or coordinate location data from INI files
- Calls: `ini->getNextToken`, `ini->scanReal`, `ini->parseBool`

### `getLocalEffectPos`
- Purpose: Resolves effect position from bone or coordinate data
- Calls: `draw->getPristineBonePositions`, `GameLogicRandomValue`

### `onBodyDamageStateChange`
- Purpose: Handles damage state transitions and triggers appropriate effects
- Calls: `TheParticleSystemManager->destroyParticleSystemByID`, `FXList::doFXPos`, `ObjectCreationList::create`, `TheParticleSystemManager->createParticleSystem`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Common/Xfer.h`, `GameClient/Drawable.h`, `GameClient/FXList.h`, `GameLogic/GameLogic.h`, `GameLogic/Object.h`, `GameLogic/ObjectCreationList.h`, `GameLogic/Module/TransitionDamageFX.h`
- `INI`, `Xfer`, `DamageInfo`, `ParticleSystem`, `ParticleSystemTemplate`

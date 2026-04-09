# Generals/Code/GameEngine/Source/GameLogic/Object/Damage/TransitionDamageFX.cpp

## Purpose
This file implements the `TransitionDamageFX` module, which handles various effects triggered by damage transitions in game objects.

## Responsibilities
- Parses configuration data for damage effects.
- Manages particle systems and object creation lists based on damage states.
- Handles transitions between different body damage states.

## Key Types
- **TransitionDamageFXModuleData (Class)**: Stores configuration data for damage effects, including FX lists, OCLs, and particle systems.
- **TransitionDamageFX (Class)**: Manages the application of damage effects during state transitions.
- **FXLocInfo (Struct)**: Contains information about the location where an effect should be applied.

## Key Functions
### parseFXLocInfo
- Purpose: Parses location information for effects from INI files.
- Calls: `ini->getNextToken`, `stricmp`, `AsciiString`, `ini->parseBool`.

### getLocalEffectPos
- Purpose: Determines the local position for an effect based on bone or coordinate data.
- Calls: `draw->getPristineBonePositions`, `GameLogicRandomValue`.

## Globals
- None

## Dependencies
- **Includes**: "PreRTS.h", "Common/Xfer.h", "GameClient/Drawable.h", "GameClient/FXList.h", "GameLogic/GameLogic.h", "GameLogic/Object.h", "GameLogic/ObjectCreationList.h", "GameLogic/Module/TransitionDamageFX.h".
- **External Symbols**: `TheGameLogic`, `TheParticleSystemManager`, `IS_CONDITION_WORSE`, `getDamageTypeFlag`.

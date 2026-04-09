# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Die/CrushDie.cpp

## Purpose
Handles crush damage effects for objects, determining crush location and applying visual/audio feedback.

## Responsibilities
- Determines which part of an object was crushed (front/back/total)
- Plays crush sound effects based on crush type
- Updates object's crushed state and model conditions
- Serializes crush die module data

## Key Types
- **CrushDie (Class)**: Manages crush damage effects for objects
- **CrushEnum (Enum)**: Represents crush types (NO_CRUSH, FRONT_END_CRUSH, BACK_END_CRUSH, TOTAL_CRUSH)

## Key Functions
### crushLocationCheck
- Purpose: Determines which crush point was hit based on object positions and directions
- Calls: None (uses object methods)

### CrushDie::onDie
- Purpose: Handles crush damage effects when an object dies
- Calls: crushLocationCheck, isDieApplicable, GameLogicRandomValue, TheAudio->addAudioEvent

### CrushDie::crc
- Purpose: Serializes crush die module data for save/load
- Calls: DieModule::crc

### CrushDie::xfer
- Purpose: Handles data transfer for crush die module
- Calls: DieModule::xfer

## Globals
- None

## Dependencies
- Common/Player.h, Common/PlayerList.h, Common/RandomValue.h, Common/ThingFactory.h, Common/ThingTemplate.h, Common/Xfer.h
- GameClient/Drawable.h, GameLogic/GameLogic.h, GameLogic/Object.h, GameLogic/Module/BodyModule.h, GameLogic/Module/CrushDie.h
- PreRTS.h, AudioEventRTS, TheGameLogic, TheAudio

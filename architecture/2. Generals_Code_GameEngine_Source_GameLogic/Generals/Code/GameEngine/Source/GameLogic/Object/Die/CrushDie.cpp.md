# Generals/Code/GameEngine/Source/GameLogic/Object/Die/CrushDie.cpp

## Purpose
This file contains the implementation for the `CrushDie` module, which handles crush damage logic in the game engine.

## Responsibilities
- Determine the type of crush damage based on the location and orientation of objects.
- Play appropriate sound effects when crush damage occurs.
- Update the visual state of the damaged object to reflect crushing.

## Key Types
- CrushDie (Class): Handles crush die logic for objects.
- CrushEnum (Enum): Represents different types of crush points.

## Key Functions
### crushLocationCheck
- Purpose: Determines which crush point was hit based on the positions and orientations of the crusher and victim objects.
- Calls:
  - `getBodyModule()->getFrontCrushed()`
  - `getBodyModule()->getBackCrushed()`
  - `getPosition()`
  - `getUnitDirectionVector2D()`
  - `getGeometryInfo().getMajorRadius()`

### CrushDie::onDie
- Purpose: Handles the die callback for crush damage, playing sounds and updating object states.
- Calls:
  - `isDieApplicable(damageInfo)`
  - `TheGameLogic->findObjectByID()`
  - `crushLocationCheck(damageDealer, getObject())`
  - `getCrushDieModuleData()->m_crushSounds[crushType].getEventName().isEmpty()`
  - `GameLogicRandomValue(0, 99)`
  - `AudioEventRTS::setObjectID()`
  - `TheAudio->addAudioEvent(&crushSound)`
  - `getBodyModule()->setFrontCrushed()`
  - `getBodyModule()->setBackCrushed()`
  - `getDrawable()->clearAndSetModelConditionFlags()`

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/Player.h"
  - "Common/PlayerList.h"
  - "Common/RandomValue.h"
  - "Common/ThingFactory.h"
  - "Common/ThingTemplate.h"
  - "Common/Xfer.h"
  - "GameClient/Drawable.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"
  - "GameLogic/Module/BodyModule.h"
  - "GameLogic/Module/CrushDie.h"

- External symbols used:
  - `TheGameLogic`
  - `TheAudio`

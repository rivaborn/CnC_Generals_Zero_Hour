# Generals/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/JetAIUpdate.cpp

## Purpose
Handles AI updates for jet aircraft, including state management, movement, and interactions with airfields.

## Responsibilities
- Manages jet-specific AI states such as takeoff, landing, and circling.
- Handles parking at airfields and reloading ammo.
- Processes commands and ensures proper execution of AI tasks.
- Updates the jet's locomotion and model conditions (e.g., afterburners).

## Key Types
- **TaxiType (Enum)**: Defines taxiing directions.
- **JetAIStateType (Enum)**: Enumerates various states for jet AI, including takeoff, landing, and circling.
- **PartitionFilterHasParkingPlace (Class)**: Filters objects based on parking availability.
- **JetAwaitingRunwayState (Class)**: Manages the state of waiting for runway clearance.
- **JetOrHeliCirclingDeadAirfieldState (Class)**: Handles circling behavior when no suitable airfield is available.
- **JetOrHeliReturningToDeadAirfieldState (Class)**: Manages returning to a dead airfield.

## Key Functions
### isOutOfSpecialReloadAmmo
- Purpose: Checks if all special reload weapons are out of ammo.
- Calls: getWeaponInWeaponSlot, getStatus

### getPP
- Purpose: Retrieves the parking place behavior interface for an object.
- Calls: findObjectByID, isEffectivelyDead, isKindOf, testStatus, getParkingPlaceBehaviorInterface

### findSuitableAirfield
- Purpose: Finds a suitable airfield based on various filters.
- Calls: getClosestObject, MAKE_KINDOF_MASK, OBJECT_STATUS_UNDER_CONSTRUCTION, OBJECT_STATUS_SOLD

## Globals
- **BIGNUM (Real)**: A large number used for calculations.

## Dependencies
- Key includes:
  - "Common/ActionManager.h"
  - "Common/GlobalData.h"
  - "GameLogic/AIPathfind.h"
  - "GameLogic/Object.h"
  - "GameLogic/PartitionManager.h"
  - "GameLogic/Weapon.h"

- External symbols used:
  - TheGameLogic
  - TheAudio
  - TheThingFactory
  - TheActionManager
  - ThePartitionManager

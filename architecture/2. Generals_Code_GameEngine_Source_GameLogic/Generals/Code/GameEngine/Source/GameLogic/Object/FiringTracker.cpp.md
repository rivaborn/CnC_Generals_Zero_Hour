# Generals/Code/GameEngine/Source/GameLogic/Object/FiringTracker.cpp

## Purpose
This file implements the `FiringTracker` class, which tracks shots fired and targets for weapons that require a history of such actions in Command & Conquer Generals.

## Responsibilities
- Track consecutive shots at a target.
- Manage weapon cooldowns and reload times.
- Handle audio events for firing sounds.
- Adjust weapon fire rates based on conditions.

## Key Types
- `FiringTracker` (Class): Tracks shooting activity and manages related game logic.

## Key Functions
### FiringTracker::shotFired
- Purpose: Updates tracking information when a shot is fired.
- Calls:
  - `TheGameLogic->getFrame()`
  - `weaponFired->getAutoReloadWhenIdleFrames()`
  - `weaponFired->getContinuousFireCoastFrames()`
  - `weaponFired->getPossibleNextShotFrame()`
  - `weaponFired->getContinuousFireOneShotsNeeded()`
  - `weaponFired->getContinuousFireTwoShotsNeeded()`
  - `getObject()->testWeaponBonusCondition()`
  - `coolDown()`
  - `speedUp()`
  - `TheAudio->addAudioEvent()`
  - `setWakeFrame(getObject(), calcTimeToSleep())`

### FiringTracker::update
- Purpose: Updates the firing tracker's state and handles cooldowns.
- Calls:
  - `TheGameLogic->getFrame()`
  - `getObject()->reloadAllAmmo(TRUE)`
  - `TheAudio->removeAudioEvent(m_audioHandle)`
  - `coolDown()`
  - `calcTimeToSleep()`

### FiringTracker::calcTimeToSleep
- Purpose: Calculates the sleep time for the firing tracker.
- Calls:
  - `TheGameLogic->getFrame()`

### FiringTracker::speedUp
- Purpose: Increases the fire rate of the weapon.
- Calls:
  - `getObject()->testWeaponBonusCondition()`
  - `self->setWeaponBonusCondition()`
  - `self->clearWeaponBonusCondition()`
  - `self->clearAndSetModelConditionFlags(clr, set)`

### FiringTracker::coolDown
- Purpose: Decreases the fire rate of the weapon.
- Calls:
  - `getObject()->testWeaponBonusCondition()`
  - `getObject()->clearWeaponBonusCondition()`
  - `getObject()->clearAndSetModelConditionFlags(clr, set)`

## Globals
- None

## Dependencies
- Key includes and external symbols used but not defined here:
  - `PreRTS.h`
  - `Common/AudioHandleSpecialValues.h`
  - `Common/GameType.h`
  - `Common/GameAudio.h`
  - `Common/PerfTimer.h`
  - `Common/ThingTemplate.h`

# Generals/Code/GameEngine/Source/GameLogic/Object/Update/StealthUpdate.cpp

## Purpose
This file contains the implementation of the `StealthUpdate` class, which handles stealth-related logic for game objects in Command & Conquer Generals.

## Responsibilities
- Manage stealth status and conditions for objects.
- Handle disguise transitions and effects.
- Update stealth detection and visibility based on player relationships.
- Process stealth-related events and animations.

## Key Types
- `StealthUpdateModuleData` (struct): Stores configuration data for stealth updates.
- `StealthUpdate` (class): Manages stealth behavior for game objects.

## Key Functions
### setWakeupIfInRange
- Purpose: Marks nearby enemy units to wake up and target the object if it is detected.
- Calls:
  - `Object::getVisionRange()`
  - `Coord3D::sub()`
  - `Coord3D::length()`
  - `AIUpdateInterface::wakeUpAndAttemptToTarget()`

## Globals
- None

## Dependencies
- Key includes and external symbols used but not defined here:
  - `GameState.h`
  - `Player.h`
  - `ThingTemplate.h`
  - `Drawable.h`
  - `Weapon.h`
  - `StealthUpdateModuleData`
  - `TheGameLogic`
  - `ThePlayerList`
  - `TheGameClient`
  - `TheThingFactory`
  - `TheAudio`
  - `TheRadar`
  - `TheInGameUI`
  - `TheControlBar`

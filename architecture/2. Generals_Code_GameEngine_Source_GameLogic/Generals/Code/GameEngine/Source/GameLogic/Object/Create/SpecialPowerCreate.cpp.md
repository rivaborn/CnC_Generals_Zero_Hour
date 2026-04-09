# Generals/Code/GameEngine/Source/GameLogic/Object/Create/SpecialPowerCreate.cpp

## Purpose
This file implements the `SpecialPowerCreate` class, which handles special power creation logic when a building is created or completes its build process in Command & Conquer Generals.

## Responsibilities
- Initialize and manage special powers for buildings.
- Notify special power modules when a building is built.
- Handle CRC (Cyclic Redundancy Check) and Xfer (transfer) operations for the module.

## Key Types
- `SpecialPowerCreate` (Class): Manages special power creation logic for buildings.
- None

## Key Functions
### SpecialPowerCreate::onBuildComplete
- Purpose: Notifies special power modules when a building is built.
- Calls:
  - `shouldDoOnBuildComplete`
  - `CreateModule::onBuildComplete`
  - `getBehaviorModules`
  - `getSpecialPower`
  - `onSpecialPowerCreation`

### SpecialPowerCreate::crc
- Purpose: Handles CRC operations for the module.
- Calls:
  - `CreateModule::crc`

### SpecialPowerCreate::xfer
- Purpose: Handles Xfer (transfer) operations for the module, including versioning.
- Calls:
  - `xferVersion`
  - `CreateModule::xfer`

### SpecialPowerCreate::loadPostProcess
- Purpose: Performs post-load processing for the module.
- Calls:
  - `CreateModule::loadPostProcess`

## Globals
- None

## Dependencies
- Key includes and external symbols used but not defined here:
  - `PreRTS.h`
  - `Common/Xfer.h`
  - `GameLogic/Object.h`
  - `GameLogic/Module/SpecialPowerCreate.h`
  - `GameLogic/Module/SpecialPowerModule.h`

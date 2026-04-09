# Generals/Code/GameEngine/Source/GameLogic/Object/Create/VeterancyGainCreate.cpp

## Purpose
This file contains the implementation for the `VeterancyGainCreate` module, which handles setting an object's veterancy level upon creation based on required science.

## Responsibilities
- Initialize and manage the veterancy gain module data.
- Set the starting veterancy level of an object when created.
- Check if the controlling player has the required science to set the veterancy level.

## Key Types
- `VeterancyGainCreateModuleData (struct)`: Stores data for the veterancy gain module, including starting level and required science.
- `VeterancyGainCreate (class)`: Inherits from `CreateModule` and implements the logic for setting an object's veterancy level on creation.

## Key Functions
### VeterancyGainCreateModuleData::VeterancyGainCreateModuleData
- Purpose: Initializes the veterancy gain module data with default values.
- Calls: None

### VeterancyGainCreateModuleData::buildFieldParse
- Purpose: Builds field parsing for the veterancy gain module data.
- Calls: `CreateModuleData::buildFieldParse`

### VeterancyGainCreate::VeterancyGainCreate
- Purpose: Constructor for the `VeterancyGainCreate` class.
- Calls: None

### VeterancyGainCreate::~VeterancyGainCreate
- Purpose: Destructor for the `VeterancyGainCreate` class.
- Calls: None

### VeterancyGainCreate::onCreate
- Purpose: Sets the starting veterancy level of an object when created, based on required science.
- Calls: `getVeterancyGainCreateModuleData`, `getObject()->getControllingPlayer()`, `hasScience`, `getExperienceTracker`, `setMinVeterancyLevel`

### VeterancyGainCreate::crc
- Purpose: Handles CRC (Cyclic Redundancy Check) for the module.
- Calls: `CreateModule::crc`

### Veterancy

# Generals/Code/GameEngine/Source/GameClient/System/CampaignManager.cpp

## Purpose
Manages campaign flow, missions, and progression in the game.

## Responsibilities
- Loads and parses campaign data from INI files
- Tracks current campaign and mission state
- Handles mission transitions and progression
- Manages campaign-specific data like rank points and difficulty

## Key Types
- **CampaignManager (Class)**: Main campaign management system
- **Campaign (Class)**: Represents a campaign with missions and metadata
- **Mission (Class)**: Represents individual missions within a campaign
- **FieldParse (Struct)**: INI parsing configuration structure

## Key Functions
### CampaignManager::init
- Purpose: Initializes the campaign manager by loading campaign data
- Calls: INI::load

### CampaignManager::gotoNextMission
- Purpose: Advances to the next mission in the current campaign
- Calls: Campaign::getNextMission

### CampaignManager::parseMissionPart
- Purpose: Parses mission-specific data from INI files
- Calls: INI::initFromINI

### CampaignManager::xfer
- Purpose: Handles serialization/deserialization of campaign state
- Calls: Xfer::xferVersion, Xfer::xferAsciiString, Xfer::xferInt, Xfer::xferUser

## Globals
- **TheCampaignManager (CampaignManager*)**: Global instance of the campaign manager

## Dependencies
- Common/INI.h
- Common/Xfer.h
- GameClient/CampaignManager.h
- GameClient/GameClient.h
- PreRTS.h

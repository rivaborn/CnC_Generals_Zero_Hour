# GeneralsMD/Code/GameEngine/Include/GameClient/CampaignManager.h

## Purpose
Header defining campaign and mission management for the game, including data structures and the CampaignManager singleton.

## Responsibilities
- Define Mission and Campaign data structures
- Declare CampaignManager singleton for campaign progression
- Provide snapshot serialization for campaign state
- Manage campaign/mission transitions and victory conditions

## Key Types
- **Mission (Class)**: Represents a single mission with name, map, objectives, and audio.
- **Campaign (Class)**: Represents a campaign containing multiple missions and metadata.
- **CampaignManager (Class)**: Singleton managing campaign state, progression, and serialization.
- **AsciiString (Class)**: String type used for mission/campaign labels.
- **Image (Class)**: Forward reference for image handling.
- **MAX_OBJECTIVE_LINES (Enum)**: Constant for max objective lines (5).
- **MAX_DISPLAYED_UNITS (Enum)**: Constant for max displayed units (3).

## Key Functions
### CampaignManager::gotoNextMission
- Purpose: Advances to the next mission in the current campaign.
- Calls: Not inferable from header.

### CampaignManager::setCampaignAndMission
- Purpose: Sets the current campaign and mission by name.
- Calls: Not inferable from header.

### CampaignManager::xfer
- Purpose: Serializes campaign state for snapshot system.
- Calls: Not inferable from header.

### Campaign::newMission
- Purpose: Creates a new mission and adds it to the campaign.
- Calls: Not inferable from header.

## Globals
- **TheCampaignManager (CampaignManager*)**: Singleton instance of the campaign manager.

## Dependencies
- **Common/Snapshot.h**: For snapshot serialization.
- **Common/AudioEventRTS.h**: For audio event handling.
- **std::list**: For mission/campaign storage.
- **MemoryPoolObject

# Generals/Code/GameEngine/Source/Common/RTS/Science.cpp

## Purpose
This file manages science definitions, storage, and retrieval in the game. It handles parsing science data from INI files, checking player prerequisites for sciences, and providing information about available sciences.

## Responsibilities
- Parse science definitions from INI files.
- Store and manage science information.
- Check player prerequisites for sciences.
- Provide lists of purchasable sciences for players.

## Key Types
- ScienceStore (Class): Manages the storage and retrieval of science data.
- ScienceInfo (Class): Stores individual science information, including prerequisites and costs.
- ScienceType (Enum): Represents different types of sciences in the game.

## Key Functions
### init
- Purpose: Initializes the science store by clearing existing science data.
- Calls: None

### reset
- Purpose: Resets the science store by deleting overrides for each science.
- Calls: deleteOverrides, erase

### getScienceFromInternalName
- Purpose: Retrieves a science type from its internal name.
- Calls: nameToKey

### getInternalNameForScience
- Purpose: Retrieves the internal name for a given science type.
- Calls: keyToName

### friend_getScienceNames
- Purpose: Returns a vector of all known science names (for use by WorldBuilder).
- Calls: keyToName, getFinalOverride

### addRootSciences
- Purpose: Adds root sciences to a vector.
- Calls: findScienceInfo, addRootSciences

### findScienceInfo
- Purpose: Finds and returns the ScienceInfo for a given science type.
- Calls: getFinalOverride

### friend_parseScienceDefinition
- Purpose: Parses science definitions from an INI file.
- Calls: getNextToken, parseScienceVector, parseInt, parseBool, parseAndTranslateLabel, initFromINI, markAsOverride, setNextOverride, addRootSciences

### getSciencePurchaseCost
- Purpose: Retrieves the purchase cost for a given science type.
- Calls: findScienceInfo

### isScienceGrantable
- Purpose: Checks if a science can be granted to a player.
- Calls: findScienceInfo

### getNameAndDescription
- Purpose: Retrieves the name and description of a given science type.
- Calls: findScienceInfo

### playerHasPrereqsForScience
- Purpose: Checks if a player has all prerequisites for a given science.
- Calls: findScienceInfo, hasScience

### playerHasRootPrereqsForScience
- Purpose: Checks if a player has root prerequisites for a given science.
- Calls: findScienceInfo, hasScience

### getPurchasableSciences
- Purpose: Returns lists of sciences a player can purchase now and potentially in the future.
- Calls: findScienceInfo, hasScience, playerHasPrereqsForScience, playerHasRootPrereqsForScience

### friend_lookupScience
-

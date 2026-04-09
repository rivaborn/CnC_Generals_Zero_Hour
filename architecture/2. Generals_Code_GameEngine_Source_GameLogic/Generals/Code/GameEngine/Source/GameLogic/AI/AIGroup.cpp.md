# Generals/Code/GameEngine/Source/GameLogic/AI/AIGroup.cpp

## Purpose
This file contains the implementation of the `AIGroup` class, which manages a group of AI-controlled game objects in Command & Conquer Generals. It handles operations like adding/removing members, computing group properties, and issuing commands to all members.

## Responsibilities
- Manage a list of AI-controlled objects.
- Compute group properties such as speed and center position.
- Issue commands to all members of the group.
- Handle serialization and deserialization of group data.

## Key Types
- `AIGroup` (Class): Manages a group of AI objects, providing methods for adding/removing members, computing group properties, and issuing commands.

## Key Functions
### makeMemberStop
- Purpose: Stops a member from moving.
- Calls: Not inferable.

### getID
- Purpose: Returns the unique ID of the group.
- Calls: None

### getAllIDs
- Purpose: Returns the IDs of all members in the group.
- Calls: `m_memberList.begin()`, `m_memberList.end()`

### getSpeed
- Purpose: Returns the speed of the slowest member in the group.
- Calls: `recompute()`

### isMember
- Purpose: Checks if an object is a member of the group.
- Calls: `std::find()`

### add
- Purpose: Adds an object to the group.
- Calls: `obj->getAIUpdateInterface()`, `obj->enterGroup()`

### remove
- Purpose: Removes an object from the group.
- Calls: `std::find()`, `obj->leaveGroup()`

### containsAnyObjectsNotOwnedByPlayer
- Purpose: Checks if the group contains any objects not owned by a specified player.
- Calls: `m_memberList.begin()`, `m_memberList.end()`

### removeAnyObjectsNotOwnedByPlayer
- Purpose: Removes objects not owned by a specified player from the group.
- Calls: `remove()`

### getCenter
- Purpose: Computes the centroid of the group.
- Calls: `obj->getPosition()`

### getMinMaxAndCenter
- Purpose: Computes the bounding box and center of the group.
- Calls: `obj->getPosition()`

### isIdle
- Purpose: Checks if all members in the group are idle.
- Calls: `ai->isIdle()`, `obj->isEffectivelyDead()`

### isBusy
- Purpose: Checks if all members in the group are busy.
- Calls: `ai->isBusy()`, `obj->isEffectivelyDead()`

### isGroupAiDead
- Purpose: Checks if all AI members in the group are dead.
- Calls: `obj->isEffectivelyDead()`

### getSpecialPowerSourceObject
- Purpose: Returns an object that can perform a special power.
- Calls: `TheSpecialPowerStore->findSpecialPowerTemplateByID()`, `object->getSpecialPowerModule()`

### getCommandButtonSourceObject
- Purpose: Returns an object with a specific command button.
- Calls: `TheControlBar->findCommandSet()`, `commandSet->getCommandButton()`

### groupSetEmoticon
- Purpose: Sets an emoticon for all members in the group.
- Calls: `draw->setEmoticon()`

### groupOverrideSpecialPowerDestination
- Purpose: Overrides the destination of a special power for all members.
- Calls: `object->findSpecialPowerWithOverridableDestinationActive()`, `spuInterface->setSpecialPowerOverridableDestination()`

### crc
- Purpose: Handles CRC serialization of the group data.
- Calls: `xfer->xferUser()`, `xfer->xferUnsignedInt()`, `xfer->xferObjectID()`, `xfer->xferReal()

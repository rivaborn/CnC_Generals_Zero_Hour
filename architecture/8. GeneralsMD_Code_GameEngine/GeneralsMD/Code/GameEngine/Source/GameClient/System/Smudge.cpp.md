# GeneralsMD/Code/GameEngine/Source/GameClient/System/Smudge.cpp

## Purpose
Implements the smudge system for managing temporary visual effects (smudges) in the game.

## Responsibilities
- Manages creation and reuse of smudge objects via object pooling
- Handles smudge sets (groups of related smudges)
- Tracks smudge usage and hardware support status
- Provides initialization and cleanup for the smudge system

## Key Types
- SmudgeManager (Class): Manages all smudge sets and global smudge state
- SmudgeSet (Class): Groups related smudges together
- Smudge (Class): Represents individual smudge visual effects

## Key Functions
### SmudgeManager::addSmudgeSet
- Purpose: Creates or reuses a smudge set from the free pool
- Calls: W3DNEW

### SmudgeSet::addSmudgeToSet
- Purpose: Creates or reuses a smudge object from the free pool
- Calls: W3DNEW

### SmudgeManager::reset
- Purpose: Releases all smudge sets and returns them to the free pool
- Calls: SmudgeSet::reset

### SmudgeSet::reset
- Purpose: Returns all smudges in the set to the free pool
- Calls: None

## Globals
- SmudgeSet::m_freeSmudgeList (DLListClass<Smudge>): Pool of unused smudge objects

## Dependencies
- "GameClient/Smudge.h" (header)
- W3DNEW (memory allocation)
- DLListClass (double-linked list implementation)

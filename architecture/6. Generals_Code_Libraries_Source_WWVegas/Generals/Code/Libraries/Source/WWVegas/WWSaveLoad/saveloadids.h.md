# Generals/Code/Libraries/Source/WWVegas/WWSaveLoad/saveloadids.h

## Purpose
Defines chunk ID ranges for the save-load system and various subsystems in the SAGE engine.

## Responsibilities
- Defines enumerated chunk ID ranges for different subsystems (e.g., WW3D, WWPHYS, WWAUDIO).
- Establishes IDs for save-load system components (e.g., DEFMGR, TWIDDLER).
- Prevents ID collisions by allocating distinct ranges (e.g., 0x00010000 for WW3D).

## Key Types
- (anonymous enum) (Enum): Defines chunk ID ranges for save-load and subsystem components.

## Key Functions
None.

## Globals
None.

## Dependencies
- None.

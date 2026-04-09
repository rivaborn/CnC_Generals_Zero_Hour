# Generals/Code/GameEngine/Source/Common/System/KindOf.cpp

## Purpose
This file defines the `KindOfMaskType` class and initializes a global instance of it, `KINDOFMASK_NONE`, which is used to manage various object properties in the game.

## Responsibilities
- Define and initialize the `KindOfMaskType` class.
- Provide a list of bit names representing different kinds or properties of objects in the game.

## Key Types
- KindOfMaskType (Class): Manages object properties using bitmask flags.

## Key Functions
None

## Globals
- KINDOFMASK_NONE (KindOfMaskType): An instance initialized to all zeroes, representing no properties set.

## Dependencies
- "Common/KindOf.h"
- "Common/BitFlagsIO.h"

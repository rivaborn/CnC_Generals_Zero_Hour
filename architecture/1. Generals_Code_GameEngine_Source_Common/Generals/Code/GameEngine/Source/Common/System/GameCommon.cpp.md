# Generals/Code/GameEngine/Source/Common/System/GameCommon.cpp

## Purpose
This file contains common utility functions and definitions used across the game engine, including angle normalization and string arrays for veterancy and relationship statuses.

## Responsibilities
- Provides utility functions for mathematical operations.
- Defines global string arrays for game-related constants.
- Ensures angle values are within a standard range.

## Key Types
- None

## Key Functions
### normalizeAngle
- Purpose: Normalizes an angle to be within the range of -Ï to Ï.
- Calls: 
  - `_isnan(angle)`

## Globals
- TheVeterancyNames (const char*[]): Array of strings representing veterancy levels.
- TheRelationshipNames (const char*[]): Array of strings representing relationship statuses.

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/GameCommon.h"
- External symbols used but not defined here:
  - `Real` (type)
  - `_isnan(angle)` (function)
  - `PI` (constant)
  - `DEBUG_ASSERTCRASH` (macro)

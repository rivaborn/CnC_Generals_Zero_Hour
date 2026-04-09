# GeneralsMD/Code/GameEngine/Include/Common/UnitTimings.h

## Purpose
Header file to control compilation of unit timing features via a preprocessor define.

## Responsibilities
- Defines a preprocessor flag to enable/disable unit timing functionality
- Prevents multiple inclusions of the header
- Provides a central location for timing-related feature toggles

## Key Types
None

## Key Functions
None

## Globals
- `dont_DO_UNIT_TIMINGS` (macro): Disables unit timing functionality when defined

## Dependencies
- Standard C++ preprocessor directives
- No external symbols or includes used

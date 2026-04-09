# GeneralsMD/Code/Libraries/Source/WPAudio/AUD_Level.cpp

## Purpose
Manages audio level transitions and adjustments over time.

## Responsibilities
- Initialize audio level parameters
- Set, force, or adjust audio levels
- Calculate level changes over time
- Update audio levels based on elapsed time
- Retrieve current audio level values

## Key Types
- AudioLevel (struct): Tracks audio level state, including current level, target level, change rate, and flags

## Key Functions
### AudioLevelInit
- Purpose: Initialize an audio level with a starting value
- Calls: AudioGetTime(), AudioLevelSetDuration(), AudioLevelSet(), AudioLevelUpdate()

### AudioLevelSet
- Purpose: Set a new target audio level immediately
- Calls: None

### AudioLevelForce
- Purpose: Force an immediate update to the target level
- Calls: None

### AudioLevelAdjust
- Purpose: Adjust the target level with smooth transition
- Calls: AudioGetTime()

### AudioLevelSetDuration
- Purpose: Set the duration and range for level transitions
- Calls: None

### AudioLevelUpdate
- Purpose: Update the current audio level based on elapsed time
- Calls: AudioGetTime()

### AudioLevelGetVal
- Purpose: Retrieve the current audio level value
- Calls: None

## Globals
- None

## Dependencies
- wpaudio/altypes.h
- wpaudio/level.h
- wpaudio/time.h
- AudioGetTime() (external)
- DBG_ASSERT, DBG_SET_TYPE, DBG_ASSERT_TYPE (debug macros)

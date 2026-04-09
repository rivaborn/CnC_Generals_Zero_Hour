# GeneralsMD/Code/Libraries/Source/WPAudio/AUD_Attributes.cpp

## Purpose
Manages audio attribute structures (volume, pitch, pan) and their transitions over time.

## Responsibilities
- Initialize audio attribute structures
- Update audio attribute levels
- Apply attribute modifications
- Calculate pitch adjustments
- Track attribute usage

## Key Types
- AudioAttribs (struct): Contains volume, pitch, and pan level attributes with transition parameters
- AudioLevel (struct): Used for volume, pitch, and pan level management (defined elsewhere)

## Key Functions
### AudioAttribsInit
- Purpose: Initializes an AudioAttribs structure with default values
- Calls: AudioLevelInit, AudioAttribsSetPitchDuration, AudioAttribsSetVolumeDuration, AudioAttribsSetPanDuration, AudioLevelSet

### AudioAttribsUpdate
- Purpose: Updates all audio levels in the structure
- Calls: AudioLevelUpdate (three times)

### AudioAttribsChanged
- Purpose: Checks if any audio attribute has changed
- Calls: AudioLevelChanged (three times)

### AudioAttribsApply
- Purpose: Applies modifications from one AudioAttribs to another
- Calls: AudioLevelSet, AudioLevelApply, AudioAttribsGetVolume, AudioAttribsGetPitch, AudioAttribsSetPitch, AudioAttribsGetPan, AudioAttribsSetPan, AudioLevelUpdate

### AudioAttribsUsed
- Purpose: Marks audio levels as used
- Calls: AudioLevelUsed (three times)

### AudioAttribsCalcPitch
- Purpose: Calculates final pitch based on current attributes
- Calls: AudioAttribsGetPitch

## Globals
- None

## Dependencies
- Key includes: `<wpaudio/altypes.h>`, `<wpaudio/level.h>`, `<wpaudio/attributes.h>`
- External symbols: AudioLevelInit, AudioLevelUpdate, AudioLevelChanged, AudioLevelSet, AudioLevelApply, AudioLevelUsed, AudioAttribsSetPitchDuration, AudioAttribsSetVolumeDuration, AudioAttribsSetPanDuration, AudioAttribsGetVolume, AudioAttribsGetPitch, AudioAttribsSetPitch, AudioAttribsGetPan, AudioAttribsSetPan, DBG_ASSERT, DBG_SET_TYPE, DBG_ASSERT_TYPE, DBG_DECLARE_TYPE

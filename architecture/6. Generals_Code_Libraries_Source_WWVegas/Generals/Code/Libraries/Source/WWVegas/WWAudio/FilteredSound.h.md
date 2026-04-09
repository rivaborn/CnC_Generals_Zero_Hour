# Generals/Code/Libraries/Source/WWVegas/WWAudio/FilteredSound.h

## Purpose
Defines a sound class that applies a reverb filter to produce a "tinny" audio effect.

## Responsibilities
- Inherits from SoundPseudo3DClass to provide filtered sound playback
- Manages a reverb filter handle for audio processing
- Overrides volume update and initialization methods
- Provides class identification and conversion methods

## Key Types
- **FilteredSoundClass (Class)**: Sound object with reverb filtering capability

## Key Functions
### FilteredSoundClass (Constructor)
- Purpose: Default constructor for FilteredSoundClass
- Calls: Not inferable

### FilteredSoundClass (Copy Constructor)
- Purpose: Copy constructor for FilteredSoundClass
- Calls: Not inferable

### ~FilteredSoundClass (Destructor)
- Purpose: Destructor for FilteredSoundClass
- Calls: Not inferable

### operator= (Assignment Operator)
- Purpose: Assignment operator for FilteredSoundClass
- Calls: Not inferable

### Get_Class_ID
- Purpose: Returns the class ID for identification
- Calls: Not inferable

### As_FilteredSoundClass
- Purpose: Returns this as FilteredSoundClass pointer
- Calls: Not inferable

### Update_Volume
- Purpose: Updates the sound volume with filtering applied
- Calls: Not inferable

### Get_Factory
- Purpose: Returns the persistence factory for this class
- Calls: Not inferable

### Initialize_Miles_Handle
- Purpose: Initializes the Miles audio handle with filter
- Calls: Not inferable

## Globals
- **m_hFilter (HPROVIDER)**: Stores the handle to the reverb filter

## Dependencies
- SoundPseudo3D.H (header include)
- Pers

# Generals/Code/Libraries/Source/WWVegas/WWAudio/listenerhandle.h

## Purpose
Defines the `ListenerHandleClass` for managing 3D audio listeners in the SAGE engine.

## Responsibilities
- Inherits from `Sound3DHandleClass` to provide listener-specific audio control.
- Overrides sample playback methods with no-op implementations (listeners don't play samples).
- Exposes RTTI via `As_ListenerHandleClass()`.

## Key Types
- **ListenerHandleClass (Class)**: Manages 3D audio listener state and inherits sample control methods.

## Key Functions
### ListenerHandleClass()
- Purpose: Default constructor.
- Calls: None.

### ~ListenerHandleClass()
- Purpose: Destructor.
- Calls: None.

### As_ListenerHandleClass()
- Purpose: RTTI cast to `ListenerHandleClass`.
- Calls: None.

### Initialize()
- Purpose: Initializes the listener with a sound buffer.
- Calls: None.

### Start_Sample(), Stop_Sample(), Resume_Sample(), End_Sample(), Set_Sample_Volume(), Set_Sample_Pan(), Set_Sample_Loop_Count(), Set_Sample_MS_Position(), Set_Sample_Playback_Rate()
- Purpose: No-op implementations (listeners don't play samples).
- Calls: None.

### Get_Sample_Volume(), Get_Sample_Pan(), Get_Sample_Loop_Count(), Get_Sample_MS_Position(), Get_Sample_Playback_Rate()
- Purpose: Return default values (volume=0, pan=64, loop=0, rate=0).
- Calls: None.

## Globals
- None.

## Dependencies
- `sound3dhandle.h` (base class).

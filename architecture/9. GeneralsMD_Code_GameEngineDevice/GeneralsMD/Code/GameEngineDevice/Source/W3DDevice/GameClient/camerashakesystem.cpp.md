# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/camerashakesystem.cpp

## Purpose
Implements a camera shake system for visual effects during explosions or impacts.

## Responsibilities
- Manages camera shake effects via sinusoidal rotations
- Handles creation, timing, and removal of shake events
- Computes shake angles based on distance and intensity
- Provides global access to the shake system

## Key Types
- **CameraShakerClass (Class)**: Represents a single shake event with position, radius, duration, and intensity
- **CameraShakeSystemClass (Class)**: Manages the collection of shake events and their application

## Key Functions
### `CameraShakerClass::Compute_Rotations`
- Purpose: Calculates rotation angles for camera shake based on position and time
- Calls: `WWMath::Sin`, `WWMath::Sqrt`, `WWMath::Random_Float`

### `CameraShakeSystemClass::Add_Camera_Shake`
- Purpose: Creates a new camera shake event
- Calls: `new CameraShakerClass`

### `CameraShakeSystemClass::Update_Camera_Shaker`
- Purpose: Applies all active shake effects to the camera position
- Calls: `CameraShakerClass::Compute_Rotations`, `WWMath::Clamp`

## Globals
- **MIN_OMEGA (float)**: Minimum angular frequency for shake
- **MAX_OMEGA (float)**: Maximum angular frequency for shake
- **END_OMEGA (float)**: Final angular frequency for shake
- **MIN_PHI (float)**: Minimum phase offset for shake
- **MAX_PHI (float)**: Maximum phase offset for shake
- **AXIS_ROTATION (Vector3)**: Maximum rotation per axis
- **CameraShakerSystem (CameraShakeSystemClass)**: Global instance of the shake system

## Dependencies
- `<stdio.h>`, `<stdlib.h>`, `<string.h>`
- `Vector3`, `Matrix3D`, `WWMath`
- `MultiListClass`, `MultiListIterator`
- `Camera` (from WW3D2)

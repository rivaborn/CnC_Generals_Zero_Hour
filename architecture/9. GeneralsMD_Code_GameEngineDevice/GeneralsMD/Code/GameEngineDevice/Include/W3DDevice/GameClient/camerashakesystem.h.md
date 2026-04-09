# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/camerashakesystem.h

## Purpose
Manages camera shake effects triggered by in-game events like explosions or earthquakes.

## Responsibilities
- Tracks active camera shakers
- Updates shake intensity over time
- Applies shakes to camera based on position
- Handles shake expiration and cleanup

## Key Types
- **CameraShakeSystemClass (Class)**: Main system managing camera shakes
- **CameraShakerClass (Class)**: Represents individual shake effects with position, duration, and intensity
- **(anonymous enum) (Enum)**: Flags for shake behavior (e.g., ignore position)

## Key Functions
### Add_Camera_Shake
- Purpose: Adds a new camera shake effect
- Calls: CameraShakerClass constructor

### Timestep
- Purpose: Updates all active shakes over time
- Calls: CameraShakerClass::Timestep

### Update_Camera_Shaker
- Purpose: Applies shake rotations to camera based on its position
- Calls: CameraShakerClass::Compute_Rotations

### CameraShakerClass::Compute_Rotations
- Purpose: Calculates rotation angles for a shake effect
- Calls: None

## Globals
- **CameraShakerSystem (CameraShakeSystemClass)**: Singleton instance of the shake system

## Dependencies
- `Vector3.h` (for position/rotation math)
- `MultiList.h` (for object management)
- `MemPool.h` (for memory allocation)

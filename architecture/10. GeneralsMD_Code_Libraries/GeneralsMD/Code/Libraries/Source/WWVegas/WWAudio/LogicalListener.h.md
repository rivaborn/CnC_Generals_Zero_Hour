# GeneralsMD/Code/Libraries/Source/WWVegas/WWAudio/LogicalListener.h

## Purpose
Defines the `LogicalListenerClass`, representing audio listeners in the game world that react to logical sounds.

## Responsibilities
- Manages listener position, scale, and type mask for sound filtering
- Handles scene integration (add/remove)
- Provides timestamp management for sound events
- Implements persistence (save/load) for game state

## Key Types
- **LogicalListenerClass (Class)**: Represents a listener entity in the audio system that can hear and react to sounds.

## Key Functions
### LogicalListenerClass()
- Purpose: Default constructor for LogicalListenerClass.
- Calls: None

### ~LogicalListenerClass()
- Purpose: Destructor for LogicalListenerClass.
- Calls: None

### Set_Type_Mask(uint32 mask)
- Purpose: Sets the type mask for filtering sounds.
- Calls: None

### Get_Type_Mask()
- Purpose: Retrieves the current type mask.
- Calls: None

### Set_Position(const Vector3 &position)
- Purpose: Updates the listener's position in 3D space.
- Calls: None

### Get_Position()
- Purpose: Returns the listener's current position.
- Calls: None

### Set_Transform(const Matrix3D &transform)
- Purpose: Sets position from a transformation matrix.
- Calls: Matrix3D::Get_Translation()

### Get_Transform()
- Purpose: Returns a transformation matrix based on position.
- Calls: Matrix3D constructor, Set_Translation()

### Add_To_Scene(bool start_playing)
- Purpose: Adds listener to the active sound scene.
- Calls: None

### Remove_From_Scene()
- Purpose: Removes listener from the active sound scene.
- Calls: None

### Set_Scale(float

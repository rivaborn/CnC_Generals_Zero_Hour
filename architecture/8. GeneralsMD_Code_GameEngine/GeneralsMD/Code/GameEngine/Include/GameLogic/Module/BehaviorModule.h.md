# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/BehaviorModule.h

## Purpose
Defines the BehaviorModule class and its interfaces for game entity behavior management in the SAGE engine.

## Responsibilities
- Declares behavior-related module interfaces (e.g., ParkingPlaceBehaviorInterface, TransportPassengerInterface)
- Defines the BehaviorModule class hierarchy and its virtual methods
- Provides accessor methods for various behavior sub-modules
- Declares data structures for behavior-specific information (e.g., PPInfo for parking places)
- Defines enums for behavior states (e.g., RunwayReservationType)

## Key Types
- **BehaviorModuleData (Class)**: Module data container for behavior modules
- **BehaviorModuleInterface (Class)**: Interface for behavior module functionality
- **BehaviorModule (Class)**: Base behavior module implementation
- **ParkingPlaceBehaviorInterface (Class)**: Interface for parking place behavior (e.g., runways, hangars)
- **TransportPassengerInterface (Class)**: Interface for transport passenger behavior
- **CaveInterface (Class)**: Interface for cave-related behavior
- **LandMineInterface (Class)**: Interface for land mine behavior
- **RunwayReservationType (Enum)**: Type of runway reservation (takeoff/landing)

## Key Functions
### BehaviorModule::BehaviorModule
- Purpose: Constructor for BehaviorModule
- Calls: ObjectModule constructor

### BehaviorModule::crc
- Purpose: Generate CRC checksum for serialization
- Calls: Not inferable

### BehaviorModule::xfer
- Purpose: Serialize/deserialize module data
- Calls: Not inferable

### BehaviorModule::loadPostProcess
- Purpose: Post-processing after loading
- Calls: Not inferable

## Globals
- None

## Dependencies
- Common/GameType.h
- Common/Module.h
- MultiIniFieldParse (forward reference)
- Various module interface classes (forward declared)

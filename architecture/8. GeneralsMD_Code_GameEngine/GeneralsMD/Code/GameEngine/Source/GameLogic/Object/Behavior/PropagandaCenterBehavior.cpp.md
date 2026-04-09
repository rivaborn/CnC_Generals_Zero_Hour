# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/PropagandaCenterBehavior.cpp

## Purpose
Implements the propaganda center behavior for brainwashing captured units in Command & Conquer Generals Zero Hour.

## Responsibilities
- Manages brainwashing of captured units inside the propaganda center
- Tracks brainwashed units and restores their original ownership on deletion
- Handles unit exit logic after successful brainwashing
- Serializes brainwashing state for network synchronization

## Key Types
- `PropagandaCenterBehaviorModuleData` (Class): Stores brainwash duration configuration
- `PropagandaCenterBehavior` (Class): Main behavior class handling brainwashing logic
- `BrainwashedIDList` (Type): List tracking brainwashed unit IDs

## Key Functions
### `update`
- Purpose: Handles brainwashing logic and unit exit processing
- Calls: `PrisonBehavior::update`, `reserveDoorForExit`, `exitObjectViaDoor`, `TheGameLogic->findObjectByID`

### `onDelete`
- Purpose: Cleans up brainwashed units when propaganda center is destroyed
- Calls: `PrisonBehavior::onDelete`, `TheGameLogic->findObjectByID`, `Object::restoreOriginalTeam`

### `xfer`
- Purpose: Serializes brainwashing state for network synchronization
- Calls: `PrisonBehavior::xfer`, `Xfer::xferObjectID`, `Xfer::xferUnsignedInt`, `Xfer::xferSTLObjectIDList`

## Globals
- `m_brainwashingSubjectID` (ObjectID): Currently brainwashed unit
- `m_brainwashingSubjectStartFrame` (UnsignedInt): Frame when brainwashing started
- `m_brainwashedList` (BrainwashedIDList): List of permanently brainwashed units

## Dependencies
- `PrisonBehavior` (base class)
- `Xfer` (serialization)
- `TheGameLogic` (game state access)
- `Object` (unit management)
- `Player` (team management)
- `AIUpdateInterface` (surrender status)

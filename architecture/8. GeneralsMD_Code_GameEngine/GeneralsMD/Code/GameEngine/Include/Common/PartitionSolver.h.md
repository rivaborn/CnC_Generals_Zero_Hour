# GeneralsMD/Code/GameEngine/Include/Common/PartitionSolver.h

## Purpose
Header for a partition problem solver used to match entries (nuggets) to spaces (holes) of appropriate sizes.

## Responsibilities
- Define data structures for partition problem inputs/outputs
- Declare `PartitionSolver` class for solving the partition problem
- Provide enum for solution preference (speed vs. correctness)

## Key Types
- `PairObjectIDAndUInt` (typedef): Pair of ObjectID and unsigned integer (nugget ID and size)
- `PairObjectID` (typedef): Pair of two ObjectIDs (entry ID and hole ID)
- `EntriesVec` (typedef): Vector of `PairObjectIDAndUInt` (list of nuggets)
- `SpacesVec` (typedef): Vector of `PairObjectIDAndUInt` (list of holes)
- `SolutionVec` (typedef): Vector of `PairObjectID` (solution mapping)
- `SolutionType` (enum): Preference for fast or correct solution

## Key Functions
### `PartitionSolver::solve`
- Purpose: Solve the partition problem (may take long time as it's NP-complete)
- Calls: Not inferable (implementation in .cpp)

### `PartitionSolver::getSolution`
- Purpose: Retrieve the best solution found
- Calls: None

## Globals
- None

## Dependencies
- `<vector>` (via `std::vector`)
- `ObjectID` (forward-declared)
- `UnsignedInt` (forward-declared)

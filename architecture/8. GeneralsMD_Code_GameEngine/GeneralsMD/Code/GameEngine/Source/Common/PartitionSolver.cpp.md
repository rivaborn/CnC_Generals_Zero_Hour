# GeneralsMD/Code/GameEngine/Source/Common/PartitionSolver.cpp

## Purpose
Implements a general-purpose partition solver for NP-complete problems, attempting to distribute elements into spaces efficiently.

## Responsibilities
- Solves partitioning problems by distributing elements into available spaces
- Supports two solution modes: fast (greedy) and correct (not implemented)
- Handles sorting of elements and spaces by size for optimal placement
- Tracks leftover space and solution quality

## Key Types
- `PartitionSolver` (Class): Main solver class managing partitioning logic
- `PairObjectIDAndUInt` (Type): Pair of object ID and unsigned integer (size/weight)
- `SolutionType` (Enum): Solver mode (PREFER_FAST_SOLUTION, PREFER_CORRECT_SOLUTION)

## Key Functions
### `greater_than`
- Purpose: Comparison function for sorting pairs by their unsigned integer value
- Calls: None

### `PartitionSolver::solve`
- Purpose: Executes the partitioning algorithm based on selected solution type
- Calls: `std::sort`, `DEBUG_CRASH`

### `PartitionSolver::getSolution`
- Purpose: Returns the computed solution after solving
- Calls: None

## Globals
- `greater_than` (Static function): Comparison function for sorting

## Dependencies
- `Common/PartitionSolver.h`
- `PreRTS.h`
- `std::sort`, `DEBUG_CRASH`

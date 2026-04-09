# GeneralsMD/Code/GameEngine/Include/Common/SparseMatchFinder.h

## Purpose
Template class for finding best-matching objects based on bitmask conditions.

## Responsibilities
- Efficiently match objects using bitmask conditions
- Cache results to avoid repeated searches
- Handle ambiguous matches with tiebreakers
- Support debug validation of matches

## Key Types
- **SparseMatchFinder (Class)**: Main template class for sparse matching.
- **HashMapHelper (Class)**: Provides hash and equality operations for BITSET.
- **MapHelper (Class)**: Implements custom ordering for BITSET in map.
- **MatchMap (Class)**: Typedef for map storing best matches.

## Key Functions
### `findBestInfoSlow`
- Purpose: Slow but exhaustive search for best match.
- Calls: `countConditionIntersection`, `countConditionInverseIntersection`

### `findBestInfo`
- Purpose: Fast lookup with caching fallback to slow search.
- Calls: `m_bestMatches.find`, `findBestInfoSlow`

### `clear`
- Purpose: Clears cached matches.
- Calls: `m_bestMatches.clear`

## Globals
- None

## Dependencies
- `Common/BitFlags.h`
- `Common/STLTypedefs.h`
- `std::map`, `std::vector`
- `BITSET` operations (`test`, `size`, `countIntersection`, `countInverseIntersection`)

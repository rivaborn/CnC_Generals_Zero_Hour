# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/sampler.cpp

## Purpose
Implements various sampling algorithms for generating points in a hypercube, used for rendering and other purposes.

## Responsibilities
- Provides random, regular, stratified, and quasi-Monte Carlo sampling methods
- Manages sampling state (indexing) for iterative sampling
- Uses Mersenne Twister for random number generation
- Implements Halton sequence for low-discrepancy sampling

## Key Types
- `RandomSamplingClass` (Class): Random sampling using Mersenne Twister
- `RegularSamplingClass` (Class): Regular grid sampling
- `StratifiedSamplingClass` (Class): Stratified sampling with random offsets
- `QMCSamplingClass` (Class): Quasi-Monte Carlo sampling using Halton sequence
- `SamplingClass` (Class): Base class for sampling methods (not shown in file)

## Key Functions
### `RandomSamplingClass::Sample`
- Purpose: Generates random samples in a hypercube
- Calls: `Random.Get_Float()`

### `RegularSamplingClass::Sample`
- Purpose: Generates samples on a regular hypergrid
- Calls: None

### `StratifiedSamplingClass::Sample`
- Purpose: Generates stratified samples with random offsets
- Calls: `Random.Get_Float()`

### `QMCSamplingClass::Sample`
- Purpose: Generates samples using the Halton sequence
- Calls: `RadInv()`

### `RadInv`
- Purpose: Computes the radical inverse of a number in a given base
- Calls: None

## Globals
- `Random` (Random4Class): Global random number generator instance
- `primes` (int[]): Array of first 100 prime numbers for Halton sequence

## Dependencies
- `always.h`, `sampler.h`, `random.h`, `<math.h>`, `<assert.h>`, `<memory.h>`
- `W3DNEWARRAY` macro for memory allocation
- `Random4Class` from `random.h`

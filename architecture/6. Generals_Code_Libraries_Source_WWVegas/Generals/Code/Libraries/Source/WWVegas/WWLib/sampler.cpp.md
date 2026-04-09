# Generals/Code/Libraries/Source/WWVegas/WWLib/sampler.cpp

## Purpose
Implements various sampling algorithms for generating points in a hypercube, used for rendering and other purposes.

## Responsibilities
- Provides random, regular, stratified, and quasi-Monte Carlo sampling methods
- Manages sampling state (indices, dimensions, divisions)
- Implements Halton sequence for low-discrepancy sampling
- Handles memory allocation/deallocation for sampling indices

## Key Types
- **SamplingClass** (Class): Base class for sampling algorithms
- **RandomSamplingClass** (Class): Random sampling using Mersenne Twister
- **RegularSamplingClass** (Class): Regular grid sampling
- **StratifiedSamplingClass** (Class): Stratified sampling with random offsets
- **QMCSamplingClass** (Class): Quasi-Monte Carlo sampling using Halton sequence

## Key Functions
### RandomSamplingClass::Sample
- Purpose: Generates random samples using Mersenne Twister
- Calls: Random.Get_Float()

### RegularSamplingClass::Sample
- Purpose: Generates samples on a regular hypergrid
- Calls: None

### StratifiedSamplingClass::Sample
- Purpose: Generates stratified samples with random offsets
- Calls: Random.Get_Float()

### QMCSamplingClass::Sample
- Purpose: Generates samples using Halton sequence
- Calls: RadInv()

### RadInv
- Purpose: Computes radical inverse for Halton sequence
- Calls: None

## Globals
- **Random** (Random4Class): Global random number generator
- **primes** (const static int[]): First 100 prime numbers for Halton sequence

## Dependencies
- "always.h", "sampler.h", "random.h"
- <math.h>, <assert.h>, <memory.h>
- W3DNEWARRAY macro
- Random4Class, SamplingClass (base class)

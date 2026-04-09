# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/sampler.h

## Purpose
Defines abstract and concrete sampling classes for generating points in multidimensional space using various algorithms.

## Responsibilities
- Provide base `SamplingClass` interface for sampling algorithms
- Implement concrete samplers: random, regular grid, stratified, and quasi-Monte Carlo
- Manage sampling state (dimensions, divisions, internal indices)
- Support resetting and offsetting sample sequences

## Key Types
- **SamplingClass (Class)**: Abstract base class for sampling algorithms
- **RandomSamplingClass (Class)**: Random sampling using Mersenne Twister
- **RegularSamplingClass (Class)**: Regular hypergrid sampling
- **StratifiedSamplingClass (Class)**: Stratified hypergrid sampling with perturbations
- **QMCSamplingClass (Class)**: Quasi-Monte Carlo sampling (Halton-Hammersly sequence)

## Key Functions
### SamplingClass::Sample
- Purpose: Abstract method to generate next sample point
- Calls: None (pure virtual)

### RandomSamplingClass::Sample
- Purpose: Generate random sample point
- Calls: Not inferable (uses Random4Class internally)

### RegularSamplingClass::Sample
- Purpose: Generate regular grid sample point
- Calls: None

### StratifiedSamplingClass::Sample
- Purpose: Generate stratified grid sample point with perturbation
- Calls: None

### QMCSamplingClass::Sample
- Purpose: Generate quasi-Monte Carlo sample point
- Calls: None

## Globals
- None

## Dependencies
- `Random4Class` (used by `RandomSamplingClass`)
- Standard C++ headers (not explicitly shown)

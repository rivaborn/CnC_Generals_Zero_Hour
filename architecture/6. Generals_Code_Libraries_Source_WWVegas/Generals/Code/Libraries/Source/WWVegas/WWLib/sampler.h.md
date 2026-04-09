# Generals/Code/Libraries/Source/WWVegas/WWLib/sampler.h

## Purpose
Defines abstract and concrete sampling classes for generating points in multidimensional space using various algorithms.

## Responsibilities
- Provide base interface for sampling algorithms
- Implement random, regular grid, stratified, and quasi-Monte Carlo sampling
- Manage sampling state and dimensions
- Support resetting and sampling operations

## Key Types
- **SamplingClass (Class)**: Abstract base class for sampling algorithms
- **RandomSamplingClass (Class)**: Random sampling using Mersenne Twister
- **RegularSamplingClass (Class)**: Regular hypergrid sampling
- **StratifiedSamplingClass (Class)**: Stratified sampling with random perturbations
- **QMCSamplingClass (Class)**: Quasi-Monte Carlo sampling using Halton-Hammersly sequence

## Key Functions
### SamplingClass::Sample
- Purpose: Abstract method to generate a sample point
- Calls: None

### RandomSamplingClass::Sample
- Purpose: Generate random sample using Mersenne Twister
- Calls: Not inferable

### RegularSamplingClass::Sample
- Purpose: Generate sample on regular hypergrid
- Calls: Not inferable

### StratifiedSamplingClass::Sample
- Purpose: Generate stratified sample with perturbations
- Calls: Not inferable

### QMCSamplingClass::Sample
- Purpose: Generate quasi-Monte Carlo sample using Halton-Hammersly
- Calls: Not inferable

## Globals
- None

## Dependencies
- `Random4Class` (forward declaration)
- Standard C++ headers (not explicitly shown)

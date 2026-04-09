# Generals/Code/GameEngine/Source/Common/INI/INIParticleSys.cpp

## Purpose
This file contains the implementation for parsing Particle System definitions from INI files.

## Responsibilities
- Parses Particle System definitions from INI files.
- Manages creation and initialization of `ParticleSystemTemplate` objects.

## Key Types
- None

## Key Functions
### parseParticleSystemDefinition
- Purpose: Parses a Particle System definition from an INI file.
- Calls:
  - `getNextToken`
  - `set`
  - `findTemplate`
  - `newTemplate`
  - `initFromINI`

## Globals
- None

## Dependencies
- Key includes and external symbols used but not defined here:
  - `PreRTS.h`
  - `Common/INI.h`
  - `GameClient/ParticleSys.h`
  - `AsciiString`
  - `ParticleSystemTemplate`
  - `TheParticleSystemManager`

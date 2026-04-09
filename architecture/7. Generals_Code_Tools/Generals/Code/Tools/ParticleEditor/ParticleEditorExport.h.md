# Generals/Code/Tools/ParticleEditor/ParticleEditorExport.h

## Purpose
Header file defining the C interface for the Particle Editor tool, exposing functions for managing particle systems and templates.

## Responsibilities
- Declares C-compatible functions for particle system management
- Defines behavior flags for editor operations
- Provides access to particle system parameters and state

## Key Types
- ParticleSystemTemplate (Class): Represents a particle system template

## Key Functions
### CreateParticleSystemDialog
- Purpose: Creates the particle system editor dialog
- Calls: Not inferable

### DestroyParticleSystemDialog
- Purpose: Destroys the particle system editor dialog and frees resources
- Calls: Not inferable

### AppendParticleSystem
- Purpose: Adds a particle system to the editor
- Calls: Not inferable

### UpdateCurrentParticleSystem
- Purpose: Updates the currently selected particle system
- Calls: Not inferable

### NextParticleEditorBehavior
- Purpose: Returns the next behavior flag for the editor
- Calls: Not inferable

## Globals
- None

## Dependencies
- "Lib/BaseType.h" (for Bool type)
- ParticleSystemTemplate class (forward declared)

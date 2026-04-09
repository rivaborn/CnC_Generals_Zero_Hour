# Generals/Code/Tools/ParticleEditor/EmissionTypePanels.h

## Purpose
Defines UI panels for different particle emission types in the Particle Editor tool.

## Responsibilities
- Provide specialized panels for Point, Line, Box, Sphere, and Cylinder emission types
- Handle UI initialization and synchronization with particle system data
- Manage user input for emission parameters
- Implement message handling for particle system edits

## Key Types
- **EmissionPanelPoint (Class)**: Panel for point emission type
- **EmissionPanelLine (Class)**: Panel for line emission type
- **EmissionPanelBox (Class)**: Panel for box emission type
- **EmissionPanelSphere (Class)**: Panel for sphere emission type
- **EmissionPanelCylinder (Class)**: Panel for cylinder emission type
- **IDD (Enum)**: Dialog resource IDs for each panel type

## Key Functions
### EmissionPanelPoint/performUpdate
- Purpose: Synchronizes UI and particle system data
- Calls: Not inferable

### EmissionPanelLine/performUpdate
- Purpose: Synchronizes UI and particle system data
- Calls: Not inferable

### EmissionPanelBox/performUpdate
- Purpose: Synchronizes UI and particle system data
- Calls: Not inferable

### EmissionPanelSphere/performUpdate
- Purpose: Synchronizes UI and particle system data
- Calls: Not inferable

### EmissionPanelCylinder/performUpdate
- Purpose: Synchronizes UI and particle system data
- Calls: Not inferable

### OnParticleSystemEdit (all panels)
- Purpose: Handles particle system edit events
- Calls: Not inferable

## Globals
- None

## Dependencies
- `resource.h`: For dialog resource IDs
- `ISwapablePanel`: Base class for panel functionality
- MFC classes (CWnd, afx_msg)
-

# Generals/Code/Tools/WorldBuilder/include/TeamBehavior.h

## Purpose
Defines the `TeamBehavior` class, a property page for configuring team AI behavior in WorldBuilder.

## Responsibilities
- Manages team behavior script selection and configuration
- Handles UI events for behavior options
- Provides methods to set and update team behavior scripts
- Integrates with the team dictionary for script data

## Key Types
- **TeamBehavior (Class)**: Property page for team behavior configuration
- **(anonymous enum) (Enum)**: Dialog resource ID
- **IDD (Enum)**: Dialog resource ID

## Key Functions
### TeamBehavior()
- Purpose: Standard constructor for TeamBehavior.
- Calls: None

### DoDataExchange()
- Purpose: Handles DDX/DDV data exchange for the dialog.
- Calls: None

### setupScript()
- Purpose: Sets up a behavior script for a given key and control ID.
- Calls: None

### updateScript()
- Purpose: Updates a behavior script for a given key and control ID.
- Calls: None

### setTeamDict()
- Purpose: Sets the team dictionary for script data.
- Calls: None

### OnSelchangeOnCreateScript()
- Purpose: Handles script selection change for "OnCreate" behavior.
- Calls: None

### OnInitDialog()
- Purpose: Initializes the dialog controls.
- Calls: None

### OnTransportsReturn()
- Purpose: Handles "Transports Return" behavior event.
- Calls: None

### OnAvoidThreats()
- Purpose: Handles "Avoid Threats" behavior event.
- Calls: None

### OnSelchangeOnEnemySighted()
- Purpose: Handles script selection change for "OnEnemySighted" behavior.
- Calls: None

### OnSelchangeOnDestroyed()
- Purpose: Handles script selection change for "OnDestroyed"

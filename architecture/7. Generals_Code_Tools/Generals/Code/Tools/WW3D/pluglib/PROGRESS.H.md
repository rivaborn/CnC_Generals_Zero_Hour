# Generals/Code/Tools/WW3D/pluglib/PROGRESS.H

## Purpose
Defines a progress meter class for tracking and displaying export progress in a 3D tool pipeline.

## Responsibilities
- Tracks progress percentage and increments
- Handles user cancellation requests
- Updates the UI progress bar via an Interface object
- Manages nested progress meters via constructor chaining

## Key Types
- Progress_Meter_Class (Class): tracks and updates export progress with cancellation support

## Key Functions
### Progress_Meter_Class (constructor)
- Purpose: Initializes progress meter with base, range, and interface
- Calls: None

### Progress_Meter_Class (copy constructor)
- Purpose: Creates a sub-progress meter from another
- Calls: None

### Finish_In_Steps
- Purpose: Divides remaining progress into equal steps
- Calls: None

### Add_Increment
- Purpose: Advances progress by one step increment
- Calls: Set_Amount_Done

### Set_Amount_Done
- Purpose: Updates progress percentage and triggers UI update
- Calls: Max->ProgressUpdate, MessageBox, Max->GetCancel, Max->SetCancel

### Cancelled
- Purpose: Returns cancellation status
- Calls: None

## Globals
- None

## Dependencies
- "always.h"
- Interface class (external)
- MessageBox, MB_ICONQUESTION, MB_YESNO, IDYES (Windows API)

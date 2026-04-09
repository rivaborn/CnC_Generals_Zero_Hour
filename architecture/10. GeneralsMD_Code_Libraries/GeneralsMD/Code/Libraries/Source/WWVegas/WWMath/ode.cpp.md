# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/ode.cpp

## Purpose
Implements numerical integration methods for solving ordinary differential equations (ODEs) in the game engine.

## Responsibilities
- Provides Euler, Midpoint, Runge-Kutta 4th order, and Runge-Kutta 5th order integration methods
- Manages temporary state vectors for intermediate calculations
- Interfaces with ODESystemClass for state management and derivative computation

## Key Types
- **IntegrationSystem** (Class): Container for integration methods
- **ODESystemClass** (Class): Abstract ODE system interface (external)
- **StateVectorClass** (Class): Vector container for state values (external)

## Key Functions
### Euler_Integrate
- Purpose: Performs first-order Euler integration
- Calls: `sys->Get_State`, `sys->Compute_Derivatives`, `sys->Set_State`

### Midpoint_Integrate
- Purpose: Implements midpoint (Runge-Kutta 2) integration method
- Calls: `sys->Get_State`, `sys->Compute_Derivatives`, `sys->Set_State`

### Runge_Kutta_Integrate
- Purpose: Implements 4th-order Runge-Kutta integration
- Calls: `sys->Get_State`, `sys->Compute_Derivatives`, `sys->Set_State`

### Runge_Kutta5_Integrate
- Purpose: Implements 5th-order Runge-Kutta integration with error estimation
- Calls: `odesys->Get_State`, `odesys->Compute_Derivatives`, `odesys->Set_State`

## Globals
- **Y0** (StateVectorClass): Stores initial state vector
- **Y1** (StateVectorClass): Stores integrated state vector
- **_WorkVector0-7** (StateVectorClass): Temporary work vectors for intermediate calculations

## Dependencies
- `ode.h` (header for ODE system interface)
- `assert.h` (for debugging assertions)
- `ODESystemClass` (external class for ODE system interface)
- `StateVectorClass` (external class for vector operations)

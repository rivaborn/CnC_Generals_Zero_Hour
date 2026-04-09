# Generals/Code/Libraries/Source/WWVegas/WWMath/ode.cpp

## Purpose
Implements numerical integration methods for solving ordinary differential equations (ODEs) in the game engine.

## Responsibilities
- Provides Euler, Midpoint, Runge-Kutta 4th order, and Runge-Kutta 5th order integration methods
- Manages state vectors and work vectors for integration calculations
- Interfaces with ODESystemClass for state management and derivative computation

## Key Types
- **IntegrationSystem** (Class): Contains integration methods
- **ODESystemClass** (Class): Abstract ODE system interface (external)
- **StateVectorClass** (Class): Vector storage for ODE states and derivatives

## Key Functions
### Euler_Integrate
- Purpose: Performs Euler integration of ODE system
- Calls: sys->Get_State, sys->Compute_Derivatives, sys->Set_State

### Midpoint_Integrate
- Purpose: Implements midpoint (Runge-Kutta 2) integration method
- Calls: sys->Get_State, sys->Compute_Derivatives, sys->Set_State

### Runge_Kutta_Integrate
- Purpose: Implements 4th order Runge-Kutta integration
- Calls: sys->Get_State, sys->Compute_Derivatives, sys->Set_State

### Runge_Kutta5_Integrate
- Purpose: Implements 5th order Runge-Kutta integration with error estimation
- Calls: odesys->Get_State, odesys->Compute_Derivatives, odesys->Set_State

## Globals
- **Y0** (StateVectorClass): Stores initial state vector
- **Y1** (StateVectorClass): Stores integrated state vector
- **_WorkVector0-7** (StateVectorClass): Temporary work vectors for calculations

## Dependencies
- Key includes: "ode.h", <assert.h>
- External symbols: ODESystemClass, StateVectorClass, WWASSERT

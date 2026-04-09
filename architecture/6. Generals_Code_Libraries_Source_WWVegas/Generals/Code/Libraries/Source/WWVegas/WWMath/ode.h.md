# Generals/Code/Libraries/Source/WWVegas/WWMath/ode.h

## Purpose
Defines classes and interfaces for solving ordinary differential equations (ODEs) using various numerical integration methods.

## Responsibilities
- Provides state vector management for ODE systems
- Defines ODE system interface for derivative computation
- Implements multiple numerical integration methods (Euler, Midpoint, Runge-Kutta)
- Supports dynamic resizing of state vectors

## Key Types
- **StateVectorClass (Class)**: Dynamic vector for storing ODE state variables
- **ODESystemClass (Class)**: Abstract base class defining ODE system interface
- **IntegrationSystem (Class)**: Static class containing ODE integration methods

## Key Functions
### StateVectorClass::Reset
- Purpose: Clears the active state vector count
- Calls: None

### StateVectorClass::Resize
- Purpose: Resizes the state vector if needed
- Calls: DynamicVectorClass<float>::Resize

### ODESystemClass::Get_State
- Purpose: Virtual method to retrieve current system state
- Calls: None

### ODESystemClass::Set_State
- Purpose: Virtual method to set system state from vector
- Calls: None

### ODESystemClass::Compute_Derivatives
- Purpose: Virtual method to compute ODE derivatives
- Calls: None

### IntegrationSystem::Euler_Integrate
- Purpose: Performs Euler integration of ODE system
- Calls: ODESystemClass methods

### IntegrationSystem::Midpoint_Integrate
- Purpose: Performs midpoint integration of ODE system
- Calls: ODESystemClass methods

### IntegrationSystem::Runge_Kutta_Integrate
- Purpose: Performs 4th-order Runge-Kutta integration
- Calls: ODESystemClass methods

### IntegrationSystem::Runge_Kutta

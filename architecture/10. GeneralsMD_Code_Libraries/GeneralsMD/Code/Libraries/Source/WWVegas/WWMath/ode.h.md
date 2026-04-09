# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/ode.h

## Purpose
Defines classes and interfaces for solving ordinary differential equations (ODEs) using various numerical integration methods.

## Responsibilities
- Provides abstract base class for ODE systems
- Implements state vector management
- Offers multiple ODE integration methods (Euler, Midpoint, Runge-Kutta)
- Handles state serialization for ODE systems

## Key Types
- **StateVectorClass (Class)**: Dynamic vector for storing ODE state variables
- **ODESystemClass (Class)**: Abstract interface for ODE systems
- **IntegrationSystem (Class)**: Static class providing ODE integration methods

## Key Functions
### StateVectorClass::Reset
- Purpose: Clears the active state vector
- Calls: None

### StateVectorClass::Resize
- Purpose: Resizes the state vector if needed
- Calls: DynamicVectorClass<float>::Resize

### ODESystemClass::Get_State
- Purpose: Abstract method to retrieve current system state
- Calls: None

### ODESystemClass::Set_State
- Purpose: Abstract method to set system state from vector
- Calls: None

### ODESystemClass::Compute_Derivatives
- Purpose: Abstract method to compute ODE derivatives
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

### IntegrationSystem::Runge_Kutta5_Integrate
-

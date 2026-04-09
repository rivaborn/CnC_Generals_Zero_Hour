# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/Except.cpp

## Purpose
Handles Windows exceptions, stack walking, and symbol lookup for debugging in the SAGE engine.

## Responsibilities
- Catches and processes exceptions (e.g., access violations, stack overflows)
- Walks the call stack to generate crash reports
- Loads symbols from IMAGEHLP.DLL for debugging
- Manages thread registration for exception handling
- Provides callbacks for application-specific exception handling

## Key Types
- SymCleanupType (Function pointer): SymCleanup function from IMAGEHLP.DLL
- SymGetSymFromAddrType (Function pointer): SymGetSymFromAddr function from IMAGEHLP.DLL
- SymInitializeType (Function pointer): SymInitialize function from IMAGEHLP.DLL
- SymLoadModuleType (Function pointer): SymLoadModule function from IMAGEHLP.DLL
- SymSetOptionsType (Function pointer): SymSetOptions function from IMAGEHLP.DLL
- SymUnloadModuleType (Function pointer): SymUnloadModule function from IMAGEHLP.DLL
- StackWalkType (Function pointer): StackWalk function from IMAGEHLP.DLL
- SymFunctionTableAccessType (Function pointer): SymFunctionTableAccess function from IMAGEHLP.DLL
- SymGetModuleBaseType (Function pointer): SymGetModuleBase function from IMAGEHLP.DLL

## Key Functions
### Dump_Exception_Info
- Purpose: Dumps machine state information into a buffer for crash reports.
- Calls: Add_Txt, Last_Error_Text, LoadLibrary, GetProcAddress, _SymInitialize, _SymSetOptions, _SymLoadModule

### Exception_Handler
- Purpose: Exception handler filter function that processes exceptions.
- Calls: Dump_Exception_Info, Lookup_Symbol, Stack_Walk, AppCallback, AppVersionCallback

### Stack_Walk
- Purpose: Walks the stack and retrieves the last n return addresses.
- Calls: Load_Image_Helper, _StackWalk, _SymFunctionTableAccess, _SymGetModuleBase

### Lookup_Symbol
- Purpose: Retrieves the symbol name for a given code address.
- Calls: _SymGetSymFromAddr

### Load_Image_Helper
- Purpose: Loads IMAGEHLP.DLL and initializes symbol-related functions.
- Calls: LoadLibrary, GetProcAddress, _SymSetOptions, _SymInitialize, _SymLoadModule

## Globals
- ExceptionText (char[65536]): Buffer for dumping exception information.
- SymbolsAvailable (bool): Flag indicating if symbols are available.
- ImageHelp (HINSTANCE): Handle to IMAGEHLP.DLL.
- AppCallback (void (*)(void)): Application-specific exception callback.
- AppVersionCallback (char *(*)(void)): Application version callback.
- ExitOnException (bool): Flag to exit on exception.
- TryingToExit (bool): Flag indicating if the application is trying to exit.
- ExceptionReturnStack (unsigned long): Register dump variable for restarting.
- ExceptionReturnAddress (unsigned long): Register dump variable for restarting.
- ExceptionReturnFrame (unsigned long): Register dump variable for restarting.
- ExceptionRecursions (int): Count of exception handler recursions.
- ThreadList (DynamicVectorClass<ThreadInfoType*>): List of registered threads.
- _SymCleanup (SymCleanupType): Function pointer to SymCleanup.
- _SymGetSymFromAddr (SymGetSymFromAddrType): Function pointer to SymGetSymFromAddr.
- _SymInitialize (SymInitializeType): Function pointer to SymInitialize.
- _SymLoadModule (SymLoadModuleType): Function pointer to SymLoadModule.
- _SymSet

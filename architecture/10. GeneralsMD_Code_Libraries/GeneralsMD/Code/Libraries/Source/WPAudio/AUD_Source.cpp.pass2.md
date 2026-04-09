# GeneralsMD/Code/Libraries/Source/WPAudio/AUD_Source.cpp - Enhanced Analysis

## Architectural Role
This file is part of the WPAudio subsystem, handling low-level audio format parsing and sample management. It bridges the gap between file I/O (via `wsys/file.h`) and higher-level audio playback systems, providing format-aware seeking and MP3 header parsing.

## Cross-References
### Incoming
- Likely called by audio playback/streaming components (e.g., `AUD_Stream.cpp`) for format detection and sample creation
- Used by modding tools or audio asset pipelines for format validation

### Outgoing
- Calls into `wsys/file.h` for file operations (read, seek, position)
- Relies on `wpaudio/memory.h` for memory allocation/deallocation
- Uses `wpaudio/time.h` for timing calculations (inferred from includes)

## Design Patterns
- **Resource Pooling**: `AudioCreateSample` allocates memory for audio samples, suggesting a pool-based approach for managing audio buffers.
- **Format Strategy**: Different handling for MP3 vs. ADPCM formats indicates a strategy pattern for compression-specific operations.
- **Lookup Tables**: Precomputed `sample_rate` and `bit_rate` tables for MP3 parsing reflect a data-driven approach to format handling.

*Not inferable*: No clear use of Observer, Factory, or Visitor patterns in the provided snippet.

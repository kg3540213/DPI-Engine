# DPI Engine Project

## Overview
This project implements a Deep Packet Inspection (DPI) engine in C++. It provides tools and libraries for analyzing network traffic, extracting protocol information, and managing rules for packet inspection. The project is modular, supporting multi-threaded processing and extensibility for various network analysis tasks.

## Features
- High-performance DPI engine
- Multi-threaded packet processing
- Connection tracking
- Rule management
- SNI (Server Name Indication) extraction
- Load balancing and fast path support
- PCAP file reading and parsing

## Directory Structure
```
.
├── CMakeLists.txt           # Build configuration
├── dpi_engine/              # (Optional) Engine binaries or libraries
├── include/                 # Header files
│   ├── connection_tracker.h
│   ├── dpi_engine.h
│   ├── fast_path.h
│   ├── load_balancer.h
│   ├── packet_parser.h
│   ├── pcap_reader.h
│   ├── platform.h
│   ├── rule_manager.h
│   ├── sni_extractor.h
│   ├── thread_safe_queue.h
│   └── types.h
├── src/                     # Source files
│   ├── connection_tracker.cpp
│   ├── dpi_engine.cpp
│   ├── dpi_mt.cpp
│   ├── fast_path.cpp
│   ├── load_balancer.cpp
│   ├── main.cpp
│   ├── main_dpi.cpp
│   ├── main_simple.cpp
│   ├── main_working.cpp
│   ├── packet_parser.cpp
│   ├── pcap_reader.cpp
│   ├── rule_manager.cpp
│   ├── sni_extractor.cpp
│   └── types.cpp
├── generate_test_pcap.py    # Script to generate test PCAP files
├── output.pcap              # Example output PCAP file
├── test_dpi.pcap            # Test PCAP file
├── threaded.pcap            # Multi-threaded test PCAP file
```

## Build Instructions

### Prerequisites
- CMake (version 3.10 or higher)
- C++17 compatible compiler (e.g., GCC, Clang, MSVC)

### Build Steps
1. Clone the repository:
   ```sh
   git clone <repo-url>
   cd <project-directory>
   ```
2. Create a build directory and run CMake:
   ```sh
   mkdir build
   cd build
   cmake ..
   cmake --build .
   ```
3. The binaries will be generated in the `build` directory.

## Usage
- Run the main executable(s) generated in the build directory.
- Use the provided PCAP files or generate your own using `generate_test_pcap.py`.

## Contributing
Contributions are welcome! Please open issues or submit pull requests for improvements or bug fixes.

## License
Specify your license here (e.g., MIT, Apache 2.0, etc.).

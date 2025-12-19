# Smart Home Energy Optimizer

A comprehensive energy management system for smart homes that optimizes energy consumption, schedules device operations, and enables community energy sharing using advanced data structures and algorithms.

## Features

- **Device Management**: Register and manage smart home devices with real-time monitoring
- **Load Management**: Automatic load shedding to prevent overloads and protect critical devices
- **Scheduling System**: Priority-based scheduling for device operations to optimize energy usage
- **Usage History**: Track and query device usage history with time-based searches
- **Community Energy Sharing**: Connect with neighboring homes to share excess energy using graph algorithms
- **Data Persistence**: Automatic save/load functionality for devices and community data
- **Comprehensive Reporting**: Generate detailed reports on energy consumption, utilization, and savings

## Data Structures & Algorithms

This project demonstrates the implementation and use of several fundamental data structures:

- **HashMap**: Fast O(1) average-case lookup for device registry and graph node storage
- **Binary Search Tree (BST)**: Efficient time-based history tracking with range queries
- **Priority Queue (Heap)**: Priority-based scheduling and load management
- **Graph**: Community network representation with BFS and Dijkstra's algorithm for energy sharing

## Project Structure

```
DSA-PROJECT/
├── main.cpp                 # Application entry point
├── energy_system.h/cpp      # Main system orchestration
├── device.h                 # Device model and behavior
├── hashmap.h                # Generic HashMap implementation
├── history.h                # BST-based usage history
├── priority_queue.h         # Priority queue (heap) implementation
├── community_graph.h/cpp    # Graph algorithms for energy sharing
├── file_manager.h           # File I/O utilities
├── utils.h                  # Utility functions
└── tests/                   # Unit tests for components
    ├── test_hashmap.cpp
    ├── test_priority_queue.cpp
    ├── test_community_graph.cpp
    └── test_energy_system_basic.cpp
```

## Build & Run Instructions

### Prerequisites

- C++17 compatible compiler (g++ recommended)
- Unix-like system (macOS/Linux) or Windows with appropriate tools

### Build the Main Application

```bash
cd /path/to/DSA-PROJECT
g++ -std=c++17 main.cpp energy_system.cpp community_graph.cpp -o energy_optimizer
```

### Run the Application

```bash
./energy_optimizer
```

### Build Tests

```bash
# Build HashMap tests
g++ -std=c++17 tests/test_hashmap.cpp -o tests/test_hashmap

# Build Priority Queue tests
g++ -std=c++17 tests/test_priority_queue.cpp -o tests/test_priority_queue

# Build Community Graph tests
g++ -std=c++17 tests/test_community_graph.cpp community_graph.cpp -o tests/test_community_graph

# Build Energy System tests
g++ -std=c++17 tests/test_energy_system_basic.cpp energy_system.cpp community_graph.cpp -o tests/test_energy_system_basic
```

### Run Tests

```bash
./tests/test_hashmap
./tests/test_priority_queue
./tests/test_community_graph
./tests/test_energy_system_basic
```

## Usage

Upon running the application, you'll be presented with an interactive menu:

1. **Add Device**: Register new smart home devices with consumption rates, priority, and critical status
2. **Monitor Devices**: View real-time status of all registered devices
3. **Toggle Device**: Turn devices on/off with automatic capacity checking
4. **View Critical Devices**: List all devices marked as critical
5. **View History**: Query device usage history by time range
6. **Schedule Device**: Schedule device operations with priority-based queuing
7. **View Schedule**: Display the current scheduling queue
8. **Setup Community**: Configure community energy sharing network
9. **Request Energy**: Find optimal energy sharing paths using graph algorithms
10. **Generate Report**: Create comprehensive energy usage and optimization reports

## Key Components

### Device Management
- Devices are stored in a HashMap for O(1) average-case lookup
- Each device tracks consumption rate, status, priority, and critical flag
- Automatic energy calculation based on runtime

### History Tracking
- Binary Search Tree implementation for efficient time-based queries
- Supports range queries for usage history analysis
- Automatic timestamp tracking for all device operations

### Scheduling & Load Management
- Priority queue (min-heap) for scheduling tasks
- Automatic load shedding when capacity is exceeded
- Critical devices are protected during load shedding operations

### Community Energy Sharing
- Graph representation of homes and connections
- BFS for neighbor discovery
- Dijkstra's algorithm for finding optimal energy sharing paths
- Cost-benefit analysis for energy sharing decisions

## File Persistence

The system automatically saves and loads:
- Device registry and configurations
- Usage history
- Community network structure
- Home energy data

Data is persisted to files in the project directory and loaded automatically on startup.

## Testing

Comprehensive unit tests are provided for each major component:
- HashMap operations and collision handling
- Priority queue operations and heap properties
- Graph traversal algorithms (BFS, Dijkstra)
- System integration and load shedding logic

Run all tests to verify system functionality before deployment.

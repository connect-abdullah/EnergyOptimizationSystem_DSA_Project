## Build & Run Instructions

### 1. Go to the project directory

```bash
cd "/DSA-Project Folder"
{wherever your project is located}
```

### 2. Build the main application

```bash
g++ -std=c++17 main.cpp energy_system.cpp community_graph.cpp -o energy_optimizer
```

### 3. Run the main application

```bash
./energy_optimizer
```

---

### 4. Build all tests

```bash
g++ -std=c++17 tests/test_hashmap.cpp -o tests/test_hashmap
g++ -std=c++17 tests/test_community_graph.cpp community_graph.cpp -o tests/test_community_graph
g++ -std=c++17 tests/test_priority_queue.cpp -o tests/test_priority_queue
g++ -std=c++17 tests/test_energy_system_basic.cpp energy_system.cpp community_graph.cpp -o tests/test_energy_system_basic
```

### 5. Run all tests

```bash
./tests/test_hashmap
./tests/test_community_graph
./tests/test_priority_queue
./tests/test_energy_system_basic
```


# Thermal Conductivity in Graphs

This project simulates thermal conductivity in graph structures. The application takes a graph represented by an adjacency list, where each vertex has a user-defined temperature, and computes the heat transfer over time.

## Project Structure

```
Termal-conductivity-in-graphs/
├── CMakeLists.txt
├── data/
│   ├── input.json
│   ├── output.json
├── docs/
│   ├── README.md
│   ├── DESIGN.md
├── external/
│   ├── json/  # nlohmann/json library
│   ├── eigen/ # Eigen library
├── include/
│   ├── Controller.hpp
│   ├── Graph.hpp
│   ├── HeatTransferModel.hpp
│   ├── HeatTransferFacade.hpp
│   ├── Observer.hpp
│   ├── Subject.hpp
│   ├── View.hpp
├── python/
│   ├── visualization.py
├── src/
│   ├── main.cpp
│   ├── controller/
│   │   ├── Controller.cpp
│   ├── model/
│   │   ├── Graph.cpp
│   │   ├── HeatTransferModel.cpp
│   ├── facade/
│   │   ├── HeatTransferFacade.cpp
│   ├── observer/
│   │   ├── Observer.cpp
│   │   ├── Subject.cpp
│   ├── view/
│   │   ├── View.cpp
```

## Dependencies

This project uses the following libraries:
- [nlohmann/json](https://github.com/nlohmann/json) for JSON parsing.
- [Eigen](https://gitlab.com/libeigen/eigen) for matrix computations.

## Getting Started

### Cloning the Repository

Clone the repository and initialize submodules to get the required libraries.

```bash
git clone https://github.com/yourusername/Termal-conductivity-in-graphs.git
cd Termal-conductivity-in-graphs
git submodule update --init --recursive
```

### Building the Project

1. Make sure you have CMake and a C++ compiler installed.
2. Create a build directory and navigate to it.

```bash
mkdir build
cd build
```

3. Run CMake to configure the project and generate build files.

```bash
cmake ..
```

4. Build the project.

```bash
make
```

### Running the Simulation

After building the project, you can run the executable with the default input data:

```bash
./TermalConductivityInGraphs
```

### Input and Output Data

- The input data is stored in `data/input.json`. The format is as follows:

```json
{
  "adjacency_list": {
    "0": [1, 2],
    "1": [0, 2],
    "2": [0, 1, 3],
    "3": [2]
  },
  "temperatures": {
    "0": 100.0,
    "1": 150.0,
    "2": 200.0,
    "3": 250.0
  }
}
```

- The output data will be saved in `data/output.json` after running the simulation.

### Visualization

A Python script is provided for visualizing the results. Make sure you have `matplotlib` and `networkx` installed.

```bash
pip install matplotlib networkx
```

Run the visualization script:

```bash
python python/visualization.py
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request or open an Issue on GitHub.

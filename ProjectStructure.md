# Project Description #

Common system structure is shown on figure 1.

Figure 1. Common system structure.
Here are descriptions of each module:
1.	Marker
…
2.	Topology configurator
This module is responsible for creating network configuration description files.  The configuration file will store the following parameters: topology, node performance, latency, transfer rate. We assume to use objects associations for network topology modeling. Every network element will be represented by an object of correspondence type with its own unique identifier. Such network structure can be easily serialized to xml file. Object-oriented class structure is shown on figure 2.

Figure 2. Object-oriented class structure.
3.	Simulator
Simulator is a component for interpretation and simulation xml markup files. It will analyze xml markup data and simulate parallel program execution with the help of data exchange and routing algorithms. Data exchange simulation algorithms will be used for calculation of data exchange time between processors. The rooting algorithms are responsible for finding all open-ended roots between two defined nodes, and choosing the best one.
Component model of Simulator module is shown on Figure 3. Main responsibilities of detailed components are listed below.

Figure 3. Component model of Simulator module


Program Execution Simulator reads in turn xml nodes, analyzes control structures (e.g. conditions, loops, etc.), finds command nodes and creates correspondent object for command.  As soon as an object is created, it is sent to Execution Time Analyzer component in order to define command execution time.  Execution Time Analyzer classifies “command” objects and determines appropriate module for computing command execution times. Memory Access Emulator calculates time spending on memory access operations; Operation Execution Emulator calculates time spending on computing. Network Topology Emulator calculates data exchange time between processors. Besides, Network Topology Emulator can be integrated with GRID services resources.

4.	Optimizer
This module will optimize parallel algorithm parameters using iterative scheme. Due to nonlinear parallel programs behavior optimization module will be based on a genetic algorithm. The optimization mechanism is shown on figure 4.

Figure 4. Optimizator structure.
Input parameters for simulator are: processors number, network topology, algorithms parameters, etc. Output parameters are: execution time, network load, processors load.
We have good experience in optimizing parallel LU factorization algorithm. Using generic optimization algorithm made it possible to reduce program execution time easy.
5.	Log Visualizer

Log Visualizer will visualize log files, showing detailed information about work of parallel algorithms.  This module will make it possible to visually analyze parallel algorithms in process. Log Visualizer will be implemented as a web service and will have user web interface.
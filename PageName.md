### Summary of Project Description ###
We are working on creation of an interactive system of analysis and enhancement of parallel and distributed computing performance (DCPAES).

The purpose of the project is to improve the process of high performance software development, providing a number of online services and tools. The system will make users able to control and analyze performance of parallel and distributed applications on every phase of its development.

In this project we are concentrating on MPI standard developers, as MPI is widely used in HPC and GRID. Our next target is to support other modern parallel programming technologies and standards.

The process of interaction between user and DCPAES is planned to be the following:
> - User submits program code through web-interface.
> - DCPAES marks up the program code with XML tags containing performance valuable attributes. The user has possibility to correct markup and select parameters for automatic optimization.
> - The user creates or chooses computational environment description (CED), which is used for program simulation. The environment description includes network topology and performance parameters of nodes, or as an option, could be integrated with GRID services in future.
> - Simulation module uses resulting XML to get performance estimates and simulated execution profile.
> - DCPAES analyses hot spots of program and weak chains of computational environment.
> - Optimization algorithm (Genetic Algorithm) works with the parameters.
> - DCPAES provides the user with recommendations on program optimization, network topology improvement and hardware upgrades.

With help of hardware simulation module containing in DCPAES it is possible to estimate and improve application performance without access to the target hardware.  So DCPAES user will be able to optimize own hardware structure and parameters to suit his/her purposes the best way.

Our approach allows working with up-to-date programming systems and requires minimum effort from user.  Analysis is based on user’s program code.
As a future target of our project, customization for other distributed and high performance development technologies will be created. DCPAES will be a good toolset for Cloud Computing.

## Summary of Project Deliverables ##

We are going to implement and provide the DCPAES as a service containing the following modules.
> - Program Simulation module as a web-service
> - Network Simulator and Load Analyzer module as a web-service
> - Program Code Markup module
> - Optimization module as a web-service based on Genetic algorithm
> - Web-interface for the proposed system, including program code submitting form, network topology editor, XML marked program code presentation and editing, simulation profiling results presentation.

All system components will be well-integrated and will support program code on C/C++ programming languages and MPI standard. The system is going to be tested and verified on the common open source MPI programs and will be accessible for everyone to make experiments and use the DCPAES for own needs.
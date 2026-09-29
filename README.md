# Intelligent Traffic Management and Deadlock Prevention System


https://github.com/TAIMOURMUSHTAQ/Intelligent-Traffic-Management-OS/releases/download/v1.0.0/OS.Presentation.1.mp4
A C-based Linux simulation that demonstrates fundamental Operating System concepts through a simulated traffic management environment.

The project models vehicles as processes or concurrent entities and uses CPU scheduling, synchronization, resource allocation, deadlock management, inter-process communication, and Linux signals to demonstrate how operating system mechanisms can be applied to a real-world-inspired scenario.

## Project Overview

Traffic intersections can be viewed as shared-resource environments where multiple vehicles compete for limited resources such as lanes and intersection access.

This project maps these traffic-management problems to core Operating System concepts, providing a practical simulation of:

* Process creation and management
* CPU scheduling
* Process synchronization
* Resource allocation
* Deadlock prevention and detection
* Inter-process communication
* Linux signal handling

The system is designed to run on Ubuntu Linux using C and standard Linux/POSIX mechanisms.

## Key Features

### Process Management

* Process creation using `fork()`
* Parent-child process coordination using `wait()`
* Process timing and simulation using `sleep()`

### CPU Scheduling

The system demonstrates multiple scheduling algorithms:

* First Come First Serve (FCFS)
* Shortest Job First (SJF)
* Round Robin (RR)
* Multilevel Queue Scheduling (MQS)

Multilevel queues can represent different vehicle categories such as emergency vehicles, public transport, and regular vehicles.

### Synchronization

Synchronization mechanisms are used to control concurrent access to shared resources.

* POSIX mutexes
* Semaphores
* Critical-section protection
* Race-condition demonstration
* Shared traffic and intersection resources

### Banker’s Algorithm

The project implements Banker’s Algorithm to demonstrate safe resource allocation and avoid unsafe system states.

In the traffic simulation, resources can represent road lanes or intersection access.

### Deadlock Management

The system simulates traffic situations where processes can block one another.

It demonstrates:

* Deadlock scenarios
* Deadlock detection
* Prevention of unsafe resource allocation
* Recovery from blocked states

### Signals

Linux signals are used for process control and traffic-related events, including:

* `SIGSTOP`
* `SIGCONT`
* `SIGINT`

### Inter-Process Communication

The project demonstrates communication between processes using:

* Pipes
* Shared memory
* Message queues

## System Modules

| Module                  | Description                                          |
| ----------------------- | ---------------------------------------------------- |
| Vehicle Generator       | Creates vehicle processes                            |
| Traffic Scheduler       | Applies CPU scheduling algorithms                    |
| Synchronization Manager | Handles mutexes and semaphores                       |
| Deadlock Detector       | Detects circular waiting conditions                  |
| Banker Module           | Checks safe resource allocation                      |
| IPC Module              | Provides inter-process communication                 |
| Signal Handler          | Handles process control and emergency-related events |

## Technology Stack

| Component            | Technology                                |
| -------------------- | ----------------------------------------- |
| Programming Language | C                                         |
| Operating System     | Ubuntu Linux                              |
| Compiler             | GCC                                       |
| Thread Library       | POSIX Threads (`pthread`)                 |
| Synchronization      | Mutexes and Semaphores                    |
| IPC                  | Pipes, Shared Memory, Message Queues      |
| Interface            | Linux Terminal / ncurses where applicable |
| Virtual Environment  | VMware                                    |

## Project Structure

The exact source-file structure may vary depending on the implementation, but the project is organized around the major system modules documented above.

A typical repository layout is:

```text
intelligent-traffic-management-os/
│
├── src/
│   ├── process/
│   ├── scheduling/
│   ├── synchronization/
│   ├── deadlock/
│   ├── banker/
│   ├── ipc/
│   └── signals/
│
├── docs/
│   └── Project Documentation.pdf
│
├── presentation/
│   └── Project Presentation.mp4
│
├── README.md
└── ...
```

> Replace the example folder structure above with the actual structure of the uploaded project before publishing if the source archive uses different folders.

## Requirements

To build and run the project, you should have:

* Ubuntu Linux
* GCC
* POSIX thread support
* Standard Linux system libraries
* VMware or another Linux environment if running Ubuntu virtually

## Compilation

For a basic C program:

```bash
gcc main.c -o traffic_management
```

For programs using POSIX threads:

```bash
gcc main.c -o traffic_management -pthread
```

If the project contains multiple source files, compile them according to the source structure. For example:

```bash
gcc src/*.c -o traffic_management -pthread
```

The exact compilation command should be adjusted to match the final source files included in the repository.

## Running the Project

After compilation:

```bash
./traffic_management
```

The program provides terminal-based interaction for demonstrating the implemented operating system concepts.

## Demonstrated Concepts

The project brings several Operating System concepts together in one simulation:

```text
                 Intelligent Traffic System
                           |
          +----------------+----------------+
          |                |                |
     Process Mgmt      Scheduling      Synchronization
          |                |                |
       fork()        FCFS / SJF / RR     Mutex
       wait()             / MQS          Semaphore
          |                |                |
          +----------------+----------------+
                           |
                  Resource Management
                           |
              +------------+------------+
              |                         |
        Banker's Algorithm        Deadlock Management
              |                         |
              +------------+------------+
                           |
                    Process Communication
                           |
                    IPC + Linux Signals
```

## Expected Demonstrations

The project documentation includes demonstrations of:

* Main system menu
* FCFS scheduling
* SJF scheduling
* Round Robin scheduling
* Round Robin execution and Gantt chart
* Multilevel Queue Scheduling
* Mutex and semaphore synchronization
* Race-condition results
* Banker’s Algorithm
* Banker’s Algorithm results
* Deadlock simulation
* IPC demonstrations
* Vehicle information table
* Project completion state

## Documentation

Detailed project documentation is included in the repository and covers the system design, Operating System concepts, modules, requirements, development methodology, feasibility analysis, testing visuals, and references.

See:

```text
docs/Project Documentation.pdf
```

## Project Presentation

A video presentation demonstrating the project is included in the repository.

See:

```text
presentation/Project Presentation.mp4
```

## Development Methodology

The project follows an incremental development approach in which individual modules are developed and tested separately.

The documented development sequence covers:

1. Project setup and planning
2. Process creation
3. CPU scheduling algorithms
4. Mutex and semaphore implementation
5. Banker’s Algorithm and deadlock handling
6. IPC and signal handling
7. Testing and debugging
8. Documentation and presentation

## Future Enhancements

Potential future improvements include:

* Graphical user interface
* AI-based traffic optimization
* Network-based distributed traffic management
* Real-time sensor integration
* Database connectivity

## Learning Outcomes

This project provides practical experience with:

* Linux system programming
* C programming
* Process management
* CPU scheduling
* Concurrent programming
* Synchronization
* Resource allocation
* Deadlock management
* Inter-process communication
* Linux signals
* POSIX threads

## References

The project documentation references the following resources:

1. *Operating System Concepts* Abraham Silberschatz
2. *Advanced Programming in the UNIX Environment*  W. Richard Stevens
3. Linux Manual Pages
4. GNU GCC Documentation
5. POSIX Thread Programming Guide
6. Ubuntu Linux Documentation

## Academic Project

Developed as an Operating Systems project for the Department of Computer Science, Federal Urdu University of Arts, Science and Technology, Islamabad.
Under kind supervision of *Ms. Kinza Naseer*

**Semester:** 4th
**Section:** A
**Year:** 2026

### Contributors

* Taimour Mushtaq (Project Lead)
* Hafiz Muhammad Abdullah Idrees (Documentation)
* Abdur Rahman (Project Analysis)
* Zahid Ali Akbar (Support)

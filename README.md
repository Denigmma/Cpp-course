# Cpp-course


# ***Lab Work №1. Loading and Processing Raster Images***

## Objective
1. Learn how images are interpreted during computer processing.
2. Understand how image storage in memory correlates with human perception.
3. Study the BMP image format.
4. Learn to load data from files into memory.
5. Master manipulating data in memory: modifying and rearranging it.
6. Learn to save images.


## Input Data
### Complexity Levels:
- **Level A+**: A color raster image in BMP format.
- **Level A**: A grayscale raster image in BMP format with 8-bit depth.
- **Level B**: A grayscale raster image with 8-bit depth in a "raw" format (file contains only pixel intensities, stored row by row; image dimensions are provided).

## Tasks
1. Determine the amount of memory required to load the image.
2. Load the image into memory.
3. Rotate the image 90° clockwise and save the result.
4. (Optional) Rotate the image 90° counterclockwise and save the result.
5. Apply a Gaussian filter to the rotated image and save the result.

**Note:**
- For Level A+ and A, the results must be saved in BMP format.
- For Level B, results can be saved in either "raw" format or BMP.

## Constraints
The lab work must be implemented using the C++ Standard Library ([cppreference.com](https://cppreference.com)).

## Grading Criteria
### Level A+
- The program meets all the following requirements:
  1. Demonstrates results for tasks 3, 3', and 4.
  2. Executes in real time.
  3. Allocates no more than 200% of the memory required to store the original image and has no memory leaks.

### Level A
- One or two criteria from Level A+ are partially achieved:
  1. Demonstrates results for task 4, but results for tasks 3 or 3' are missing.
  2. Executes within 3 minutes.
  3. Allocates no more than 250% of the memory required to store the original image and has no memory leaks.

### Level B
- One or two criteria from Level A are achieved with inaccuracies:
  1. Demonstrates results only for tasks 3 or 3'.
  2. Executes within 6 minutes.
  3. Allocates more than 250% of the required memory but has no memory leaks.

### Level D
- Demonstrates results for tasks 3, 3', and 4, but the program does not meet the time or memory criteria of Level C.

### Level E
- Same as Level D, but results for task 4 are missing.


# ***Lab Work №2. Console Game with Game Core***

## Project Description
This project involves the implementation of a console-based game by developing a game engine (Game Core). The primary objective was to create a program structure that showcases fundamental and advanced object-oriented programming (OOP) skills in C++.

## Project Objectives
- **Develop a Game Engine**: Create a game core that manages game objects and their interactions.
- **Demonstrate OOP Skills**:
  - **Classes and Inheritance**: Utilize classes to model game entities and employ inheritance to establish hierarchies.
  - **Encapsulation**: Use `private` and `public` access specifiers to protect data and expose necessary interfaces.
  - **Getters and Setters**: Implement getter and setter methods for safe access and modification of class members.
  - **Polymorphism**: Demonstrate polymorphic behavior by interacting with different objects through base class pointers or references.
- **Architectural Design**: Build a robust architecture adhering to OOP principles to ensure scalability and maintainability.

## Project Features

1. **Game Core**:
   - **Basic Game Logic**: Implements essential game mechanics and rules.
   - **Object Management**: Handles the creation, state management, and interaction of game objects.
   - **Modularity and Flexibility**: Designed to allow easy addition of new features and game elements.

2. **Architecture and OOP**:
   - **Class Modeling**: Uses classes to represent various game objects and their behaviors.
   - **Inheritance Hierarchies**: Establishes base and derived classes to promote code reuse and logical organization.
   - **Data Encapsulation**: Protects class members using `private` or `protected` access and provides `public` methods for interaction.
   - **Polymorphic Interactions**: Enables handling of different object types through a unified interface.

3. **Getters and Setters**:
   - **Private Members**: All class attributes are kept private to ensure data integrity.
   - **Accessor Methods**: `get` and `set` methods are provided to safely access and modify private data members.

4. **Game Mechanics**:
   - **Initialization**: Sets up the initial state of the game, including player and enemy positions.
   - **Game Loop**: Continuously updates the game state, processes player input, and handles enemy actions.
   - **Win/Lose Conditions**: Checks for game-ending conditions based on defined criteria.

5. **Console Interface**:
   - **User Interaction**: Facilitates player input and displays game state information through the console.
   - **Interactive Gameplay**: Provides a responsive and engaging experience within the console environment.

## Main Components

1. **Game Core Classes**:
   - **GameObject**: 
     - *Description*: The base class for all game entities.
     - *Attributes*: Common properties such as coordinates and state.
     - *Methods*: Virtual methods for interaction and behavior.
   
   - **Player**:
     - *Description*: Represents the player character.
     - *Inheritance*: Inherits from `GameObject`.
     - *Methods*: Implements player-specific actions and controls.
   
   - **Enemy**:
     - *Description*: Represents enemy characters.
     - *Inheritance*: Inherits from `GameObject`.
     - *Methods*: Defines enemy behaviors, movements, and attack patterns.
   
   - **GameEngine**:
     - *Description*: Manages the overall game state and flow.
     - *Responsibilities*: Updates game objects, processes events, and maintains game logic.

2. **Use of Getters and Setters**:
   - **Health Management**:
     - `getHealth()` / `setHealth(int health)`: Access and modify the health of game objects.
   - **Position Management**:
     - `getPosition()` / `setPosition(int x, int y)`: Retrieve and update the coordinates of game objects.
   - **Additional Accessors**: Methods to access other private attributes as needed.

3. **Game Logic**:
   - **Object Initialization**: Sets up game objects with initial states and positions.
   - **State Updates**: Continuously updates the state of the game through a loop, handling player turns and enemy actions.
   - **Condition Checks**: Evaluates win or lose conditions to determine the end of the game.

# ***Lab Work №3.  Deterministic Finite Automaton (DFA)***

## Project Description
This project implements a **Deterministic Finite Automaton (DFA)**—a basic computational model used to process and validate input strings. The program accepts input defining the structure of the automaton and checks whether a given string can lead from the initial state to a terminal state while following the defined transitions.

## Project Goals
- Develop an efficient DFA implementation using **C++**.
- Demonstrate skills in algorithm and data structure design.
- Implement the logic for DFA processing, including validation of transitions and string acceptance.
- Provide a user-friendly way to define the automaton's structure.

## Features
- **Alphabet**: A set of symbols that the automaton can recognize.
- **Terminal States**: States where the automaton must end after processing the string.
- **Transition Rules**: A set of rules defining state transitions based on input symbols.
- **Initial State**: The starting state of the automaton.
- **Input String**: A sequence of symbols to be validated by the automaton.

## Input Format
1. **Automaton Definition**:
   - **Alphabet**: A list of valid symbols.
   - **Terminal States**: A set of valid terminal states.
   - **Transition Rules**: Each rule is defined as a triplet `(current state, symbol, next state)`.

2. **String Processing**:
   - The input string consists of symbols from the alphabet.
   - The automaton verifies whether it can transition from the initial state to a terminal state by following the defined rules.

### Example Input

Alphabet: a, b Terminal States: S2 Initial State: S1 Transition Rules: S1 a S2 S2 b S1 Input String: ab

### Program Output
- **Success**: If the automaton reaches a terminal state, it outputs a confirmation.
- **Failure**: If the automaton cannot reach a terminal state or encounters an invalid transition, it outputs an error.



# ***Lab Work №4. Graph Visualization***

## Objective
1. Gain practical experience with the concept of graphs and their representations.
2. Learn to convert between different graph representations.
3. Master the creation of raster images.

## Input Data
The program takes as input a file containing a list of graph edges in the following format:
1. **V E** – the first line specifies the number of vertices and edges.
2. **u v** – each of the following E lines specifies an edge as a pair of vertex numbers.

### Complexity Levels
- **Level A**: The number of vertices ≤ 500. The graph can be arbitrary.
- **Level B**: The number of vertices ≤ 1000. The graph is planar.
- **Level C**: The number of vertices ≤ 500. The graph is planar.
- **Level D**: The number of vertices ≤ 1000. The graph is a tree.
- **Level E**: The number of vertices ≤ 500. The graph is a tree.

## Task
Develop a program to generate images of undirected graphs defined by an edge list. The program must:
1. Handle input data for the declared complexity level and below correctly.
2. Generate images with minimal edge crossings.
3. Meet the following visual requirements:
   - Vertices are displayed as circles with a diameter of 7–10 pixels.
   - Vertices are labeled with text using a 12-point font size.
   - Edge lengths are at least 30 pixels.
   - The graph is evenly distributed across the image.
   - The image format is BMP.
   - Overlaps of vertices and edges are minimized.
   - Adjacent vertices are placed close to each other, and non-adjacent vertices are far apart.

4. Use **CMake** to generate the build script.
5. Follow the **Google Code Style** guidelines.

## Constraints
The lab work must be implemented exclusively using the C++ Standard Library ([cppreference.com](https://cppreference.com)).

## Grading Criteria
The program must meet all the specified requirements. The final grade is determined by the complexity level of the input data:
- **Level A**: Basic.
- **Levels B, C, D, E**: Higher complexity, graded accordingly.


# ***Lab Work №5.  Multithreaded Server Implementation***

## Objective
Develop and test a simple multithreaded server capable of handling substantial requests effectively.

## General Requirements
1. **Define a Meaningful Context**: 
   - Propose a scenario for the server where it will experience high load, either in terms of request complexity or volume.
   - Agree on the scenario with the instructor.

2. **Design the Architecture**:
   - Outline the application’s architecture in text or diagram form.
   - Choose the tools and technologies required for implementation.
   - Submit the design for approval.

3. **Server Implementation**:
   - Develop a multithreaded server capable of dispatching and executing requests in parallel.
   - Ensure the most computationally demanding parts of the server are implemented in parallel.
   - Synchronize thread operations to avoid race conditions and deadlocks in critical sections.

4. **Load Testing**:
   - Design and implement a testing framework to simulate server load.
   - Conduct performance testing to evaluate the server under heavy load.

5. **Coding Standards**:
   - The implementation must adhere to the **Google Code Style**.

## Grading Criteria
- **Grade E**: 
  - Implement the server with two physical threads.
  - Conduct local testing.
- **Grade D**: 
  - Implement the server with more than two physical threads.
  - Conduct local testing.
- **Grade C**: 
  - Implement the server with two physical threads.
  - Conduct online testing.
- **Grade B**: 
  - Implement the server with more than two physical threads.
  - Conduct online testing.
- **Grade A**: 
  - Implement the server with more than two physical threads.
  - Enable the use of the maximum available number of threads.
  - Conduct online testing.

## Notes
- The server must handle requests in a **thread-safe manner**.
- **Critical sections** must be synchronized to prevent race conditions and deadlocks.
- The application should be stress-tested to evaluate its performance under high load conditions.

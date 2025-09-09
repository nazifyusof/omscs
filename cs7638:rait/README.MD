# CS7646: Robotics AI Techniques

## Techniques Covered
- **Probabilistic Inference & Filtering**
    - **Histogram Filters**  
      Represent the state space as a grid of bins, each holding a probability of the robot’s position.
        - Good for discrete environments (e.g., warehouse grid).
        - Simple but computationally heavy for large spaces.

    - **Kalman Filters**  
      Assume the robot’s state and noise follow Gaussian distributions.
        - Use prediction (motion model) + update (sensor model) steps.
        - Efficient and elegant for **linear, Gaussian** systems.
        - Example: tracking asteroid motion with noisy sensor readings.

    - **Particle Filters**  
      Represent belief as a set of weighted particles, approximating complex distributions.
        - Flexible: works with **nonlinear, non-Gaussian** systems.
        - Example: localizing a spaceship in a solar system using noisy gravitational data.

- **Planning & Search Algorithms**
    - **Dijkstra’s Algorithm**  
      Expands nodes in order of path cost → guarantees shortest path.
        - Comprehensive but can explore too much.

    - **A\* Search**  
      Improves on Dijkstra’s by using a **heuristic** to guide search.
        - Finds shortest path more efficiently.
        - Widely used in robotics for pathfinding.

- **Control**
    - **PID Control (Proportional–Integral–Derivative)**  
      A feedback controller that adjusts actions based on error (difference between desired and actual state).
        - Proportional: responds to current error.
        - Integral: accounts for past error.
        - Derivative: anticipates future error.
        - Example: stabilizing a drone in hover mode.

- **Path Smoothing**
    - Raw search paths (Dijkstra’s, A*) are jagged and unnatural.
    - Path smoothing optimizes them into smooth trajectories for real robots.
    - Improves efficiency and safety of motion.

- **SLAM (Simultaneous Localization and Mapping)**
    - Problem: a robot must **map an unknown environment** while also figuring out **where it is**.
    - Uses sensor data + motion models + probabilistic inference.
    - **GraphSLAM**: represents the problem as a graph of poses and constraints, solved with optimization.
    - Essential for autonomous navigation in unknown worlds.
## Projects
- **Project 1: Warehouse Search**
    - Implement path search in a 2D grid using Dijkstra’s and A*.
    - Learn about optimality, heuristics, and pathfinding efficiency.

- **Project 2: Asteroid Navigation**
    - Use **Kalman filters** to track and predict asteroid positions.
    - Navigate a spaceship safely through space.

- **Project 3: Particle Filter Localization**
    - Apply **particle filters** for non-parametric localization in a noisy solar system environment.

- **Project 4: Drone PID Control**
    - Implement a **PID controller** to stabilize and control a quadcopter drone.

- **Project 5: SLAM (Simultaneous Localization and Mapping)**
    - Build and visualize a **GraphSLAM** system.
    - Localize while simultaneously mapping the environment.ld and visualize simultaneous mapping & localization
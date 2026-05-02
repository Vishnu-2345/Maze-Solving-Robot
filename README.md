# 🤖 Autonomous Maze Solving Robot (TurtleBot3)

An autonomous robotics project that enables a TurtleBot3 robot to navigate through a maze using intelligent path planning and ROS2-based navigation.

---

## 📌 Overview

Autonomous navigation in unknown environments is a key challenge in robotics. Traditional maze-solving approaches such as random exploration or wall-following are inefficient and unreliable.

This project solves that problem using:

- 🧠 A* Pathfinding Algorithm (optimal path)
- 🤖 ROS2 (robot middleware)
- 🗺️ SLAM (real-time mapping)
- 🚗 Navigation2 Stack (autonomous navigation)
- 🌍 Gazebo Simulator (3D simulation)
- 📊 RViz2 (visualization)

The robot successfully navigates from a start point to a goal without prior knowledge of the optimal path.

---

## 🎯 Objectives

- Implement fully autonomous maze navigation
- Use A* algorithm to compute shortest path
- Integrate ROS2 + Navigation2 stack
- Enable real-time mapping using SLAM
- Visualize robot behavior in Gazebo & RViz2
- Ensure collision-free navigation

---

## ⚙️ Tech Stack

| Tool | Purpose |
|------|--------|
| ROS2 (Humble) | Robotics middleware |
| Navigation2 | Autonomous navigation |
| Python3 | Programming |
| SLAM Toolbox | Mapping |
| Gazebo Classic | Simulation |
| RViz2 | Visualization |

---

## 🧠 Methodology

### 🔹 A* Pathfinding Algorithm

- Uses:
  - `g(n)` → cost from start
  - `h(n)` → heuristic to goal
  - `f(n) = g(n) + h(n)`
- Guarantees shortest path
- Efficient and widely used in robotics

### 🔹 AMCL Localization
- Uses particle filters
- Estimates robot position accurately
- Handles uncertainty

### 🔹 DWB Local Planner
- Generates safe velocity commands
- Avoids obstacles in real-time

---

## 🚀 How It Works

1. Robot starts in maze environment
2. SLAM builds a 2D map
3. A* computes optimal path
4. Navigation2 executes movement
5. RViz2 visualizes path + robot state
6. Robot reaches goal autonomously

---

## 🛠️ Setup & Installation

### 1. Clone Repository
```bash
git clone https://github.com/Vishnu-2345/Maze-Solving-Robot.git
cd Maze-Solving-Robot
### 🔹 2. Install Dependencies

Make sure ROS2 and required packages are installed.

```bash
sudo apt update
rosdep update
rosdep install --from-paths src --ignore-src -r -y
### 🔹 3. Build Workspace

```bash
colcon build
### 🔹 4. Source Workspace

```bash
source install/setup.bash
### 🔹 5. Launch Simulation

```bash
ros2 launch autonomous_tb3 tb3_maze_navigation.launch.py
### 🔹 6. Run Maze Solver

Open a **new terminal**:

```bash
source install/setup.bash
ros2 run autonomous_tb3 maze_solver.py
### 🔹 7. Expected Output

- Robot navigates maze autonomously  
- Shortest path computed using A*  
- Real-time visualization in RViz2  
- Simulation running in Gazebo  

# Dynamic Pathfinding Agent
Got it! You want your **new project “Dynamic Pathfinding Agent”** with **A* and Greedy Best-First Search** to have a README and documentation structure similar to your **previous “Blind Grid Search” project**—professional, detailed, and visually appealing, including GUI, dynamic obstacles, metrics, and usage instructions. I can help you craft that. Here's a fully updated version for your new project:

---

<div align="center">

**🤖 Dynamic Pathfinding Agent with A* & Greedy Best-First Search**

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org)
[![Tkinter](https://img.shields.io/badge/Tkinter-GUI-green.svg)](https://docs.python.org/3/library/tkinter.html)
[![License](https://img.shields.io/badge/License-Educational-green.svg)](#license)
[![GitHub](https://img.shields.io/badge/GitHub-NaeemUlRehman-blue.svg)](https://github.com/NaeemUlRehman)

</div>

---

## Overview

This project implements a **dynamic pathfinding agent** capable of navigating a grid environment with obstacles. It supports **A* and Greedy Best-First Search (GBFS)** algorithms, featuring **dynamic obstacle spawning**, **real-time GUI visualization**, and a **metrics dashboard**.

**Key Features:**

* 🟢 Start and goal positioning with interactive grid editing
* ⚫ Obstacles: static or dynamic (spawn during movement)
* 🔀 Two search algorithms: A* and GBFS
* 📏 Heuristics: Manhattan and Euclidean distances
* 🎨 Real-time GUI using Tkinter
* 📊 Metrics: nodes visited, path cost, and execution time
* 🔄 Automatic re-planning when obstacles block the path

---

## Quick Start

```bash
# 1. Clone the repository
git clone https://github.com/NaeemUlRehman/Dynamically-Path-Finding-Agents.git
cd Dynamically-Path-Finding-Agents

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the application
python3 main.py
```

**Note:** Ensure `python3-tk` is installed:

```bash
sudo apt install python3-tk
```

---

## GUI Controls

| Control                        | Description                                   |
| ------------------------------ | --------------------------------------------- |
| **Algorithm dropdown**         | Choose between A* and GBFS                    |
| **Heuristic dropdown**         | Choose Manhattan or Euclidean distance        |
| **Dynamic Obstacles checkbox** | Enable random obstacles during agent movement |
| **Run button**                 | Find and display the path                     |
| **Reset button**               | Clear grid and restart                        |
| **Click on grid cells**        | Toggle obstacles on/off                       |

---

## Color Guide

| Color  | Meaning     |
| ------ | ----------- |
| Orange | Start point |
| Green  | Goal point  |
| Black  | Obstacle    |
| Yellow | Path found  |
| White  | Empty cell  |

---

## Algorithms Implemented

### 1. **A***

* **Strategy:** Best-first search considering cost so far + heuristic
* **Heuristics:** Manhattan or Euclidean
* **Optimality:** ✓ Optimal if heuristic is admissible
* **Completeness:** ✓ Yes

### 2. **Greedy Best-First Search (GBFS)**

* **Strategy:** Selects node closest to goal according to heuristic
* **Heuristics:** Manhattan or Euclidean
* **Optimality:** ✗ Not guaranteed
* **Completeness:** ✗ May fail in some obstacle configurations

---

## Dynamic Obstacles

* Random obstacles appear during agent movement if enabled
* Agent **re-plans automatically** when path is blocked
* Obstacle spawn probability configurable (0.0 - 1.0)

**Example Scenario:**

```
Step 1: Node (5,5) added to path
Step 3: Obstacle spawns at (5,5)
Step 4: Agent detects obstacle, re-plans path
Step 5: Agent continues toward goal
```

---

## Performance Metrics

Metrics tracked in real-time:

* **Nodes Visited** – Total number of nodes explored
* **Path Cost** – Number of steps in the path
* **Execution Time** – Time taken to find path

---

## Configuration

```python
from agent.agent import Agent
from grid.grid import Grid
from algorithms.astar.astar import AStar
from algorithms.gbfs.gbfs import GBFS
from gui.gui import GUI

grid = Grid(width=30, height=30, start=(0,0), goal=(29,29), num_obstacles=50)
agent = Agent(grid)
gui = GUI(grid, agent)

# Run GUI main loop
gui.run()
```

### Recommended Settings

| Grid Size | Obstacles | Dynamic Probability |      |
| --------- | --------- | ------------------- | ---- |
| Small     | 20×20     | 10                  | 0.01 |
| Medium    | 30×30     | 50                  | 0.02 |
| Large     | 50×50     | 250                 | 0.05 |

---

## Project Structure

```
Dynamically-Path-Finding-Agents/
├── main.py                  # Entry point
├── grid/
│   ├── grid.py              # Grid class
│   ├── map_generator.py     # Random obstacle generation
│   └── editor.py            # Toggle obstacles
├── algorithms/
│   ├── heuristics.py        # Manhattan & Euclidean heuristics
│   ├── astar/
│   │   └── astar.py         # A* algorithm
│   └── gbfs/
│       └── gbfs.py          # GBFS algorithm
├── agent/
│   └── agent.py             # Agent movement & logic
├── gui/
│   └── gui.py               # Tkinter GUI visualization
├── metrics/
│   └── metrics.py           # Tracks nodes, path cost, time
└── requirements.txt         # Dependencies
```

---

## Troubleshooting

**Issue:** GUI doesn’t start
**Solution:** Install `python3-tk`

**Issue:** Path not found
**Solution:** Ensure start/goal not blocked and enough space exists

**Issue:** Algorithm very slow
**Solution:** Reduce grid size or number of obstacles, disable visualization

---

## License

Educational Use Only – Free to learn, modify, and distribute

---

## Author

**Naeeem Ul Rehman**
GitHub: [@NaeemUlRehman](https://github.com/https://github.com/NaeemUlRehman))

---

This version mirrors the **professional style** of your previous “Blind Grid Search” README: detailed, structured, with GUI, metrics, dynamic obstacles, algorithm details, and visual color guide.


---


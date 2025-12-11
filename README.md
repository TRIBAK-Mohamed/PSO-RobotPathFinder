# 🤖 PSO-RobotPathFinder

![Project Status](https://img.shields.io/badge/status-active-success.svg)
![Python Version](https://img.shields.io/badge/python-3.8%2B-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

## 📖 Overview

**PSO-RobotPathFinder** is an intelligent navigation framework designed to solve complex robotic path planning challenges using **Particle Swarm Optimization (PSO)**. 

This project goes beyond simple A* or Dijkstra implementations by using evolutionary algorithms to generate **continuous, smooth, and kinematically feasible cubic spline paths**. It effectively balances the trade-off between path shortness and safety margins, ensuring robots can navigate narrow corridors and obstacle-rich environments without collision.

Ideal for autonomous mobile robot (AMR) researchers, students, and developers looking for a Python-based, visualized approach to path optimization.

## ✨ Key Features

-   **🧠 particle Swarm Optimization (PSO)**: Efficient global search algorithm for finding optimal control points.
-   **📐 Cubic Spline Smoothing**: Generates kinematically feasible and smooth paths suitable for real-world robot navigation.
-   **🖥️ Interactive Streamlit Dashboard**: A powerful web-based UI for real-time parameter tuning, environment configuration, and visual debugging.
-   **🚧 Dynamic Environment Modeling**: Supports adjustable workspace dimensions, start/goal positions, and custom circular obstacles.
-   **⚡ Real-time Visualization**: Live feedback of the optimization process, showing particle convergence and path evolution.

## 🛠️ Installation

### Prerequisites

Ensure you have Python 3.8+ installed.

### 1. Clone the Repository

```bash
git clone https://github.com/TRIBAK-Mohamed/PSO-RobotPathFinder.git
cd PSO-RobotPathFinder
```

### 2. Install Dependencies

It is recommended to use a virtual environment.

```bash
pip install -r requirements.txt
# OR manually:
pip install numpy matplotlib scipy streamlit
```

## 🚀 Usage

### Option A: Interactive Web App (Recommended)

Launch the Streamlit dashboard for a full interactive experience.

```bash
streamlit run streamlit.py
```

**Dashboard Capabilities:**
*   **Environment Setup:** Adjust width, height, and robot radius.
*   **Obstacle Editor:** Add, remove, or modify obstacles dynamically.
*   **PSO Tuning:** Fine-tune `c1`, `c2`, `inertia`, and `population size` on the fly.
*   **Visualization:** Watch the solver converge in real-time.

### Option B: Desktop Demo

Run the standalone Matplotlib demo for a quick test without the web interface.

```bash
python main.py
```

## 🧩 Project Architecture

The codebase is modular and organized for scalability:

| File/Module | Description |
| :--- | :--- |
| `streamlit.py` | Main entry point for the interactive web application. |
| `pso.py` | Core implementation of the Particle Swarm Optimization algorithm. |
| `main.py` | Lightweight desktop demo script. |
| `path_planning/` | **Core Logic Package** |
| ├── `solution.py` | Handles Cubic Spline generation and path interpolation. |
| ├── `environment.py` | Defines the workspace bounds and obstacle properties. |
| ├── `cost.py` | Computes the fitness function (Path Length + Collision Penalty). |
| └── `plots.py` | Visualization utilities for Matplotlib. |

## ⚙️ Configuration & Tuning

To achieve the best results, you can tune the PSO hyperparameters:

*   **Population Size**: Higher values improve search thoroughness but increase computation time.
*   **Inertia Weight (`w`)**: Controls the momentum of particles. Higher `w` favors exploration; lower `w` favors exploitation.
*   **Coefficients (`c1`, `c2`)**: Balance the particle's tendency to follow its own best position (`c1`) vs. the swarm's global best (`c2`).

## 🤝 Contributing

Contributions are welcome! Please fork the repository and submit a pull request for any enhancements or bug fixes.

---

<p align="center">
  Made with ❤️ by <strong>TRIBAK Mohamed</strong><br>
  📧 <a href="mailto:mohamedtribak912@gmail.com">mohamedtribak912@gmail.com</a>
</p> without formatting artifacts

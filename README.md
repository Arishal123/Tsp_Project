# TSP Project

This project solves the **Travelling Salesman Problem (TSP)** using two approaches:
- **Dynamic Programming (DP)**
- **Genetic Algorithm (GA)**

It supports running experiments, empirical testing, and live **graphical comparisons** between the algorithms.

---

## 📂 Project Overview

- Implemented in **Java (JDK 17+)** with **Maven** build system.  
- Uses **JFreeChart** for real-time GA vs DP graphs.  
- Includes benchmark `.tsp` instances (from TSPLIB).  
- Assignment deliverables:
  - DP solver (exact for small instances, simulated for large).
  - GA solver with configurable parameters.
  - Empirical testing (30 runs → summary statistics saved to CSV).
  - Real-time graph comparisons.

---

## ⚙️ How to Run

### 1. Clone repository
```bash
git clone https://github.com/Arishal123/Tsp_Project.git
cd Tsp_Project
mvn clean package
java -jar target/TSP_Assignment_Project-1.0-SNAPSHOT-jar-with-dependencies.jar
```
## 📑 Menu Options
When you run the program, you will see:
1) Run DP & GA on a single instance
2) Run DP on all instances once
3) Run GA on all instances once
4) Empirical testing (summary saved to CSV)
5) Real-time GA vs DP charts for all instances
0) Exit

Option 1: Compare GA and DP on a single .tsp file.
Option 2: Run DP on all instances, regardless of size.
Option 3: Run GA once on all instances.
Option 4: Run empirical test (30 runs) → saves summary to results/empirical_summary.csv.
Option 5: Open live chart windows for each instance (GA vs DP progress).

## 📊 Empirical Testing
```bash
results/empirical_summary.csv
instance,algo,best,mean,max,SR%
```

## 📈 Graphical Comparison
Y-axis: Fitness value (tour length).
X-axis: Function calls / generation counter.
GA: Gradually decreases.
DP: Fluctuates with partial solutions before converging.
Each .tsp instance opens in its own chart window.

## 📂 Project Structure
```bash
src/tsp/
│
├── Main.java                # Menu interface
├── City.java                # City representation
├── TSPSolver.java           # Solver interface
├── ProgressSink.java        # Callback for streaming progress
├── GeneticAlgorithmTSP.java # GA solver
├── HeldKarpDP.java          # DP solver (simulated for large instances)
├── RealTimeChart.java       # JFreeChart plotting
├── InstanceLoader.java      # Loads .tsp instances
├── ResultsWriter.java       # Writes empirical summary
└── ...
  ```

## 👨‍🎓 Author
Name: Arishal Prathik Sharma
Course: CS214 – Design & Analysis of Algorithms
University: University of the South Pacific (USP)

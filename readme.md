# UTP Artificial Intelligence

This repository contains my lab activities, implementations, and experiments for the Artificial Intelligence course at Universiti Teknologi PETRONAS (UTP).

The labs cover different Artificial Intelligence concepts and techniques, with practical implementations using Python.

## Course Information

- **Course:** TEB2023 Artificial Intelligence
- **University:** Universiti Teknologi PETRONAS (UTP)
- **Programming Language:** Python
- **Tools:** Jupyter Notebook, NumPy, Pandas, Matplotlib

## Lab Activities

| Lab | Topic | Status |
|---|---|---|
| Lab 01 | Uninformed Search | Completed |
| Lab 02 | Informed Search | Completed |
| Lab 03 | Search Engineering | Completed |
| Lab 04 | To be updated | Coming Soon |
| Lab 05 | To be updated | Coming Soon |
| Lab 06 | To be updated | Coming Soon |
| Lab 07 | To be updated | Coming Soon |
| Lab 08 | To be updated | Coming Soon |

## Lab 01: Uninformed Search

### Overview

This lab explores uninformed search algorithms using an airline network. Airports are represented as nodes, while flight routes represent connections between airports.

The objective is to find routes between airports using different search algorithms and compare their performance.

### Algorithms Implemented

- **Breadth-First Search (BFS):** Explores nodes level by level and finds a path with the fewest edges in an unweighted graph.
- **Depth-First Search (DFS):** Explores one branch as deeply as possible before backtracking.
- **Uniform-Cost Search (UCS):** Expands the node with the lowest accumulated path cost.

### Performance Comparison

The algorithms are evaluated using the following metrics:

- **Number of Hops:** Number of edges or flight connections in the resulting path.
- **Path Cost:** Total cost of travelling along the selected route.
- **Nodes Expanded:** Number of nodes explored during the search.
- **Maximum Frontier Size:** Largest number of nodes waiting to be explored.
- **Runtime:** Time taken to execute the search algorithm.

### Dataset

The airline network uses the following datasets:

- `lab01-03_airports.csv`
- `lab01-03_routes.csv`

These datasets contain airport and route information used to construct the search graph.

## Lab 02: Informed Search

### Overview

This lab explores informed search algorithms using the airline network. Unlike uninformed search, informed search uses heuristic information to guide the search towards a goal.

The lab focuses on using estimated distances between airports to guide route finding.

### Topics Covered

- Heuristic search
- Greedy Best-First Search (GBFS)
- A* Search
- Haversine distance as a heuristic
- Heuristic evaluation
- Search performance comparison

### Objectives

- Implement informed search algorithms for the airline network.
- Use heuristic information to guide the search process.
- Compare informed search algorithms with uninformed search methods.
- Evaluate search performance using relevant metrics.

### Dataset

The lab uses the airline network datasets:

- `lab01-03_airports.csv`
- `lab01-03_routes.csv`

## Lab 03: Search Engineering

### Overview

This lab focuses on developing and organizing search algorithms into a more structured and reusable implementation.

It builds on the search techniques explored in earlier labs by emphasizing software organization, testing, command-line execution, and performance benchmarking.

### Topics Covered

- Search algorithm implementation
- Code organization and modularity
- Automated testing
- Command-line interface (CLI)
- Search algorithm benchmarking
- Performance evaluation

### Objectives

- Organize search algorithms into reusable components.
- Test the correctness of search implementations.
- Support running search algorithms through a command-line interface.
- Benchmark search algorithms using multiple queries.
- Compare algorithm performance using experimental results.

### Dataset

The lab uses the airline network datasets:

- `lab01-03_airports.csv`
- `lab01-03_routes.csv`

## Repository Structure

```text
UTP-Artificial-Intelligence/
│
├── all_datasets/
│   ├── lab01-03_airports.csv
│   ├── lab01-03_routes.csv
│   ├── lab04-AirQuality.csv
│   ├── lab05-sensor_readings_24.csv
│   ├── lab06-ocr-handwritten-prescription.zip
│   ├── lab07-Tweets.csv
│   └── lab08-insurance.csv
│
├── all_experiments/
│   ├── lab1.ipynb
│   ├── lab2.ipynb
│   ├── lab3.ipynb
│   └── utils/
│
├── results/
│   ├── lab01/
│   ├── lab02/
│   └── lab03/
│
└── README.md
```

---

## 🛠️ Tools & Technologies

- Python 3
- Jupyter Notebook
- NumPy
- Pandas
- Matplotlib

---

## ▶️ Running the Labs

Clone the repository:

```bash
git clone https://github.com/kwahsont/UTP-Artificial-Intelligence.git
```

Navigate into the repository:

```bash
cd UTP-Artificial-Intelligence
```

Open the notebooks using **VS Code** or **Jupyter Notebook**.

---

## 👨‍💻 Author

**Ammir**

Artificial Intelligence  
Universiti Teknologi PETRONAS
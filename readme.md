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
| Lab 04 | Fuzzy Logic | Completed |
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


## Lab 04: Fuzzy Logic and ANFIS with Air-Quality Data

This lab explores the application of fuzzy logic and Adaptive Neuro-Fuzzy Inference Systems (ANFIS) using air-quality data. It combines expert-defined rules with data-driven prediction to develop a ventilation controller and predict carbon-monoxide concentration.

### Objectives
- Preprocess air-quality data by handling missing values and removing empty rows and columns.
- Implement a Mamdani fuzzy logic controller using temperature and relative humidity to determine ventilation demand.
- Define triangular membership functions and expert rules for low, medium, and high ventilation levels.
- Validate the fuzzy controller using fixed operating points and a control-surface visualisation.
- Implement a first-order Sugeno ANFIS model to predict carbon-monoxide concentration from sensor readings.
- Compare ANFIS models with linear regression using RMSE and MAE evaluation metrics.

### Dataset
- `all_datasets/lab04-AirQuality.csv`

The dataset contains hourly air-quality sensor readings from the UCI Air Quality dataset. Preprocessing includes handling semicolon-separated values, decimal commas, missing-value markers (`-200`), and empty rows.

**Prediction task:**
- **Target:** `CO(GT)`
- **Input features:** `PT08.S1(CO)` and `PT08.S2(NMHC)`

Temperature (`T`) and relative humidity (`RH`) are used as inputs for the fuzzy ventilation controller.

### Algorithms and Techniques
- **Mamdani Fuzzy Logic:** Uses temperature and relative humidity, triangular membership functions, expert-defined rules, minimum for logical AND, maximum to combine rules, and centroid defuzzification.
- **Sugeno ANFIS:** Uses Gaussian membership functions and first-order linear rule outputs to model nonlinear relationships in the sensor data.
- **Linear Regression:** Serves as the baseline model for comparison.
- **Data Splitting:** Divides complete observations into training, validation, and test sets using a 70/15/15 ratio with random seed 42.
- **Feature Standardisation:** Uses statistics calculated from the training set only.
- **Model Selection:** Selects the ANFIS configuration based on validation RMSE before evaluating it on the test set.

### Evaluation Metrics
- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)
- Fuzzy controller validation using fixed operating points
- Visual comparison of predicted and actual carbon-monoxide concentrations

### Reference Results

| Model | Validation RMSE | Test RMSE | Test MAE |
|---|---:|---:|---:|
| Linear Regression | 0.5103 | 0.5365 | 0.3821 |
| ANFIS (2 Membership Functions) | 0.4550 | 0.4715 | 0.3264 |
| ANFIS (3 Membership Functions) | 0.4489 | 0.4672 | 0.3246 |

The ANFIS model with three membership functions achieves the lowest validation RMSE and is selected as the final model. Based on the activity's reference results, it improves test RMSE by approximately 12.9% compared with linear regression.

### Notebook
- `all_experiments/lab04_fuzzy_anfis_worked.ipynb`

### Generated Results
Results are saved in `results/lab04/`:

- `temperature_humidity.png` - Scatter plot of temperature against relative humidity.
- `fuzzy_memberships.png` - Membership functions for temperature, humidity, and ventilation demand.
- `fuzzy_fixed_points.csv` - Outputs for selected fuzzy-controller test cases.
- `fuzzy_control_surface.png` - Visualisation of ventilation demand across different conditions.
- `split.csv` - Training, validation, and test split assignments.
- `metrics.csv` - Model evaluation metrics.
- `predicted_vs_actual.png` - Predicted versus actual carbon-monoxide concentrations.

### Libraries and Tools
- Python
- Jupyter Notebook
- NumPy
- Pandas
- Matplotlib
- SciPy
- scikit-learn


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
│   ├── lab4.ipynb
│   └── utils/
│
├── results/
│   ├── lab01/
│   ├── lab02/
│   ├── lab03/
│   └── lab04/
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
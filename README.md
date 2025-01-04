# Traveling Salesman Problem (TSP) - Evolutionary Algorithm (EA)

## 📌 Overview
This project implements an **Evolutionary Algorithm (EA)** to solve the **Traveling Salesman Problem (TSP)**. The objective is to find the shortest possible route that visits each city exactly once and returns to the starting point. As TSP is classified as **NP-Hard**, evolutionary algorithms provide a practical heuristic approach to approximate near-optimal solutions.  

### Key Components:
- **Selection**: Tournament Selection  
- **Recombination**: Cyclic Crossover (CX)  
- **Mutation**: Insert Mutation for introducing variability  

### Datasets (from TSPLIB95):
- **bayg29** – 29 cities  
- **ali535** – 535 cities  

---

## 📖 Table of Contents
1. [Algorithm Overview](#algorithm-overview)  
2. [Setup and Installation](#setup-and-installation)  
3. [Usage](#usage)  
4. [Parameters and Configurations](#parameters-and-configurations)  
5. [Figures](#figures)  

---

## ⚙️ Algorithm Overview
### Evolutionary Process  
The Evolutionary Algorithm (EA) follows these steps:  

1. **Initialization** – Generate an initial random population.  
2. **Selection** – Apply tournament selection to choose parents for reproduction.  
3. **Recombination (Cyclic Crossover)** – Perform cyclic crossover to exchange genetic material.  
4. **Mutation (Insert Mutation)** – Apply insert mutation with a **2% mutation rate**.  
5. **Survivor Selection** – Replace the old population with newly generated offspring.  
6. **Termination** – The process stops after a fixed number of generations or upon reaching convergence criteria.  

---

### 🏆 Selection – Tournament Selection  
- Random subsets of individuals are chosen from the population.  
- The best individual from each subset is selected to become a parent.  

---

### 🔄 Recombination – Cyclic Crossover (CX)  
- Cycles of genes between two parents are identified.  
- Genes within the same cycle are swapped to produce offspring.  

---

### 🔄 Mutation – Insert Mutation  
- A gene is randomly selected, removed, and reinserted at a different position within the chromosome.  

---

## 🛠️ Setup and Installation  
### Requirements  
- **numpy**  
- **matplotlib**  
- **pandas**  
- **random**  

### Installation  
Clone the repository using the following command:  
```bash
git clone https://github.com/yourusername/TSP-EA.git
```  

---

## 🚀 Usage  
Run the Jupyter notebook to execute the algorithm on the datasets:  
```bash
jupyter notebook ali535_bayg29_GA.ipynb
```  
- You can modify dataset paths and configurations directly in the notebook.  

---

Plots of **best, worst, and average fitness values** over generations are generated for performance evaluation.  

---

## ⚙️ Base Parameters and Configurations  
- **Population Size**: 200  
- **Crossover Rate**: 90%  
- **Mutation Rate**: 2%  
- **Epoch**: 1000  
- **Tournament Selection Size**: 3  

> These values can be adjusted in the configuration section of the notebook.  

---

## 📈 Figures  

### 1. Algorithm Flowchart  
![Algorithm Flowchart](Image/EA.jpg)  

### 2. Cyclic Crossover Process  
![Cyclic Crossover](Image/Cyclic-Crossover.jpg)  

---

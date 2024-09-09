

# Frequent Itemset Mining

## Overview

This repository contains an implementation of the Apriori algorithm for frequent itemset mining. The project was completed as part of a data mining course assignment.

Student Information:
- **Student ID**: 21127670
- **Student Name**: Hồ Thế Phúc

## Table of Contents

1. [Introduction](#introduction)
2. [Background](#background)
3. [Implementation](#implementation)
4. [Usage](#usage)
5. [File Structure](#file-structure)
6. [Dependencies](#dependencies)
7. [How to Run](#how-to-run)
8. [Results](#results)
9. [Contributing](#contributing)
10. [License](#license)

## Introduction

Frequent itemset mining (FIM) is a fundamental task in data mining that aims to discover combinations of items that occur frequently in a transactional database. This project implements the Apriori algorithm, a classic approach to solving the FIM problem.

## Background

### Historical Context

The field of frequent itemset mining was pioneered by two seminal papers:

1. Rakesh Agrawal, Tomasz Imielinski, Arun N. Swami: "Mining Association Rules between Sets of Items in Large Databases." SIGMOD Conference 1993: 207-216
2. Rakesh Agrawal, Ramakrishnan Srikant: "Fast Algorithms for Mining Association Rules in Large Databases." VLDB 1994: 487-499

These papers are credited with giving birth to the field of Data Mining.

### Applications

Frequent itemset mining has various real-world applications, including:

- Market basket analysis in retail
- Web usage mining
- Plagiarism detection
- Bioinformatics

### Key Concepts

- **Transactional Database**: A collection of transactions, where each transaction is a set of items.
- **Itemset**: A collection of one or more items.
- **Support**: The frequency of occurrence of an itemset in the database.
- **Frequent Itemset**: An itemset whose support is greater than or equal to a predefined minimum support threshold.

### The Apriori Principle

The Apriori algorithm is based on the following principle:
- If an itemset is frequent, then all of its subsets must also be frequent.
- If an itemset is infrequent, then all of its supersets must be infrequent.

## Implementation

This project implements the Apriori algorithm using Python. The main steps of the algorithm are:

1. Generate candidate 1-itemsets
2. Find frequent 1-itemsets
3. Iteratively generate candidate k-itemsets from frequent (k-1)-itemsets
4. Prune candidates using the Apriori principle
5. Find frequent k-itemsets by scanning the database
6. Repeat steps 3-5 until no more frequent itemsets are found

The implementation uses efficient data structures like defaultdict for counting itemset supports.

## Usage

To use this implementation:

1. Prepare your transactional database in a text file, with one transaction per line and items separated by spaces.
2. Set the minimum support threshold in the script.
3. Run the script and analyze the output of frequent itemsets.

## File Structure

```
21127670/
├── frequent_itemset_mining.ipynb
├── README.md
├── data/
│   └── sample_database.txt
└── results/
    └── frequent_itemsets.txt
```

## Dependencies

- Python 3.x
- collections (standard library)

## How to Run

1. Clone this repository:
   ```
   git clone https://github.com/yourusername/frequent-itemset-mining.git
   ```
2. Navigate to the project directory:
   ```
   cd frequent-itemset-mining
   ```
3. Open and run the Jupyter notebook:
   ```
   jupyter notebook frequent_itemset_mining.ipynb
   ```

## Results

The script outputs frequent itemsets along with their support counts. Results are stored in `results/frequent_itemsets.txt`.

## Contributing

This project was completed as part of a course assignment. While it's not open for direct contributions, feedback and suggestions are welcome. Please open an issue to discuss any improvements or questions.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

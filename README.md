# WWSCAN Project

This document provides an overview of the directory structure for the WWSCAN project.

## Directory Layout

WWSCAN/  
├── data/ # Data for training and testing  
│ ├── raw/ # Raw data files (e.g., fasta files)  
│ │ ├── virus.fasta  
│ │ ├── plant.fasta  
│ │ └── bacteria.fasta  
│ ├── processed/ # Processed data for models  
│ │ ├── encoded_train_500.hdf5  
│ │ ├── encoded_train_1000.hdf5  
│ │ ├── seqs_virus_sampled_500_20000.fasta  
│ │ ├── seqs_plant_sampled_500_20000.fasta  
│ │ └── seqs_bacteria_sampled_500_20000.fasta  
│ └── README.md # Data description  
│  
├── src/ # Source code of the project  
│ ├── init.py # Package initialization  
│ ├── data_preparation/ # Modules for data preparation  
│ │ ├── init.py  
│ │ ├── dataset_nn.py # Data preparation for neural networks  
│ │ ├── dataset_rf.py # Data preparation for random forests  
│ │ └── utils.py # Utility functions  
│ ├── models/ # Modules for model handling  
│ │ ├── init.py  
│ │ ├── neural_network.py # Neural network training and evaluation logic  
│ │ └── random_forest.py # Random forest training and evaluation logic  
│ └── main.py # Main script to run the project  
│  
├── notebooks/ # Jupyter notebooks for analysis and experiments  
│ ├── data_exploration.ipynb # Data exploration and visualization  
│ └── model_training.ipynb # Model training experiments  
│  
├── tests/ # Tests for functionality checks  
│ ├── init.py  
│ ├── test_data_preparation.py # Tests for data preparation  
│ ├── test_models.py # Tests for models  
│ └── test_utils.py # Tests for utility functions  
│  
├── output/ # Results of the work (models, logs, visualizations)  
│ ├── logs/ # Execution logs  
│ ├── models/ # Saved models  
│ └── plots/ # Visualizations  
│  
├── config/ # Configuration files  
│ └── config.json # Configuration file (if needed)  
│  
├── environment.yml # Python dependencies  
├── setup.py # Package installation script  
└── README.md # Main project documentation  

## TODO:
- [x] Remove Ray library  
- [ ] Perform benchmarks on prepare.py  
- [ ] Get at least twice the speedup on the maximum number of threads  
- [ ] Transform project to desired structure
- [ ] prepare.py
    - [ ] Remove config logic  
    - [ ] Turn on using multithreading preprocessing 

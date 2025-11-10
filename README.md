# Applied Data Analytics (ADA) Projects

This repository contains projects completed for the Applied Data Analytics (ADA) course.

### Project 01: Time Series Analysis and Forecasting for Network Link Utilization

This project applies time series forecasting techniques to predict network link utilization using the `linkstats.csv` dataset. The workflow includes data cleaning, converting UNIX timestamps, and resampling data to an hourly frequency to create a `TotalUtilization` metric. Three distinct forecasting models are implemented and compared: **Linear Regression** with time-based features, **ARIMA**, and **Holt-Winters (Exponential Smoothing)**. Each model's performance is evaluated using RMSE and R², with the Holt-Winters model proving most effective due to its ability to capture the data's seasonality.

---

### Project 02: Machine Learning for Network Traffic Classification

This project uses machine learning to classify network traffic flows into specific web service categories. The analysis is performed on the large-scale Unicauca dataset, which contains over 2.7 million flow records and 50 features. The pipeline includes comprehensive data exploration, feature selection, and preprocessing. Four different classification algorithms are trained and evaluated: **Logistic Regression**, **XGBoost**, **KNeighbors Classifier**, and **Random Forest**. The **Random Forest** model delivered the best performance, achieving an F1-score of approximately 0.98, demonstrating that ensemble methods are highly effective for this classification task.

---

### Project 02.1: PCAP to Network Flow Conversion

This utility project demonstrates the process of generating network flow data from raw packet captures. Using the `scapy` library, the script reads a `.pcap` file (`http.pcap`), processes the packets, and aggregates them into bidirectional network flows. For each flow, it calculates key statistics such as total packets, total bytes, first seen, last seen, and duration. The resulting flow data is then structured and saved to a `flows.csv` file for further analysis.

---

### Project 03: Malware Detection and Classification using Machine Learning

This project builds a robust pipeline for network malware detection using the `netflow.csv` dataset. A key challenge addressed is the severe class imbalance, which is managed using a sample weighting strategy. The analysis involves a two-tiered feature engineering approach to create behavioral flow statistics and protocol-level context. Several models, including **XGBoost** and **Random Forest**, are trained for both binary (Benign vs. Attack) and multi-class (attack type) classification. The **XGBoost Classifier** proved to be the most effective model, achieving high F1-scores for critical threats like `Exploits` (0.80) and `Reconnaissance` (0.83).

---

### Project 04: Community Detection in the Enron Email Network

This project analyzes the `Email-Enron.txt` dataset (36k+ nodes, 183k+ edges) to identify communication communities within the corporation. Using the `networkx` library, the analysis compares the performance and scalability of multiple community detection algorithms: **Louvain**, **Label Propagation**, **Spectral Clustering**, **Girvan-Newman**, and **Hierarchical Clustering**. The **Louvain** algorithm demonstrated the best results, successfully partitioning the entire graph into 1,265 distinct communities with a high modularity score of 0.6122, while other methods like Label Propagation produced a single "monster community".

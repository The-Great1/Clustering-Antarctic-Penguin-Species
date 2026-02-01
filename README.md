# Clustering Antarctic Penguin Species (Unsupervised Learning)

## 📌 Project Overview

A team of researchers studying penguins in Antarctica collected physical measurement data but were unable to record the **species labels**. However, they know that at least **three penguin species** are native to the region:

* **Adelie**
* **Chinstrap**
* **Gentoo**

The goal of this project is to use **unsupervised machine learning** to identify natural groupings in the data that may correspond to these species.

---

## 🎯 Objective

* Apply **clustering techniques** to group penguins based on physical characteristics.
* Determine an appropriate number of clusters.
* Analyze cluster characteristics to understand differences between groups.

---

## 📂 Dataset

**File:** `penguins.csv`

### 📚 Data Source

Data were collected and made available by **Dr. Kristen Gorman** and the **Palmer Station, Antarctica LTER**, a member of the **Long Term Ecological Research Network**.

---

## 🧾 Feature Description

| Column              | Description                         |
| ------------------- | ----------------------------------- |
| `culmen_length_mm`  | Culmen (bill) length in millimeters |
| `culmen_depth_mm`   | Culmen (bill) depth in millimeters  |
| `flipper_length_mm` | Flipper length in millimeters       |
| `body_mass_g`       | Body mass in grams                  |
| `sex`               | Penguin sex                         |

📌 **Note:**

* The dataset contains **332 observations**.
* Species labels are **not included**, motivating an unsupervised approach.

---

## 🛠️ Methodology

### 1️⃣ Exploratory Data Analysis (EDA)

* Inspected data types and distributions
* Verified absence of missing values

### 2️⃣ Data Preprocessing

* Encoded the categorical `sex` feature using **one-hot encoding**
* Scaled all features using **StandardScaler** to ensure fair distance calculations

### 3️⃣ Choosing the Number of Clusters

* Applied the **Elbow Method** using KMeans inertia
* Identified **3 clusters** as an optimal choice

### 4️⃣ Clustering

* Performed **KMeans clustering** with `n_clusters = 3`
* Assigned cluster labels to each observation

### 5️⃣ Cluster Analysis

* Visualized clusters using key feature pairs
* Computed mean feature values per cluster to interpret group differences

---

## 📊 Model Used

* **KMeans Clustering**

  * Distance-based unsupervised algorithm
  * Suitable for identifying natural groupings in numerical data

---

## 📈 Results

* The dataset was successfully segmented into **three distinct clusters**
* Each cluster shows unique characteristics in:

  * Body mass
  * Flipper length
  * Culmen dimensions
* These clusters likely correspond to the three known penguin species in the region

📌 Final cluster assignments were appended to the original dataset for analysis.

---

## 🧠 Key Insights

* Feature scaling is critical for distance-based clustering algorithms.
* Physical measurements alone are sufficient to separate penguin populations into meaningful groups.
* Unsupervised learning can uncover structure even without labeled data.

---

## 📦 Tech Stack

* **Python 3**
* **pandas**
* **NumPy**
* **scikit-learn**
* **Matplotlib**

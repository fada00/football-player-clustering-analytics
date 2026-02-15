# ⚽ Next-Gen Football Player Profiling & Role Detection

![Status](https://img.shields.io/badge/Status-In%20Development-yellow) ![Method](https://img.shields.io/badge/ML-GMM%20%2B%20Decision%20Trees-blue) ![App](https://img.shields.io/badge/Target-Interactive%20Web%20App-green)

> **Concept:** Bringing the tactical depth of **Football Manager** roles into real world analytics using advanced statistical modeling.

## 🎯 Project Vision
In modern football, broad position labels like "Midfielder" or "Defender" are insufficient. A "Midfielder" can be a creative *Deep-Lying Playmaker* or a destructive *Ball-Winning Midfielder*.

**The Goal:** To build an automated **Role Classification Engine** that takes raw match data and assigns granular tactical roles (e.g., *Inverted Winger, False 9, Carrilero*) to players, visualizing this via an interactive web dashboard.

## 🧠 Methodology: The Hybrid Approach
This project moves beyond simple clustering by combining **Unsupervised** and **Supervised** learning techniques:

### 1. Discovery Phase (Gaussian Mixture Models - GMM)
Unlike K-Means which forces hard assignments, **GMM** allows for "Soft Clustering."
* **Why GMM?** Footballers are versatile. A player might operate as a hybrid. GMM provides the *probability* of a player belonging to a specific role (e.g., 70% Box-to-Box, 30% Mezzala), capturing the nuance of real world tactics.

### 2. Explanation Phase (Decision Trees)
While GMM finds the groups, it acts as a "black box."
* **Why Decision Trees?** I will train Decision Trees on the GMM clusters to extract **human-readable rules**.
* *Example Output:* `IF (Interceptions > 5.0) AND (Pass_Completion < 80%) THEN Role = "Ball Winning Midfielder"`

## 💻 The Product: Interactive Web App (Planned)
The final output will be a web application serving as a scouting tool:
* **Role Calculator:** Users can upload a player's stats (CSV) and the model will predict their specific tactical role.
* **Visual Profiling:** Radar charts comparing a player's stats against each other and the "Ideal Prototype" of their assigned role.
* **Historical Evolution:** Tracking how player roles have shifted from 1992 to 2025.

## 📂 Dataset & Acknowledgements
This project utilizes a comprehensive public dataset obtained from **Kaggle**, covering player statistics from the top 5 European leagues spanning over three decades.

* **Dataset Name:** [Football Players 1992-2025 | Top 5 Leagues]
* **Source:** Kaggle
* **Original Data Provider:** Data scraped from **FBref** (via StatsBomb).
* **Content:** The dataset includes `All_Players_1992-2025.csv`, featuring advanced metrics such as:
    * **Expected Goals (xG) & Assists (xA)**
    * **Progressive Carries & Passes**
    * **Defensive Actions (Tackles, Interceptions)**
    * **Possession & Passing Zones**
      
> **Note:** The data is used here strictly for educational and non-commercial analytical purposes to demonstrate advanced clustering techniques.

## 🗺️ Roadmap
- [x] **Data Collection:** Acquired historical data (30+ years).
- [ ] **Feature Engineering:** Creating per-90 metrics and possession-adjusted stats.
- [ ] **Modeling:** Implementing GMM to identify distinct tactical clusters per position.
- [ ] **Interpretation:** Using Decision Trees to define the boundaries of these roles.
- [ ] **Deployment:** Building the frontend interface for the "Role Calculator."

---
*Project designed by Fatih Dallı - Statistics Undergraduate*

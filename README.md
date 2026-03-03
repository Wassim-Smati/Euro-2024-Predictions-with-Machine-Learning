# Football Match Modeling via Poisson Law - Euro 2024 Prediction

![Euro 2024 Final Bracket](Capture%20d’écran%202026-03-03%20144117.jpg)

## 📌 Project Overview
This project explores the mathematical modeling of football matches using the **Poisson Distribution** to predict scores and match outcomes. The project culminates in a full simulation of the **Euro 2024** tournament, comparing algorithmic predictions against real bookmaker data.

## 🧠 Modeling Approach
The project follows an iterative refinement process to improve prediction accuracy:

### 1. Simple Poisson Model
* **Hypothesis**: The number of goals scored by each team is treated as two independent Poisson distributions.
* **Formula**: The probability of $x$ goals is calculated using $P(x)=\frac{e^{-\lambda}\lambda^{x}}{x!}$.
* **Parameter Selection**: $\lambda$ (average goals) is determined by multiplying a team's attacking strength by the opponent's defensive strength.

### 2. Poisson Regression (GLM)
* **Optimization**: Uses a **Generalized Linear Model (GLM)** to find the most suitable parameters for the dataset by maximizing the **Likelihood Function**.
* **Method**: The log-likelihood is maximized to cancel out gradients and find the optimal attack ($\alpha$) and defense ($\beta$) coefficients for every team.

### 3. Integration of FIFA Rankings
* **Variable Addition**: The model incorporates **FIFA Ranking points** as a corrective variable to better reflect the global standing of each nation.
* **Impact**: This iteration proved to be **3 times more accurate** than the initial model, reducing the variance compared to bookmaker odds down to approximately 5%.

## 📊

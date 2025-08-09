
# 📊 Options Pricing Using Machine Learning Algorithms

**Author:** MD Amir Khan  
**Degree:** Master of Science in Financial Engineering

---

## 📝 Abstract
In the evolving landscape of quantitative finance, machine learning is emerging as a powerful tool for forecasting the prices of financial instruments.  
This study explores the application of several machine learning algorithms to predict **vanilla put option prices**, using a **synthetic dataset generated from the Black–Scholes model** with realistic market characteristics, including volatility skew.

Results reveal that the **Neural Network (MLP) Regressor** delivers the highest predictive accuracy on out-of-sample data, outperforming tree-based and linear models. Tree-based models (Random Forest, Decision Tree) also show strong predictive ability, while traditional Linear Regression lags due to its inability to capture nonlinear dynamics.

---

## 📌 Introduction
Options are essential in risk management, hedging, and speculation. Traditional pricing models, notably Black–Scholes, have been foundational in the field but rely on assumptions that may not hold in real markets (e.g., constant volatility, lognormal returns).  
Machine learning offers a **data-driven, assumption-light** approach to pricing, capable of modeling complex nonlinear relationships and adapting to changing market conditions.

---

## 🔬 Methodology

### 1. Data Generation
- **100,000 synthetic vanilla put options** generated from the Black–Scholes framework.
- Parameters randomly sampled across realistic ranges for:
  - Spot price
  - Strike price
  - Time to maturity
  - Risk-free rate
  - Volatility (with **volatility skew** incorporated)

### 2. Option Pricing
- Black–Scholes formula applied to compute baseline put prices.
- Adjustments for **volatility skew** to mimic out-of-the-money (OTM) pricing asymmetries.

### 3. Data Splitting
- **80% training** / **20% testing** split to evaluate generalization performance.

### 4. Machine Learning Models
Five models were trained and evaluated:
1. **Linear Regression** – baseline model for comparison.
2. **Decision Tree Regressor** – captures nonlinear relationships.
3. **Random Forest Regressor** – ensemble method improving stability and accuracy.
4. **Gradient Boosted Trees Regressor** – sequentially reduces residual errors.
5. **Neural Network (MLP) Regressor** – deep learning approach for complex relationships.

---

## 📈 Model Performance Summary

| Model                       | Mean Squared Error | Mean Absolute Error | R² Score |
|-----------------------------|--------------------|---------------------|----------|
| Linear Regression           | 82.31              | 7.41                | 0.802    |
| Decision Tree               | 2.22               | 1.10                | 0.995    |
| Random Forest               | 0.62               | 0.58                | 0.9985   |
| Gradient Boosted Trees      | 3.01               | 1.37                | 0.9928   |
| Neural Network (MLP)        | **0.12**           | **0.20**            | **0.9997** |

**Key Takeaways:**
- **Neural Network** achieved near-perfect predictions (R² ≈ 0.9997).
- **Random Forest** closely follows, offering strong accuracy with better interpretability.
- **Linear Regression** underperforms, highlighting the nonlinear nature of option pricing.

---

## 📊 Visualizations

### Actual vs. Predicted Prices
Scatter plots for each model show how closely predicted values align with actual prices.  
The red dashed line represents the ideal prediction (Perfect Fit).

*(Example plot from the notebook)*  
![Scatter Plots](docs/scatter_plots.png)

---

## 📂 Repository Structure
```

├── Options\_pricing\_using\_Algorithms.ipynb   # Main notebook with all code & analysis
├── docs/
│   ├── scatter\_plots.png                    # Actual vs Predicted plots
│   └── performance\_metrics.png              # Model comparison chart
└── README.md

````

---

## 🛠 How to Run

1. **Clone this repository**:
```bash
git clone https://github.com/Mkhan2317/Options_Pricing_Using_Machine_Learning_Algorithms.git
cd Options_Pricing_Using_Machine_Learning_Algorithms
````

2. **Install dependencies**:

```bash
pip install -r requirements.txt
```

3. **Open the Jupyter Notebook**:

```bash
jupyter notebook Options_pricing_using_Algorithms.ipynb
```

4. **Run all cells** to generate results and visualizations.

---

## 📚 References

* Black, F., & Scholes, M. (1973). *The Pricing of Options and Corporate Liabilities*. Journal of Political Economy.
* Hull, J. (2017). *Options, Futures, and Other Derivatives*. Pearson.
* Breiman, L. (2001). *Random Forests*. Machine Learning.
* Goodfellow, I., Bengio, Y., & Courville, A. (2016). *Deep Learning*. MIT Press.

---

## ⚠️ Disclaimer

This notebook is intended for **educational and research purposes only**.
It does **not** constitute financial advice. Options trading involves substantial risk and is not suitable for all investors.

---

## 📬 Contact

* **Email:** [mkhan37@stevens.edu](mailto:mkhan37@stevens.edu)
* **LinkedIn:** [Amir Khan](https://linkedin.com/in/amirkhan2317)
* **Portfolio:** [mkhan2317.github.io](https://mkhan2317.github.io/)
* **GitHub Repo:** [Options Pricing Using ML Algorithms](https://github.com/Mkhan2317/Options_Pricing_Using_Machine_Learning_Algorithms)





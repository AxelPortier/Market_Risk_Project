# Market_Risk_Project
> Comprehensive financial risk modeling using non-parametric methods, Extreme Value Theory, and wavelet analysis.  
> Built with Python (NumPy, Pandas, Matplotlib) - All estimators implemented manually from scratch.

---

## 👥 Team

**Developed by**: Axel Portier & Gaspard Salluron-Besnard  
**School**: ESILV - École Supérieure d'Ingénieurs Léonard de Vinci  
**Program**: 4th Year Financial Engineering (2025/2026)  
**Course**: Market Risk   

---

## 🎯 Project Overview

Advanced quantitative risk assessment platform featuring:

- **Non-parametric VaR** with 4 bandwidth selection methods
- **Extreme Value Theory** for tail risk modeling (Pickands estimator)
- **Bouchaud's price impact model** calibration via gradient descent
- **Haar wavelet analysis** for multi-scale correlation (Epps effect detection)
- **Hurst exponent estimation** for long-range dependence & volatility scaling

**📊 Datasets**: Natixis stock prices (2015-2018), Transaction data, FX rates (GBP/EUR, SEK/EUR, CAD/EUR)

---

## 🚀 Quick Start
```bash
# Clone repository
git clone https://github.com/AxelPortier/market-risk-project.git
cd market-risk-project

# Install dependencies
pip install pandas numpy matplotlib 


> ⚠️ **Note**: No specialized statistical packages used - all estimators coded manually per academic requirements.

---

## 📦 Key Features

### 🔹 Question A: Non-Parametric VaR
- **Biweight kernel density estimation** for historical VaR (95% confidence)
- **4 bandwidth methods**: Under-smoothing, Silverman, Scott, Over-smoothing
- **Backtesting**: Out-of-sample validation (2017-2018 data)

### 🔹 Question B: Expected Shortfall
- **ES calculation** for all bandwidth methods
- **Comparison**: ES consistently 1.5-1.6% higher than VaR
- **Validation**: Confirms coherent risk measure properties

### 🔹 Question C: Extreme Value Theory
- **Pickands estimator** with stability analysis (k ∈ [5, n/4])
- **Tail classification**: Losses = Fréchet (ξ=0.374) | Gains = Weibull (ξ=-0.175)
- **EVT-based VaR**: 90%-99.9% confidence levels

### 🔹 Question D: Bouchaud's Price Impact Model
- **Model**: `p_t = p_0 + Σ G(t-s) × ε_s × S_s × V_s^r` where `G(t) = t^(-γ)`
- **Optimization methods**: Grid Search, Gradient Descent, GD + Volatility Scaling
- **Parameters**: r, γ
- **Limitation**: Parameter instability due to small sample (131 fully completed observations)

### 🔹 Question E: Wavelet & Hurst Analysis
- **Haar wavelets**: 9 resolution levels (30 min → 5.3 days)
- **Epps effect detected**: Correlation increases with window size (overlapping method)
- **Hurst exponents**: GBP/EUR (0.67), SEK/EUR (0.65), CAD/EUR (0.66)

---

## 📂 Project Structure
```
market-risk-project/
│
├── 📄 MR_Project_PORTIER_SALLURON__BESNARD_IF5.pdf           # Full report (37 pages)
├── 📊 natixis_stock.txt                                      # Natixis daily prices (2015-2018)
├── 📊 Dataset_TD4.xlsx                                       # Transaction data
├── 📊 Dataset_TD5.xlsx                                       # FX rates
├── 💻 MR_Project_Notebook_PORTIER_SALLURON-BESNARD.ipynb     # Main implementation
```

---

**📧 Contact**: [axel.portier@edu.devinci.fr](mailto:axel.portier@edu.devinci.fr) | [gaspard.salluron-besnard@edu.devinci.fr](mailto:gaspard.salluron-besnard@edu.devinci.fr)

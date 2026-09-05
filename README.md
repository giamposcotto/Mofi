# Cross-Section Moment-Curvature Analysis Tool (Fiber Method)

A Python-based structural engineering application for Windows designed to calculate, visualize, and compare moment-curvature ($M-\chi$) diagrams for reinforced concrete beams and columns using the Fiber Method.

---

## 📌 Repository Description (For GitHub Setup)

> **Short Description / Tagline:**
> *A Python app to compute moment-curvature diagrams for RC sections using the Fiber Method, Eurocode chord rotations, and Excel export.*

---

## 🚀 Key Features

* **Fiber Method Discretization:** Accurate nonlinear analysis of RC cross-sections with customizable geometry, longitudinal reinforcement, and material constitutive models.
* **Key Structural Limit States:**
  * **Cracking Moment ($M_{cr}$):** Moment when the bottom tensile edge reaches maximum concrete tensile strength.
  * **Yielding Moment ($M_y$):** Moment corresponding to the yielding of the outermost tension steel reinforcement.
* **Beam & Column Analysis (v1.2+):**
  * Full support for axial load ($N$) effects (eccentric compression/tension).
  * Consideration of concrete tensile strength within the $M-\chi$ response curve.
* **Eurocode Chord Rotations:** Automatically calculates notable chord rotation limit states ($\theta_y$, $\theta_{um}$) using Eurocode 8-3 formulations for existing buildings (with customizable parameters).
* **Comparative Multi-Analysis:** Run and overlay multiple parametric analyses on a single graph to evaluate cross-section behavior under varying parameters.
* **Data & Graphic Export:** Export detailed result tables to **Microsoft Excel (`.xlsx`)** and save high-resolution graph plots.
* **Bilingual Interface:** Toggle seamlessly between **English** and **Italian** languages directly inside the GUI.
* **Built-in Examples:** Pre-loaded sample files for both a **beam** and a **column** accessible from the main menu.

---

## ⚙️ Technical Methodology

### 1. Fiber Method Integration
The section is divided into $N$ discrete longitudinal fibers (concrete fibers + steel reinforcing bars). Strain compatibility is maintained under the Bernoulli-Euler hypothesis:

$$\varepsilon(y) = \varepsilon_0 + \chi \cdot y$$

Section equilibrium is iteratively solved for a given curvature $\chi$:

$$N(\chi) = \sum_{i=1}^{N_c} \sigma_c(\varepsilon_i) A_{c,i} + \sum_{j=1}^{N_s} \sigma_s(\varepsilon_j) A_{s,j} = N_{ext}$$

$$M(\chi) = \sum_{i=1}^{N_c} \sigma_c(\varepsilon_i) A_{c,i} y_i + \sum_{j=1}^{N_s} \sigma_s(\varepsilon_j) A_{s,j} y_j$$

### 2. Eurocode 8-3 Chord Rotation Assessment
Evaluates plastic deformation capacity for existing RC structures:
* Yield Chord Rotation ($\theta_y$)
* Ultimate Chord Rotation ($\theta_{um}$)

---

## 💡 Quick Start

1. **Launch App:** Run the application executable on any Windows PC.
2. **Select Language:** Switch between English and Italian via the interface settings.
3. **Load Example File:** Select either the integrated **Beam** or **Column** example from the main menu.
4. **Input Geometry & Materials:** Define section dimensions, rebar layout, concrete/steel constitutive laws, and axial force $N$.
5. **Run & Compare:** Generate moment-curvature curves, inspect cracking/yielding points, compare multiple runs, and export tables to **Excel**.

---

## 🏷️ Suggested GitHub Topics

`structural-engineering` `moment-curvature` `fiber-method` `reinforced-concrete` `eurocode-8` `beam-column` `civil-engineering` `python-gui` `excel-export` `windows-app`

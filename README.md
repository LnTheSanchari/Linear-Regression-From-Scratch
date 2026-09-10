# 📐 Linear Regression From Scratch

> **Understanding Linear Regression through mathematics, geometry, and implementation.**

This project implements **Linear Regression from scratch** with a focus on understanding what happens underneath the usual `model.fit()`.

The goal is to connect:

**Linear Algebra → Matrix Calculus → Loss Functions → Gradient Descent → Optimization**

---

## 🧠 What I Explore

### 🔹 Linear Regression

* Model formulation
* Simple Linear Regression
* Multiple Linear Regression
* Matrix representation

### 🔹 📉 Loss Functions

* Mean Squared Error (MSE)
* Mean Absolute Error (MAE)
* Derivation of gradients
* Understanding the geometry of loss

### 🔹 ∇ Gradient Descent

* Deriving gradients using matrix calculus
* Parameter updates
* Learning rate
* Convergence
* Visualizing optimization

### 🔹 ⚖️ Feature Scaling

Feature scaling is explored from an **optimization perspective**.

Without scaling, the loss surface can become highly elongated:

$$
\text{Poor Conditioning}
\quad\Longrightarrow\quad
\text{Slow / Difficult Gradient Descent}
$$

After scaling:

$$
\text{Better Conditioning}
\quad\Longrightarrow\quad
\text{More Efficient Optimization}
$$

The notebook visualizes this using **loss surfaces and contour plots**.

### 🔹 📐 Geometry

The project also explores the geometric interpretation of linear regression, including:

* Level curves of the loss function
* Curvature
* Hessian matrices
* Eigenvalues
* Conditioning
* Projection and least squares

---

## 🧮 From Scratch

Rather than relying entirely on high-level ML libraries, the core ideas are implemented manually.

The overall flow is:

```text
        Model
          ↓
       Prediction
          ↓
      Loss Function
          ↓
       ∇ Gradient
          ↓
    Gradient Descent
          ↓
       Parameters
          ↓
       Minimum
```

This makes it possible to see how the mathematics translates directly into code.

---

## 🏠 Dataset

The project uses a house-price regression dataset containing features such as:

* 📏 Square Footage
* 🛏️ Number of Bedrooms
* 🛁 Number of Bathrooms
* 🏗️ Year Built
* 🌳 Lot Size
* 🚗 Garage Size
* 🏘️ Neighborhood Quality

🎯 **Target:** House Price

The dataset is loaded directly from GitHub, making the notebook reproducible in **Google Colab**.

```python
url = "https://raw.githubusercontent.com/LnTheSanchari/Linear-Regression-From-Scratch/main/house_price_regression_dataset.csv"

df = pd.read_csv(url)
```

---

## 📊 Visualizing Optimization

A major part of the project is making the optimization process visible.

Instead of thinking only in terms of numbers:

$$
w \rightarrow w'
$$

we can visualize the parameter space as a surface:

$$
J(w,b)
$$

and understand gradient descent as:

> **Moving through the geometry of the loss surface toward a minimum.**

---

## 📐 Multiple Linear Regression

The project naturally extends from:

$$
\hat{y} = wx + b
$$

to:

$$
\hat{\mathbf{y}} = X\mathbf{w} + b
$$

The same mathematical ideas continue to apply:

**Model → Loss → Gradient → Optimization**

This demonstrates how the concepts developed for simple regression generalize to higher-dimensional problems.

---

## 🎓 A Different Route to the Normal Equation

If matrix calculus isn't your thing, there is another beautiful route.

Professor **Gilbert Strang** presents the geometric perspective through **projection**, showing how least squares and the Normal Equation arise naturally from geometry.

> 📌 **Projection → Orthogonality → Least Squares → Normal Equation**

---

## 🛠️ Tools

* 🐍 Python
* 🔢 NumPy
* 🐼 Pandas
* 📈 Matplotlib
* 📓 Jupyter Notebook
* ☁️ Google Colab

---

## 📂 Repository Structure

```text
Linear-Regression-From-Scratch/
│
├── 📓 Linear Regression From Scratch.ipynb
├── 📄 house_price_regression_dataset.csv
└── 📖 README.md
```

---

## 🎯 Purpose

This project is not about reinventing `scikit-learn`.

It is about understanding **why** Linear Regression works.

> **Don't just call the algorithm. Understand the mathematics behind it.**

---

## 🚀 Running the Project

The notebook can be opened directly in **Google Colab** and executed sequentially.

No external dataset setup is required.

---

### ⭐ If you find the project useful

Feel free to explore the notebook, experiment with the implementation, and modify the experiments.

**Happy learning! 📐 ∇ 📊**

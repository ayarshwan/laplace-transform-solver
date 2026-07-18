# Laplace Transform Solver 🔁

An interactive Python tool that computes **Laplace** and **Inverse Laplace** transforms symbolically, built on top of [SymPy](https://www.sympy.org/). Originally built as an ODE-solving helper — enter a function, get its transform instantly.

## ✨ Features
- Compute the **Laplace Transform** of any function of `t`
- Compute the **Inverse Laplace Transform** of any function of `s`
- Supports powers, exponentials, sine, cosine, natural log, and combinations of these
- Handles **unit step (shifted) functions** using `u(t-a)`
- Automatic **partial fraction decomposition** before inverting
- Simple interactive CLI loop — solve multiple equations in one session

## 🧠 How it works
The tool uses `sympy.laplace_transform` and `sympy.inverse_laplace_transform` under the hood, with extra logic to:
- Simplify and rewrite results in terms of `sin`/`cos`
- Clean up Heaviside step function outputs
- Apply partial fraction decomposition automatically for cleaner inverse transforms

## 📥 Input Examples
| You want | Type this |
|---|---|
| t² | `t**2` |
| e^(-2t) | `exp(-2*t)` |
| sin(t) | `sin(t)` |
| ln(t) | `ln(t)` |
| Combined | `exp(-2*t)*sin(3*t)` |
| Shifted (unit step) | `u(t-3)*t**2` |

## ▶️ Usage
```bash
python laplace_solver.py
```
Then follow the prompts:
1. Choose `1` for Laplace Transform or `2` for Inverse Laplace Transform
2. Enter your function
3. Get the result instantly
4. Type `exit` anytime to quit

## 🛠️ Requirements
```bash
pip install sympy
```
## 📌 Example
Input Function: 8t**3 + tsin(3t) - 4exp(2t)
Laplace Transform: I/(2(s + 3*I)2) - I/(2(s - 3I)2) - 4/(s - 2) + 48/s4

## 🚀 Possible Improvements
- Add a simple GUI (Tkinter or Streamlit)
- Support systems of ODEs
- Export results as LaTeX

---


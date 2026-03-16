# 📊 ANOVA Lab — One-Way ANOVA Interactive Simulation

An interactive, browser-based simulation designed for **MBA classrooms** to teach One-Way Analysis of Variance (ANOVA). Students journey from the historical origins of ANOVA through theory, a fully worked business example, hands-on exercises, and a live coding sandbox — all in a single responsive web app.

> **Built for:** Center for Distance and Online Education (CDOE), ICFAI Foundation for Higher Education (IFHE), Hyderabad

---

## ✨ Features

### 🏛️ History of ANOVA
A visual timeline tracing ANOVA from Sir Ronald Fisher's pioneering work at Rothamsted Experimental Station in the 1910s through the computing revolution to modern-day applications in Python and R. Nine key milestones help students appreciate the intellectual heritage behind the technique.

### 📐 Theory Section
Covers the four essentials every MBA student needs:
- **What** is One-Way ANOVA and how does it work?
- **When** should you use it? (with business scenarios)
- **Assumptions**: Independence, Normality, Homogeneity of Variance
- **Core Logic**: Variance decomposition, the F-ratio, and decision rules

### 📝 Step-by-Step Worked Example
A complete business case — *"Comparing Customer Satisfaction Across Three Marketing Strategies"* — solved in **6 interactive steps**:
1. State the hypotheses (H₀ and H₁)
2. Organize data and compute group means
3. Calculate Sum of Squares Between (SSB)
4. Calculate Sum of Squares Within (SSW)
5. Compute degrees of freedom and mean squares
6. Calculate the F-statistic and make the decision

Each step reveals progressively, with full formulas, intermediate calculations, and a complete ANOVA table.

### 🧮 Interactive Calculator
Students enter their own data (any number of groups) and instantly receive:
- Complete ANOVA table (SS, df, MS, F, p-value)
- F-critical value at α = 0.05
- Decision (Reject / Fail to Reject H₀)
- Group means summary

### 💼 Four Business Exercises
Real-world scenarios with data, hints, and full solutions:

| # | Exercise | Groups | Domain |
|---|----------|--------|--------|
| 1 | Employee Productivity Across Shift Timings | 3 shifts × 6 workers | Operations |
| 2 | Sales Revenue by Store Layout | 4 layouts × 5 stores | Retail Strategy |
| 3 | Training Method Effectiveness | 3 methods × 7 employees | Human Resources |
| 4 | Customer Wait Time by Service Channel | 4 channels × 6 interactions | Banking / Service |

Each exercise includes:
- Data table and hypothesis hint
- Show/Hide solution toggle with ANOVA table
- Ready-to-use **R code** and **Python code**
- One-click button to load code into the sandbox

### 💻 Code Sandbox
A built-in code editor supporting both **Python** and **R** syntax. Students can:
- Write or paste ANOVA code
- Click **Run** to simulate execution
- See full output: ANOVA table, F-statistic, p-value, decision, group means, and pairwise comparisons

The sandbox parses data arrays from the code and computes ANOVA using JavaScript — no server required. For full R/Python execution, students can copy the code to RStudio, Jupyter, or Google Colab.

---

## 🖥️ Compatibility

- **Laptop / Desktop**: Full-screen layout with side-by-side content
- **Tablet**: Responsive grid that adapts gracefully
- **Smartphone**: Fully mobile-friendly with collapsible navigation, scrollable tables, and touch-optimized controls

---

## 🚀 Deployment

### Deploy on Vercel (Recommended)

1. **Fork or clone this repository**

2. **Go to [vercel.com](https://vercel.com)** and sign in with GitHub

3. **Add New Project** → Import this repository

4. **Settings:**
   - Framework Preset: **Other**
   - Build Command: *(leave empty)*
   - Output Directory: *(leave empty)*

5. Click **Deploy**

Your app will be live at `https://your-project.vercel.app` within seconds.

### Run Locally

No build tools needed. Simply open `index.html` in any modern browser:

```bash
# Clone the repo
git clone https://github.com/sanjayfuloria/anova-sim.git
cd anova-sim

# Open in browser
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

### Host Anywhere

Since this is a static site (single HTML file), it works on any hosting platform:
- **GitHub Pages**: Enable in repo Settings → Pages → Deploy from branch
- **Netlify**: Drag and drop the folder
- **Any web server**: Just serve the `index.html` file

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| UI Framework | React 18 (via CDN) |
| Transpilation | Babel Standalone (in-browser JSX) |
| Styling | Custom CSS with CSS variables |
| Typography | Playfair Display, Source Sans 3, JetBrains Mono (Google Fonts) |
| Statistics | Pure JavaScript (F-distribution, beta functions, p-values — no external stats library) |
| Deployment | Static HTML — zero build step |

---

## 📁 Project Structure

```
anova-sim/
├── index.html        # Complete application (single file)
├── vercel.json       # Vercel routing config
├── package.json      # Project metadata
├── .gitignore
└── README.md
```

---

## 📚 Statistical Methods Implemented

The app computes all statistics in-browser using pure JavaScript:

- **Grand Mean** and **Group Means**
- **Sum of Squares**: SSB (Between), SSW (Within), SST (Total)
- **Degrees of Freedom**: df₁ = k − 1, df₂ = N − k
- **Mean Squares**: MSB, MSW
- **F-statistic**: MSB / MSW
- **p-value**: Computed via regularized incomplete beta function and F-distribution CDF
- **F-critical value**: Binary search over the inverse F-distribution at α = 0.05
- **Pairwise mean differences**: Displayed when H₀ is rejected

---

## 🎓 Pedagogical Design

The simulation follows a deliberate learning progression:

```
History → Theory → Worked Example → Interactive Calculator → Exercises → Code Sandbox
  (Why)    (What)     (How)           (Practice)           (Apply)      (Implement)
```

This mirrors Bloom's taxonomy — moving students from **knowledge** and **comprehension** (history, theory) through **application** (worked example, calculator) to **analysis** and **synthesis** (exercises, coding).

---

## 📄 License

This project is created for educational purposes at ICFAI Foundation for Higher Education (IFHE), Hyderabad. Feel free to use and adapt for academic instruction.

---

## 👤 Author

**Prof. Sanjay Fuloria**
Director, Center for Distance and Online Education (CDOE)
ICFAI Foundation for Higher Education (IFHE), Hyderabad

---

*Built with care for the MBA classroom.*

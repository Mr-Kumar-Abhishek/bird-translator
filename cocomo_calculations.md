# COCOMO Model Calculations

The Constructive Cost Model (COCOMO) is a procedural software cost estimation model developed by Barry Boehm. It estimates the effort, development time, and average staff size required for a software project based on the estimated size of the project in Kilo Lines of Code (KLOC).

COCOMO categorizes software projects into **three types (or modes)** based on project complexity and team experience:

1. **Organic**: Small, relatively simple projects with a small team and familiar requirements (e.g., simple business systems).
2. **Semi-detached**: Medium-sized projects with mixed team experience and moderate complexity (e.g., utility programs, operating systems).
3. **Embedded**: Complex projects with tight constraints, strict requirements, and specialized hardware/software interfaces (e.g., avionics, real-time control systems).

---

## 1. Formulas

### Basic COCOMO Equations

- **Effort ($E$)** = $a \times (KLOC)^b$ 
  *Unit: Person-Months (PM)*
- **Development Time ($T_{dev}$)** = $c \times (E)^d$ 
  *Unit: Months (M)*
- **Average Staff Size ($P$)** = $E / T_{dev}$ 
  *Unit: Persons (Headcount)*
- **Productivity** = $KLOC / E$ 
  *Unit: KLOC / Person-Month*

### Constants Table

| Project Type | $a$ | $b$ | $c$ | $d$ |
| :--- | :--- | :--- | :--- | :--- |
| **Organic** | 2.4 | 1.05 | 2.5 | 0.38 |
| **Semi-detached** | 3.0 | 1.12 | 2.5 | 0.35 |
| **Embedded** | 3.6 | 1.20 | 2.5 | 0.32 |

---

## 2. Example Calculation

Let's calculate the Effort, Development Time, and Average Staff Size for a software project estimated to be **50 KLOC (50,000 lines of code)** across all three project types.

### A. Organic Type
Using the constants: $a = 2.4$, $b = 1.05$, $c = 2.5$, $d = 0.38$

* **Effort ($E$)**:
  $E = 2.4 \times (50)^{1.05}$
  $E = 2.4 \times 60.426$
  $E \approx 145.02 \text{ Person-Months}$

* **Development Time ($T_{dev}$)**:
  $T_{dev} = 2.5 \times (145.02)^{0.38}$
  $T_{dev} = 2.5 \times 6.643$
  $T_{dev} \approx 16.61 \text{ Months}$

* **Average Staff Size ($P$)**:
  $P = E / T_{dev} = 145.02 / 16.61$
  $P \approx 8.73 \text{ Persons} \approx \mathbf{9 \text{ Persons}}$

---

### B. Semi-detached Type
Using the constants: $a = 3.0$, $b = 1.12$, $c = 2.5$, $d = 0.35$

* **Effort ($E$)**:
  $E = 3.0 \times (50)^{1.12}$
  $E = 3.0 \times 81.339$
  $E \approx 244.02 \text{ Person-Months}$

* **Development Time ($T_{dev}$)**:
  $T_{dev} = 2.5 \times (244.02)^{0.35}$
  $T_{dev} = 2.5 \times 6.745$
  $T_{dev} \approx 16.86 \text{ Months}$

* **Average Staff Size ($P$)**:
  $P = E / T_{dev} = 244.02 / 16.86$
  $P \approx 14.47 \text{ Persons} \approx \mathbf{15 \text{ Persons}}$

---

### C. Embedded Type
Using the constants: $a = 3.6$, $b = 1.20$, $c = 2.5$, $d = 0.32$

* **Effort ($E$)**:
  $E = 3.6 \times (50)^{1.20}$
  $E = 3.6 \times 109.336$
  $E \approx 393.61 \text{ Person-Months}$

* **Development Time ($T_{dev}$)**:
  $T_{dev} = 2.5 \times (393.61)^{0.32}$
  $T_{dev} = 2.5 \times 6.942$
  $T_{dev} \approx 17.36 \text{ Months}$

* **Average Staff Size ($P$)**:
  $P = E / T_{dev} = 393.61 / 17.36$
  $P \approx 22.67 \text{ Persons} \approx \mathbf{23 \text{ Persons}}$

---

## 3. Summary of the 50 KLOC Example

| Metric | Organic | Semi-detached | Embedded |
| :--- | :--- | :--- | :--- |
| **Effort** (Person-Months) | 145.02 | 244.02 | 393.61 |
| **Time** (Months) | 16.61 | 16.86 | 17.36 |
| **Staff Size** (Persons) | ~9 | ~15 | ~23 |

As demonstrated, while the estimated development time remains somewhat consistent across the three types, the **effort** and **required staff size** increase dramatically as the project type moves from Organic (simple) to Embedded (highly complex).

# Mathematical Specification: Policy Thermodynamics Engine

## 1. System Baseline (Calibration)
The simulator is calibrated based on the 2024–2025 Japanese economic baseline. These constants represent the "Idle State" of the national circuit before new policy injections.

*   **Base Grounded Income ($Y_{base}$):** 4.60 Million JPY / year (The average real-world disposable income).
*   **Base Thermal Loss ($\pi_{base}$):** 1.5% (The baseline inflation rate).
*   **Base System Impedance ($D_{base}$):** 1.0 (The standard level of structural friction/overhead).

---

## 2. Input Variables and Energy Conversions
User selections are treated as changes to the physical potentials of the system. Every policy choice modifies one or more of the following four "Energy Scores":

### 2.1 Consumption Tax Potentials
Tax reduction increases the voltage (available cash) but reduces the system's "Insulation," leading to heat (inflation) and long-term structural strain.
*   **Income Energy ($\Delta S_{inc}$):** $(10 - \text{TaxRate}) \times 2.0$
*   **Maintenance Penalty (if TaxRate < 5%):**
    *   **Future Load:** $+ (5 - \text{TaxRate}) \times 15$
    *   **Heat Generation:** $+ (5 - \text{TaxRate}) \times 0.4$

### 2.2 Fiscal Investment (System Capacity Logic)
The "Fiscal Spend" slider determines the speed of energy injection. This model follows the **Law of Entropic Elasticity**: if the injection volume exceeds the system's **Potential Capacity ($C_{pot}$)**, the energy is rejected and turns into friction.

*   **Level 3 (Volume Overload):** $S_{inc} +35$, $S_{inf} +3.0$, **$S_{dist} +0.45$**, $S_{load} +50$
    *   *Logic:* Injection exceeds $C_{pot}$. Excess energy is "ejected" from the local loop and consumed by central overhead (General Contractors), causing a surge in **Distortion**.
*   **Level 2 (Within Capacity):** $S_{inc} +15$, $S_{load} +10$
    *   *Logic:* Injection is near the capacity limit. Gains are visible with minimal rebound.
*   **Level 1 (Maintain):** No change to baseline.
*   **Level 0 (Tighten):** $S_{inc} -10$, $S_{load} -20$

### 2.3 Circuit Architectures (Structural Models)
This variable reconfigures how energy flows through the system, primarily affecting the **Resistance ($D$)**.

| Architecture Type | Engineering Logic | Parameter Impact |
| :--- | :--- | :--- |
| **System Optimization** | Minimizes "Leakage" by removing middle-men. | $S_{inc} +15, D -0.35$ |
| **Direct Distribution** | Bypasses bureaucratic resistance; direct grounding. | $S_{inc} +45, D +0.2, S_{inf} +1.2$ |
| **Centralized Public** | Nationalization; higher insulation but high inertia. | $S_{inc} +42, S_{inf} +0.9, S_{load} +45$ |
| **Flux Reversal** | Re-activates stagnant corporate energy back into labor. | $S_{inc} +30, D -0.15$ |

---

## 3. The Governing Equations (Final Output)

The simulator applies physical laws to the accumulated scores to determine if the system stabilizes or breaks down.

### 3.1 The Net Grounding Equation (Real Income)
Real disposable income is the total energy divided by structural resistance, minus the "Heat Dissipation" caused by inflation.

$$Y_{final} = Y_{base} + \left( \frac{\sum S_{inc}}{\sum D_{final}} \right) - (\sum S_{inf} \times 8)$$

*   **The Divider Principle:** Distortion ($D$) acts as a **denominator**. If the system capacity is exceeded (high $D$), adding more budget ($\sum S_{inc}$) results in diminishing grounding energy for the household.
*   **Inflation Weight:** Inflation is weighted at **8.0**, representing the "Heat" that evaporates the value of cash before it can be used for work.

### 3.2 Total System Resistance (Distortion Index)
$$D_{final} = D_{base} + \Delta S_{dist}$$
A $D_{final} > 1.25$ indicates **Thermal Overload**, where the system's internal friction (bureaucracy/extraction) consumes more energy than it delivers to the people.

---

## 4. Rationale for Fixed Constants (The Debugging Logic)

This simulator intentionally uses **linear fixed values** for policy impacts to ensure the structural defects are visible.

### 4.1 Traceability (Root Cause Analysis)
To "Debug" a social system, every outcome must be clearly traceable. Using fixed constants ensures the user understands exactly which policy choice caused the system to "Rebound" or "Overheat."

### 4.2 Identification of "Ejection Points"
By using fixed values, the simulator highlights the **Capacity Limit**. It proves that throwing money at a "Distorted" system is mathematically equivalent to pouring water into a bucket full of holes.

---

## 5. Engineering Conclusion
The simulator's mathematics demonstrate the **"Conservation of Pain"**:
1.  **Elastic Rebound:** Forcing money into a region faster than its $C_{pot}$ can grow results in the wealth being "ejected" to the center (Tokyo).
2.  **The Denominator Trap:** In a high-distortion circuit, the state must burn massive amounts of energy just to provide a tiny increase in grounded income.

**The Optimization Goal:** Users must find the specific configuration where structural resistance ($D$) is minimized, allowing energy to reach the ground without turning into inflationary heat.

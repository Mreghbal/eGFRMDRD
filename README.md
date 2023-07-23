# eGFRMDRD Calculator

## Table of Contents
- [Introduction](#introduction)
- [Meaning and Applications](#meaning-and-applications)
- [Running the Code](#running-the-code)
- [Explanation](#explanation)
- [Follow Me](#follow-me)

## Introduction
Welcome to the eGFRMDRD Calculator! This calculator is a Python implementation of the Estimated Glomerular Filtration Rate (eGFR) using the Modification of Diet in Renal Disease (MDRD) equation. It allows you to estimate kidney function based on age, gender, serum creatinine level, and race.

## Meaning and Applications
The Estimated Glomerular Filtration Rate (eGFR) is a measure used to assess kidney function. It estimates the rate at which kidneys filter waste from the blood. The eGFR is an important indicator for diagnosing and monitoring chronic kidney disease (CKD). It helps healthcare professionals determine the stage of CKD and make treatment decisions.

The MDRD equation is one of the commonly used equations to estimate eGFR. It takes into account factors such as age, gender, serum creatinine level, and race to provide a more accurate estimation of kidney function.

## Running the Code
To use the eGFRMDRD Calculator, follow these steps:

1. Clone the repository:
   ```
   git clone https://github.com/Mreghbal/eGFRMDRD.git
   ```

2. Navigate to the project directory:
   ```
   cd eGFRMDRD-Calculator
   ```

3. Install the required dependencies (if any) by running:
   ```
   pip install -r requirements.txt
   ```

4. Open the code file `calculate_egfr.py` in your preferred Python editor or IDE.

5. Run the code and provide the requested information when prompted:
   - Enter the age.
   - Enter the gender (male/female).
   - Enter the serum creatinine level in mg/dL.
   - Enter the race (white/black).

6. The eGFR value will be calculated and displayed.

## Explanation
The `calculatefr` function in the code takes four parameters: `age`, `gender`, `serum_creatinine`, and `race`. It follows the MDRD equation to estimate the eGFR based on the provided inputs.

### Validating Input Values
Before performing the calculation, the function validates the input values to ensure they meet the required criteria. Here are the validation rules:

- Age and serum creatinine must greater than zero.
- Gender must be either "male" or "female".
- Race must be either "white" or "black".

If any of the input values fail the validation, a `ValueError` is raised with an appropriate error message.

 Calculating eGFR
The MDRD equation coefficients differ based on gender and race. The function assigns the appropriate coefficients (`a`, `b`, and `c`) based on the provided gender and race. Then, it calculates the eGFR using the formula:

```
egfr = a * (serum_creatinine ** b) * (age ** c)
```

Finally, the calculated eGFR value is returned by the function.

## Follow Me
If you find this project helpful, feel free to follow me on LinkedIn and Twitter for more updates and interesting projects:

LinkedIn: [Reza Eghbal](https://www.linkedin.com/in/mreghbal)

Twitter: [Reza Eghbal](https://twitter.com/mreghbal)

Thank you for using the eGFRMDRD Calculator! If you have any questions or suggestions, please don't hesitate to reach out.

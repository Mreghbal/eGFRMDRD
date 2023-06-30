def calculate_egfr(age, gender, serum_creatinine, race):
    # Validate input values
    if age <= 0 or serum_creatinine <= 0:
        raise ValueError("Age and serum creatinine must be greater than zero.")

    # Validate gender
    gender = gender.lower().strip()
    if gender not in ["male", "female"]:
        raise ValueError("Gender must be either 'male' or 'female'.")

    # Validate race
    race = race.lower().strip()
    if race not in ["white", "black"]:
        raise ValueError("Race must be either 'white' or 'black'.")

    # Calculate eGFR using MDRD equation
    if gender == "female":
        if race == "black":
            a, b, c = 175, 1.154, 0.203
        else:
            a, b, c = 144, 0.7, 0.7
    else: # gender == "male"
        if race == "black":
            a, b, c = 163, 1.212, 0.212
        else:
            a, b, c = 141, 0.9, 0.9

    egfr = a * (serum_creatinine ** b) * (age ** c)
    return egfr

# Example usage
try:
    age = int(input("Enter age: "))
    gender = input("Enter gender (male/female): ")
    serum_creatinine = float(input("Enter serum creatinine level (mg/dL): "))
    race = input("Enter race (white/black): ")

    egfr = calculate_egfr(age, gender, serum_creatinine, race)
    print("eGFR:", egfr)

except ValueError as e:
    print("Error:", str(e))

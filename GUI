import tkinter as tk
from tkinter import messagebox

def calculate_egfr():
    try:
        age = int(age_entry.get())
        gender = gender_entry.get()
        serum_creatinine = float(serum_creatinine_entry.get())
        race = race_entry.get()

        egfr = calculate_egfr(age, gender, serum_creatinine, race)
        result_label.config(text="eGFR: {:.2f}".format(egfr))
    except ValueError as e:
        messagebox.showerror("Error", str(e))

root = tk.Tk()
root.title("eGFR Calculator")

# Age
age_label = tk.Label(root, text="Age:")
age_label.grid(row=0, column=0, padx=5, pady=5)
age_entry = tk.Entry(root)
age_entry.grid(row=0, column=1, padx=5, pady=5)

# Gender
gender_label = tk.Label(root, text="Gender:")
gender_label.grid(row=1, column=0, padx=5, pady=5)
gender_entry = tk.Entry(root)
gender_entry.grid(row=1, column=1, padx=5, pady=5)

# Serum Creatinine
serum_creatinine_label = tk.Label(root, text="Serum Creatinine (mg/dL):")
serum_creatinine_label.grid(row=2, column=0, padx=5, pady=5)
serum_creatinine_entry = tk.Entry(root)
serum_creatinine_entry.grid(row=2, column=1, padx=5, pady=5)

# Race
race_label = tk.Label(root, text="Race:")
race_label.grid(row=3, column=0, padx=5, pady=5)
race_entry = tk.Entry(root)
race_entry.grid(row=3, column=1, padx=5, pady=5)

# Calculate Button
calculate_button = tk.Button(root, text="Calculate", command=calculate_egfr)
calculate_button.grid(row=4, column=0, columnspan=2, padx=5, pady=5)

# Result Label
result_label = tk.Label(root, text="")
result_label.grid(row=5, column=0, columnspan=2, padx=5, pady=5)

root.mainloop()

def calculate_dosage(weight, age, concentration, bsa, creatinine_clearance):
    # Perform dosage calculation based on the given parameters
    if age < 18:
        dosage = weight * concentration
    else:
        dosage = weight * concentration * bsa

    if creatinine_clearance < 30:
        dosage *= 0.5 # Adjust dosage for decreased renal function

    return dosage

# Prompt user for input
weight = float(input("Enter patient weight in kg: "))
age = int(input("Enter patient age in years: "))
concentration = float(input("Enter desired concentration: "))
bsa = float(input("Enter patient's Body Surface Area (BSA): "))
creatinine_clearance = float(input("Enter patient's creatinine clearance: "))

# Calculate dosage
dosage = calculate_dosage(weight, age, concentration, bsa, creatinine_clearance)

# Print the calculated dosage
print("The calculated dosage is:", dosage)

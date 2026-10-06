# AC and DC Power Calculation
# DC Power: P = V * I
# AC Power: P = V * I * Power Factor

print("AC and DC Power Calculator")
print("1. DC Power")
print("2. AC Power")

choice = int(input("Enter your choice (1 or 2): "))

if choice == 1:
    voltage = float(input("Enter DC voltage (V): "))
    current = float(input("Enter DC current (A): "))

    power = voltage * current

    print("DC Power =", round(power, 2), "W")

elif choice == 2:
    voltage = float(input("Enter AC voltage (V): "))
    current = float(input("Enter AC current (A): "))
    power_factor = float(input("Enter power factor: "))

    if 0 <= power_factor <= 1:
        power = voltage * current * power_factor
        print("AC Real Power =", round(power, 2), "W")
    else:
        print("Power factor must be between 0 and 1.")

else:
    print("Invalid choice. Please select 1 or 2.")
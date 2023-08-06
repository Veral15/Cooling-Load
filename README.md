# Cooling-Load
tells the cooling load 
area = int(input("Enter the Area of the Building "))
occupants = int(input("Enter the Number of occupants in the Building "))
btype = input("Enter the Type of Building (residential/commercial): ").lower()

while btype not in ["residential", "commercial"]:
    print("Choose from 'residential' or 'commercial'.")
    btype = input("Enter the Type of Building (residential/commercial): ").lower()


otemp = int(input("Enter the Outdoor Temperature (In Celcius) "))
itemp = int(input("Enter the Indoor Temperature (In Celcius) "))

if btype == "residential":
        cload = 100 * occupants
elif btype == "commercial":
        cload = 150 * occupants

U = 30

Q_conduction = U * area * (otemp - itemp)
sensible_cooling_load = Q_conduction + cload


print(f"The sensible cooling load is {sensible_cooling_load} Watts. ")


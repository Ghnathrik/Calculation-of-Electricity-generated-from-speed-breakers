# Constants
speed_breaker_length = 4.0  # meters
speed_breaker_width = 2.5  # meters
speed_breaker_thickness = 0.1  # meters
piezoelectric_coefficient = 0.1  # Piezoelectric coefficient (arbitrary units)
compression_force = 5000  # Newtons (force exerted by vehicles on the speed breaker)

# Function to calculate generated voltage
def calculate_voltage(length, width, thickness, coefficient, force):
    area = length * width
    voltage = coefficient * area * thickness * force
    return voltage

# Simulation
voltage_generated = calculate_voltage(speed_breaker_length, speed_breaker_width, speed_breaker_thickness, piezoelectric_coefficient, compression_force)
print("Voltage generated: {:.2f} volts".format(voltage_generated))
# Constants
voltage_generated = (piezoelectric_coefficient * speed_breaker_length*speed_breaker_width*speed_breaker_thickness *compression_force)  # volts (example voltage generated from speed breaker)
load_resistance = 10  # ohms (example load resistance)

# Function to calculate current using Ohm's Law (I = V / R)
def calculate_current(voltage, resistance):
    current = voltage / resistance
    return current

# Function to calculate Electricity using P = VI
def calculate_Electricity(voltage, current):
    Electricity = voltage * current
    return Electricity

# Simulation
current = calculate_current(voltage_generated, load_resistance)
Electricity_generated = calculate_Electricity(voltage_generated, current)

print("Current flowing through the load: {:.2f} amperes".format(current))
print("Electricity generated: {:.2f} watts".format(Electricity_generated))# Calculation-of-Electricity-generated-from-speed-breakers

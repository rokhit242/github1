# transformer.py
# Simple Transformer simulation

class Transformer:
    def __init__(self, name, primary_voltage, turns_ratio):
        self.name = name
        self.primary_voltage = primary_voltage
        self.turns_ratio = turns_ratio  # Np/Ns
        self.secondary_voltage = 0

    def calculate_secondary_voltage(self):
        self.secondary_voltage = self.primary_voltage / self.turns_ratio
        return self.secondary_voltage

    def status(self):
        return (f"{self.name}: Primary Voltage = {self.primary_voltage} V, "
                f"Turns Ratio = {self.turns_ratio}, "
                f"Secondary Voltage = {self.secondary_voltage:.2f} V")

# Example usage
if __name__ == "__main__":
    transformer1 = Transformer("Transformer A", 230, 10)
    print("Secondary Voltage:", transformer1.calculate_secondary_voltage())
    print(transformer1.status())

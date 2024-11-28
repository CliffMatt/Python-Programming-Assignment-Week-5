# Python-Programming-Assignment-Week-5
Assignment
# Parent Class
class Smartphone:
    def __init__(self, brand, model, price):
        self.brand = brand
        self.model = model
        self.price = price

    def get_details(self):
        return f"{self.brand} {self.model} costs ${self.price}"

# Child Class for Advanced Smartphones
class AdvancedSmartphone(Smartphone):
    def __init__(self, brand, model, price, camera_quality, battery_life):
        super().__init__(brand, model, price)
        self.camera_quality = camera_quality
        self.battery_life = battery_life

    def get_details(self):
        return (f"{self.brand} {self.model} costs ${self.price}, has a {self.camera_quality}MP camera, "
                f"and lasts {self.battery_life} hours on a full charge.")

# Creating objects
basic_phone = Smartphone("Nokia", "3310", 50)
advanced_phone = AdvancedSmartphone("Apple", "iPhone 14", 999, 48, 20)

# Printing details
print(basic_phone.get_details())  # Output: Nokia 3310 costs $50
print(advanced_phone.get_details())  # Output: Apple iPhone 14 costs $999, has a 48MP camera, and lasts 20 hours on a full charge


# Parent Class
class Vehicle:
    def move(self):
        pass  # Placeholder for polymorphic behavior

# Subclasses with different implementations of move()
class Car(Vehicle):
    def move(self):
        return "Driving 🚗"

class Plane(Vehicle):
    def move(self):
        return "Flying ✈️"

class Boat(Vehicle):
    def move(self):
        return "Sailing 🚤"

# Function to demonstrate polymorphism
def demonstrate_movement(vehicle):
    print(vehicle.move())

# Creating objects
car = Car()
plane = Plane()
boat = Boat()

# Demonstrating polymorphism
demonstrate_movement(car)    # Output: Driving 🚗
demonstrate_movement(plane)  # Output: Flying ✈️
demonstrate_movement(boat)   # Output: Sailing 🚤

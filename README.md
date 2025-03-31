# git-clone-repository_url-
Add OOP class design and polymorphism examples
# Parent class (base class)
class Device:
    def __init__(self, brand, model):
        self.brand = brand
        self.model = model

    def display_info(self):
        return f"Brand: {self.brand}, Model: {self.model}"

# Smartphone class inheriting from Device class
class Smartphone(Device):
    def __init__(self, brand, model, os, battery_life):
        super().__init__(brand, model)  # Inherit from Device class
        self.os = os
        self.battery_life = battery_life  # Battery life in hours

    def make_call(self, number):
        return f"Calling {number}..."

    def charge(self):
        return f"Charging the {self.brand} {self.model}."

    def display_info(self):
        # Overriding the method to include smartphone-specific details
        return f"{super().display_info()}, OS: {self.os}, Battery Life: {self.battery_life} hours"

# Example usage
phone = Smartphone("Apple", "iPhone 13", "iOS", 20)
print(phone.display_info())  # Displays information about the smartphone
print(phone.make_call("123-456-7890"))  # Calls a number
print(phone.charge())  # Charging the phone
# Base class
class Vehicle:
    def move(self):
        print("This vehicle is moving")

# Car class inherits from Vehicle
class Car(Vehicle):
    def move(self):
        print("Driving 🚗")

# Plane class inherits from Vehicle
class Plane(Vehicle):
    def move(self):
        print("Flying ✈️")

# Boat class inherits from Vehicle
class Boat(Vehicle):
    def move(self):
        print("Sailing ⛵")

# Example usage
vehicles = [Car(), Plane(), Boat()]

for vehicle in vehicles:
    vehicle.move()  # Polymorphism: Different behavior for each class

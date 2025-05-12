# # Python OOP Practice: Classes, Inheritance, and Polymorphism

This project includes two activities to practice Object-Oriented Programming (OOP) concepts in Python: creating classes, using inheritance, and exploring polymorphism.

## Assignment 1: Design Your Own Class 🏗️

### Objective
Design a class representing a **Smartphone** with attributes and methods. Use inheritance to create specialized classes with unique behaviors.

### Example

We designed a base class `Smartphone` with attributes like `brand`, `model`, and `storage`, and methods like `call()` and `take_picture()`. We also created a derived class `CameraPhone` that overrides the `take_picture()` method to provide a specialized behavior for high-resolution photos.

```python
# Base Class: Smartphone
class Smartphone:
    def __init__(self, brand, model, storage):
        self.brand = brand
        self.model = model
        self.storage = storage

    def call(self, number):
        print(f"Calling {number}...")

    def take_picture(self):
        print(f"Taking a picture with the {self.model} camera!")

# Derived Class: CameraPhone
class CameraPhone(Smartphone):
    def __init__(self, brand, model, storage, camera_resolution):
        super().__init__(brand, model, storage)
        self.camera_resolution = camera_resolution

    def take_picture(self):
        print(f"Taking a high-res picture with {self.camera_resolution}MP camera!")

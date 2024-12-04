# ASSIGNMENT-WEEK-5
CLASS DESIGN

class Smartphone:
    def __init__(self, brand, model, battery_life, price):
        # Constructor to initialize the attributes
        self.brand = brand
        self.model = model
        self.battery_life = battery_life
        self.price = price

    def make_call(self, number):
        # Method to simulate making a call
        print(f"Calling {number} from {self.brand} {self.model}...")

    def send_message(self, number, message):
        # Method to simulate sending a message
        print(f"Sending message to {number}: {message}")

    def check_battery(self):
        # Method to check battery life
        print(f"Battery life is {self.battery_life} hours.")

# Inheritance Example: LuxurySmartphone that inherits from Smartphone
class LuxurySmartphone(Smartphone):
    def __init__(self, brand, model, battery_life, price, luxury_features):
        # Inherit from Smartphone and add extra features
        super().__init__(brand, model, battery_life, price)
        self.luxury_features = luxury_features

    def show_luxury_features(self):
        print(f"Luxury Features of {self.brand} {self.model}: {', '.join(self.luxury_features)}")

# Creating objects of both classes
basic_phone = Smartphone("Samsung", "Galaxy S21", 20, 799)
luxury_phone = LuxurySmartphone("Apple", "iPhone 14 Pro Max", 24, 1099, ["Gold-Plated Body", "Diamond-Encrusted Back"])

# Calling methods
basic_phone.make_call("123-456-7890")
luxury_phone.send_message("123-456-7890", "Luxury message from iPhone!")
luxury_phone.show_luxury_features()


#TASK 2
POLYMORPHISM CHALLENGE
POLYMORPHISM WITH ANIMALS

class Animal:
    def move(self):
        raise NotImplementedError("Subclasses must implement the move method")

class Dog(Animal):
    def move(self):
        print("The dog is running on four legs! 🐕")

class Bird(Animal):
    def move(self):
        print("The bird is flying in the sky! 🐦")

class Fish(Animal):
    def move(self):
        print("The fish is swimming in the water! 🐟")

# Creating instances of different animals
dog = Dog()
bird = Bird()
fish = Fish()

# Calling the move method for each animal
animals = [dog, bird, fish]

for animal in animals:
    animal.move()

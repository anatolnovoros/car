# car
class Car:
    def __init__(self, make, model, year, color):
        self.make = make
        self.model = model
        self.year = year
        self.color = color
        self.odometer_reading = 0

    def get_descriptive_name(self):
        return f"{self.year} {self.color} {self.make} {self.model}"

    def read_odometer(self):
        return f"This car has {self.odometer_reading} miles on it."

    def update_odometer(self, mileage):
        if mileage >= self.odometer_reading:
            self.odometer_reading = mileage
            print("Odometer has been updated.")
        else:
            print("You can't roll back an odometer!")

    def increment_odometer(self, miles):
        self.odometer_reading += miles
        print("Odometer has been incremented.")


def main():
    my_car = Car("Toyota", "Corolla", 2022, "Red")

    print("Car details:", my_car.get_descriptive_name())
    print(my_car.read_odometer())

    my_car.update_odometer(100)
    my_car.increment_odometer(50)

    print(my_car.read_odometer())


if __name__ == "__main__":
    main()

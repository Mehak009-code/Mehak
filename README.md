// Base class
class Animal {
    public void makeSound() {
        System.out.println("Some generic animal sound");
    }
}

// Derived class Dog
class Dog extends Animal {
    @Override
    public void makeSound() {
        System.out.println("Woof! Woof!");
    }
}

// Derived class Cat
class Cat extends Animal {
    @Override
    public void makeSound() {
        System.out.println("Meow! Meow!");
    }
}

// Main class to demonstrate polymorphism
public class AnimalSoundDemo {
    public static void main(String[] args) {
        // Create an Animal reference that can hold a Dog object
        Animal myDog = new Dog();
        // Create an Animal reference that can hold a Cat object
        Animal myCat = new Cat();

        // Call the makeSound() method on both objects
        myDog.makeSound(); // Outputs: Woof! Woof!
        myCat.makeSound(); // Outputs: Meow! Meow!

        // Demonstrating polymorphism with an array of Animals
        Animal[] animals = {new Dog(), new Cat()};

        // Loop through the array and call makeSound() on each animal
        for (Animal animal : animals) {
            animal.makeSound(); // Outputs the specific sound for each animal
        }
    }
}

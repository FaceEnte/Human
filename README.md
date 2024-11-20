# Human

This project implements a simple class hierarchy in Java to represent a `Human` and a subclass `Athlete`. The goal is to demonstrate method overriding in inheritance.

## Class Hierarchy

### Human
- **Method**:
    - `public void run()`: Prints "Running like an average human."

### Athlete (extends Human)
- **Method**:
    - `public void run()`: Overrides the method from `Human` to print "Running really fast."

## Example Implementation

### Human.java
```java
public class Human {
    public void run() {
        System.out.println("Running like an average human.");
    }
}
```

### Athlete.java
```java
public class Athlete extends Human {
    @Override
    public void run() {
        System.out.println("Running really fast.");
    }
}
```

### Test Class
```java
public class TestClass {
    public static void main(String[] args) {
        Human human = new Human();
        Athlete athlete = new Athlete();

        System.out.println("Human:");
        human.run();  // Calls the run method of Human

        System.out.println("\nAthlete:");
        athlete.run();  // Calls the overridden run method of Athlete
    }
}
```

## What to Notice

1. When you create an object of the `Human` class and call the `run()` method, it outputs:
   ```
   Running like an average human.
   ```

2. When you create an object of the `Athlete` class and call the `run()` method, it outputs:
   ```
   Running really fast.
   ```

3. The key observation here is that the `Athlete` class overrides the `run()` method from the `Human` class. This demonstrates polymorphism in Java, where the method that gets executed is determined at runtime based on the object type.

## Getting Started

1. **Create the `Human` and `Athlete` classes**: Implement the classes as specified above.
2. **Write a test class**: Implement the `TestClass` to create instances of `Human` and `Athlete`, and call their `run()` methods.
3. **Compile and run the program**: Ensure that you have the necessary Java environment set up to compile and run the program.

## Notes

- You can extend the functionality of these classes by adding more attributes and methods as needed.

Happy coding! 🎉
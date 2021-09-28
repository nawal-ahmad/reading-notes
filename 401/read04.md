# Read: 04 - OOP

## Java OO Tutorial:

- **An object** is a software bundle of related state and behavior, Software objects are often used to model the real-world objects that you find in everyday life, ex: car.

- All objects share two characteristics state and behavior.

**example**: Dogs have state (name, color, breed), ...etc and behavior (barking, fetching, ..etc)

- Software objects are conceptually similar to real world objects, they also consist of state and related behavior.
- object stores the state in fields (variables or properties) and behavior expressed through methods (functions).

- **A class** is a blueprint or prototype from which objects are created

- Class and instance (object) example:

  ```java
  class Bicycle {
    //fields
    int cadence = 0;
    int speed = 0;
    int gear = 1;
    //methods
    void changeCadence(int newValue) {
         cadence = newValue;
    }

    void changeGear(int newValue) {
         gear = newValue;
    }
  }

  // create instances on other class
  class BicycleDemo {
    public static void main(String[] args) {

        // Create two different
        // Bicycle objects
        Bicycle bike1 = new Bicycle();
        Bicycle bike2 = new Bicycle();

        // Invoke methods on
        // those objects
        bike1.changeCadence(50);
        bike2.changeCadence(60);
    }
  }

  ```

- Example of class and subclass

```java
public class Bicycle {

  // the Bicycle class has
  // three fields
  public int cadence;
  public int gear;
  public int speed;

  // the Bicycle class has
  // one constructor
  public Bicycle(int startCadence, int startSpeed, int startGear) {
      gear = startGear;
      cadence = startCadence;
      speed = startSpeed;
  }

  // the Bicycle class has
  // four methods
  public void setCadence(int newValue) {
      cadence = newValue;
  }
  public void setGear(int newValue) {
      gear = newValue;
  }
  public void applyBrake(int decrement) {
      speed -= decrement;
  }
  public void speedUp(int increment) {
      speed += increment;
  }
}
```

A class declaration for a class is a (subclass) look like this:

```java
public class MountainBike extends Bicycle {

  // the MountainBike subclass has
  // one field
  public int seatHeight;

  // the MountainBike subclass has
  // one constructor
  public MountainBike(int startHeight, int startCadence,
                      int startSpeed, int startGear) {
      super(startCadence, startSpeed, startGear);
      seatHeight = startHeight;
  }

  // the MountainBike subclass has
  // one method
  public void setHeight(int newValue) {
      seatHeight = newValue;
  }
}
```

## Binary, Decimal and Hexadecimal Numbers:

- Base 10 (Decimal) — > Represent any number using 10 digits (0–9).
- Base 2 (Binary) — > Represent any number using 2 digits (0–1).
- Base 16(Hexadecimal) — > Represent any number using 10 digits and 6 characters (0–9, A, B, C, D, E, F).

\


## References:

[Java OO Tutorial](https://docs.oracle.com/javase/tutorial/java/concepts/)
<br/>

[Java Classes](https://docs.oracle.com/javase/tutorial/java/javaOO/classes.html)
<br/>

[Binary, Decimal and Hexadecimal Numbers](https://www.mathsisfun.com/binary-decimal-hexadecimal.html)

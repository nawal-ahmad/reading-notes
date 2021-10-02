# Read: 06 - Inheritance and Interfaces


## Object-Oriented Programming Concepts

### Inheritance 

- when a different objects have share some common characteristics, object oriented programming **(OOP)** allow classes to inherit commonly used state and behavior from other classes.

- In java programming language, each class is allowed to have one one direct superclass, and each superclass is allowed to have unlimited number of subclasses. 

- subclass: is a class that is derived from another class, also known as (derived class, extended class, or child class).

- superclass: is the class from which the subclass is derived, also known as (base class or a parent class).

- `Classes can be derived from classes that are derived from classes that are derived from classes, and so on.`

- Subclass does not inherit the private members of its parent class.

- if the superclass has public or protected methods for accessing its private fields, these can also be used by the subclass.


![inheritance](https://www.scientecheasy.com/wp-content/uploads/2020/07/java-is-a-relationship.png)

**The syntax for creating a subclass:**

```
class MountainBike extends Bicycle {

    // new fields and methods defining 
    // a mountain bike would go here

}
```

## Interface

- An interface: is a group of related methods with empty bodies.

- **In java** an interface is: a reference type, similar to a class, that can contain only constants, method signatures, default methods, static methods, and nested types.

- Interfaces cannot be instantiated.

- Interfaces can only be implemented by classes or extended by other interfaces.

example:

```
interface Bicycle {

    //  wheel revolutions per minute
    void changeCadence(int newValue);

    void changeGear(int newValue);

    void speedUp(int increment);

    void applyBrakes(int decrement);
}
```

 **Implementing an interface** allows a class becoming more formal about the behavior it promises to provide interfaces form a contract between the class and the outside world, and this contract is enforced at build time by the compiler.
  If your class implement an interface, all methods defined by that interface must appear in its source code before the class will successfully compile. 

![interface](https://pediaa.com/wp-content/uploads/2018/09/Difference-Between-Abstract-Class-and-Interface-in-Java-Comparison-Summary-700x1024.jpg)


## Package

- A package: is a name space that organizes a set of related classes and interfaces.

- Java platform provides an enormous class library (set of packages) suitable for use in  applications. This library known as the "Application Programming Interface" => **API**.


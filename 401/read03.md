# Read: 03 - Maps, primitives, File I/O

## Java Primitives versus Objects

- java has 2 type system for folding consisting of:
    - primitives: such as int and boolean.
    - reference types: such as Integer and Boolean.


### Primitive:

- Every primitive type corresponds to a reference type.
- wrapper classes are immutable and are final.
- auto-boxing: converting a primitive type to a reference type.
- unboxing: converting a reference type to a primitive type.

**- Single primitive item size in memory:**
    - boolean – 1 bit
    - byte – 8 bits
    - short, char – 16 bits
    - int, float – 32 bits
    - long, double – 64 bits

### Reference

- The reference types are objects, they live on the heap and are relatively slow to access in relative to primitives.

**- Single reference item size in memory:**
    - Boolean – 128 bits
    - Byte – 128 bits
    - Short, Character – 128 bits
    - Integer, Float – 128 bits
    - Long, Double – 192 bits

- primitive type live in the stack and they are accessed fast.
- arrays of the primitive types long and double need more memory than their wrapper classes Long and Double
- single-element arrays of primitive types are almost always more expensive (except for long and double) than the corresponding reference type.
- Java language specification doesn't allow usage of primitive types in the parametrized types, in the Java collections or the Reflection API.


## Exceptions in Java

### What Is an Exception?

- An exception: is an event, which occurs during the execution of a program, that disrupts the normal flow of the program's instructions.

![Call Stack](/401/img/call-stack.png)
![searching for exception](/401/img/searching-for-exception.png)

- Exception object: created when an error occurs whithin a method, and contains information about the error, including its type and the state of the program when the error occur.

- Exception Handler components are: -->try, catch & finally

The code might throw exceptions must be enclosed by:
1. try statement that catches the exception. 
2. the method that specifies that it can throw the exception.

### throwable classes :
![throwable](https://docs.oracle.com/javase/tutorial/figures/essential/exceptions-throwable.gif)
   


## Using Scanner to read in a file in Java

- We use scanning to break down formatted input into tokens and translate individual tokens according to their type, treats all input tokens as simple String values.
- We have to mention the locale, because thousands separators and decimal symbols are locale specific.

```
import java.io.FileReader;
import java.io.BufferedReader;
import java.io.IOException;
import java.util.Scanner;
import java.util.Locale;

public class ScanSum {
    public static void main(String[] args) throws IOException {

        Scanner s = null;
        double sum = 0;

        try {
            s = new Scanner(new BufferedReader(new FileReader("usnumbers.txt")));
            s.useLocale(Locale.US);

            while (s.hasNext()) {
                if (s.hasNextDouble()) {
                    sum += s.nextDouble();
                } else {
                    s.next();
                }
            }
        } finally {
            s.close();
        }

        System.out.println(sum);
    }
}
```


## References

[Primitives vs. Objects](https://www.baeldung.com/java-primitives-vs-objects)
<br/>

[Exceptions in Java ](https://docs.oracle.com/javase/tutorial/essential/exceptions/index.html)
<br/>

[Using Scanner to read in a file in Java](https://docs.oracle.com/javase/tutorial/essential/io/scanning.html)
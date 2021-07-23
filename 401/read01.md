# read01

## Pain vs. Suffering

It is important to prepare ourselves mentally for the pain we’re expected to experience in the coming 10-week spectacular learning journey. A good thing to keep in mind is that the pain won’t be aimless, it won’t be suffering. It will be pain in favor of growth.

- The pain that we will experience during this course:

* mentally, having to think your way through problems that you had only even heard about a few hours beforehand.
* emotionally, constantly confronted with your own lack of understanding of a topic.

**_The greater the growth, the greater the pain._**

</br></br>

## A beginner's guide to Big O notation

**_Big O notation :_** describe the performance or complexity of an algorithm. Big O specifically describes the worst-case scenario, and can be used to describe the execution time required or the space used (e.g. in memory or on disk) by an algorithm.

![BigO](401/images/BigO.jpg)

**_O(1) :_** describes an algorithm that will always execute in the same time (or space) regardless of the size of the input data set.

```
bool IsFirstElementNull(IList<String> elements)
{
    return elements[0] == null;
}
```

**_O(N) :_** describes an algorithm whose performance will grow linearly and in direct proportion to the size of the input data set

```
bool ContainsValue(IEnumerable<string> elements, string value)
{
    foreach (var element in elements)
    {
        if (element == value) return true;
    }
    return false;
}
```

**_O(N2) :_** represents an algorithm whose performance is directly proportional to the square of the size of the input data set.

```
bool ContainsDuplicates(IList<string> elements)
{
    for (var outer = 0; outer < elements.Count; outer++)
    {
        for (var inner = 0; inner < elements.Count; inner++)
        {
            // Don't compare with self
            if (outer == inner) continue;

            if (elements[outer] == elements[inner]) return true;
        }
    }
    return false;
}
```

**_O(2N) :_** denotes an algorithm whose growth doubles with each additon to the input data set.

```
int Fibonacci(int number)
{
    if (number <= 1) return number;

    return Fibonacci(number - 2) + Fibonacci(number - 1);
}
```

**_O(log N) :_** The iterative halving of data sets produces a growth curve that peaks at the beginning and slowly flattens out as the size of the data sets increase

</br></br>

## Facts and Myths about Python names and values

### Facts

- Names refer to values.
- Many names can refer to one value.
- Names are reassigned independently.
- Values live until no references.
- Assignment never copies data.
- Changes are visible through all names.
- Immutable values such as _ints_, _floats_ _strings_ _tuples_, can't alias
- Types of changes:
  - Changing an int: **rebinding**
  - Changing a list: **mutating**
- Reference can be more than just names, they can be:
  - Object attributes.
  - List elements.
  - Dictionaries values(and Keys).
  - Anything on the left side of an assignment.
- Lots of things are assignments.
- Names have no types and Values have no scope.

### Myths

- Mutable and immutable are assigned the same.
- Python has no variables.

</br></br>

## How to Setup an Awesome Python Environment for Data Science or Anything Else

**The most important thing when working with python: the interpreter.**

**Pyenv :** Pyenv is a set of three tools, from which I present two here, that are pyenv(used to install python) and pyenv-virtualenv(used to configure your global tools).

- we can use pyenv to install almost any python interpreter, including pypy, and anaconda,etc ..

**Dependency Management**

**Poetry :** comes with all the tools you might need to manage your projects dependencies in a deterministic way.

**\*poetry helps us to easily :**

- manage projects’ dependencies

- separate projects through virtual environments

- build both applications as well as libraries without headaches

* Coding in Python is awesome due to the massive amount of freely available libraries, its readability, and the recently introduced type annotations.

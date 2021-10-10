# Read: 12 - Spring RESTful Routing & Static Files

## RequestMapping Basics

```
@RequestMapping(value = "/ex/foos", method = RequestMethod.GET)
@ResponseBody
public String getFoosBySimplePath() {
    return "Get some Foos";
}
```

+ @RequestMapping — the HTTP Method

```
@RequestMapping(value = "/ex/foos", method = POST)
@ResponseBody
public String postFoos() {
    return "Post some Foos";
}
```

### RequestMapping and HTTP Headers
+ @RequestMapping With the headers Attribute

```
@RequestMapping(value = "/ex/foos", headers = "key=val", method = GET)
@ResponseBody
public String getFoosWithHeader() {
    return "Get some Foos with Header";
}
```

+ @RequestMapping Consumes and Produces

```
@RequestMapping(
  value = "/ex/foos", 
  method = GET, 
  headers = "Accept=application/json")
@ResponseBody
public String getFoosAsJsonFromBrowser() {
    return "Get some Foos with Header Old";
}
```

### RequestMapping With Path Variables
+  Single @PathVariable

```
@RequestMapping(value = "/ex/foos/{id}", method = GET)
@ResponseBody
public String getFoosBySimplePathWithPathVariable(
  @PathVariable("id") long id) {
    return "Get a specific Foo with id=" + id;
}
```

+ Multiple @PathVariable

```
@RequestMapping(value = "/ex/foos/{fooid}/bar/{barid}", method = GET)
@ResponseBody
public String getFoosBySimplePathWithPathVariables
  (@PathVariable long fooid, @PathVariable long barid) {
    return "Get a specific Bar with id=" + barid + 
      " from a Foo with id=" + fooid;
}
```

## Accessing Data with JPA
**Spring Boot** JPA is a Java specification for managing relational data in Java applications.
It allows us to access and persist data between Java object/ class and relational database.
**JPA** follows Object-Relation Mapping (ORM), It is a set of interfaces and it is also provides a runtime Entity Manager API for processing queries and transactions on the objects against the database. 
It uses a platform-independent object-oriented query language JPQL (Java Persistent Query Language).


### starting spring initializer
1. Spring Initializr to generate new project with the required dependencies, here is the build gradle file content:

```
plugins {
	id 'org.springframework.boot' version '2.5.2'
	id 'io.spring.dependency-management' version '1.0.11.RELEASE'
	id 'java'
}

group = 'com.example'
version = '0.0.1-SNAPSHOT'
sourceCompatibility = '1.8'

repositories {
	mavenCentral()
}

dependencies {
	implementation 'org.springframework.boot:spring-boot-starter-thymeleaf'
	implementation 'org.springframework.boot:spring-boot-starter-web'
	developmentOnly 'org.springframework.boot:spring-boot-devtools'
	testImplementation 'org.springframework.boot:spring-boot-starter-test'
}

test {
	useJUnitPlatform()
}
```

2. manual initialization: when we want to manually initialize the project we must follow some steps:
- navigate to https://start.spring.io .
- choose gradle and java as the language . 
- click dependencies and select spring web, thymeleaf, and spring boot devtools.
- click generate.
- Download the resulting ZIP file, which is an archive of a web application that is configured with your choices.


## CrudRepository

example of **CRUD** repository interface:

```
public interface CrudRepository<T, ID extends Serializable>
  extends Repository<T, ID> {

    <S extends T> S save(S entity);

    T findOne(ID primaryKey);

    Iterable<T> findAll();

    Long count();

    void delete(T entity);

    boolean exists(ID primaryKey);
}
```

### CRUD functionality:

- save(…): save an Iterable of entities. Here, we can pass multiple objects to save them in a batch
- findOne(…): get a single entity based on passed primary key value
- findAll(): get an Iterable of all available entities in database
- count(): return the count of total entities in a table
- delete(…): delete an entity based on the passed object
- exists(…): verify if an entity exists based on the passed primary key value


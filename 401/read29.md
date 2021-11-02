# Read: 29 - Room

 **Room**: is a persistence library which provides an abstraction layer over SQLite to allow fluent database access while harnessing the full power of SQLite.


## benefits of using Room

- Compile-time verification of SQL queries.
- Convenience annotations that minimize repetitive.
- Streamlined database migration paths.

*the above benefits makes using Room is much better than using the SQL API's directly.*

## Setup
in order to use Room there are some setups which you must add to your application dependencies:

```
dependencies {
    def room_version = "2.3.0"

    implementation "androidx.room:room-runtime:$room_version"
    annotationProcessor "androidx.room:room-compiler:$room_version"

    // optional - RxJava2 support for Room
    implementation "androidx.room:room-rxjava2:$room_version"

    // optional - RxJava3 support for Room
    implementation "androidx.room:room-rxjava3:$room_version"

    // optional - Guava support for Room, including Optional and ListenableFuture
    implementation "androidx.room:room-guava:$room_version"

    // optional - Test helpers
    testImplementation "androidx.room:room-testing:$room_version"

    // optional - Paging 3 Integration
    implementation "androidx.room:room-paging:2.4.0-alpha04"
}
```

## Primary components

Room has three main components which are :

1. The **database class**, under some conditions:

- The class must be annotated with a @Database annotation that includes an entities array that lists all of the data entities associated with the database.
- The class must be an abstract class that extends RoomDatabase.
- For each DAO class that is associated with the database, the database class must define an abstract method that has zero arguments and returns an instance of the DAO class.

syntax example:

```
@Database(entities = {User.class}, version = 1)
public abstract class AppDatabase extends RoomDatabase {
    public abstract UserDao userDao();
}
```

2. **Data entities**, example of its syntax:

```
@Entity
public class User {
    @PrimaryKey
    public int uid;

    @ColumnInfo(name = "first_name")
    public String firstName;

    @ColumnInfo(name = "last_name")
    public String lastName;
}
```

3. **Data access objects** (DAOs), here is an example of its syntax:

```
@Dao
public interface UserDao {
    @Query("SELECT * FROM user")
    List<User> getAll();

    @Query("SELECT * FROM user WHERE uid IN (:userIds)")
    List<User> loadAllByIds(int[] userIds);

    @Query("SELECT * FROM user WHERE first_name LIKE :first AND " -
           "last_name LIKE :last LIMIT 1")
    User findByName(String first, String last);

    @Insert
    void insertAll(User... users);

    @Delete
    void delete(User user);
}
```

![room](https://media.geeksforgeeks.org/wp-content/uploads/20210506144355/output.png)



### Defining data using entities

we use the define entities to represent the objects we want to store in the database, and each entity corresponds to a table in the associated Room database, and each instance of an entity represents a row of data in the corresponding table.

- Each Room entity must define a primary key, The most straightforward way of doing this is to annotate a single column with @PrimaryKey.

- to assign automatic IDs to entity instances, set the autoGenerate property of @PrimaryKey to true.

- If an entity has fields that you don't want to persist, you can annotate them using @Ignore.

- if an entity inherits fields from a parent entity, use the ignoredColumns property of the @Entity attribute.

### relationships between objects in database

**embedded objects:**
we use it when we have a class which has a field of type other class, here is the syntax:

```
public class Address {
    public String street;
    public String state;
    public String city;

    @ColumnInfo(name = "post_code") public int postCode;
}

@Entity
public class User {
    @PrimaryKey public int id;

    public String firstName;

    @Embedded public Address address;
}
```

**one-to-one relationships**
we use it when each instance of the parent entity corresponds to exactly one instance of the child entity.
sytax example:

```
@Entity
public class User {
    @PrimaryKey public long userId;
    public String name;
    public int age;
}

@Entity
public class Library {
    @PrimaryKey public long libraryId;
    public long userOwnerId;
}
```

**one-to-many relationships**
when each instance of the parent entity corresponds to zero or more instances of the child entity, but each instance of the child entity can only correspond to exactly one instance of the parent entity.

**many-to-many relationships**
where each instance of the parent entity corresponds to zero or more instances of the child entity, and vice-versa.

**nested relationships**
when three or more tables are all related to each other.

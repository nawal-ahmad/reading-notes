# Read: 18 - Web App Security

## Hibernate Many to Many 

simple Entity relationship **many to many**:

![img](https://cdn.journaldev.com/wp-content/uploads/2014/05/Many-To-Many-Mapping-Tables.png)

In this scenario, any given item can be assigned to multiple carts and a cart may have multiple items in it, leading to a **many-to-many** association between the two.

- In the model classes there is some additional code we have to write in order to make a many to many relation, example:

```
@Entity
@Table(name = "Employee")
public class Employee { 
    // ...
 
    @ManyToMany(cascade = { CascadeType.ALL })
    @JoinTable(
        name = "Employee_Project", 
        joinColumns = { @JoinColumn(name = "employee_id") }, 
        inverseJoinColumns = { @JoinColumn(name = "project_id") }
    )
    Set<Project> projects = new HashSet<>();
   
    // standard constructor/getters/setters
}
```

```
@Entity
@Table(name = "Project")
public class Project {    
    // ...  
 
    @ManyToMany(mappedBy = "projects")
    private Set<Employee> employees = new HashSet<>();
    
    // standard constructors/getters/setters   
}
```

- in the previous example we can see that both the Employee class and Project classes refer to one another, which means that the association between them is bidirectional.

- The **@ManyToMany** annotation is used in both classes to create the many-to-many relationship between the entities.

- This association has two sides i.e. the owning side and the inverse side. In our example, the owning side is Employee so the join table is specified on the owning side by using the @JoinTable annotation in Employee class. The @JoinTable is used to define the join/link table. In this case, it is Employee_Project.

- The @JoinColumn annotation is used to specify the join/linking column with the main table. Here, the join column is employee_id and project_id is the inverse join column since Project is on the inverse side of the relationship.

- In the Project class, the mappedBy attribute is used in the @ManyToMany annotation to indicate that the employees collection is mapped by the projects collection of the owner side.

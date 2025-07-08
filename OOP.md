

## Object Oriented Programming 

Here's a clear explanation of getters, setters, static constructors, and static fields :

 1. Getters and Setters : 
	
- Purpose:
They are used to control access to class fields in a safe and controlled way.

```sql
public string Model { get; set; }  // Auto-implemented property
```

- Getter retrieves the value:

```sql
string carModel = myCar.Model;
```

- Setter sets the value:

```sql
myCar.Model = "Toyota";
```

- Benefits:

Allow encapsulation (hiding internal data).

Can add logic like validation in custom getter/setter methods.

2. Static Fields
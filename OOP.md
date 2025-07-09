

## Object Oriented Programming 

Here's a clear explanation of getters, setters, static constructors, and static fields :

 1. Getters and Setters : 

- What Are They?
They are methods that control access to the internal fields (data) of a class.

- Why Use Them?
Protect data from direct modification.

Add validation logic.

Encapsulation: hiding how data is stored or processed.


public class Person
{
    private string name; // private field

   

- Example:
``` public class Person
{
    private string name; // private field

    public string Name  // property with getter and setter
    {
        get { return name; }
        set 
        { 
            if (value.Length >= 2)
                name = value;
            else
                Console.WriteLine("Name must be at least 2 characters.");
        }
    }
}

```

Usage:

```    Person p = new Person();
p.Name = "Al";      // Sets the name using setter
Console.WriteLine(p.Name);  // Gets the name using getter

```
	
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

2. Static Fields :

 - What Are They?

Fields that are shared across all instances of a class.

- Purpose:
A static field belongs to the class itself rather than any object (shared by all instances).

- Why Use Them?

You want a common setting or value for all objects (e.g., max speed limit).

Reduce memory usage — only one copy exists.

- Example:
```sql
public static int MaxAllowedSpeed;
public static string DefaultFuelType;
```
These fields are shared among all objects of the class.

Can be accessed like this:
```sql
Console.WriteLine(Car.MaxAllowedSpeed);
```

3. Static Constructor : 

- Purpose:
Initializes static fields of a class. It runs once only — the first time the class is used.

- Example:
```sql
static Car()
{
    MaxAllowedSpeed = 180;
    DefaultFuelType = "Petrol";
    Console.WriteLine("Static constructor called.");
}
```

- Notes:

No access modifiers (like public or private).

No parameters.

Called automatically before any static members or first object creation.


| Concept            | Access Type  | Shared?         | Called Automatically? | Can Have Parameters? |
| ------------------ | ------------ | --------------- | --------------------- | -------------------- |
| Getter/Setter      | Object-level | No (per object) | No                    | N/A                  |
| Static Field       | Class-level  | Yes (shared)    | N/A                   | N/A                  |
| Static Constructor | Class-level  | Yes (once only) |  Yes                  |  No                  |




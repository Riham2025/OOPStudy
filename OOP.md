

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

2. Static Fields :

- Purpose:
A static field belongs to the class itself rather than any object (shared by all instances).

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
| Static Constructor | Class-level  | Yes (once only) | ✅ Yes                 | ❌ No                 |

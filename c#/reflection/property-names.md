Get all `public` method names of a Class
------

```C#
using System.Reflection;

public class Employee 
{
   public static void AddEmployee() { ... }
   public static string GetEmployeeName() { ... }
   protected static bool DeleteEmployee() { ... }
   private static bool EmployeeExists() { ... }
}

MethodInfo[] methodInfos = typeof(Employee).GetMethods(BindingFlags.Public | BindingFlags.Static);
        
foreach (var methodInfo in methodInfos)
{
  Console.WriteLine(methodInfo.Name);
}

/*
  AddEmployee
  GetEmployeeName
*/
```

Get all properties of a Class
------

```C#
using System.Reflection;

public class Employee 
{
   public static string FirstName = "John";
   public static string LastName = "Doe";
   public static int Age = 40;
   private static bool IsAuthorized = false;
}

PropertyInfo[] propertyInfos = typeof(Employee).GetProperties(BindingFlags.Public | BindingFlags.Static);

foreach (PropertyInfo propertyInfo in propertyInfos)
{
  Console.WriteLine(propertyInfo.Name);
}

/*
  FirstName
  LastName
  Age
*/
```

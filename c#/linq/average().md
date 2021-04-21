## LINQ: Average()

Calculate the average of a list of integers
------

```C#
var numbers = new List<int> { 11, 2, -3, 54, 90 };

double avg = numbers.Average();  // result: 30.8
```
<br />


Calculate the average of a list of nullable integers
------

```C#
var numbers = new List<int?> { 100, null, 50, 55, 75 };

double? avg = numbers.Average();  // result: 70
```
<br />


Calculate the average length of a list of nullable strings
------

```C#
var strings = new List<string> { "apples", "oranges", "cherries", "pomegranate" };

double avg = strings.Select(x => x.Length).Average();  // result: 8
double avg = strings.Average(x => x.Length);           // result: 8
```

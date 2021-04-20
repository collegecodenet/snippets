Get the sum of values from a list of integers
------

```C#
var numbers = new List<int> { 10, 8, 4, -1, 5 };

int sum = numbers.Sum();  // sum: 26
```
<br />

Get the sum of values from a list of decimals
------

```C#
var numbers = new List<decimal> { 1m, 200.8m, -20.2m, 41m, 55.3m };

decimal sum = numbers.Sum();  // sum: 277.9
```
<br />

Get the sum of values from a list of nullable integers
------

```C#
var numbers = new List<int?> { 18, -22, null, 301, null, 53 };

int? sum = numbers.Sum();  // sum: 350
```
<br />

Calculate the total length of all strings in a list
------

```C#
var stringList = new List<string> { "college", "code", "sum", "example" };

int lengthSum = stringList.Sum(x => x.Length); // lengthSum: 21
int lengthSum = (from x in stringList select x.Length).Sum(); // lengthSum: 21
```

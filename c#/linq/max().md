Get the lagest number from a list of integers
------

```
var numbers = new List<int> { 10, -4, 31, 200, 198 };

int maxNumber = numbers.Max(); // maxNumber: 200
```
<br />

Get the lagest number from a list of decimals
------

```
var numbers = new List<decimal> { 0.9m, 51.1m, 33.5m, 20.5m };
    
decimal maxNumber = numbers.Max(); // maxNumber: 51.1
```
<br />

Get the lagest number from a list of nullable integers

------
```
var numbers = new List<int?> { 8, 91, null, -3, -8, 18 };

int? maxNumber = numbers.Max(); // maxNumber: 91
```
<br />

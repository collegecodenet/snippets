#### Get the minimal number from a list of integers

```
var numbers = new List<int> { 18, 22, 21, -3, 33 };

int minNumber = numbers.Min(); // minNumber: -3
```

#### Get the minimal number from a list of decimals

```
var numbers =  new List<decimal> { 0.8m, 8.7m, 4.1m, 22.1m, 14m };

decimal minNumber = numbers.Min(); // minNumber: 0.8
```

#### Get the minimal number from a list of nullable integers

```
var numbers = new List<int?> { 2, 64, null, 13, 89 };

int? minNumber = numbers.Min(); // minNumber: 2
```

#### Get the shortest string length from a list of strings

```
var stringList = new List<string> { "college", "code", "min", "example" };

int minLength = stringList.Min(x => x.Length); // minLength: 3
int minLength = (from x in stringList select x.Length).Min(); // minLength: 3
```

Count the number of items in a collection
------

```
var emptyList = new List<string>();
int emptyCount = emptyList.Count(); // count: 0

var items = new List<string> { "Apples", "Oranges", "Blueberries", "" };
int count = items.Count(); // count: 4
```
<br />

Count the number of filtered items in a collection
------

```
var items = new List<int> { 18, -4, 22, -1, 0, 8 };

int count = items.Where(x => x <= 0).Count(); // count: 3
int count = items.Count(x => x <= 0); // count: 3
```
<br />

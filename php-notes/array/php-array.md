# php array

1. `range()`  - to create an array using a range of data
```php
$arr = range(2, 6); // $arr = array(2,3,4,5,6);
```

2. `$arr[] = "New Values"` -  append data to end of the array
```php
$arr = array("Ashiq", "Rubel");
$arr[]  = "Mostafa"; // $arr = array("Ashiq", "Rubel", "Mostafa);
```

3. `array_pad()` - to padded data in array
```php
$item = array(apple, tomato);
$padded = array_pad($item, 5, 'ball'); // $padded is now array(apple, tomato, ball, ball, ball)
``` 

4. `list($var, ...) = $arr;` - Extracting Multiple Values
```php
person = array("MHR", 75, "Maya Ali", "Engineer");
list($name, $age, $wife) = $person; // $name is "MHR", $age is 75, $wife is "Maya Ali"
```

Two or more consecutive commas in the list() skip values in the
array:
```php
$values = array('a', 'b', 'c', 'd', 'e');
list($m, , , $n) = $values; // $m is "a", $n is "d
```

5. `array_slice($array, $offest, $length)` - to slice an array
```php
$people = array("Tom", "Dick", "Harriet", "Brenda", "Jo");
$middle = array_slice($people, 2, 3); // $middle is new array("Harriet", "Brenda", "Jo);

```
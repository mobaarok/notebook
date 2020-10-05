## is_array
is_array — Finds whether a variable is an array  
Function Description: `is_array ( mixed $var ) : bool`
#### Example:
``` php
$arr = array('this', 'is', 'an array');
echo is_array($arr) ? 'It's an Array' : 'not an Array';
// output: It's an Array
```

## explode
explode — Split a string by a string. Returns an array of strings.  
Function Description:  `explode ( string $delimiter , string $string [, int $limit = PHP_INT_MAX ] ) : array`  
#### Example:  
``` php
$pizza  = "piece1, piece2, piece3, piece4";
$pieces = explode(" , ", $pizza);
// output: $pieces will be, ['piece1', 'piece2', 'piece3', 'piece4,]
```

## implode
implode — Join array elements with a string  
Function Description: `implode ( string $glue , array $pieces ) : string`  
#### Example:  
``` php
$array = array('lastname', 'email', 'phone');
$comma_separated = implode(",", $array);

echo $comma_separated; // lastname,email,phone
```
## str_split  
str_split — Convert a string to an array  
Function Description: `str_split ( string $string [, int $split_length = 1 ] ) : array`  
#### Example:
``` php
$str = "Hello Friend";

$arr1 = str_split($str);
$arr2 = str_split($str, 3);

print_r($arr1);
print_r($arr2);
```
``` php
//output:  
Array
(
    [0] => H
    [1] => e
    [2] => l
    [3] => l
    [4] => o
    [5] =>
    [6] => F
    [7] => r
    [8] => i
    [9] => e
    [10] => n
    [11] => d
)

Array
(
    [0] => Hel
    [1] => lo
    [2] => Fri
    [3] => end
)
```

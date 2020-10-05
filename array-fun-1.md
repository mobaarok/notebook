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

# PHP Note:

## Array Functions:

### 1. array_change_key_case($array, $case)
array_change_key_case ফাংশান   /অ্যারে এর কী গুলো কে লোয়ারকেস অথবা আপারকেস করে দেয়।
~~~ php
$array = ["FirSt" => 1, "SecOnd" => 4];
print_r(array_change_key_case($array, CASE_UPPER)); // or CASE_LOWER
//Array ( [first] => 1 [second] => 4 [0] => 5 [1] => 1 )
~~~
### 2. array_chunk ($array, $size, $preserve_keys)

~~~ php
$input_array = array('a', 'b', 'c', 'd', 'e');
print_r(array_chunk($input_array, 2));
print_r(array_chunk($input_array, 2, true));
/*
*output one:
Array
(
    [0] => Array
        (
            [0] => a
            [1] => b
        )

    [1] => Array
        (
            [0] => c
            [1] => d
        )

    [2] => Array
        (
            [0] => e
        )

)
output two: 
Array
(
    [0] => Array
        (
            [0] => a
            [1] => b
        )

    [1] => Array
        (
            [2] => c
            [3] => d
        )

    [2] => Array
        (
            [4] => e
        )

)

*/
~~~

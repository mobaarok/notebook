# PHP Note:

## Array Functions:

### 1. array\_change\_key\_case\($array, $case\)

array\_change\_key\_case ফাংশান অ্যারে এর কী গুলো কে লোয়ারকেস অথবা আপারকেস করে দেয়।

```php
$array = ["FirSt" => 1, "SecOnd" => 4];
print_r(array_change_key_case($array, CASE_UPPER)); // or CASE_LOWER
//Array ( [first] => 1 [second] => 4 [0] => 5 [1] => 1 )
```

### 2. array\_chunk \($array, $size, $preserve\_keys\)

array\_chunk অ্যারে কে given size এর ভিত্তিতে ছোট ছোট অ্যারে তে ভাগ করে একটি multidimensional অ্যারে রটার্ন করে। এটি তিনটি প্যারামিটার নেয়। _$array_ _$size_ _$preserve\_keys_

$preserve\_keys এর value true অথবা false হবে। ture defined করলে index array এর key আগের টাই থাকবে। false হলে zero index থে্কে key শুরু হবে।

```php
$input_array = array('a', 'b', 'c', 'd', 'e');
print_r(array_chunk($input_array, 2));
print_r(array_chunk($input_array, 2, true));
```

```php
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
```

## array\_column

array\_column — Return the values from a single column in the input array Description `array_column ( array $input , mixed $column_key [, mixed $index_key = NULL ] ) : array`


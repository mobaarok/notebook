# PHP Note:

## Array Functions:

### array_change_key_case()
array_change_key_case ফাংশান   /অ্যারে এর কী গুলো কে লোয়ারকেস অথবা আপারকেস করে দেয়।
~~~ php
$array = ["FirSt" => 1, "SecOnd" => 4];
print_r(array_change_key_case($array, CASE_UPPER)); // or CASE_LOWER
//Array ( [key] => 1 [second] => 4 [0] => 5 [1] => 1 )
~~~

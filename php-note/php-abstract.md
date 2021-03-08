# php-abstract

## Abstract Class

Abstract Class হচ্ছে এক ধরনের বিশেষ class যার থেকে কোনো instance তৈরী করা যায় না। কিন্তু এই Class থেকে child class তৈরী বা inherit/extends করা যাবে।

abstract class-এ property, constant, abstract method এবং non-abstract method সব ধরনের method ই থাকতে পারে এবং সবগুলো method এর Visibility public অথবা protected থাকতে পারে ।

কোনো class কে abstract ঘোষণা করতে হলে class keyword এর সামনে abstract keyword টি দিতে হয়। যেমন- `abstract class className{....}` কোন class এর মধ্যে যদি এক বা একাধিক abstract Method থাকে, সেটিকে অবশ্যই Abstract class হিসেবে Declare করতে হবে ।

```php
abstract class AbstractClass
{
    public $color = "red";
    abstract protected function getName($name);
    public function show()
    {
        echo "this a non-abstract method inside of Abstarct class";
    }
}
```

```php
class childClass extends AbstractClass{
    public function getName($name) {
        return 'Hi '.$name.' !';
    }
}
```

## PHP তে Abstract Method

PHP তে Abstract Method একধরণের বিশেষ Class Method যার বডিতে কোনো code define করা থাকেনা শুধু Method Signature থাকে , অর্থাৎ শুধুমাত্র Method এর নাম এবং Parameter সমূহ Declare করা থাকে।

কোনো Method কে abstract ঘোষণা করতে হলে function keyword এর সামনে abstract keyword টি দিতে হয়। যেমন- `abstract function functionName();` abstract method কে private ঘোষণা করা যায়না।


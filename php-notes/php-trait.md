# Trait 
পি এইচ পি তে এক সাথে একের অধিক  Inheritance সাপোর্ট করেনা না। আর  Trait পি এইচ পি - এর সীমাবদ্ধতা দূর করে। Trait কে Define করা হয় ক্লাসের মত করেই trait কিওয়ার্ডটি ব্যবহার করে। তবে এর থেকে class এর মত object তৈরী করা যায়না।

Trait ব্যবহার এর ফলে  কোড রিইউজ করা সহজ হয়।

```php
trait Foo
 {
    public function sayHello(){
         return "Hello";
    }
    public function sayWorld(){
     return "World";
    }
 }
 ```

 ক্লাসের ভিতরে `use ` কিওয়ার্ডটি দ্বারা Trait কে include করতে পারি। এবং Trait এর ভিতরে থাকা মেথড গুলো যে কোন ক্লাস এ  ব্যাবহার করতে পারি। 
 
 ```php
class User
{
    use Foo;
    public function anotherFun()
    {
        echo 'another fun';
    }
}

$user = new User;
$user->sayHello(); //output: Hello
```
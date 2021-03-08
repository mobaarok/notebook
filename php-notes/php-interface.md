# Php Interface

পিএইচপি তে `interface` keyword দ্বারা ইন্টারফেইস ডিফাইন করা হয়। ইন্টারফেইসে শুধু মাত্র এবস্ট্রাক্ট মেথড থাকতে পারে। কোন প্রোপার্টিজ থাকে না। এবং সব মেথড এর Visibility public থাকে।

ইন্টারফেইসের মেথডগুলোর শুধু সিগনেচার \(কি কি প্যারামিটার নেয়\) ডিফাইন করে দেওয়া হয় কিন্তু এই মেথডগুলোর বডি ডিফাইন করা হয় না।

```php
interface TypeCChargable
{
    public function chargeByTypeC($param);
}
```

ইন্টারফেইসের এর instance তৈরি করা যায় না। একে class-এ implement করা হয়। inherit বা extend করা যায় না।

```php
class SamsungMobile implements TypeCChargable
{
    public function chargeByTypeC($param)
    {
        //defined body
    }
}
```

`ইন্টারফেইস কে আমরা একটা চুক্তি(Contract) বলতে পারি। যারা যারা এই চুক্তিতে স্বাক্ষর করবে তাদের সবাইকে চুক্তির সব কিছু মেনে চলতে হবে।`

`অর্থাৎ, যে সকল class কোন একটি ইন্টারফেইস কে ইমপ্লিমেন্ট করবে তাদের কে অবশ্যই ঐ ইন্টারফেইসের সব মেথড ইমপ্লিমেন্ট করতে হবে।`

## Abstract class আর Interface এর পার্থক্য:

* abstract class আর interface প্রায় একই
* পার্থক্য হচ্ছে abstract class-এ property, constant, abstract Method এবং non-abstract Method সব ধরনের Method ই থাকতে পারে এবং সবগুলো Method এর Visibility public অথবা protected থাকতে পারে ।
* কিন্তু interface এর মধ্যে শুধু method থাকতে পারবে এবং সবগুলো Method বাই ডিফল্ট abstract Method হিসেবে থাকে এবং সবগুলো Method এর Visibility অবশ্যই public হতে হবে।

## Here is an example

```php
interface LoggerInterface
{
    public function log();
}
```

```php
class LogToFile implements LoggerInterface 
{
    public function log()
    {
        echo "Log To File";
    }
}

class LogToDatabase implements LoggerInterface 
{
    public function log()
    {
        echo "Log To Database";
    }
}
```

```php
class Controller 
{
    protected $logger;

    public function __construct(LoggerInterface $logger) 
    {
        $this->logger = $logger;
    }

    public showLog()
    {
        $this->logger->log();
    }
}

$controller = new Controller(new LogToDatabase); 
//or new LogToFile
$controller->showLog();
```


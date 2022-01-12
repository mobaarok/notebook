# php 7 

#  PHP স্ট্রিক্টলি টাইপ ঃ  
তবে এখানে একটা খেয়াল রাখার মত বিষয় হচ্ছে, Scalar Type hinting সুবিধা কাজে লাগানোর জন্য আপনি কেবলমাত্র ফাংশনের প্যারামিটারের সাথে Scalar Type টা বলে দিলেই হবে না। সেক্ষেত্রে PHP নিজে নিজে পাস করা ডাটাকে আপনার দেয়া টাইপে কনভার্ট করে ফেলার চেষ্টা করবে আর না পারলে আস্তে করে ফেইল করে বসে থাকবে। কোন আওয়াজ করবে না। তাহলে তো লাভ হলো না, তাই না? কারণ আমরা চাই টাইপ না মিললে PHP যাতে সাউন্ড করে, Error খায়। এজন্য একটা কাজ করতে হবে। আর তা হলো আপনার ফাইলের একেবারে শুরুতে declare(strict_types=1); এই লাইনটা বলে দিতে হবে। তাহলে PHP স্ট্রিক্টলি টাইপ চেক করবে। আরেকটা জিনিস এখানে মনে রাখতে হবে যে, এই লাইনটা আপনি যেই ফাইলে এড করবেন এটা কেবলমাত্র সেই ফাইলেই স্ট্রিক্ট চেকিং করবে, অন্য কোন ফাইলে না। এমনকি আপনি এই ফাইলে অন্য কোন ফাইল ইনক্লুড করলে সেগুলোতেও না। আলাদা আলাদা করে ফাইলগুলোতে এই লাইনটা বলে দিতে হবে। একইসাথে এটাও মনে রাখা জরুরী যে, strict মূলত চেক করবে যেখান থেকে আপনি ফাংশনটা কল করছেন সেখান থেকে, যেখানে ফাংশনটা ডিফাইন করেছেন সেখান থেকে না। তাই ফাংশন কলের ফাইলটাতে যেন strict এর লাইনটা থাকে সেটা খেয়াল রাখতে হবে।

# Scalar Type Declaration/Hinting
PHP 7 -এ  Scalar বা Primitive টাইপের Type hinting সুবিধা যুক্ত হয়েছে। তাই এখন আমরা ফাংশনের প্যারামিটারে int, float, bool, string এই টাইপগুলোর জন্যও টাইপ বলে দিতে পারব।

```php
declare(strict_types=1);
function add(int $a, int $b) {
   return $a + $b;
}
echo add(1, 2); // shows 3
echo add(1, '2'); //shows TypeError Exception
```


# Return Type Declaration
 ফাংশন কি টাইপের ডাটা রিটার্ন করবে এটা বলে দেয়া যাবে । এটাকে বলা হচ্ছে ‘Return Type Declaration’.
```php
function sum(float $a, float $b) : float {
    ...
}
//or
function welcome(string $message) : void {
    echo $message;
}
```
#  PSR - PHP Standards Recommendations
PSR - পিএসআর (PHP Standards Recommendations) হচ্ছে একটি  পিএইচপি স্পেসিফিকেশন যা PHP Framework Interop Group প্রকাশ করে। আরো সহজ করে বললে, এটি কিছু নিয়ম এর সমষ্টি যা পিএইচপি কোড লেখার ক্ষেত্রে ফলো করতে বলা হয়ে থাকে। PSR দ্বারা পিএইচপি প্রোগ্রামিং এর একটি স্ট্যান্ডার্ড বা মানসম্মত প্রোগ্রামিং  প্রাকটিস  এবং প্রোগ্রামিং স্টাইল নির্ধারণ করা হয়। যাতে কিছু নিয়ম মেনে মানসম্মত এবং সর্বোত্তম  প্রোগ্রাম লেখা সম্ভব হয়।

বর্তমানে অনেক গুলো পিএসআর  ট্যান্ডার্ড আছে। যেমনঃ- PSR-0, PSR-1, PSR-4, PSR-11, PSR-12.


PSR-0 তে Autoloading Standard এর গাইড প্রধান করা হয়েছে। কিন্তু PSR-0 এখন 	Deprecated. তাই Autoloading Standard  এর জন্য এখন PSR-4 ফলো করা হয়।
PSR-1 এ  ব্যাসিক কোডিং ট্যান্ডার্ড এর গাইড বর্ণনা করা হয়েছে।  ঠিক তেমনি Coding Style এর গাইড PSR-2 তে বর্ণনা করা হয়েছে। তবে   PSR-2 ও এখন Deprecated. এর পরিবর্তে কোডিং স্টাইলের জন্য  PSR 12 ব্যবহার করতে বলা হয়ে থাকে। 
পি এস আর এর এই আর্টিকেল টি যাতে অনেক বড় না হয়ে যায় তাই এই পর্বে শুধুমাত্র PSR-1 নিয়ে লিখব। 


# PSR-1: Basic Coding Standard

# 1. Overview
- পিএইচপি ফাইল অবশ্যই  `<?php` ও short-echo `<?=` টেগ ব্যবহার করবে। 

- পিএইচপি  ফাইল অবশ্যই  UTF-8 ক্যারেক্টার এনকোডিং ব্যবহার করবে এবং BOM ব্যবহার করা যাবে না। 

- ফাইলে হয় symbols (classes, functions, constants) declare করা যাবে অথবা side-effects (echoing text, .ini settings) সৃষ্টি হতে পারে এমন স্টেটমেন্ট declare করা যাবে। তবে উভয় নয়।

- নেইমস্পেস ও ক্লাস কে “autoloading” PSR: [PSR-0, PSR-4 ফলো করতে হবে।

- ক্লাসের নাম StudlyCaps-এ declared করতে হবে।


- ক্লাস কনস্টেন্ট কে অবশ্যই আন্ডারস্কোর সেপারটর আপার কেস -এ ডিক্লেয়ার করতে হবে।

- মেথড এর নাম অবশ্যই ক্যামেল কেস-এ ডিক্লেয়ার করতে হবে।


# 2.1. PHP Tags
পিএসআর ১ অনুযায়ী অবশ্যই পিএইচপি  ফাইলের শুরু `<?php` syntex দ্বারা শুরু করতে হবে। এবং প্রিন্ট করার ক্ষেত্রে  short-echo `<?= ?>` syntex ব্যবহার করা যাবে। 


# 2.2. Character Encoding
অবশ্যই পিএইচপি  ফাইলের  character encoding UTF-8 ব্যবহার করতে হবে। এবং BOM ব্যবহার করা যাবে না। 


# 2.3. Side Effects
একটি ফাইলে হয় symbols (classes, functions, constants, etc.) declare করা যাবে অথবা side-effects/পার্শ্ব-প্রতিক্রিয়া (কোন লজিক এক্সিকিউট  করা বা কোন কিছু প্রিন্ট করা বা .ini ফাইলের  সেটিংস)  সৃষ্টি হতে পারে এমন স্টেটমেন্ট declare বা লেখা যাবে। 
### তবে উভয় symbols ও side-effects যুক্ত কোড একই ফাইলে 
declare বা লেখা উচিত নয়।

 যখন একটি  পিএইচপি ফাইলে functions, classes and constants ইত্যাদি declare থাকে তখন এই ফাইলটি যদি অন্য কোন ফাইলে ইনক্লুড করা হয় তবে যে ফাইলে ইনক্লুড করা হয়েছে সে ফাইলে এর কোন সাইড ইফেক্ট পড়বে না। শুধুমাত্র ওই ফাইলে functions, classes and constants গুলো ব্যবহার করতে পারব, অন্য কিছু হবে না।

অন্যদিকে,

যদি পিএইচপি ফাইলে এমন কোন  statements থাকে যা  কোন class or function এর
 ভিতরে না, অর্থাৎ সরাসরি ফাইলে গ্লোবাল স্কোপ এ থেকে থাকে । তাহলে ওই স্টেটমেন্ট টি ফাইলটি অন্য কোথায় ইনক্লুড করার সাথে সাথে-ই এক্সিকিউট হয়ে যাবে। ফলে এটি অন্য ডেভেলপার এর কোড কোন ওয়ার্নিং ছাড়া ই ব্রেক করে ফেলবে এবং অযাচিত সমস্যা তৈরি করবে।

অর্থাৎ- কোন ফাইল ইনক্লুড করার ফলে যে কোডটি সরাসরি এক্সিকিউট  হয় তাকে বলা হয়  side-effects যুক্ত কোড।
তাই একটি ফাইলে হয়  functions, classes and constants ইত্যাদি declare করা যাবে।
অথবা side-effects যুক্ত কোড লেখা যাবে। তবে উভয়-ই একই ফাইলে লেখা উচিত নোয়।
এবং side-effects যুক্ত কোডে যথাযত ডুকুমেন্টেশন রাখা উচিত।

## side-effects সৃষ্টি করার কিছু কারণঃ- 
 * কোন কিছু ইকো বা প্রিন্ট করা
 *  কোন লজিক এক্সিকিউট  করা
 *  অন্য ফাইল ইনক্লুড করা
 *   .ini ফাইলের  সেটিংস modifying করা
 *  external services
 * গ্লোবাল বা স্টাটিক ভ্যারিয়েবল মোডিফাই করা।

> Code that’s directly executed upon inclusion of the file is called code with side effects.


এই এক্সাম্পল টি ডিক্লারেশন এন্ড সাইড এফেক্ট যুক্ত কোড ( যা করা উচিত নয়):-
```
<?php
// side effect: change ini settings
ini_set('error_reporting', E_ALL);

// side effect: loads a file
include "file.php";

// side effect: generates output
echo "<h1>Hello Wordl</h1>";

// declaration
function foo()
{
    // function body
}
```

হয় শুধুমাত্র ডিক্লারেশন...
```
// declaration
function foo()
{
    // function body
}

// conditional declaration is *not* a side effect
if (! function_exists('bar')) {
    function bar()
    {
        // function body
    }
}
```

অথবা সাইড এফেক্ট যুক্ত কোড...
```
<?php
// side effect with properly documention.
/*
* Error report set for all
**/
ini_set('error_reporting', E_ALL);
```

# 3. Namespace and Class Names
নেইমস্পেস এবং ক্লাস কে অবশ্যই  PSR-0 অথবা PSR-4  “autoloading” ফলো করতে হবে।

অর্থাৎ একটি ফাইলে একটিমাত্র ক্লাস থাকা উচিত।  এবং এর নেইমস্পেস top-level vendor name হওয়া উচিত।
ক্লাস এর নাম অবশ্যই StudlyCaps ফলো করা উচিৎ।  like, `Foo` , `UserDetails` .

PHP 5.3 এবং এর পরের ভার্শন  গুলো তে ফরমাল নেইমস্পেস ব্যাবহার  করা উচিত।

For example
```
<?php
// PHP 5.3 and later:
namespace Vendor\Model;

class FooBaz
{
}
```

PHP  5.2.x এবং এর আগের ভার্শন  গুলো তে সুডো-নেইমস্পেস কনভেনশন  ব্যাবহার  করা উচিত।

```
<?php
// PHP 5.2.x and earlier:
class Vendor_Model_Foo
{
}
```

# 4. Class Constants, Properties, and Methods

The term “class” refers to all classes, interfaces, and traits.

## 4.1. Constants
ক্লাসের মধ্যে কনস্টেন্ট কে অবশ্যই আন্ডারস্কোর সেপারটর আপার কেস -এ ডিক্লেয়ার করতে হবে।  

example:
```
<?php
namespace Vendor\Model;

class Foo
{
    const VERSION = '1.0';
    const DATE_APPROVED = '202১-06-01';
}
```
সুপারিশ

4.2. Properties
পিএসআর-১ ইচ্ছাকৃতভাবে প্রোপারটিস বা ভ্যারিয়েবলের নামকরণের কোন গাইড করা হয় নাই।
প্রোপারটিস নামকরণের ক্ষেত্রে যে কোনও কনভেনশন ব্যবহার করা যেতে পারে। তবে নাম গুলো কাজের সঙ্গে যুক্তিসঙ্গত হওয়াই ভাল।
আমি বাক্তিগত ভাবে   প্রোপারটিস বা ভ্যারিয়েবলের নামকরণের ক্ষেত্রে আন্ডারস্কোর সেপারটর  লোয়ার কেস  পছন্দ করি। আপনারা নিজেদের পছন্দ ও সুবিধা অনুযায়ী ব্যবহার করতে পারেন। 

4.3. Methods
মেথড অবশ্যই ক্যামেল কেস  "camelCase()" -এ লিখেতে হবে।

##  References
https://www.php-fig.org/psr/psr-1/

https://en.wikipedia.org/wiki/PHP_Standard_Recommendation

http://www.independent-software.com/introduction-to-php-standard-recommendation-psr-1.html

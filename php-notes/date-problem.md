# date-problem

## doctor appoinment date problem 

বার এর নাম দেওয়া থাকবে, সেই অনুসারে পরবর্তী এক মাসের তারিখের একটা লিস্ট তৈরি করতে হবে। উদাহরণঃ monday এবং friday  দেওয়া আছে। পরবর্তী ৩০ দিনের মধ্যে যে যে তারিখে এই বার গুলো আছে ওই তারিখ গুলো কে খুঁজে বের করে লিস্ট করতে হবে।

```php
    $startDate = date('d-m-Y');
    $endDate = date('d-m-Y', strtotime('+30 days'));
    // change string to date time object 
    $startDate = new DateTime($startDate); 
    $endDate = new DateTime($endDate); 

    $arr = ['Monday', 'Friday'];
    $arrlen = count($arr);

    while($startDate <= $endDate) {
        //  timestamp value of start date 
        $timestamp = strtotime($startDate->format('d-m-Y'));
        // find day name
        $barname = date('l', $timestamp);

        for($j = 0; $j < $arrlen; $j++) {
            if($arr[$j] == $barname) {
                $res =  $barname . ' ' . $startDate->format('d-F-Y');
                echo "$res \n";
            }
        }
        $startDate->modify('+1 day');
    }


/*
Output: 
Monday 05-October-2020
Friday 09-October-2020
Monday 12-October-2020
Friday 16-October-2020
Monday 19-October-2020
Friday 23-October-2020
Monday 26-October-2020
Friday 30-October-2020
Monday 02-November-2020
*/
```

## Sample Solution for date problem

```php
$arr = ['sunday', 'monday', 'tuesday', 'sunday', 'friday'];
$day = ['sunday', 'monday'];
$total = count($arr);
for($i = 0;  $i <= 5; $i++){
    for($j=0; $j <= 2; $j++) {
        // echo " $day[$j]" ;
            if($day[$j] == $arr[$i]) {
            echo " $arr[$i] \n ";
        }
    }         
}
```


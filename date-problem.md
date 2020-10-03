### date problem 

~~~ php
<?php

    // input start and end date 
    $startDate = date('d-m-Y');
    $endDate = date('d-m-Y', strtotime('+30 days'));
    // change string to date time object 
    $startDate = new DateTime($startDate); 
    $endDate = new DateTime($endDate); 
	
	$arr = ['Monday', 'Friday'];
	$arrlen = count($arr);
  
	while($startDate <= $endDate) {
		$timestamp = strtotime($startDate->format('d-m-Y'));
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

~~~

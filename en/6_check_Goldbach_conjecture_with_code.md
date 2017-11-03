><b>Description:</b><br>
    Goldbach's conjecture is one of the oldest and best-known unsolved problems in number theory and all of mathematics. It states: 
    Every even integer greater than 2 can be expressed as the sum of two primes.
    The conjecture has been shown to hold for all integers less than 4 × 1018, but remains unproven despite considerable effort.
    The above is from wikipedia.
    This programe will check Goldbach's conjecture from 2 to 10 million with php code. It takes about 25 minute.

![Goldbach's conjecture screenshots](http://images.vimkid.com/1_100/6_1.jpg "Goldbach's conjecture screenshots")
![Goldbach's conjecture screenshots](http://images.vimkid.com/1_100/6_2.jpg "Goldbach's conjecture screenshots")
![Goldbach's conjecture screenshots](http://images.vimkid.com/1_100/6_3.jpg "Goldbach's conjecture screenshots")

><b>Alglorithm:</b><br>
    1. Taking a even interger from 2 to 10 million to the programe's loops in order.

    2. Using the prime pool, circulating the prime pool,
       then plus every two of the prime numbers as result, 
       if the result equal to the loops even interger, then break, otherwise continue.

    3. Spliting the loops even interger to two part in average. 
       If one of the result is odd integer, continue.
       If one of the result is even integer, then plus 1. the other one minus 1.
       Then we get two odd integer. 

    4. Judging these two odd interger, if they are prime interger, it means, this even interger 
       in this circulation is right to the Goldbach's conjecture, puting these two prime integer to 
       the prime pool, then go to the next circulation. If they are not prime integer, then 
       minus one of the number with 2, the other number plus 2, continuing the judgement until 
       the number to 1. if the number equals 1, that means Goldbach's conjecture is wrong!

><b>Optimizing:</b><br>
    1. Excluding 2, 3 ,5, 7 multiple.

    2. Take the prime interger to the prime pool in counting. At the next loop,
       Take priority from prime pool to calculate.


####Code:
```c
<?php
/************************** VimKid ****************************
 * Author:      VimKid
 * Description: This programe will check Goldbach's conjecture 
                from 2 to 10 million with php code. 
                It takes about 25 minute.
 * Email:       1779156598@qq.com
 * qq:          1779156598
 * Time:        2016.6.26
 * Web:         www.vimkid.com
 *
 ************************  www.vimkid.com **********************/
class GDBH {
    public function __construct(){
        $this->queue = array();
        $range = "10000000";  
        $beginTime=microtime(true);
        $this->mainFunction($range,$beginTime);
    }
    function mainFunction($range,$beginTime){
        // 1. Taking a even interger from 2 to 10 million to the programe's loops in order.
        for($i=2;$i<=$range;$i=$i+2){
            if($i%10000==0){  // count time use
                print_r(microtime(true)-$beginTime);
                print_r(" second-----".$i."used\n");
            }
            // 2. Using the prime pool, if the result is true, then continue.
            $queueResult = $this->checkQueue($i);
            if($queueResult == true){
                continue;  
            }
            // 3. Spliting the loops even interger to two part in average. 
            //    If one of the result is odd integer, continue.
            //    If one of the result is even integer, then plus 1. the other one minus 1.
            //    Then we get two odd integer. 
            $number1 = $i/2;
            $number2 = $number1;
            if($this->getTwo($number1)){ // if it's even integer, then change to odd integer
                $number1 = $number1-1;
                $number2 = $number2+1;
            }
            while($number1>0){
                if($number1==1 && $i!=2){  
                    // when all the number can not fit, then print
                    echo "Congratulations, you found that Goldbach conjecture was wrong! And the number is".$i; die;

                }
                // Checking the multiple of 3 or 5, if true, continue
                if($this->checkNumber($number1) || $this->checkNumber($number2)){ 
                    $number1 = $number1-2;
                    $number2 = $number2+2;
                    continue;
                }else{
                    // Checking the multiple of 2 or 3 or 5, if true, continue
                    if($this->checkZhiShu($number1) && $this->checkZhiShu($number2)){ 
                        // // echo the prime integer from even number 
                        // echo $i."=".$number1."+".$number2."\n"; 
                        $this->putQueue($number1);
                        $this->putQueue($number2);
                        break;
                    }else {
                        $number1 = $number1-2;
                        $number2 = $number2+2;
                        continue;
                    }
                }
            }
        }
    }

    // Checking the multiple of 3 or 5
    function checkNumber($number){
        if($this->getFive($number)){
            return true;
        }else if($this->getThree($number)){
            return true;
        }else {
            return false;
        }
    }

    // Checking the prime integer
    function checkZhiShu($test){
        //$test = 12345; // test number
        $check = true;
        $i = 7;  // Because exclude the multiple of 2,3,4,5,6, so it begin with 7
        $n = floor( sqrt( $test ) );
        while( $i < $n ){
            if( $test % $i == 0 ){
                $check = false;
                $i = $n;
            }else{
                $i = $i+2;
            }
        }
        if( $check ){
            return true;
        }else{
            return false;
        }
    }

    // Checking the multiple of 2
    function getTwo($number){
        $last = substr($number,-1);
        if(($last == 0 || $last ==2 || $last == 4 || $last ==6 || $last == 8 ) && $number!=2){
            return true;
        }else{
            return false;
        }
    }

    // Checking the multiple of 3
    function getThree($number){
        $length = strlen($number);
        $sum = 0;
        for($i=0;$i<$length;$i++){
            $sum=$sum + substr($number,$i,1);
        }
        if($sum%3==0 && $length!=1){
            return true;
        }else{
            return false;
        }
    }

    // Checking the multiple of 5
    function getFive($number){
        $last = substr($number,-1);
        $length = strlen($number);
        if($last == 5 && $length!=1){  // 排除数字5,因为5是质数
            return true;
        }else {
            return false;
        }
    }

    // Checking the multiple of 7, 11, 13
    function getFilter($number){
        if( $number%7 == 0 && $number != 7  ){
            return true;
        }
        if( $number%11 == 0 && $number != 11 ){
            return true;
        }
        if( $number%13 == 0 && $number !=13 ){
            return true;
        }
        if( $number%17 == 0 && $number !=17 ){
            return true;
        }
        if( $number%19 == 0 && $number !=19 ){
            return true;
        }
        if( $number%23 == 0 && $number !=23 ){
            return true;
        }
        if( $number%29 == 0 && $number !=29 ){
            return true;
        }
        return false;
    }

    // prime pool, storage the latest prime number, use the queue
    function putQueue($number){
        // if the nubmer is not exist, then put it in 
        if(!in_array($number,$this->queue)){
            // if the number of queue is bigger than 50 , then push it from queue
            //if(count($this->queue) > 50 ){
            if(count($this->queue) > strlen($number)*8 ){
                array_shift($this->queue);
                array_push($this->queue,$number);
            }else{
                array_push($this->queue,$number);
            }
        }
    }  
    // check if the number is in the prime pool
    function checkQueue($number){
        $result = false;
        foreach($this->queue as $k => $v){
            foreach($this->queue as $x => $y){
                if($v + $y == $number){
                    // echo $number."=".$v."+".$y."\n";
                    $result = true;
                    return $result;
                }
            }
        }
        return $result;
    }
}
$init = new GDBH();
?>

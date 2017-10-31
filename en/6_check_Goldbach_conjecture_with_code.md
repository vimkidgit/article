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
    一. 排除2, 3 ,5, 7　倍数.
    二. 质数池:将前后加入计算的质数放入质数池，计算下一个数时先从质数池里循环,质数池随着计算规模变大自动变大


####Code:
```c
<?php
/************************** VimKid ****************************
 * Author:     VimKid
 * Description:哥德巴赫猜想2－1000万 的偶数正确性验证
 * Email:      1779156598@qq.com
 * qq:         1779156598
 * Time:       2016.6.26
 * Web:        www.vimkid.com
 *
 ************************  www.vimkid.com **********************/
class GDBH {
    public function __construct(){
        $this->queue = array();
        $range = "10000000";  /* 范围，认证1000000以内的偶数正确性 */
        $beginTime=microtime(true);
        $this->mainFunction($range,$beginTime);
    }
    function mainFunction($range,$beginTime){
        // 1. 循环2到指定数字
        for($i=2;$i<=$range;$i=$i+2){
            if($i%10000==0){  // 统计每一万次计算耗时
                print_r(microtime(true)-$beginTime);
                print_r(" 秒-----".$i."用时\n");
            }
            // 2. 判断如果在质数池能找到结果,则不执行后面
            $queueResult = $this->checkQueue($i);
            if($queueResult == true){
                continue;  //结束单次循环
            }
            //3. 将偶数一分为二，如质数性质可知，偶数必然不是质数,那么偶数一分为二
            //   后如果为偶数，则将分割后第一个数减１，另一个数加1,就可以得到两个奇数
            $number1 = $i/2;
            $number2 = $number1;
            if($this->getTwo($number1)){ // 如果为偶数，则变为奇数
                $number1 = $number1-1;
                $number2 = $number2+1;
            }
            while($number1>0){
                if($number1==1 && $i!=2){  
                    // 当所有数字都不符合的时候，说明存在偶数不能表示为两个质数,那么哥德巴赫猜想错误
                    echo "恭喜你！！！，你找到了不符合哥德巴赫猜想的数值!!!,数字为:".$i; die;
                }
                //检查是否3,5 是则跳过数字
                if($this->checkNumber($number1) || $this->checkNumber($number2)){ 
                    $number1 = $number1-2;
                    $number2 = $number2+2;
                    continue;
                }else{
                    //检查是否2,3,5 规则是则跳过数字
                    if($this->checkZhiShu($number1) && $this->checkZhiShu($number2)){ 
                        // 输出偶数对应的质数
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

    /* 检查是否3,5 规则*/
    function checkNumber($number){
        if($this->getFive($number)){
            return true;
        }else if($this->getThree($number)){
            return true;
        }else {
            return false;
        }
    }
    /* 检查是否是质数 */
    function checkZhiShu($test){
        //$test = 12345; //待检测的数字
        $check = true;
        $i = 7;  // 由于排除了2,3,4,5,6, 所以由７，开始的奇数计算
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

    /* 获取数字和是否2倍数,是返回true */
    function getTwo($number){
        $last = substr($number,-1);
        if(($last == 0 || $last ==2 || $last == 4 || $last ==6 || $last == 8 ) && $number!=2){
            return true;
        }else{
            return false;
        }
    }

    /* 获取数字和是否3倍数,是返回true */
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

    /* 获取数字和是否5倍数,是返回true */
    function getFive($number){
        $last = substr($number,-1);
        $length = strlen($number);
        if($last == 5 && $length!=1){  // 排除数字5,因为5是质数
            return true;
        }else {
            return false;
        }
    }

    /* 获取数字和是否7, 11 ,13 倍数,是返回true */
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

    /* 质数池--(存放最接近要求偶数一半的100个数) 用队列 */
    function putQueue($number){
        // 如果已经存在元素则不入队
        if(!in_array($number,$this->queue)){
            // 如果队列大于50 则出队
            //if(count($this->queue) > 50 ){
            if(count($this->queue) > strlen($number)*8 ){
                array_shift($this->queue);
                array_push($this->queue,$number);
            }else{
                array_push($this->queue,$number);
            }
        }
    }  
    /* 检查是否在质数池 */
    function checkQueue($number){
        $result = false;
        foreach($this->queue as $k => $v){
            foreach($this->queue as $x => $y){
                if($v + $y == $number){
                    // 输出偶数对应的质数
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
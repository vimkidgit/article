####Count triangles with code


><b>Description:</b><br>
    Recently I found that picture from my friends circle,that's a picuture of counting the number of the triangles, so i want to counted it with code. 

<br>
><b>Question:</b><br>
    Please count the number of triangles in the picture.

![Count triangles with code](http://images.vimkid.com/1_100/10_1.png "count triangles with code")

<br>
><b>Resolve and Analysis:</b><br>
    Taking the letters to each of the corner and cross point.
    Using undirected graph, if there have three point and these three point are not in a straight line, that means it's a triangle.


<br>
><b>Resolve:</b><br>

![Coun triangles with code](http://images.vimkid.com/1_100/10_2.png "Count triangles with code")

####code:
```c
<?php
	$beginTime=microtime(true);
	$string = array();
	$string["a"] = array("ab","ac","ad","ae","af","ag","ai","aj");
	$string["b"] = array("ba","bc","bd","be","bf","bh","bj","bi");
	$string["c"] = array("ca","cb","cd","ce","cf","ci");
	$string["d"] = array("da","db","dc","de","dg","dj");
	$string["e"] = array("ea","eb","ec","ed","eg","eh","ei","ej");
	$string["f"] = array("fa","fb","fc","fh","fi","fj");
	$string["g"] = array("ga","gd","ge","gh","gi","gj");
	$string["h"] = array("hb","he","hf","hg","hi","hj");
	$string["i"] = array("ia","ib","ic","ie","if","ig","ih","ij");
	$string["j"] = array("ja","jb","jd","je","jf","jh","jg","ji");
	$order=array("a","b","c","d","e","f","g","h","i","j");
	$result = array();
	foreach($order as $h=>$i){
		foreach ($string[$i] as $k=>$v ){
			foreach($string[$i] as $a=>$b){
				if($b>$i){
					foreach ($string[substr($b,1)] as $bk=>$bv ){
						if(substr($bv,1)!=substr($v,0)){
							if(substr($bv,1)==substr($v,1)){
								if(substr($b,1)>$i&&substr($v,1)>substr($b,1)){
									$result[]=$i.substr($b,1).substr($v,1);
								}
							}
						}
					}
				}
			}
		}
	}
	$third = array("acf","aci","afi","adg","adj","agj","bcd","bce","bde","bfh","bfj","bhj","cde","cfi","dgj","egh","egi","ehi","fhj","ghi"); // exclude the three point in a straight line
	$result = array_diff($result,$third);
	print_r($result);
	print_r("Totals:".count($result));
	echo "\n";
	$endTime=microtime(true);
	$useTime=$endTime-$beginTime;
	echo "Time used:".$useTime;

?>
```

####Result：

![Result](http://images.vimkid.com/1_100/10_3.jpg "Result")

    The result is 35.

####Extension：　

    That's not the best way, you can fix it as you want.

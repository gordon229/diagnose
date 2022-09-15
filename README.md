<html>
<head>
<style>
ul#block li {
  display:inline-block;
}
</style>
</head>
<ul id="block">
<li>
【感冒、流感、新冠、Omicron初步診斷】<BR><BR>
請選擇您的症狀：
<form action="index.php" method="POST">
發燒<input type="checkbox" name="a"><BR>
發熱<input type="checkbox" name="a_2"><BR>
頭痛<input type="checkbox" name="b"><BR>
鼻塞<input type="checkbox" name="c"><BR>
流鼻水<input type="checkbox" name="d"><BR>
咳嗽<input type="checkbox" name="e"><BR>
乾咳<input type="checkbox" name="e_2"><BR>
喉嚨痛<input type="checkbox" name="f"><BR>
喉嚨沙啞<input type="checkbox" name="g"><BR>
肌肉痠痛<input type="checkbox" name="h"><BR>
疲倦乏力<input type="checkbox" name="i"><BR>
極度疲勞<input type="checkbox" name="j"><BR>
腹瀉<input type="checkbox" name="k"><BR>
失去味嗅覺<input type="checkbox" name="l"><BR><BR>
<input type="submit" value="診斷" name="submit">
</form>

<?php
if(isset($_POST['a']) OR isset($_POST['a_2']) OR isset($_POST['e']) OR isset($_POST['d']) OR isset($_POST['c']) OR isset($_POST['f']) OR isset($_POST['b']) OR isset($_POST['h']) OR isset($_POST['i'])){
		if(!(isset($_POST['k']) OR isset($_POST['l']) OR isset($_POST['a_2'])))
		    echo "可能是感冒<BR>";
}

if(isset($_POST['a']) OR isset($_POST['a_2']) OR isset($_POST['h']) OR isset($_POST['b']) OR isset($_POST['e']) OR isset($_POST['d']) OR isset($_POST['c']) OR isset($_POST['f']) OR isset($_POST['b']) OR isset($_POST['h']) OR isset($_POST['i'])){
		if(!(isset($_POST['k']) OR isset($_POST['l']) OR isset($_POST['a_2'])))
		echo "可能是流感<BR>";
}

if(isset($_POST['a']) OR isset($_POST['a_2']) OR (isset($_POST['e'])  OR isset($_POST['e_2'])) OR isset($_POST['i']) OR isset($_POST['k']) OR isset($_POST['l']) OR isset($_POST['c']) OR isset($_POST['d']) OR isset($_POST['h'])){
	if(!(isset($_POST['b']) OR isset($_POST['e']) OR isset($_POST['f'])))
	echo "可能是新冠肺炎<BR>";
}

if(isset($_POST['a']) OR isset($_POST['a_2']) OR (isset($_POST['e']) OR isset($_POST['e_2'])) OR isset($_POST['j']) OR isset($_POST['l']) OR isset($_POST['g']) OR isset($_POST['h']) OR isset($_POST['c'])){
	if(!(isset($_POST['b']) OR isset($_POST['d']) OR isset($_POST['c']) OR isset($_POST['f']) OR isset($_POST['k'])))
	echo "可能是Omicron<BR>";
}
?>
</li>
<li>
<img src="symptoms.jpeg" width="650" height="650">
</li>
</ul>
</html>


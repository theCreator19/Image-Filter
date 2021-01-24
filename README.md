# Image-Filter
<!DOCTYPE html>
<html>
<head>
	<link rel="icon" type="images/jpg" href="https://i.pinimg.com/236x/e7/98/5b/e7985b66353bf9a98762d4026bf3e7a4--alphabet-wall-decals-alphabet-letters.jpg">
	<title>Aman's Filter</title>
	<script src="https://www.dukelearntoprogram.com/course1/common/js/image/SimpleImage.js" >
</script>
<!--
	This link is to use "Font Awesome".
-->
<link rel="stylesheet" href="https://pro.fontawesome.com/releases/v5.10.0/css/all.css" integrity="sha384-AYmEC3Yw5cVb3ZcuHtOA93w35dYTsvhLPVnYs9eStHfGJvOvKxVfELGroGkvsg+p" crossorigin="anonymous"/>
<!--
	this script is to link "Javascript".
-->

<script type="text/javascript" src="filter.js"></script>
<!--
	This link is to link "CSS".
-->

<!--
	Javascript coding
	
-->
<script type="text/javascript">
	var fgImage = null;
var bgImage = null;
var fgCanvas;
var bgCanvas;

function loadForegroundImage() {
  var file = document.getElementById("fgfile");
  fgImage = new SimpleImage(file);
  fgCanvas = document.getElementById("fgcan");
  fgImage.drawTo(fgCanvas);

}
function loadBackgroundImage() {
  var file = document.getElementById("bgfile");
  bgImage = new SimpleImage(file);
  bgCanvas = document.getElementById("bgcan");
  bgImage.drawTo(bgCanvas);
}

function myf(){
var x;
x=document.getElementById("fgcan").className="c1";
document.getElementById("bgcan").className="c1";
}
function myf2(){
document.getElementById("fgcan").className="c2";
document.getElementById("bgcan").className="c2";
}
function myf0(){
  document.getElementById("fgcan").className="c0";
  document.getElementById("bgcan").className="c0";
}
function myf4(){
  document.getElementById("fgcan").className="c4";
  document.getElementById("bgcan").className="c4";
}function myf5(){
  document.getElementById("fgcan").className="c5";
  document.getElementById("bgcan").className="c5";
}function myf6(){
  document.getElementById("fgcan").className="c6";
  document.getElementById("bgcan").className="c6";
}function myf7(){
  document.getElementById("fgcan").className="c7";
  document.getElementById("bgcan").className="c7";
}function myf8(){
  document.getElementById("fgcan").className="c8";
  document.getElementById("bgcan").className="c8";
}
function myf9(){
  var file = document.getElementById("fgfile");
  fgImage = new SimpleImage(file);
  
  for (var pixel of fgImage.values()){
    if (pixel.getY()<=(fgImage.getHeight())/7){
        pixel.setRed(255);
    }
    else if(pixel.getY()<2*(fgImage.getHeight())/7){
        pixel.setGreen(255);
    }
    else if(pixel.getY()<3*(fgImage.getHeight())/7){
        pixel.setGreen(255);
    }
    else if(pixel.getY()<4*(fgImage.getHeight())/7){
        pixel.setGreen(255);
    }
    else if(pixel.getY()<5*(fgImage.getHeight())/7){
        pixel.setGreen(255);
    }
    else if(pixel.getY()<6*(fgImage.getHeight())/7){
        pixel.setGreen(255);
    }
    else{
        pixel.setBlue(255);
    }
}
fgCanvas = document.getElementById("fgcan");
fgImage.drawTo(fgCanvas);

}
	
</script>


<link rel="stylesheet" type="text/css" href="filter.css">

<!--
	CSS Coding
-->
<style type="text/css">
	header{
	border: 2px solid green;
	font-size: 20pt;
	border-radius: 15px;
	text-align: center;
	background-color: #ccffcc;
}
body {
  background-color: black;
  font-family: Verdana;
  margin: 40px;
  color: violet
}
button{
	background-color: orange;
	border-color: red;
	color: pink;
}
summary{
	font-size: 20pt;
}
canvas {
  border: 1px solid #c3c3c3;
  height: 200px;
  background-color: #0d1a00;
}

.c1{
filter:blur(3px);

}
.c2{
filter:sepia(80%);
}
input {
  font-size: 12pt;
  color: blue;
  border-radius: 15px;
  border: 2px orange solid;
}
.c4{
	filter: contrast(150%) brightness(100%);
}
.c0{
	filter: none;
}
.c5{
	filter: saturate(8);
}
.c6{
	filter: opacity(30%);
}
.c7{
	filter: grayscale(100%);

}
.c8{
	filter: hue-rotate(90deg);

}
footer{
	color: #ccffcc;
}
#ol1{
	color: #ff4da6;
}
#ifu{
	margin: 25px;
	color: #ff8080;
	border: 1px solid white;
	border-radius: 15px;
	padding: 6px;
	padding-left: 10px;
	background-color: #ccffff;
}
#Avail{
	color: #ff9933;
}
</style>
</head>
<body>

<header>
	Image Filters
</header>
<br>
<br>

<canvas id = "fgcan">
</canvas>
<canvas id = "bgcan">
</canvas>

<p>
IMAGE 1: <input type="file"  multiple="false" accept="image/*" id="fgfile" onchange="loadForegroundImage()" >
</p>

<p>
IMAGE 2: <input type="file" multiple="false" accept="image/*" id="bgfile" onchange="loadBackgroundImage()" >
</p>

<h2 id="Avail">Available Filters</h2>
<div id="aval">
<ul>
<li><input type="button" value="Original" onclick="myf0()"></li><br>
<li><input type="button" value="Blur" onclick="myf()"></li><br>
<li><input type="button" value="Sepia" onclick="myf2()"></li><br>
<li><input type="button" value="Contro-Bright" onclick="myf4()"></li><br>
<li><input type="button" value="Saturate" onclick="myf5()"></li><br>
<li><input type="button" value="Opacity" onclick="myf6()"></li><br>
<li><input type="button" value="Grayscale" onclick="myf7()"></li><br>
<li><input type="button" value="Hue-rotate" onclick="myf8()"></li><br>
<li><input type="button" value="color 1" onclick="myf9()"></li>
</ul>
</div>
<br>
<br>
<details>
	<summary>How To Use</summary>
	<ol id="ol1">
		<li>You will find two different options for choosing two different images.</li>
		<li>Now choose image which you want to filter by selecting choose file option.</li>
		<li>You will also find different filters in the "Available Filters" Heading.</li>
		<li>By selecting on different filters your images will be Updated.</li>
	</ol>
</details>
<br><br>
<details>
		<summary>Information for You</summary>
		<div id="ifu">
		<p>~ I hope Your are fine. But being fine is not sufficient you have to be protective. </p>
		<p>~ Stay Home, Stay Secure.</p>
		<p>~ Always wear mask while going out.</p>
		</div>

</details>
<footer>
	<p align="center">Copyright &copy 2020 All rights reserved.<br>This website is created By Aman Agarwal&#128519</p>

</footer>
</body>
</html>

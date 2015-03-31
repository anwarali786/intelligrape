jQuery Exercises

1. <a href='http://www.google.com/policy.pdf'>Policy</a>
<a href='www.yahoo.com/logo.png' title='yahoo logo'>View Logo</a>
<a href='http://www.facebook.com' title='Facebook'>Facebook</a>

Select all anchor tags that link to a pdf document.

CODE:-
<!DOCTYPE html>
<html>
	<head>
		<script src=" jquery-1.11.2.min.js ">
	</script>
	<script>
		$(document).ready(function()
		{	
  
		 	$('a[href$="pdf"]').hide();
	
		});
	</script>
	</head>
	<body>
		<a href='http://www.google.com/policy.pdf'>Policy</a>
		<a href='www.yahoo.com/logo.png' title='yahoo logo'>View Logo</a>
		<a href='http://www.facebook.com' title='Facebook'>Facebook</a>
	</body>
</html>

Select all anchor tags that start with http

CODE:-
<!DOCTYPE html>
<html>
	<head>
		<script src=" jquery-1.11.2.min.js ">
	</script>
	<script>
		$(document).ready(function()
		{	
  
		 	$('a[href^="http"]').hide();
	
	});
	</script>
	</head>
	<body>
		<a href='http://www.google.com/policy.pdf'>Policy</a>
		<a href='www.yahoo.com/logo.png' title='yahoo logo'>View Logo</a>
		<a href='http://www.facebook.com' title='Facebook'>Facebook</a>
	</body>
</html>

Select all anchor tags that have title attribute

CODE:-
<!DOCTYPE html>
<html>
	<head>
		<script src=" jquery-1.11.2.min.js "></script>
		<script>
			$(document).ready(function()
			{
 				$('a[title]').show();
  			});
		</script>
	</head>
	<body>
		<a href=' http://www.google.com/policy.pdf '>Policy</a>
		<a href='www.yahoo.com/logo.png' title='yahoo logo'>View Logo</a>
		<a href='http://www.facebook.com' title='Facebook'>Facebook</a>
	</body>
</html>

2. Create an anchor tag using jQuery and add href attribute and assign it a value http://www.google.com

CODE:-
<!DOCTYPE html>
<html>
	<head>
		<script src="jquery-1.11.2.min.js"></script>
		<script>
			$(document).ready(function()
			{
   $('a').after("&nbsp<a href='http://www.google.com'>www.google.com</a>");
			});
		</script>
	</head>
	<body>
		<a href='http://www.google.com/policy.pdf'>Policy</a>


	</body>
</html>
3. Create a simple button and one(or two?) paragraph with text “Hi”. Once the button is clicked, the paragraph text should change to “Hello”. If button is clicked once again, the paragraph text should again change to “Hi”. This process must repeat on subsequent clicks. 

CODE:-
<!DOCTYPE html>
<html>
<head>
<script src="jquery-1.11.2.min.js"></script>
<script>
$(document).ready(function(){
  $("#change").click(function(){
        if($('#para').text()=="hi")
	$('#para').text('hwllo');
	else
	$('#para').text("hi");
    });
});
</script>
</head>
<body>
<input type="button" id=change value="change">
<p id=para> hi</p>
</body>
</html>

4. Create toggle buttons, i.e there should be div's which has a class of "toggle-button", bind a click event on it and whenever the button is clicked, classes "on" and "off" should toggle(if class is 'on' change it to 'off' and vice-versa) changing the background-color of that clicked DIV.
<!doctype html>
	<html >
	<head> 
 		 <title>toggle </title>
  		<style>
 		 p {
    		margin: 10px;
    		font-size: 16px;
    		font-weight: bolder;
  		  cursor: pointer;
		  }
  .blue {
    color: blue;
  }
  .highlight {
    background: yellow;
  }
  </style>
  <script src="jquery-1.11.2.min.js"></script>
</head>
<body>
 <div >
<p class="blue highlight">Click to toggle</p>
<p class="blue ">highlight</p>
</div>
<div ><p class="blue">on these</p>
<p class="blue">paragraphs</p>
</div>
 
<script>
$( "div" ).click(function() {
 $(this).toggleClass("highlight");
});
</script>
 
</body>
</html>

5. Create a simple animation of a DIV (update left property) which starts on click event of a button, the button also resets the animation when clicked again.
<!DOCTYPE html>
<html>
	<head>
		<script src="jquery-1.11.2.min.js"></script>
		<script>
			$(document).ready(function()
			{
    				$("#btn1").click(function(){
        				$("#box").animate({height: "300px" width: "300px"});
    			});
    			$("#btn2").click(function()
			{
        				$("#box").animate({height: "100px"});
    			});
		});
</script>
</head>
<body>
<button id="btn1">Animate height</button>
<button id="btn2">Reset height</button>
<div id="box" style="background:Blue;height:100px;width:100px;margin:6px;"></div>

</body>
</html>

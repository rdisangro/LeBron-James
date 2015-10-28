# LeBron-James
Project 2 about LeBron

<!doctype html>
<html>
<head><p style="font-size:74px;text-align:center;font-family:arial;">LeBron James' Field Goal Percentage From Certain Areas on the Floor During the 2015 NBA Finals</p></head>
<head><p style="font-size:25px;background-color:gray;width:17%;color:white;">By Rocco DiSangro</p></head>
<head><p style="font-size:25px;background-color:gray;width:15%;color:white;">October 6, 2015</p></head>
	<title>LeBron James</title>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.3/jquery.min.js"></script>
   

</head>

<body>
<p style="font-size:36px;text-align:left;font-family:Cambria, 'Hoefler Text', 'Liberation Serif', Times, 'Times New Roman', serif;line-spacing:0.17em;"> LeBron James and the Cleveland Cavaliers fell to the Golden State Warriors 4-2 in a best of seven series. Although the Cavs lost, James put on one of the single greatest scoring performances in NBA Finals history. The graphic below is meant to give you a visual idea of Lebron's field goal percentage from certain areas on the court with an explanation of each marker.</p> 

<div class="container">
	<div class="marker" id="inthepaint"></div>
    <div class="marker" id="freethrow"></div>
    <div class="marker" id="threepoint"></div>
    <div class="marker" id="topofarc"></div>
    <div class="marker" id="midrange"></div>
	<img src= "http://www.conceptdraw.com/How-To-Guide/picture/Sport-Basketball-court-color-Template.png"/>
</div><!--container-->
<div class="textbox">
	<div class="popuptitle">LeBron James NBA Finals FG% 2015</div>
    LeBron James is one of the best players in the NBA and for those that want to argue against that, you can just take a look at his accolades. This chart is detailed to show LeBron's field goal percentage from certain sports on the floor during the Finals.<br 	/> <br />Click on the markers on the court to see LeBron's field goal percentage from each spot on the floor during the Finals.</div>
<div class="homebutton">Click to see LeBron's scoring totals and FG% by each Finals game </div>


<style>
.textbox {
	display: inline-block;
	width: 30%;
	padding: 20px;
	vertical-align: top;
	background-color: white;
	border-radius:5px;
	line-spacing:.01em;
	font-size:22px;
	font-family:"Gill Sans", "Gill Sans MT", "Myriad Pro", "DejaVu Sans Condensed", Helvetica, Arial, sans-serif;
}
.container img {
	width: 100%;
}
.container {
	width: 60%;
	position: relative;
	display: inline-block;
}
.marker {
	width:25px;
	height: 25px;
	background-color: black;
	border:2px solid white;
	border-radius:50%;
	position: absolute;
	cursor:pointer;
	transition: background-color 0.5s ease;
}
.marker:hover{
	background-color: orange;
}
#inthepaint {
	top:47%;
	left:88%;
}
.straighten:after{
	display:block;
	height:0;
	clear:both;
	visibility:hidden;
}

#popup {
	position:relative;
}
.hoverbox {
	position:absolute;
	padding:0.5em;
	background:#FFF;
	box-shadow: 1px 1px 8px rgba(0,0,0,.4);
	z-index:300;
	line-height:1.3em;
	min-width:100px;
	max-width:200px;
}

.popuptitle {
	color:red;
	font-family:'Roboto', Arial, sans-serif;
	letter-spacing:0.01em;
	font-size:38px;
	font-weight:700;
	clear:both;
}

#freethrow {
	top: 45%;
	right: 22%;
}
#threepoint {
	top:88%;
	right:2%;
}
#topofarc {
	top:45%;
	right:29%;
}
#midrange {
	top:20%;
	right:10%;
}
.popuptitle {
	font-weight: bold;
}
.homebutton {
	font-family:"Lucida Grande", "Lucida Sans Unicode", "Lucida Sans", "DejaVu Sans", Verdana, sans-serif;
	cursor:pointer;
	border-radius:5px;
	height:75px;
	width: 300px;
	text-align:center;
    background-color:black;
    color: #FFFFFF;
    font-family: Verdana, Arial, Sans-Serif;
    opacity: 0.5;
	font-size:20px;
	align:center;
}
</style>
<script>
$(document).ready(function() {

var data =
[{"id":"freethrow","name":"LeBron's Free-Throw %","description":"In the Finals, LeBron shot 68.7% from the free-throw line. This is below average for James, considering he is a career 74.5% FT shooter."},
{"id":"threepoint","name":"LeBron's Right Corner 3 %","description":"From the right corner of the floor, behind the 3-point line, LeBron James only took two shots, but he finished the finals 1-2 while shooting 50%."},
{"id":"inthepaint","name":"LeBron's Restricted Area FG%","description":"The restricted area is the area directly under the basket and it is outlined by a small arc. In the Finals, LeBron shot an efficient 67.9% in the restricted area, while making 36 of his 53 baskets."},
{"id":"midrange","name":"LeBron's Mid-range FG%","description":"This is the area where LeBron really struggled in the NBA Finals. Usually, James is very efficient from mid-range, but in the Finals, he shot a lousy 11-48 totaling 22.9%."},
{"id":"topofarc","name":"LeBron's FG% from the top of the arc behind the 3 point line","description":"LeBron shot almost all of his three point shots from this spot on the floor. James took 38 shots, but only managed to rattle in 12, brining his FG% from this spot on the floor to 31.6%."}
];

$('.marker').click(function(){
	$('.textbox').empty();
	for (var i = 0; i < data.length; i++) {
		if (this.id == data[i].id) {
			$('.textbox').append('<div class="popuptitle">' + data[i].name + '</div>' + data[i].description); 		 		}//if
	}//for
});
$('.homebutton').click(function() {
	$('.textbox').empty();
	$('.textbox').append('<div class="popuptitle">LeBron Game by Game FG% </div> Game 1: 44 pts. 47.4%');
	$('.textbox').append('<div class="popuptitle"></div> Game 2: 39 pts. 31.4%');
	$('.textbox').append('<div class="popuptitle"></div> Game 3: 40 pts. 41.2%'); 
	$('.textbox').append('<div class="popuptitle"></div> Game 4: 20 pts. 31.8%'); 
	$('.textbox').append('<div class="popuptitle"></div> Game 5: 40 pts. 44.1%'); 
	$('.textbox').append('<div class="popuptitle"></div> Game 2: 32 pts. 39.4%');  
});//homebutton
});//document ready



</script>	
</body>
</html>

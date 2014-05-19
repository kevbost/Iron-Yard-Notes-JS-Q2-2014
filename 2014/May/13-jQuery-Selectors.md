#jQuery Selectors
## 

#[Back to INDEX](../../Iron%20Yard%20Index.md)
## 

##Selectors

	items.forEach(function(item){
    	// var totalString = firstPart + item.Images[0].url_570xN + lastPart
    	// $('.main').append(totalString)
    	var totalString = '<a href="' + item.url + '"style="background-image: url(' + item.Images[0].url_570xN + ') " target="_blank" class="box"></a>'
    	$('.main').append(totalString)
		var totalString = '<div class="boxTitle">' + item.category_path[0] + " | " + item.category_path[1] + '</div>'
    	$('.box').last().append(totalString)
    	var totalString = '<div class="boxPrice">' + "$" + item.price + '</div>'
    	$('.boxTitle').last().append(totalString)
	})

###.prepend()
Places what's being updated at the beginning of the currently being looped code.

	Pushing things down from the beginning. On the next loop:
	1.  
	1 becomes 2. 
	1 becomes 2, 2 becomes 3.  1 becomes 2, 2 becomes 3, 3 becomes 4.

	<div class="html">
		<h1>lol</h1>
	</div>
	---
	prepending <p>rofl</p>
	<div class="html">
		<p>rofl</p>
		<h1>lol</h1>
	</div>


###.append()
Places what's being updated at the END of the currently being looped code

		1 stays 1.
		2 gets added at the end.
		3 gets added at the end.
	
		<div class="html">
			<h1>lol</h1>
		</div>
	---
		prepending <p>rofl</p>
			<div class="html">
				<h1>lol</h1>
				<p>rofl</p>
			</div>


###.last()
Selects and updates the last element that was called.
	
	    var totalString = '<div class="boxPrice">' + "$" + item.price + '</div>'
    	$('.boxTitle').last().append(totalString)
    	
###.first()
Selects and updates the FIRST element that was called.

	    var totalString = '<div class="boxPrice">' + "$" + item.price + '</div>'
    	$('.boxTitle').first().append(totalString)


###.text()

		Turns the string into plain text.
	
###.html()
Can be used to SET or GET the contents of an element.

Will obliterate the contents of any nested html.

Will return the html of the element.

		<div class="html"><h1>lol</h1></div>
	becomes
		<div class="html"></div>

###.css()
Can be used to SET or GET the style contents of an element.

Will obliterate the contents of any nested html.

Will return the html of the element.

		$(.container).css("margin | margin-left | width | height | etc")
		"0px 143px 0px 143px"

	or

		$(.container).css("margin-left", "0px")
		"0px 143px 0px 0px"


###.children()

		$(.container).children('header')
			[<header>...</header>]
			
###.addClass() OR .toggleClass()
		
		<div clsas="container">
			<div class="box box2">
				<div class="green-overlay"></div>
			</div>
		</div>
		
		.box {
			background-color: black;
			width: 400px;
			height: 200px;
		}
		.box2 {
			position:relative;
		}
		.greenOverlay {
			height: 0;
			position: absolute;
			top:0;
			right:0;
			left:0;
			background-color:green;
			transition: all 1s ease;
		}
		.green-overlay.active {
			height:auto;
			bottom:0;
			<!-- transition has been inherited from parent -->
		}
		
		
		$(".button").click(function(){
			$(".green-overlay").addClass('active')
		})
		
		OR!!!
		
		$(".button").click(function(){
			$(".green-overlay").toggleClass('active')
		})
			
##Homework

	* generate a webapp
	* pick 15 different jQuery Methods
	* for each example
		- Create a button that will run a demo of what that method does.
		- Write an explanation of what the method does, press the button and see what it does.
		
###for example			
		$('.demo12').click(function(){
			$('.demo-box).html("wow")		
		})


##afterward
###:before and :after in CSS


<html>
<head>
		<style>
		.example {
		position: relative;
		width: 400px;
		height: 400px;
		background-color: orange;
	}
	.example:before {
		position: absolute;
		content: " ";
		font-size: 40px;
		width: 500px;
		height: 400px;
		border-radius: 0px;
		background-color: red;
		left: 200px;
	}
	.example:after {
		position: absolute;
		content: " ";
		font-size: 40px;
		width: 0px;
		height: 50px;
		border-radius: 300px;
		background-color: orange;
		left: 300px;
		top: 180px;
		transition: all .5s ease;
	}
	.example:hover:after {
		top: 0px;
		left: 55px;
		border-radius: 10px;
		width: 400px;
		height: 400px;
	}
		</style>
</head>
		<div class="example">html text</div>
</html>


	<html>
	<head>
		<style>
		.example {
		position: relative;
		width: 400px;
		height: 400px;
		background-color: orange;
	}
	.example:before {
		position: absolute;
		content: " ";
		font-size: 40px;
		width: 500px;
		height: 400px;
		border-radius: 0px;
		background-color: red;
		left: 200px;
	}
	.example:after {
		position: absolute;
		content: " ";
		font-size: 40px;
		width: 0px;
		height: 50px;
		border-radius: 400px;
		background-color: orange;
		left: 300px;
		top: 180px;
		transition: all .5s ease;
	}
	.example:hover:after {
		top: 0px;
		left: 55px;
		border-radius: 0;
		width: 400px;
		height: 400px;
	}
	</style>
	</head>
	<div class="example">html text</div>
	</html>


 
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	



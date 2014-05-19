#jQuery Student Lecture Notes
## 

#[Back to INDEX](../../Iron%20Yard%20Index.md)
## 


$('.box1') --> $ denotes a function, calling a string, 
	
	$('.box1'.)
	[<div class=​"box1">​wow​</div>​]

	$('.box1').css('background', 'blue')
	[<div class=​"box1" style=​"background-color:​ blue;​ background-position:​ initial initial;​ background-repeat:​ initial initial;​">​wow​</div>​]

.text

	$('.box1').text("WOW THIS IS AWESOME")
	[<div class=​"box1">​WOW THIS IS AWESOME​</div>​]

.append

	$('.box2').append('<h1>hey guys</h1>')
	[<div class=​"box2">​…​</div>​]

.click

	$('.box1').click(function() {
    $('.box2').text('MY SIBLING GOT CLICKED');
	})
	[<div class=​"box1">​wow​</div>​]

.click for siblings

	$('.box1').click(function() {
    $('.container').append('<div class="box1"></div>')
	})
	[<div class=​"box1">​wow​</div>​]

.addClass

	$('.box1').click(function() {
    $('.box1').addClass('active')
	})
	[<div class=​"box1">​wow​</div>​]

$(this).addClass  --> in this situation THIS refers to the item being interacted with.

	$('.box1').click(function() {
	$(this).addClass('active')
	})
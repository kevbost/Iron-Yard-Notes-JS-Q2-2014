jQuery

jQuery returns jQuery objects.

	$('.box1').css('background', 'blue')
	[<div class=​"box1" style=​"background-color:​ blue;​ 	background-	position:​ initial initial;​ background-repeat:​ 	initial 	initial;​">​box1​</div>​]

or ... returns the same thing
	var box = $('.box1');
	
	.append
	$('.box2').append('<h1>hey guys</h1>')
	$('.div').append('<h1>hey guys</h1>')
	
	.click - This example effects siblings.
	$('.box1').click(function(){
		$('.box2').text('MY SIBLING GOT CLICKED');
	})
	
target the thing, decide which event you want to listen to, make anything happen upon that event


	$('.box1').click(function(){
	$('.container').append('<div class="box1"></div>')
	})

.addClass adds a class 'active'


	$('.box1').click(function(){
	$('.box1').addClass('active')
	})
	
$(this) refers to the thing captured in selector
$(this) refers to the thing being interacted with

	$('.box1').click(function(){
	$(this).addClass('active')
	})
	
Looping over datasets - takes one color code out of each "Images" array within "items" and appends the .container class with this color, for each time it comes up in the loop. (imaginary dataset)

	items.forEach(function(item){
		$('container'.append(
		'<div style="background: ' + item.Images[0].hex_code ' " 		class="box"></div>'))
	})

	
	var firstPart = '<div style="background: ';
	var lastPart =' " class="box"></div>'
	
	items.forEach(function(item){
	$'container'.append(firstPart + image.Images[0].hex_code + secondPart)
	})


filter - only returns when the returned value was true
	
	[1,2,3,4].filter(function(x){
		return x > 2;
	})


Homework - new set of data, up to me to render out what i find relevant.
Mason's Official ETSY API Key

	https://api.etsy.com/v2/listings/active?api_key=kr9rjq7dc9c24jv6fccq2hus&keywords=muppets&includes=Images
























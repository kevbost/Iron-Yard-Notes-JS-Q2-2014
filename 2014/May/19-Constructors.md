#Objects, Constructors, Prototypes
## 

#[Back to INDEX](../../Iron%20Yard%20Index.md)
## 


##May 19, 2014 - Constructors

WHEN YOU THINK "CONSTRUCTOR", ALWAYS USE "NEW" KEYWORD

	"Capitalized javascript elements without a shadow of a doubt are constructors"
	"the period will dive down from a given property into an object" - on overloaded syntax of "."
	"Constructors are nothing more than plain old functions.  Constructors are just functions.  What are constructors?  Right, they're functions.  Say it back... what are constructors?"
		-masondesu-

######When you call for a property or method, first it looks for an instance to see if that property or that method exists on that particular instance.

##Constructors

####basic levels

- var fooBar = new Array (1,2,3,4)<br>
undefined<br>
- fooBar<br>
[1,2,3,4]
<br><br>

####Every constructor has a prototype object.

- Array.prototype.coolGuy = function () { return "you're cool" }<br>
undefined<br>
- [1,2,3].coolGuy()<br>
"you're cool"
<br><br>

####What?

- var coolArray = [1,2,3]<br>
undefined
- coolArray.lastTwo = function() { return this.slice(-2) }<br>
function (){return this.slice(-2) }
- coolArray.lastTwo()<br>
[2, 3]
- Array.prototype.lastTwo = function() { return this.slice(-2) }<br>
function (){return this.slice(-2) }
- [3,4,5].lastTwo()<br>
[4, 5]
<br><br>

#####Adding a property to the Object parent itself

- Object.prototype.fooBar = "wat"<br>
"wat"
- [1,2,3].fooBar<br>
"wat"
<br><br>

####Screwing up javascript's code.

- myArray = [1,2,3]<br>
undefined
- myArray.pop()<br>
3
- myArray.pop = function(){ return this[0] }<br>
function (){ return this[0] }
- myArray.pop()
myArray.pop()<br>
1

####Return which prototype is being used

- var instance = [1,2,3]
- instance.contructor.name<br>
[returns the prototypes name]<br>
"Array"

##Creating our own constructors
In this example, .this refers to the context to which it was called, which in this case was literally the browsers window.

	function Dog () {
		this.legs = 4;
		this.bark = function () { return "WOOF" }
	}
	undefined
	
	Dog()
	undefined
	
	window.legs
	4
	
	window.bark()
	"WOOF"
	
	window
	'window.webkitStorageInfo' is deprecated. Please use 'navigator.webkitTemporaryStorage' or 	'navigator.webkitPersistentStorage' instead. VM61:437
	Window {top: Window, window: Window, location: Location, external: Object, chrome: Object…}

Using the "new" keyword allows a new object to created.
It also lets .this 
refer to THIS function, not it's parent.

	var fido = new Dog();
	undefined
	
	fido.legs
	4
	
	fido.color = "brown"
	"brown"
	
	fido.constructor.name
	"Dog"
	
	fido.constructor.prototype
	Dog {}
	
	sadie = new Dog()

##

Whenever something doesn't make sense to javascript, it will jump up the prototype chain to see if it can make sense of things.

## 

		dog = {
			name: "fido",
			species: "dog",
		}
	
		dog.woof = woof
		dog.legs = 4
				
	
##Inheritance
Classical inheritance is based off of classes. Classes are best thought as groupings.  
Class of motor-vehicles, then classes inside of that like .cars, .planes
 

###Prototypal Inheritance
When an object in javascript is created its part of a prototype chain.   
Almost everything in javascript is an object and objects can be given properties.
####Prototype chain <br>

Down each rabbit hole of an object, there are more prototypes to the prototypes.

        Object                          object
    String  Arrray					Number
    			pop()


##Homework
Create a game where you have 3 types of players.  Those will be in the form of three different constructors.  When you fire it up there should be three buttons (html) please choose your player type.

Using constructor will create a player object depending on button press.

Next, have three or for enemy constructors.

Give player points or something when it hits zero its game over.

Should have three actions that they can take (this.whatever) (this.idk).  When you run that it should target the bad guy object and mutate his object. Every time that enemy's health is at zero you move on to next bad guy.

When you get hit etc, update a div with the number.

After you defeat one bad guy, it will go on to next bad guy and a new bad guy object will be created.

Estimated lines of code.  300-400 lines of code.  Refactored could be -100 lines of code.

		ace = new Dog
		Dog { legs: 4, bark: funciton}
		
		ace.bark
		function () {return barkNoise + ' ' + barkNoise}
	
		ace.bark(badGuy)
		
	
	
		$(.choose-character).click(function() { 
		player = new Player();
		})
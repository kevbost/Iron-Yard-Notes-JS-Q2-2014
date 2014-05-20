#Constructors Day 2
## 

#[Back to INDEX](../../Iron%20Yard%20Index.md)


For inevitable huge blocks of code, you can use javascript switch case  
<https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/switch>

## 


###Empty functions  
An empty function is okay.

	function abc () { }
		undefined
<br>

###Functions with side-effects
Side effects change something that was defined globally.

	function abc () { 
		window.fakeProperty = true 
	}
<br>


###Pure Function without a side-effect
Pure functions have zero side effects and an explicit return value

	function abc (target) { 
		target.fakeProperty = true 
	}
	
	abc( window )
<br>

## 
###Class notes transcribed from chrome's console
	var player = {name: 'mason', hp: '10'};
	enemy.attack = function(){ player.hp = player.hp-5}
	enemy.attack()

	player
	{name: 'mason', hp: '5'};


	//========================
	
	var player = {name: 'mason', hp: '10'};
	enemy.attack = function(target){ 
		target.hp = target.hp-5 
	}
	enemy.attack(target)

	player
	{name: 'mason', hp: '5'};
	
	
	//======================================
	//== return player object after mutation
	//======================================
	
	var player = {name: 'mason', hp: '10'};
		enemy.attack = function(){ 
		player.hp = player.hp-5;
		return target;
	}
	enemy.attack(player)
	Object {name: 'mason', hp: '5'};
	
	
	//=========================
	// Make an object's child called inventory
	// and make it an empty array
	//=========================

	var item = {bonus: 5}
	player.inventory = []
	player.pickUp = function(item) {
		player.inventory.push(item)
	}
	
	//=========================
	//pretend function to remove item from array
	// $('.class').click(function(){
	// 	 player.inventory.pop(item);
	// })
	
	//==========================
	// Pick up many items at once
	//==========================
	
	player.pickUpMany = function(items) {
		player.inventory.concat(items);
	})
<br>
##Make a player Constructor
######Never use the new keyword when you're defining for the first time
######"THIS" will attach things to your new object to be used later on by literally anything this constructor is used for.
######Constructors DO NOT make object literals
######Dont name variables newThing, don't forget to use new Thing syntax when creating a new Object() [ie: kevin = new Player()]

	// player
	//		Object {
	//			name: "mason", 
	//			hp: 5, 
	//			Inventory: array[1]
	//		}

	function Player( ) {
		this.status = "healthy";
		this.attack = function( target ) { <!-- empty for whatever you want to pass through this function later -->
			target.hp = target.hp - 5;
		}
	}
	
	mason = new Player();
<br>
## 
###DOM Manipulation
######based on mason's game example
	
	$('.button').click(function(){
		console.log('wow');
		return true
	})
	
	or
	
	function exampleFunction (){
		console.log('wow');
	}
	
	$('.button').click( exampleFunction )
	
	
## 
###Javascript Koans
IMPORTANT  
Tests are written FIRST to avoid false positives.


## 
###Limit the length of an array (per inventory limit)
######generally a bad idea

	var arrayOfTen = [1,2,3,4,5,6,7,8,9,10]
	
	arrayOfTen.length
	10
	arrayOfTen.length = 5
	5
	arrayOfTen
	[1, 2, 3, 4, 5]
	
	
	
	//

#Github, APIs, Yeoman, Grunt, Underscore
## 

#[Back to INDEX](../../Iron%20Yard%20Index.md)
## 


##May 14, 2014
"bugs are often the compound effect of many small mistakes" - masondesu

<br>


##YEOMAN (and Grunt)
"The web's scaffolding tool for modern webapps"
	
	$ yo webapp						# scaffold out a skeleton web app project
	$ bower install underscore		# install a dependency for your project from Bower
	$ grunt							# build the application for deployment
	$ grunt serve					# tests for success by loading live in browser
<br>


##JSON API's
Javascript Object Notation

* Everything is a "string" because javascript has reserved words
	* so {"function" : "foobar"} is valid because the word function is in a string.
* A Restful API will make heavy use of URLS.
* Uses a very consistent URL syntax.
<br>


##BOWER.IO
* Is for FRONT END PACKAGES
* NPM is for BACKEND PACKAGES
* <http://bower.io/>
* Built by twitter.
		* $ bower install --save underscore 
	* (--save will tell bower that this is a permanent dependency to this project)
* INSTALLING A PACKAGE VIA BOWER DOESNT AUTOMATICALLY ADD IT TO THE HTML
<br>


##UNDERSCOREJS.ORG

* <http://underscorejs.org/>
* Full documentation available on their website.
	* Underscore is entirely mutation free.
* examples
	
		_.where(list, properties)
		_.reject(list, properties)
		_.pluck(list, propertyName)
		_.zip([*arrays],[2,1,3,4,5],[a,b,c,d,e,f])
<br>

#HOMEWORK

* Rebuild github profile.
* Loop over the array of repo objects, fetching the real data.
* github api
* <a href="api.github.com/users/kevbost">api.github.com/users/kevbost</a>

<br>
		
 
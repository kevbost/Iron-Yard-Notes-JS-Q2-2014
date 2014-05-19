##May 14, 2014


##HTTP

IE6 had a protocol built in called: 

* XMLHTTPRequest (XHR)
* web servers normally listen for traffic on port 80

has functions:

* GET - will fetch data.
* POST - will send data and PUT will send data.
* put/patch
* DELETE - well... um.  deletes data.


##AJAX

$.ajax is jQuery's solution to http requests.

	$.get( wants a url )
	$.post( wants a url, plus data )
	$.getJSON( wants a url )
	
##Synchronous and Asynchronous
Asynchronous.done()

	$.getJSON('https://api.github.com/users/kevbost/repos').done(function(data){
	  console.log(data[0].name);
	})
	
	//==============================================
	
	var repos;
	$.getJSON('https://api.github.com/users/kevbost/repos').done(function(data){
		repos = data
		console.log('ajax GET finished!', Date.now() )
		});
	console.log('repos is', repos, Date.now() );
	
	
		logs:
			repos is [Object, Object, Object, Object, Object, Object, Object, Object, Object] 1400165458613
			undefined
			ajax GET finished! 1400165458766 
			
##class example

	// Templates
	// function              function         string
	var showRepos = _.template($('.repos').text());

	// Fetch repos
	$.getJSON('https://api.github.com/users/kevbost/repos').done(function(repos){
    renderRepos(repos);
	});

	// Render functions
	// repos
	function renderRepos (arrayFoobar) {
    arrayFoobar.forEach(function(module){
        // string        function     object
        var rendered = showRepos( module );
        $('body').prepend(rendered);
    });
	}
	
	
	
##extra
templates to setup sidebar, main etc
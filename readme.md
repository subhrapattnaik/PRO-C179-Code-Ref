
Write JavaScript functions to get the current location of the user.
● Use query parameters to pass information from one page to another.
-----------------------------------------------------------------------

In JavaScript, there is a special object called “navigator” that contains a lot of things.

Refer Student Activity 1


we will be using is its geolocation property. It returns a geolocation object that can be used to locate the user’s position


Remember that this is browser-dependent. It could be the case where the user’s browser does not provide geolocation services and hence, it will not work
-------------------------------------------------------------------------
main.js 
-------

initGeolocation(){



}

Here, we are checking if there exists a navigator.geolocation object or not. If it doesn’t,we are throwing an alert for the user informing them that the browser does not support geolocation services.

The object that navigator.geolocation returns has a function called getCurrentPosition() which takes a function it should call if it can
successfully get the current position of the user.

It provides the user’s current position to the success callback function in the form of an argument


This means that if the getCurrentPosition() works properly and is able to get the user’s location, it will call the success() function in which it will provide the user’s current position as an argument.

Now in order for this to work, we will also have to create another function called success() -

---------------------------------------
Let’s now open our main.html and see what we get in the console

The console is empty because we are not calling the initGeolocation() function anywhere and it is not executing.

We should have a $(document).ready() function and call this function inside it.

So that this function can get executed as soon as the page is loaded and we get the current position of the user
-----------------------------------
We now have an object which contains a key called coords. Inside this key, we can find the latitude and the longitude.
Let’s reload this page and see what happens if we don’t allow the browser to know the position

----------------------------------
inside our success() function, let’s add an on click function first and see the things we are getting out of it -
This is another way of how we can write our jQuery functions for various events, such as click, change, etc

we can see the console.log() happening 2 times. The first time when we select the
A point (starting location) and the second time when we select the B point (destination location)

We can also see a lngLat key which contains the latitude and the longitude of the pointsvwe have clicked on.

Now assuming that the user will always select the starting point first and the destination
point second, we can create a variable destination in which we can save the latitude and
the longitude both the times, and we will receive our destination’s latitude and longitude

-----------------------------------------------

Here, anything before the question mark - (?) - is the URL and anything after that are the
query parameters.
Question Mark (?) separates the URL from the query parameters.
Now the parameters are separated by an ampersand - (&) - so in this example, we have
3 query parameters:
1. arg1=1
2. arg2=2
3. arg3=3
Now it’s easy to guess the rest of it. arg1, arg2 and arg3 are the variables whose
respective values are 1, 2 and 3

--------------------------------------

Following this format, we can pass our starting coordinates and ending coordinates to the next page.
We will have to create a click() event function on our navigate button to do that.

Now we will need ar_navigation.html for the next screen and the corresponding files for it -
ar_navigation.js and ar_navigation.css.


In the JavaScript file, the first thing that we need to do is to fetch the query
parameter.
Let’s see how to do that now(in ar_navigation.js file).


Now, there’s a method that gets the query parameters for us in JavaScript. It’s called
URLSearchParams() that takes the query parameters and creates an object for the
key-value pairs from it.

We can get our query parameters from window.location.search. This gives us the
following.

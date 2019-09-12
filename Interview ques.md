

# CSS 

1) Absolute vs Relative in depth
https://www.w3schools.com/cssref/tryit.asp?filename=trycss_position2

que : how would you make this at the bottom?using relative,height of body

~~~html
<style>

body{
   height: 100%;
}

div.relative {
  position: relative;
  bottom: 0;
  border: 3px solid #73AD21;
}

or 

div.relative {
  position: absolute;
  bottom: 0;
  border: 3px solid #73AD21;
}

</style>
</head>
<body>


<div class="relative">
This div element has position: relative;
</div>

	
~~~

2) 4 div in row , swap 3rd and 4th 

3) diff btw 3 div with relative and 3 div with absolute


Absolute 

```css

 #box_1 { 
	position: absolute;
	width: 200px;
	height: 200px;
	background: #ee3e64;
    border : 2px solid black
}

#box_2 { 
	position: absolute;
	width: 200px;
	height: 200px;
	background: #44accf;
}

#box_3 { 
	position: absolute;
	width: 200px;
	height: 200px;
	background: #b7d84b;
}


Relative


  #box_1 { 
	position: relative;
	width: 200px;
	height: 200px;
	background: #ee3e64;
    border : 2px solid black
}

#box_2 { 
	position: relative;
	left: 200px;
	width: 200px;
	height: 200px;
	background: #44accf;
}
#box_3 { 
	position: relative;
	width: 200px;
	height: 200px;
	background: #b7d84b;
}

```


4) explain box model , box sizing 

<div> <div>
	
div {

}
	


5) diff between inline and inline-block
6) what is fixed positioning : what happens to width and height if you apply the fixed positioning on some element.

```html
<body>
        <div class="parent">
            <div class="child-1">Navigation Bar</div>
            <div class="child-2">Background Image</div>
            <div class="child-3">Features</div>
        </div>
    </body>

```

que : selectors :

difference btw .class1 .class2 and .class1.class2 


que inline vs external vs internal css
https://www.w3schools.com/css/css_howto.asp


que : how to centre a div inside another div
https://www.youtube.com/watch?v=ZohZS6xLYE4&list=PL7pEw9n3GkoWn5TcqAdmSzXcvC3d_tfAh&index=3
https://www.w3schools.com/css/tryit.asp?filename=trycss_position_absolute


```html
<div class="parent">This div element has position: relative;
  <div class="child">This div element has position: absolute;</div>
</div>
```

```css

div.parent {
 
  width: 400px;
  height: 200px;
  border: 3px solid #73AD21;
} 

div.child {
  
  top: 80px;
  right: 0;
  width: 200px;
  height: 100px;
  border: 3px solid #73AD21;
}

```

### que : semantic html elements and their order 
https://www.w3schools.com/html/html5_semantic_elements.asp

### que : lazy loading images
https://app.pluralsight.com/player?course=responsive-web-design-images-sliders&author=paul-cheney&name=responsive-web-design-images-sliders-m8&clip=0&mode=live



# JS

que1 
// Function to remove two adjacent duplicate characters from a string.
// let str = 'abbbbaca';
// output: 'ca'

### que 2:
Singleton pattern


### que 3 :

explain the diff between promise and observable

### que :
 merge two arrays , remove duplicates and all positive ids only and in sorting order
 
 arr1 = [{id:1},{id:4},{id:2},{id:6}]
 arr2 = [{id:7},{id:1},{id:6},{id:3},{id: -1}]

use this : https://reactgo.com/removeduplicateobjects/

### que : 

flat a nested array 

que :

obj = {
  i = 0 ;
toString:function(){
     obj.i++
   }
}

obj == 1 , obj == 2 , obj ==3

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce#Flatten_an_array_of_arrays
https://medium.com/dailyjs/flatten-array-using-array-flat-in-javascript-ee4d0b2423e5
https://stackoverflow.com/questions/10865025/merge-flatten-an-array-of-arrays


### que : session storage vs local storage
https://javascript.info/localstorage


# React

### que 1 : https://codepen.io/deen_john/pen/qeoGLN?editors=0010
  // API - https://jsonplaceholder.typicode.com/users
// API - https://jsonplaceholder.typicode.com/posts


### que : What is a valid return from react render function?
false , string , number 
https://reactjs.org/docs/jsx-in-depth.html#booleans-null-and-undefined-are-ignored


que : is redux unidirectional or bidirectional


# Angular
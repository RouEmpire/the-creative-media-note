type:: [[Programming Framework]] 
language:: [[JavaScript]]

- Vue JS is the JavaScript framework for Front End Development, it's make HTML elements dynamic
- # Class 1
	- ## Setup Environment for learing
		- In order to set up **Vue JS** we have to make 2 files, `index.html` and `App.js`
		  logseq.order-list-type:: number
		- Put a Basic HTML Structure into the file, like this
		  logseq.order-list-type:: number
			- ```html
			  <!DOCTYPE html>
			  <html lang="en">
			  <head>
			      <meta charset="UTF-8">
			      <meta name="viewport"
			            content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
			      <meta http-equiv="X-UA-Compatible" content="ie=edge">
			      <title>My Vue Learning Project</title>
			  </head>
			  <body>
			  
			  </body>
			  </html>
			  ```
		- Add this JavaScript [[CDN]] in to the `<head>` of the html file, in this case its called *VueJS CDN*
		  logseq.order-list-type:: number
			- **VueJS CDN**
			  id:: 66b19a7d-8b9d-497f-93d1-0aca8588ba59
				- ```html
				  <script src="https://unpkg.com/vue@3/dist/vue.global.js"></script
				  ```
		- Open the browser, then open the HTML in that browser. I here, check the *console* in the *inspect menu* of the browser. make sure that you see the message that tells you that this webpage is running on Vue JS
		  logseq.order-list-type:: number
	- ## Create VueJS App
		- Open `App.js` and delcare `App` like this
		  logseq.order-list-type:: number
			- logseq.order-list-type:: number
			  ```js
			  const App;
			  ```
		- Assign `Vue.createApp()` in to `App` like this
		  logseq.order-list-type:: number
			- ```js
			  // App.js
			  const App = Vue.createApp();
			  ```
			- The command `Vue.createApp()` is the command that create and store the content of you website (eg., HTML Elements, variable, functions)
		- Now, we create app, but doesn't mount it to the HTML files anymore. I order to do that, use `App.mount()` method. Put the ID of the `<div>` you want to mount as a method argument.
		  logseq.order-list-type:: number
			- First, Make sure you have `<div>` that has an ID on it.
				- ```html
				  <!-- html -->
				  <div id="myApp">
				     
				  </div>
				  ```
			- Second, Use `mount` method in App.JS after `Vue.createApp()`
				- ```js
				  // App.js
				  const App = Vue.createApp()
				  
				  App.mount("#myApp")
				  ```
			- Third, Import the `App.js` file into HTML with the `script:src` way
				- **VueJS** `script:src`
				  id:: 66b19b3f-b2cf-4a84-b56b-d10b558d10ee
					- ```html
					  <script src="./App.js"></script>
					  ```
			- The Final form should look like this
				- ```html
				  <head>
				    <script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
				  </head>
				  
				  <body>
				      <div id="myApp"></div>
				  
				     <script src="./App.js"></script>
				  <body>
				  ```
		- After we create the **VueJS App**, there's nothing happend in the browser
		- Remeber that whatever code we wrote in the `App.js` will only affect in the `div#myApp` only, we can still make changes in other part of the HTML freely and it won't affect the `div#myApp`
	- ## Root Component
		- In order to create anything in the HTML by writing code in the `App.js`. You have to put a **Object** in the `Vue.createApp()` like this
			- ```js
			  const App = Vue.createApp({})
			  // or this way, not much different
			  const App = Vue.createApp({
			  
			  })
			  ```
			- In the object. It's the place where we control the web page (only in the `div#myApp`)
			- In the object, we can put 2 things. **Data**, **Template** and **Function** that can be run when user do something on the web page
				- **Data**
					- It's a Variable that you can *Call or Access* them in the HTML file
				- **Templete**
					- It's a group of HTML tag that will be inject directly into the HTML file
				- **Function**
					- It's a JavaScript function or method
		- ### Using Template
			- Any content in any element in the **Template** are dynamic, which mean you can put directly any words or contents, or just put it a variable name between the tag.
			- #### Injecting from App.js
				- Insert `templete:` in the object, then follow it with any HTML tag/content you like
					- ```js
					  cosnt App = Vue.createApp({
					     template: "<h1> Hello World </h1>"
					  })
					  ```
				- The HTML element in `template` will be inject into the HTML file if that HTML file has...
					- Right HTML5 Structure
					  logseq.order-list-type:: number
					- Include the ((66b19a7d-8b9d-497f-93d1-0aca8588ba59)) in the `<head>`
					  logseq.order-list-type:: number
					- has `div#myApp` or other ID name that its works as you like
					  logseq.order-list-type:: number
					- has ((66b19b3f-b2cf-4a84-b56b-d10b558d10ee)) after the `div#myApp`
					  logseq.order-list-type:: number
			- #### Code it directly in Index.html
				- Basically write any HTML tag/content in the `div#myApp` the **VueJS** will automatically consider it as a template
			- ### Variable
				- **To call**
					- To call any variable in `template`  we use **Mustache brace**
						- **Mustache brace**
						  id:: 66b84564-ef98-4088-9340-9fd88a60875c
							- We can call a variable value in the HTML file (to display it) via this method. it looks like > `{{` and `}}` we put them between the variable that to be call
							- Assume we have a variable `age` in JavaScript and we want HTML to display the value of this variable, we write `{{ age }}` such as...
								- ```html
								  <p> Hi, my name is Zeen and I'm {{ age }} years old </p>
								  ```
								- or...
								- ```js
								  ...
								  template: "Yo, my name is {{ name }}"
								  ...
								  ```
								- (If you have do both method, The `template` will replace every elements in `div#myApp`)
				- **To declare**
					- To declare a variable that can be use in the HTML file, we need to follow these step
						- In the `Vue.createApp` function, we put a `data() {}` inside. It should look like this
						  logseq.order-list-type:: number
							- ```Js
							  const App = Vue.createApp({
							     template: "Hello World",
							     data() {}
							  })
							  ```
							- if you have `template` before that data, you have to put `,` at the end of it
						- in the `data() {}` put a `return` in an object inside it, make sure it's return object too.
						  logseq.order-list-type:: number
							- ```js
							  const App = Vue.createApp({
							     template: "Hello World",
							     data() {
							        return {}
							     }
							  })
							  ```
						- In the `return {}`, you can now put in any variable you like, such as...
						  logseq.order-list-type:: number
							- ```js
							  const App = Vue.createApp({
							     template: "Hello, I'm {{ name }} and I'm {{ age }} years old",
							     data () {
							        return {
							           name : "Zeen"
							           age : 19
							        }
							     }
							  
							  })
							  ```
							- In case you have nothing in `template` , you can display it via ((66b84564-ef98-4088-9340-9fd88a60875c)) such as...
							- ```html
							  <div id="myApp">
							     <p>Hello, I'm {{ name }} and I'm {{ age }} years old</p>
							  </div>
							  ```
				- **JS Expression**
					- You can make a JS Expression inside ((66b84564-ef98-4088-9340-9fd88a60875c)) such as...
						- ```html
						  <p> The result is {{ 5 + 5 }} </p>
						  <p> "this is a string, not var" </p>
						  <p> {{'Random number: ' + Math.ceil(Math.random()*6) }} </p>
						  ```
- # Class 2
	- ## Vue Directive
	  id:: 66b85147-37f2-4b8a-80b7-e902175bb1df
		- Assumed that we have this in our *App.js*
			- ```js
			  const App = Vue.createApp({
			     data() {
			        target:"https://google.com"
			     }
			  })
			  ```
			- Trying to have a variable inside href attribute it won't work
			- ```html
			  <div>
			     <a href="{{ target }}">  Click me </a>
			  </div>
			  ``` 
			  #+BEGIN_CAUTION
			  ONLY JUST **FALSE/WRONG** SAMPLE
			  #+END_CAUTION
		- In order to do the samething bu working we need to use ((66b85147-37f2-4b8a-80b7-e902175bb1df))
		- **To make Vue Directive**
			- Every Vue Directive has `v-` prefix, then follow by the kind of Directive you need
				- v-bind
				  logseq.order-list-type:: number
				- v-if
				  logseq.order-list-type:: number
					- v-if
					  logseq.order-list-type:: number
					- v-else-if
					  logseq.order-list-type:: number
					- v-else
					  logseq.order-list-type:: number
				- v-show
				  logseq.order-list-type:: number
				- v-for
				  logseq.order-list-type:: number
				- v-on
				  logseq.order-list-type:: number
				- v-model
				  logseq.order-list-type:: number
			- **V-DIRECTIVE**
				- `v-bind`
				  logseq.order-list-type:: number
					- We put `v-bind:` in front of any HTML Attribute to make it **Dynamic** such as...
						- ```html
						  <div id="app">
						     <a v-bind:href="target"> Click me </a>
						  </div>
						  ```
						  ```js
						  const App = Vue.createApp({
						     data() {
						        return {
						           target:"https://rouempire.github.io"
						        }
						     }
						  })
						  ```
						- Now, the Attribue value in `href` in *HTML file line 2* are dynamic, and it when user click that Element in the browser, it will load `rouempire.github.io` website instead of error
					- Shorthand
						- the `v-bind` has it owns *shorthand* called `:` which do the same thing
						- This code with `:` are working the same with `v-bind:`
							- ```html
							  <div id="app">
							     <img :src="productImage">
							  </div>
							  ```
							- ```js
							  const App = Vue.createApp({
							     data() {
							        return {
							          productImage:"./MyFolder/product.jpg"
							        }
							     }
							  })
							  ```
					- TODO | Add `v-bind:class` with **Object** Value
				- `v-if`
				  logseq.order-list-type:: number
					- It's a condition, if **True** the element will be render, if not then it won't
						- ```html
						  <div id="app">
						     <p v-if="isDisplay_1"> Hello world! </p>
						  </div>
						  <!-- This <p> WILL be render on the user webpage --->
						  ```
						- ```html
						  <div id="app">
						     <p v-if="isDisplay_2"> Hello world! </p>
						  </div>
						  <!-- This <p> WON'T be render on the user webpage --->
						  ```
						- ```js
						  const App = Vue.createApp({
						     data() {
						        return {
						           isDisplay_1: true,
						           isDisplay_2: false
						        }
						     }
						  })
						  ```
					- We also can Use it with **Conditioning Check**
						- ```html
						  <p v-if="isDisplay_1 && isDisplay_2"> AND Operator </p>
						  ```
						- ```html
						  <p v-if="isDisplay_1 || isDisplay_2"> OR Operator </p>
						  ```
						- ```html
						  <p v-if="num_1 > num_2"> MORE THAN Operator </p>
						  ```
						- ```html
						  <p v-if="isDisplay_1 && isDisplay_2"> And Operator </p>
						  ```
					- More `v-if` conditoning
						- `vi-else`
						  logseq.order-list-type:: number
							- The element with `vi-else` needs *no Attribute Value*
							- The element with `vi-else` needs to be place *right after the element with `vi-if` Attribute*. If not, it will throw an error in the browser console
							- This is how it using
								- ```html
								  <div id="app">
								     <h1 v-if="myVar"> Main Header </h1>
								     <h2 v-else> Sub Header </h2>
								  </div>
								  ```
								- If...
									- The `myVar` is **true** | only `<h1>` will be render
									- The `myVar` is **false** | only `<h2>` will be render
								-
						- `vi-else-if`
						  logseq.order-list-type:: number
							-
-
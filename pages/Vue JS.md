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
			      <title>My Web Project</title>
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
		- Open `App.js` and assign `Vue.createApp()` in to `const App` like this
		  logseq.order-list-type:: number
			- ```js
			  // App.js
			  const App = Vue.createApp();
			  ```
			- The command `Vue.createApp()` is the command that create the part of the web to control
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
		- After we create the VueJS App, there's nothing happend in the browser
		- Remeber that whatever code we wrote in the `App.js` will only affect in the `div#myApp` only, we can still make changes in other part of the HTML freely and it won't affect the `div#myApp`
	- ## Root Component
		- In order to create anything in the HTML by writing code in the `App.js`. You have to put a **Object** in the `Vue.createApp()` like this
			- ```js
			  const App = Vue.createApp({})
			  // or this way
			  cosnt App = Vue.createApp({
			  
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
				- **To call** any variable in `template` you have to write it withthin `{{` and `}}`
					- Assume we have a variable `age` in JavaScript and we want HTML to display the value of this variable, we write `{{ age }}` such as...
						- ```html
						  <p> Hi, my name is Zeen and I'm {{ age }} years old </p>
						  ```
				- **To declare** a variable that can be use in the HTML file, we need to follow these step
				- In the `Vue.createApp` function, we put a `data() {}` inside. It should look like this
				  logseq.order-list-type:: number
					- logseq.order-list-type:: number
					  ```Js
					  const App = Vue.createApp({
					     template: "Hello World",
					     data() {}
					  })
					  ```
					- if you have `template` before that data, you have to put `,` at the end of it
					  logseq.order-list-type:: number
				- in the `data() {}` put a `return` in an object inside it, make sure it's return object too.
				  logseq.order-list-type:: number
					- logseq.order-list-type:: number
					  ```js
					  const App = Vue.createApp({
					     template: "Hello World",
					     data() {
					        return {}
					     }
					  })
					  ```
				- In the `return {}`, you can now put in any variable you like, such as...
				  logseq.order-list-type:: number
					- logseq.order-list-type:: number
			-
			-
-
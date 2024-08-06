- Vue JS is the JavaScript for Front End Development, it's make HTML elements dynamic
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
		- Add this JavaScript [[CDN]] in to the `<head>` of the html file
		  logseq.order-list-type:: number
			- logseq.order-list-type:: number
			  ```html
			  <script src="https://unpkg.com/vue@3/dist/vue.global.js"></script
			  ```
		- Open the browser, then open the HTML in that browser. I here, check the *console* in the *inspect menu* of the browser. make sure that you see the message that tells you that this webpage is running on Vue JS
		  logseq.order-list-type:: number
	- ## Create VueJS App
		- Open `App.js` and assign `Vue.Create()` in to `const App` like this
			- ```js
			  // App.js
			  const App = Vue.Create();
			  ```
			- The command `Vue.Create()` is the command that create the
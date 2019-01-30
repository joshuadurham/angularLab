
# angularLab

#### What is this lab about

This lab is from the 2019 Crash Course Talk for Angular 7 and TypeScript. The lab goes through building some basic components and services in a new Angular project.

If you want more information on the Angular framework and to learn more, check out [angular.io](https://angular.io) for more tutorials and up-to-date documentation

#### Downloading necessary software

The three main pieces of software needed to work on this lab are [Node.js](https://nodejs.org/en/) with the Node Package Manage (NPM), [Angular CLI](https://cli.angular.io/). The download instructions should be fairly straightforward for each of the above pieces of software.  Following the steps on the Angular CLI website for installation should also install all other dependencies such as TypeScript.  For future development projects with Angular, I recommend using [Microsoft Visual Studio Code](https://code.visualstudio.com/).  I also personally work with some free VS Code extensions that make development easier in TypeScript, namely TSLint, Path Intellisense, Bracket Pair Colorizer, and Angular Language Service.  These extensions are widely popular and should be easy to find on the VS Code built-in extensions marketplace.

#### Setting up this project

Once you have Angular CLI installed, you can run 'ng new project-name', and then Angular CLI will automatically generate a new Angular project for you with the title of 'project-name'.  Entering the directory where this project is located and running the command 'ng serve' will spawn the Angular development server, and going to [localhost:4200](localhost:4200) in your favorite browser should show you the standard web application created when building a project with Angular CLI (there should be a big red Angular logo and some links to Angular's website shown if you did this correctly).  We now have an Angular application made that we are able to add new components and services to.

#### Your Task

Your job is to create two Angular components, one component that displays the number of times that a button is pressed, and another component that creates a bulleted list of users whose data we access from an API.  You will also create a small Angular service for making HTTP requests to this API that your component can inject to access the necessary user data.

## Create the Button Component

Create a new component using 'ng generate component button-counter' to spawn a new collection of files for creating this new component.  Use the various Angular bindings discussed in the presentation slides to create one event binding such that on the click of the button, we increment the value of a counter, and another binding that allows us to display the current number of clicks in our counter as a string on the webpage.  This simple component gives us a great insight into how the Angular binding structure lets us connect HTML to TypeScript very easily.  Make sure to add a \<button-counter\> to the HTML of your app.component.html file in order to make sure that your new component shows up in the browser.

## Create the User List Component

Create a new component using 'ng generate component user-list', and now create a component that manages a list of users and displays their relevant data in a bulleted list.  Create a list variable for holding the various user objects, and use the \*ngFor directives to spawn a new bulleted list element for each user in the list found in the TypeScript code.  We will populate this list of users data after we make a service for accessing user data from an API.  Make sure to add a \<user-list\> to the HTML of your app.component.html file in order to make sure that your new component shows up in the browser.

## Create the Service for Getting User Data

Create a new service using 'ng generate service user-data', and add to this service a function that returns an observable from an HTTP GET request to an API that generates fake JSON user data [https://jsonplaceholder.typicode.com/users](https://jsonplaceholder.typicode.com/users).  Now back in your User List Component, inject the service by adding and instance of the User Data service in the constructor of our component, and in ngOnInit(), call the data service and subscribe to the returned observable to access the user data and store it in your list of users.  Check out [JSON.parse()](https://www.w3schools.com/js/js_json_parse.asp) for converting the JSON data returned by the API into a list of useable objects that your TypeScript code can manage and manipulate.

## More Tasks

If you get through the first few tasks of this lab, great job!  Keep adding more components that let you get a good feel for Angular's 

Make sure to refer to the slides or the online Angular documentation if you get stuck or want to learn more about a topic.  Ask questions if you need help, and have fun!

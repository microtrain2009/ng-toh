# ng-toh
## Angular PWA Tour of Heroes

The Tour of Heroes app helps a staffing agency manage its stable of heroes. The app has many of the features you'd expect to find in any data-driven application. The finished app acquires and displays a list of heroes, edits a selected hero's detail, and navigates among different views of heroic data.

> You will find references to and expansions of this app domain in many of the examples used throughout the Angular documentation, but you don't necessarily need to work through this tutorial to understand those examples.

By the end of this tutorial you will be able to do the following:
* Use built-in Angular directives to show and hide elements and display lists of hero data.
* Create Angular components to display hero details and show an array of heroes.
* Use one-way data binding for read-only data.
* Add editable fields to update a model with two-way data binding.
* Bind component methods to user events, like keystrokes and clicks.
* Enable users to select a hero from a master list and edit that hero in the details view.
* Format data with pipes.
* Create a shared service to assemble the heroes.
* Use routing to navigate among different views and their components.
* You'll learn enough Angular to get started and gain confidence that Angular can do whatever you need it to do.

Angular *Tour of Heroes Tutorial* [https://angular.io/tutorial]

## Build a production package
Find the file src/angular.json and follow the JSON objects the tree until you get to your build options project > architect > build > options.

Update your build options as follows.

* add a new option "baseHref": "/ng-toh/",
* change the outputPath "outputPath": "/var/www/ng-toh",
Changing the output path will allow the build process to write the distribution package to any directory you want. You could write this into the webroot of an existing project or simply write it to the webroot of your local server as demonstrated below.
```
"options": {
  "baseHref": "/ng-toh/",
  "outputPath": "/var/www/ng-toh",
  "..."
}
```
Now use the Angular CLI to build a production package.
```
ng build --prod
```
Navigating to http://localhost/ng-toh will show a working application.

`Commit your changes`

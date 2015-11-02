# MeteorBox
A starter for MeteorJS

# Folder Structure
Files are loaded alphabetically from A-Z with main being loaded last. 

##Client

###Compatibility

###Stylesheets
###Views

##Lib
###Collections
Routes.js
Permissions.js

###Public

###Server
fixtures.js
publications.js

#Packages

Iron:router
This is pretty much the standard for routing with MeteorJS.

	this.route('about');
	<template name="about">
    <h1>About</h1>
	</template>

##Collection2

meteor add aldeed:collection2

Most Meteor applications will interact with a database in some way. By default though, you’ll have to manually validate the data that users are inserting, editing, and removing from the database.

Collection2 helps with this process by extending Meteor’s functionality, allowing it to “provide support for specifying a schema and then validating against that schema when inserting and updating.” For example, you can make it so a “Books” collection has a title field that must be a string, and a lastCheckedOut field that must be a date.

	var Schemas = {};

	Schemas.Book = new SimpleSchema({
	    title: {
	        type: String,
	        label: "Title",
	        max: 200
	    },
	    author: {
	        type: String,
	        label: "Author"
	    },
	    copies: {
	        type: Number,
	        label: "Number of copies",
	        min: 0
	    },
	    lastCheckedOut: {
	        type: Date,
	        label: "Last date this book was checked out",
	        optional: true
	    },
	    summary: {
	        type: String,
	        label: "Brief summary",
	        optional: true,
	        max: 1000
	    }
	});

##AutoForm
meteor add aldeed:autoform
aldeed:autoform: Easily create forms with automatic insert and update, and automatic reactive validation.

##Kadira
meteor add meteorhacks:kadira

A performance managing service. Super awesome for Meteorjs

##Spinner
meteor add sacha:spin

	{{> spinner}}
other options
	Meteor.Spinner.options = {
	    lines: 13, // The number of lines to draw
	    length: 10, // The length of each line
	    width: 5, // The line thickness
	    radius: 15, // The radius of the inner circle
	    corners: 0.7, // Corner roundness (0..1)
	    rotate: 0, // The rotation offset
	    direction: 1, // 1: clockwise, -1: counterclockwise
	    color: '#fff', // #rgb or #rrggbb
	    speed: 1, // Rounds per second
	    trail: 60, // Afterglow percentage
	    shadow: true, // Whether to render a shadow
	    hwaccel: false, // Whether to use hardware acceleration
	    className: 'spinner', // The CSS class to assign to the spinner
	    zIndex: 2e9, // The z-index (defaults to 2000000000)
	    top: 'auto', // Top position relative to parent in px
	    left: 'auto' // Left position relative to parent in px
	};

twbs:bootstrap: Contains the Bootstrap framework. One of the most popular front-end frameworks for developing responsive, mobile first projects on the web.
ChromaGrid
==========

A fluid grid system built on top of SASS. Easy to use while being flexible enough to create your very own grid. 

For a more detailed demo and documentation, please visit our [Demo Page](http://labs.neonpastell.de/ChromaGrid).



##Requirements

- [Sass 3.2+](http://sass-lang.com/)





## Getting started

### Installation
Add the chroma-grid folder to your project and start sass watch.
Optionally you can add the chroma-mixins.


### Basic setup
Copy all files in your sass folder and start compiling your sass files.
Change the grid settings in _grid-settings.scss to your own needs and import this file at the beginning of your main styles.

	// import default settings
	@import "chroma-grid/settings" 
	
	// overwrite the default settings
	$column-amount : 6;
	$column-width  : em(130);
	$column-gutter : em(30);
	$container-width     : em(930);
	
	// and import the main grid
	@import "chroma-grid/grid";
		
If needed, import the chroma mixins and you're ready to go.

	@import "chroma-mixins/all"



### A first and simple grid

This basic example creates an responsive page container with one row element containing a sidebar and a content element. The content area displays a nested matrix of floating image-items.

**The CSS**

	.container {
		@include container();
	}
	.row {
		@include row();
	}
	.sidebar {
		@include columns(4);
	}
	.content {
		@include columns(8);
	}
	.image-item {
		@include columns(2 of 8);
		@include omega(4);
	}

**The HTML DOM**

	<div class="container">
		<div class="row">
			<div class="sidebar"></div>
			<div class="content">
				<div class="image-item"></div>
				<div class="image-item"></div>
				<div class="image-item"></div>
				<div class="image-item"></div>
				<div class="image-item"></div>
				<div class="image-item"></div>
				<div class="image-item"></div>
				<div class="image-item"></div>
			</div>
		</div>
	</div>






	
	
## Credits & Licence
The **Chroma-Grid** is © Copyright 2014 [Neonpastell GmbH &mdash; Werkstatt für Gestaltung](http://www.neonpastell.de/ "Neonpastell GmbH") and is published unter the MIT License

Journalism Portfolio Template
=============
This is a basic HTML template for displaying a journalist's portfolio and resume. It's built on the [Bootstrap](http://getbootstrap.com/) framework, which means you can use any of the built-in bootstrap [CSS classes](http://getbootstrap.com/css/).

How it works
-------------
Click the **Download Zip** button on the right side of this screen. Find the zip file in your download's folder and unzip. Next, open the folder in a plain text editor like TextMate or Sublime.

You will want to open the `index.html` file, and edit this file. The entire webpage page is in this file.

Edit the metadata in the &lt;head&gt;
-------------
First step is to personalize the data in the &lt;head&gt; of your document. This is meta data which won't display for visitors to your site, rather it will be for Google search indexing, or when people like this page on Facebook/Twitter.

```html
<!-- Make sure you add a title -->
<title>Page Title</title>

<!-- Basic Google SEO stuff -->
<meta name="description" content="{Put a description here}">
<meta name="keywords" content="{comma separate list of keywords to describe this page, (things people might search for)}">
<meta name="author" content="{Your name}">

<!-- Fill Out Twitter information (for when people share this page on Twitter) -->
<meta name="twitter:card" value="summary">
<meta name="twitter:creator" value="@"/><!-- your twitter handle -->
<meta name="twitter:url" content="{URL for this page with http:// in front}"/>
<meta name="twitter:title" content="{Title for you site here}"/>
<meta name="twitter:description" content="{Description goes here}"/>
<meta name="twitter:image" content="{URL to an image file here}"/>

<!-- Fill Out Facebook account information (for when people like this page on Facebook) -->
<meta property="og:url" content="{URL for this page with http:// in front}"/>
<meta property="og:type" content="article"/>
<meta property="og:title" content="{Page title here}"/>
<meta property="og:description" content="{Description here}">
<meta property="og:image" content="{URL to an image file here}"/>
```

Every piece of text surrounded by curly brackets needs to be edited. You shouldn't publish a page with placeholder text.

Navigation, and how links work
-------------
To customize navigation, change the text in within the `<a>` tags. 

```html
<li><a href="#home">Home</a></li>
<li><a href="#about">About Me</a></li>
<li><a href="#portfolio">Portfolio/Clips</a></li>
<li><a href="#resume">Resume</a></li>
<li><a href="#contact">Contact</a></li>
```	
	
You should also link to pound-id (#idname) of another section on the page, like this:

```html
<a href="#contact">
```

In this example, the `#contact` refers to an id set later in the page. Putting it in this &lt;a&gt; tag will cause the page will automatically scroll to that section when a visitor clicks on the link.

Later in the page, a div tag needs to have the matching id:

```html
<div class="featurette" id="contact">
```

Notice how `id="contact"` matches the `<a href="#contact">`? When they click on the link, the page will scroll down to the &lt;div&gt; with that id. Make sure you don't put the pound symbol in the actual id attribute.

Jumbotron with greeting
-------------
The Jumbotron is the big element at the top of the page displaying the author's name. Simply edit the text within the tags. You can remove the `<p>` tag if you prefer to only have your name, and don't wish to have a tagline.

```html
<div class="container" id="home">
	<div class="jumbotron">
			<h1>Hello. I'm {insert name}.</h1>
			<p class="lead">This is my web page with all of my clips.</p>
	</div>
</div>
```

In the CSS at the top of the page, you can customize the Jumbotron to a certain extent. Notably, you can add a background image. Use only images which won't distract from the text.

```css
.jumbotron {
	text-align: center;
	background:url(' ... ') no-repeat center center; 
	color:white;

}
```

Three circles promoting sections of the project
-------------
These next items are pretty self-explanatory. You can edit them as needed, or even add more. They are setup as modules, so you'll need the entire thing.

```html
<div>
	<a href="#about"><!-- links to about section -->
		<img class="img-circle" src="http://placehold.it/140x140" alt="Generic placeholder image">
	</a>
	<h2>Student</h2>
	<p>I'm a student at UC Berkeley's Graduate School of Journalism. Word. </p>
</div>
```

Notice how the &lt;a&gt; tag links to the about section later in the document. 

Featurette sections
-------------
These are the central content sections throughout the bottom of the page. They follow this basic structure:

```html
<div class="featurette">
	<h2 class="featurette-heading"><!-- section title --></h2>
	<div class="row">
		<!-- put extra content here -->
	</div>
</div>
```

It requires an openind &lt;div&gt; tag with the class `featurette`, followed by an &lt;h2&gt; tag with with the class `feature-heading`. 

Next, you have a &lt;div&gt; tag with the class `row`, which is a row of content. Inside this row div, you put more divs for content. The system is designed to put the div's side-by-side as columns (only one level deep). For example, two divs inside the row div will create two columns half the size of the page. If you want additional content which isn't setup as a column, create another row div. 

Portfolio Clips
--------------
Portfolio clips are a featurette section, which follow the rules outline earlier. Here is an example of a single portfolio clip:

```html
<div class="clip">
	<a href="#">
		<img class="featurette-image img-responsive" src="http://placehold.it/400x300/" alt="Generic placeholder image">
	</a>
	<p>A short description of this awesome clip.</p>
</div>
```

Each of these should go inside a div with class `row`. The system will put them side-by-side. For example, if you want three clips side by side, you would create a `row` div with three of these clips. Then create another `row` div with three more clips inside. Likewise, you could put two clips or four clips inside a `row` div, and they will show up side-by-side.

Edit the `src` of the &lt;img&gt; tag with your own image. You can place images in the same folder as this file, or link to images elsewhere on the web.



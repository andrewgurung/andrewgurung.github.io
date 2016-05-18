---
layout: post
title: Getting Started with Bootstrap
comments: true
---

### What is Bootstrap?
- Bootstrap is a powerful toolkit - a collection of HTML, CSS, and JavaScript tools for creating and building web pages and web applications
- Originally created by Twitter

### Benefits
- Responsive by design
- Re-usable components
- Rich extensibility using JavaScript

### Download
- Bootstrap is available in two forms:
  1. Precompiled Version:
    - Vanilla CSS
    - Note: All styles can be overridden later
  2. Source Code Version:
    - Can choose between `Less` and `Sass` preprocessor version
    - Provides flexibility to ambitious developers to customize and build their own version of Bootstrap
- URL: http://getbootstrap.com/getting-started/#download

### File Structure
- Precompiled Version comes with
  1. CSS files
  2. JavaScript files
  3. Font files: Glyphicons fonts folder should be on the same level as the CSS folder
- HTML: HTML templates can be copied and modified from Bootstrap tutorial page

```
bootstrap/
├── css/
│   ├── bootstrap.css
│   ├── bootstrap.css.map
│   ├── bootstrap.min.css
│   ├── bootstrap.min.css.map
│   ├── bootstrap-theme.css
│   ├── bootstrap-theme.css.map
│   ├── bootstrap-theme.min.css
│   └── bootstrap-theme.min.css.map
├── js/
│   ├── bootstrap.js
│   └── bootstrap.min.js
└── fonts/
    ├── glyphicons-halflings-regular.eot
    ├── glyphicons-halflings-regular.svg
    ├── glyphicons-halflings-regular.ttf
    ├── glyphicons-halflings-regular.woff
    └── glyphicons-halflings-regular.woff2
```

### Getting started
- 3 meta tags *must* come first in the head
- Include minified bootstrap CSS file
- Optional: Bootstrap interactive feature
  - Include minified bootstrap JavaScript file
  - Include jQuery library which is referenced by Bootstrap plugins
- Optional: For IE8 support
  - Include HTML5 shim and Respond.js

Start by copying the HTML below to begin a minimal Bootstrap document

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <!-- The above 3 meta tags *must* come first in the head; any other head content must come *after* these tags -->
    <title>Bootstrap Template</title>

    <!-- Bootstrap CSS-->
    <link href="css/bootstrap.min.css" rel="stylesheet">

    <!-- HTML5 shim and Respond.js for IE8 support of HTML5 elements and media queries -->
    <!-- WARNING: Respond.js doesn't work if you view the page via file:// -->
    <!--[if lt IE 9]>
      <script src="https://oss.maxcdn.com/html5shiv/3.7.2/html5shiv.min.js"></script>
      <script src="https://oss.maxcdn.com/respond/1.4.2/respond.min.js"></script>
    <![endif]-->
  </head>
  <body>
    <h1>Hello, world!</h1>
    <!-- jQuery (necessary for Bootstrap's JavaScript plugins) -->
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.2/jquery.min.js"></script>

    <!-- Include all compiled plugins (below), or include individual files as needed -->
    <!-- Bootstrap JS-->
    <script src="js/bootstrap.min.js"></script>
  </body>
</html>
```

## Building HTML pages with Bootstrap
- Bootstrap comes with include many common UI components
- These include Navigation, Grids, Buttons,Tabs, Accordions, and many others
- Many of these use JavaScript extensions and jQuery plugins

### How to use Bootstrap components
- Components are available as well-factored CSS classes
- Convenient to use through semantic class names like `.btn` and `.btn-success`

- For example,  including the `btn-success` class will paint the button in green color

  ```html
  <button type="button" class="btn btn-lg btn-success">Success</button>
  ```

### Grids
- Bootstrap can easily scales your websites with a single code base, from phones to tablets to desktops
- This responsiveness is achieved using a fluid grid system that can be applied to appropriately scale up to 12 columns
- Grid system has 4 tiers of classes:
  1. xs for phones (<768px)
  2. sm for tablets (≥768px)
  3. md for desktops (≥992px)
  4. lg for larger desktops (≥1200px)
- Wrapper contains rows
  1. Fixed-width layout: `.container` class, 1170px width
  2. Full-width layout: `.container-fluid`
- Rows contains columns
  - Max number of columns: 12

```html
<div class="container">
  <div class="row">
    <div class="col-md-8">
      Parent fixed-width column
      <div class="row">
        <div class="col-md-6">Nested column</div>
        <div class="col-md-6">Nested column</div>
      </div>
    </div>
  </div>
</div>
<div class="container-fluid">
  <div class="row">
    <div class="col-md-4">Fluid ..</div>
    <div class="col-md-4">.. and full-width ..</div>
    <div class="col-md-4">.. example</div>
  </div>
</div>
```

### Typography
- Every browser has its own default "user agent" style sheet that is applied to the HTML, and no two browsers have the same defaults
- Bootstrap comes with `Normalize.css` that makes browsers render all elements more consistently and in line with modern standards
- Bootstrap also includes simple and easily customized typography for headings, body text, lists, and more
- For example, Text Emphasis will add colors to emphasize statements
  - `.text-danger` class will display error message in red color

```html
<p class="text-danger">Error: An error has been occurred while submitting your data.</p>
```
- URL: http://getbootstrap.com/css/#type

### Forms
- Bootstrap helps in aligning and styling labels and inputs, validating forms, and showing error messages which can be tricky without some help
- All textual input elements like `input`, `textarea` and `select` are set to 100% of parent element
- Rendering labels and input fields
  - `.form-inline`: Render multiple labels and input fields in same line
  - `.form-horizontal`: Render each input in its own row
  - `.form-control-static`: Render plain text next to a form label
- Bootstrap brings validation styles for different states
  - `.has-warning`
  - `.has-error`
  - `.has-success`
- URL: http://getbootstrap.com/css/#forms


### Images and Icons
- Images can be made responsive by simply adding `.img-responsive` class
- `.img-rounded`: Applies a rounded corner
- `.img-thumbnail`: Converts to a thumbnail image
- Includes over 250 glyphs in font format from the Glyphicon Halflings set
- Font icons are scalable and easy to customize using just CSS
- URL: http://getbootstrap.com/components/#glyphicons


### Buttons, Button groups, Button dropdowns
- Bootstrap makes buttons maintain a consistent look in all browsers through `.btn` class
- `.btn-group`:  Group a series of buttons together into a single line
- Button dropdowns: Use any button to trigger a dropdown menu by placing it within a .btn-group and providing the proper menu markup.
- For example, Country Selection dropdown

```html
<div class="btn-group">
  <button type="button" class="btn btn-default dropdown-toggle" data-toggle="dropdown">
    Country <span class="caret"></span>
  </button>
  <ul class="dropdown-menu">
    <li><a href="#">Canada</a></li>
    <li><a href="#">Mexico</a></li>
    <li><a href="#">USA</a></li>
    <li role="separator" class="divider"></li>
    <li><a href="#">Nepal</a></li>
  </ul>
</div>
```

### Navbars
- Navbars are responsive meta components that serve as navigation headers
- They begin collapsed (and are toggleable) in mobile views and become horizontal as the available viewport width increases
- Under the hood, Navbars are unordered inline list of menu items
- Additional HTML elements can be added to Navbars
  - Brand image or text
  - Search bar and more

## Customizing Bootstrap

### Overriding With CSS
- The most straightforward approach is to override Bootstrap’s styles using CSS

```html
<!-- Replace bootstrap.min.css with custom css -->
<link rel="stylesheet" href="css/custom.css">
```

```css
@import url("bootstrap.min.css");
.btn {
  -webkit-border-radius: 20px;
  -moz-border-radius: 20px;
  border-radius: 20px;
}
```

### Generating A Custom Build
- Customize Bootstrap's components, Less variables, and jQuery plugins to get your very own version.
- URL: http://getbootstrap.com/customize/

### Overriding with LESS
- Download the Source code version
- URL: http://getbootstrap.com/getting-started/#download
- In the LESS directory: (Some things to note about these files)
  1. bootstrap.less
    - This is the central file
    - It imports all of the others and is the one you'll ultimately compile
  2. variables.less and mixins.less
    - Variables contains the same variables as used on the generator websites
  3. utilities.less
    - This is always the last file to be imported, in order for the classes that it contains to override the rest of the styles where necessary

For example:

- The following `.less` file looks pretty similar to css
- Things to notice:
  - `@baseFontSize`: `variable` defined in `variables.less`
  - `.border-radius`: `mixin` defined in `mixins.less`

```less
.btn-large {
   padding: 9px 14px;
   font-size: @baseFontSize + 2px;
   line-height: normal;
   .border-radius(5px);
}
```

#### Installing LESS
1. Install less using Node Package Manager (NPM)

  ```
  npm install less
  ```

2. Compile bootstrap.less

  ```
  lessc bootstrap.less > bootstrap.css
  ```

  For the minified version, use this instead:  
  
  ```
  lessc --compress bootstrap.less > bootstrap.min.css
  ```

#### Modularizing your changes
1. Download Bootstrap source code, rename it to `bootstrap` and leave it untouched
2. Create separate folder named `custom`
3. Copy these files from `bootstrap` to `custom` folder and perform necessary modifications
  - custom-variables.less: Modify the variables in this copy instead of bootstrap original file
  - custom-other.less: Any other customizations that aren't possible with the variables
  - custom-bootstrap.less: The new central file that you will compile to CSS
4. Along with the original LESS files, imports the two custom files above using the following commands

```less
@import "../bootstrap/less/bootstrap.less";
@import "custom-variables.less";
@import "custom-other.less";
@import "../bootstrap/less/utilities.less";
```

Resources:  
- [Tomislav Bacinger's post from Toptol.com](https://www.toptal.com/front-end/what-is-bootstrap-a-short-tutorial-on-the-what-why-and-how)  
- [Thomas Park's post from Smashing Magazine](https://www.smashingmagazine.com/2013/03/customizing-bootstrap/)

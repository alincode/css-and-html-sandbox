# SASS sandbox

## What is sass?
- CSS extension language

### cause
- Stylesheets are getting larger, more complex, and harder to maintain.

### Solution
- Sass lets you use features that don't exist in CSS yet like variables, nesting, mixins, inheritance and other nifty goodies that make writing CSS fun again.

## install

### Mac
```
sudo gem install sass
```

## Run
```
scss --watch style.scss:style.css
```

## Concept

### Variables
```
$font-stack:    Helvetica, sans-serif;
$primary-color: #333;

body {
  font: 100% $font-stack;
  color: $primary-color;
}
```

### Nesting
```
nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  li { display: inline-block; }

  a {
    display: block;
    padding: 6px 12px;
    text-decoration: none;
  }
}
```

### Import
```
html,
body,
ul,
ol {
   margin: 0;
  padding: 0;
}
```

```
@import 'reset';

body {
  font: 100% Helvetica, sans-serif;
  background-color: #efefef;
}
```

### Mixins
```
@mixin border-radius($radius) {
  -webkit-border-radius: $radius;
     -moz-border-radius: $radius;
      -ms-border-radius: $radius;
          border-radius: $radius;
}

.box { @include border-radius(10px); }
```

### Extend/Inheritance
```
.message {
  border: 1px solid #ccc;
  padding: 10px;
  color: #333;
}

.success {
  @extend .message;
  border-color: green;
}

.error {
  @extend .message;
  border-color: red;
}

.warning {
  @extend .message;
  border-color: yellow;
}
```
### Operators
```
.container { width: 100%; }


article[role="main"] {
  float: left;
  width: 600px / 960px * 100%;
}

aside[role="complimentary"] {
  float: right;
  width: 300px / 960px * 100%;
}
```

## Learning Resources

### Website
* [Guide](http://sass-lang.com/guide)

### Article
* [Sass vs. SCSS: which syntax is better?](http://thesassway.com/editorial/sass-vs-scss-which-syntax-is-better)

### Video
* [LevelUpTuts - Sass Tutorials ](https://www.youtube.com/playlist?list=PL2CB1F80266E986EA)

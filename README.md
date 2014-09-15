# SassyPlaceholder [![forthebadge](http://forthebadge.com/badges/built-with-love.svg)](http://forthebadge.com)

A Powerful Sass Placeholder mixin.

### Required

- Sass 3.4
- Bower `npm install -g bower`

### Installation
```ssh
bower install sassyplaceholder --save-dev
```



### How to use

Scss:
```scss
// Creating a Placeholder
// name: %default-style
@include sf-add-p(default-style){
    margin: 10px;
    border: 1px;
}



// Extending...
.header {
    // on small-only breakpoint
  @include sf-breakpoint("small-only"){
      @include sf-use-p(default-style);
  }
}

.footer {
    // on medium-only breakpoint
  @include sf-breakpoint("medium-only"){
      @include sf-use-p(default-style);
  }
}

/* normal extend */
.content{
  @extend %default-style;
}
```
Output:
```css
@media only screen and (max-width: 40em) {
  .header {
    margin: 10px;
    border: 1px; 
  } 
}
@media only screen and (min-width: 40.063em) and (max-width: 64em) {
  .footer {
    margin: 10px;
    border: 1px;
  }
}

/* normal extend */
.content {
  margin: 10px;
  border: 1px;
}
```

### Credits
- [@HugoGiraudel](https://twitter.com/HugoGiraudel)

### License

The SassyPlaceholder is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT)

# CSS conventions

## CSS3 features

#### Properties
CSS Variables are entities defined by CSS authors which contain specific values to be reused throughout a document.

##### [CSS]
 They are set using custom property notation and are accessed using the var() function.

 ```css
   --font-stack:    Helvetica, sans-serif;
   --primary-color: #333;

   body {
     font: 100% var(font-stack;
     color: $primary-color;
   }
 ```

[CSS]: https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_variables

##### [Sass]
```scss
  $font-stack:    Helvetica, sans-serif;
  $primary-color: #333;

  body {
    font: 100% $font-stack;
    color: $primary-color;
  }
```

#### Mixins
A mixin lets you make groups of CSS declarations that you want to reuse throughout your site. You can even pass in values to make your mixin more flexible. A good use of a mixin is for vendor prefixes.

##### [CSS]

```css
 --toolbar-theme: {
   background-color: hsl(120, 70%, 95%);
   border-radius: 4px;
   border: 1px solid var(--theme-color late);
 };

 @apply --toolbar-theme;
```
[CSS]: https://tabatkins.github.io/specs/css-apply-rule/

##### [SASS]

```scss
  @mixin border-radius($radius) {
   -webkit-border-radius: $radius;
      -moz-border-radius: $radius;
       -ms-border-radius: $radius;
           border-radius: $radius;
  }

  .box { @include border-radius(10px); }
```
[SASS]:http://sass-lang.com/guide#topic-6

#### [@import]
The [@import] CSS at-rule is used to import style rules from other style sheets.
[@import]:https://developer.mozilla.org/en-US/docs/Web/CSS/@import

#### [CSS Animations and Transitions]
[CSS animations] make it possible to animate transitions from one CSS style configuration to another. Animations consist of two components, a style describing the CSS animation and a set of keyframes that indicate the start and end states of the animation's style, as well as possible intermediate waypoints.
[CSS animations]:https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Animations/Using_CSS_animations
[CSS Animations and Transitions]:https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Animations/Using_CSS_animations

## Sass features


## Atomic Design

Atomic design is methodology for creating design systems. There are five distinct levels in atomic design:
- [Atoms]
- [Molecules]
- [Organisms]
- [Templates]
- [Pages]

[Atoms]: http://bradfrost.com/blog/post/atomic-web-design/#atoms
[Molecules]: http://bradfrost.com/blog/post/atomic-web-design/#molecules
[Organisms]: http://bradfrost.com/blog/post/atomic-web-design/#organisms
[Templates]: http://bradfrost.com/blog/post/atomic-web-design/#templates
[Pages]: http://bradfrost.com/blog/post/atomic-web-design/#pages

### Why Atomic Design

Atomic design provides a clear methodology for crafting design systems. Clients and team members are able to better appreciate the concept of design systems by actually seeing the steps laid out in front of them.

Atomic design gives us the ability to traverse from abstract to concrete. Because of this, we can create systems that promote consistency and scalability while simultaneously showing things in their final context. And by assembling rather than deconstructing, we’re crafting a system right out of the gate instead of cherry picking patterns after the fact.

Which makes a perfect pattern for using with web components.

## Natural language
Literally every element in nowadays web interfaces already have it's own name (or even several names). We as web developers are using them in every day life talking to other developers and designers. So why should we make up some fancy class names with prefixes or suffixes, abbreviate words or concatenate several words to make selector more unique?

Just use natural language for naming classes. These words are mostly unique already, and they make your code a lot more readable and understandable. Using this names as CSS selector gives us most descriptive and understandable language to build web pages and communicate with other developers.

## BEM
The BEM approach ensures that everyone who participates in the development of a website works with a single codebase and speaks the same language. Using proper naming will prepare you for the changes in design of the website.

In BEM there are three pieces:

### Block
Encapsulates a standalone entity that is meaningful on its own. While blocks can be nested and interact with each other, semantically they remain equal; there is no precedence or hierarchy. Holistic entities without DOM representation (such as controllers or models) can be blocks as well.

```html
HTML:

<div class="block">...</div>
```
```css
CSS:

.block { color: #042; }
```

### Element
Parts of a block and have no standalone meaning. Any element is semantically tied to its block.

```html
HTML:

<div class="block">
  ...
  <span class="block__elem">...</span>
</div>
```
```css
CSS:

.block__elem { color: #042; }
```

### Modifier
Flags on blocks or elements. Use them to change appearance, behavior or state.

```html
HTML:

<div class="block block--mod">
  ...
	<div class="block__element--mod">...</div>
</div>
```
```css
CSS:

.block__elem--mod { }
```

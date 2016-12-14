# CSS naming conventions
Naming is one of the most fundamental and important part of developer activities. Naming conventions help us a lot making our code more readable, predictable. And when it comes to code modification and debugging, conventons help us to easily find needed part of code. They also give us understanding where to put stuff, so it is extremly important to stick to conventions espesially while working in a team.

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

# JavaScript 30 Daily Recap
## Day 1 - JS Drum Kit
* audio tag and how to play audio with JavaScript
* querySelector & querySelectorAll
* classList.add() / className = ""
* addEventListener: 'keydown' and 'transitionend'
* vw: viewport width, vh: viewport height

## Day 2 - CSS and JS Clock
* transform-origin: default value is 50%
* transition-timing-function: custom transition effect
* Date Object
* style: using .style to add styles to an element

## Day 3 - CSS Variables
* When you make up html attributes, it has to have "data-" as the prefix
* To get all those "data-..." attributes as an object, we can call .dataset (ex: this.dataset)
* CSS variable
```css
/* Definition */
--base: #ffc600;

/* Use */
.hl {
    color: var(--base);
}
```
* Update CSS variable with JS

## Day 4 - Array Cardio (Day 1)
* Console.table(Array_of_Objects)
* Normal function -> Arrow function
* filter(), reduce(), map(), sort()
* For reduce(), you need an initial value of the thing you want to return
* Assign array elements to variables when you created a new array (see number 7)

## Day 5 - Flex Panel Gallery
* Using flex box - define properties for flex containers
* A item can be flex container and flex child at the same time
* Learn more about CSS flexbox [here](https://flexbox.io/)
* classList.toggle

## Day 6 - Type Ahead
* fetch() method: return a promise. You need to call appropriate function for that return promise to convert into data (we use json() in this case)
* Use of the ```... spread``` operator to push each data object into the array instead of it entirely (which would push the entire data source at index 0)
* In order to use a variable as your string to match, you need to create a RegExp object. This can then be used in match() methods, for example:
```javascript
const regex = new RegExp(wordToMatch, 'gi');
return place.city.match(regex);
```
* Use of a function to convert number to string with commas
```javascript
function numberWithCommas(x) {
    return x.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ',');
}
```

## Day 7 - Array Cardio (Day 2)
* Array.prototype.some() - Checks against the array, and returns true if at least one item meets the condition specified.
```javascript
const isAdult = people.some(person => (new Date()).getFullYear() - person.year >= 19);
```
* Array.prototype.every() - Checks against the array, and returns true if all items meets the condition specified.
```javascript
const allAdults = people.every(person => (new Date()).getFullYear() - person.year >= 19);
```
* Array.prototype.find() - Checks against the array, and returns the result of the item, that meets the criteria (in this case it is an object)
```javascript
const index = comments.find(comment => comment => comment.id === 823423);
```
* Array.prototype.findIndex() - Checks against the array, and returns the index of the item that meets the condition specified.
```javascript
const index = comments.findIndex(comment => comment.id === 823423);
```
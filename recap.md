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

## Day 8 - HTML Canvas
* canvas has "context". Context can be 2d or 3d. Get the context of a canvas:
```javascript
canvas.getContext('2d');
```
* ES6 way to assign value to multiple variables
```javascript
// Normal way
a = 0;
b = 1;
// ES6
[a, b] = [0, 1];
```
* [globalCompositeOperation](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/globalCompositeOperation)

## Day 9 - Dev Tools
* See exercises

## Day 10 - Shift to Check Boxes
* event.shiftKey

## Day 11 - Custom Video Player
* To assess whether the video is being played or paused:
```javascript
// Return a boolean
video.paused;
```
* Make a video play/pause:
```javascript
video.play();
video.pause();
```
* To change the current playing time of a video:
```javascript
video.currentTime = 60;
```

## Day 12 - Key Sequence Detection

## Day 13 - Slide in on Scroll
* Multiple properties of the window Object:
```javacript
window.innerHeight;
window.scrollY; // Where the top of the screen is currently at when user scrolls
image.offsetTop; // Where the top of the image is when it's scroll out of the screen
```
* CSS transform: translateX(0%) or translateY(0%) - move an object from its original position
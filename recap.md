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

## Day 14 - JS Reference vs Copy
### string, number and boolean
* Javascript makes copy of these type, so changing value of the original variable is fine.
### array
* Assigning an array to a variable will "reference" the original array
```javascript
const players = ['Wes', 'Sarah', 'Ryan', 'Poppy'];
const team1 = players; // Reference
```
* Ways to make copies of array:
```javascript
const team2 = players.slice();
const team3 = [].concat(players);
const team4 = [...players];
const team5 = Array.from(players);
```
### Objects
* Assigning an object to a variable will also "reference" the original object
```javascript
const person = {
      name: 'Wes Bos',
      age: 80
    };
const captain = person;
```
* Ways to make copies of object:
```javascript
const person = {
    name: 'Wes Bos',
    age: 80
};

const cap2 = Object.assign({}, person, { age: 99 });
const cap3 = JSON.parse(JSON.stringify(person));
```
* Note: Object.assign() will only copy the first level of the Object. The next levels are still under reference
```javascript
const wes = {
      name: 'Wes',
      age: 100,
      social: {
        twitter: '@wesbos',
        facebook: 'wesbos.developer'
      }
    }

// Changing level 1 - The original value will not be changed
const dev = Object.assign({}, wes);
dev.name = 'Wesley';
console.log(dev);
console.log(wes);

// Changing level 2 - The original value will also be changed
dev.social.twitter = '@coolman';
console.log(dev.social);
console.log(wes.social);
```

## Day 15 - Local Storage
* Forms
```javascript
// Prevent page to reload after hitting submit button
e.preventDefault()l
// Clear a form
form.reset();
```
* localStorage: store local data for individual webpages/browsers. This enables your pages to have continuity based on existing user behaviors.
    * data is stored as a string that has a key.
    * function: setItem(), getItem(), clear(),...
    * to store objects, we need to 'stringify' objects into strings by using JSON.stringify()
* Event Delegation
* Learn more about client-side storage:
    * localStorage, sessionStorage and cookies [here](https://www.quora.com/What-is-the-difference-between-sessionstorage-localstorage-and-Cookies)
    * getting started with client-side storage [link](http://thejackalofjavascript.com/getting-started-with-client-side-storage/)

## Day 16 - Mouse Move Shadow
* Destructuring objects: cool way to assign multiple values from an object
```javascript
// In this case, we assigning hero.offsetWidth to width, and hero.offsetHeight to height
const { offsetWidth: width, offsetHeight: height } = hero;
```
* event's offset values

## Day 17 - Sort Without Articles

## Day 18 - Adding Up Times with Reduced
* reduce with Array
* parseFloat

## Day 19 - Webcam
* Video: the source of your webcam is in the form of a URL, that can be generated by the operator object
* pixels: Browsers interpret images as a series of pixels, where each pixels' rgba values are stored in a large two dimensional array of millions of values.
* document.createElement - create an element
* insertBefore(element, position)

## Day 20 - Speech Detection
* SpeechRecognition()
* addEventListener - 'result' and 'end'

## Day 21 - Geolocation
* navigator.geolocation.watchPosition() vs. navigator.geolocation.getCurrentLocation()


## Day 22 - Follow Along Link Highlight
* getBoundingClientRect() - return an element size and position relative to the window
```javascript
const elementCoords = this.getBoundingClientRect();
const coords = {
    width: linkCoords.width,
    height: linkCoords.height,
    top: linkCoords.top + window.scrollY,
    left: linkCoords.left + window.scrollX,
}
```
* window.scrollX & window.scrollY - get the position of the window when user scrolls
* addEventListener - 'mouseenter'

## Day 23 - Speech Synthesis
* speechSynthesisUtterance
* global speechSynthesis
* functions that execute on page load vs. functions that execute on call

## Day 24 - Sticky Nav
* offsetTop, offsetHeight, offsetWidth,...
* Use of transition for animation in CSS

## Day 25 - Event Capture, Propagation, Bubbling and Once
* capture - When an event listener has been attached to an element, and that element has parent elements, triggering the event will lead to all elements registering. By default the events will be triggered from the inside out, but setting capture to ```true``` will reverse this direction to outside in.
```javascript
divs.forEach(div => div.addEventListener('click', logText, {
    capture: true
}));
```
* ```e.stopPropagation()``` will make the event only fire at the exact element, not all parent elements associated
* once - This is a useful option for the ```addEventListener``` method, that will prevent the element from triggering multiple events. It has the same functionality as ```removeEventListener```.
```javascript
divs.forEach(div => div.addEventListener('click', logText, {
    once: true
}));
```
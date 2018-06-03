# Lessons learnt

In this lesson I learn how to build a image gallery layout. This was really cool masonry like layout which I plan to recreate for a client website after this course.

## The JavaScript

In order the get create the gallery we also use a smidgen of js. I actually picked up a few tips from this section of the video most notably:

### Random number function

I have used `Math.random` in the pass but have never really needed it the practical work I have done. In the video we create a function to get a random but no higher then the upper limit.

```javascript
function randomNumber(limit) {
  return Math.floor(Math.random() * limit) + 1;
}
```

### `Array.from()`

This method allow us to create a blank array also map function which all map over the blank array.

```javascript
const digits = Array.from({length : 50}, () => [randomNumber(4), randomNumber(4)]);
```

## The CSS

To get the custom grid with different sizes we use:

### The grid container

```css
.gallery {
  display: grid;
  grid-template-columns: repeat(auto-fill, 100px);
  grid-auto-rows: 100px;
}
```

### The grid items

We then go though all of the possible size variations and set up how much they will span. For example

```css
.item.h2 {
  grid-column: span 2;
}

.item.h3 {
  grid-column: span 3;
}

.item.h4 {
  grid-column: span 4;
}
```

### Filling in the empty spaces

To fill in the empty space we use `grid-auto-flow: dense;`

### Using css grid to overlay the view button

Commonly when we need to create overlay we would have to use position absolute, however with CSS grid there is another way to do this.

We firstly make the item that we want the overlay to be on into a one column grid like so:

```css
.item {
  overflow: hidden;
  display: grid;
  grid-template-columns: 1;
  grid-template-rows: 1;
}
```

And then we span the img to cover the whole of the grid. To stop the images from stretching we use `object-fit` which cover the image and chops of the any bits that do not fit.

```css
.item img {
  grid-column: 1 / -1;
  grid-row: 1 / -1;
  width: 100%;
  height: 100%;
  object-fit: cover;
}

 .item__overlay {
  grid-column: 1 / -1;
  grid-row: 1 / -1;
  background: #ffc60032;
  position: relative;
  display: grid;
  justify-items: center;
  align-items: center;
}
```

As both the overlay and image have  `grid-row/column: 1 / -1;` set they both overlap, the z-index is then control in a similar manner to when using poisition absolute each other pretty nifty!

# Lesson learnt

This is where everything is put into practice. Creating a responsive website using grid!

Using named columns to space out content:

```css
 grid-template-areas:
    "hero hero cta1"
    "hero hero cta2"
```

The assign the named columns

```css
  grid-area: cta1;
```

## Menu

min & max autofit to space out the menu items:

```css
  grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
```

Once again the combo of auto-fit and minmax shine though. Using this to make the features responsive.

## Cool use case for CSS variables

A cool use case of css variables is when you want to overide a property you usually would repeat the css lower down in style sheet however now you can just change css variable for example:

```css
.gallery h2:before, .gallery h2:after {
  background: linear-gradient(to var(--direction, left), var(--yellow), transparent)
}

.gallery h2:after {
  --direction: right;
}
```

## Responsive change

Changing the named grid layout like something like:

```css
@media (max-width: 700px) {
  .top {
    grid-template-areas:
    "hero hero"
    "cta1 cta2"
  }
}

@media (max-width: 500px) {
  .top {
    grid-template-areas:
    "hero"
    "cta1"
    "cta2"
  }
}
```

Setting to 1fr means item span the full width of the container, handy when wanting things to collapse down.

## Animation

When creating the responsive menu I use a `perspective` this give a really cool rotating in animation.


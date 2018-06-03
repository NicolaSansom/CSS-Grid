# Lessons learnt

In this video we learn how to reorder grid items.

The default order is every item is zero. So if we give something a order of 1 it would actually comes after all of the items that do not have the order set. So to give order we need to specify it on for all.

From an accessibly stand point only use this if it does not matter what order the items of played back in because a screen reader will still go though the contents how they are in the DOM.

```css
.nav {
  grid-column: span 8;
  order: 1;
}
.logo {
  grid-column: span 2;
  order: 2;
}
.content {
  grid-column: 1 / -1;
  order: 3;
}

```

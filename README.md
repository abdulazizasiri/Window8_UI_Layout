# Window8_UI_Layout

This is the implementation that mimics Windows 8 UI.

The project includes:

1- CSS3 Grid and HTML5.

2- jQuery plug-in built from scratch.

3- Testing frameworks for browsers compatibility.


## CSS3 Grid.

It is a 2D grid layout. It is newer than flexbox which means it has less browser support.

grid is a display property


- Columns: The first thing we need to do is to define a wrapper that includes many items. These items are called grid items.

Add display grid to the wrapper.

```css
.wrapper {

  display: grid;
  grid-template-columns: repeat(3, 1fr);
}
```


The code above creates a grid with 3 columns each Coleman will take width of 1fr.

```css
.wrapper {

  display: grid;
  grid-auto-rows: 200px;
  grid-template-columns: repeat(3, 1fr);
}
```

grid-auto-rows: 200px; gives each row in the grid a width of 200px. The reason is beacsue when we add content to the grid items, it overflow.


The problem with this is, it will give all rows 200px of width which is something that er might not want to do.


To fix that,


```css
.wrapper {

  display: grid;
  grid-auto-rows: minmax(200px, auto);
  grid-template-columns: repeat(3, 1fr);
}
```

grid-template-rows gives each row a specific height.


```css
.wrapper {

  display: grid;
  /* grid-auto-rows: minmax(200px, auto); */
  grid-template-columns: repeat(3, 1fr);
    grid-template-columns: repeat(3, 200px); // Each Row will have a 200px in height.  
}
```

Adding a gap between column will make the layout look great by using:


```css
.wrapper {

  display: grid;
  grid-auto-rows: minmax(200px, auto);
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 10px; //This will add a gap between the columns.
}
```


- Grid Lines. This is a powerful way to make complex grid. This is applied to grid items. Essentially, it species the where items starts and ends on the grid.

```css
.wrapper {

  display: grid;
  grid-auto-rows: minmax(200px, auto);
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 10px; //This will add a gap between the columns.
}
```


```css
.one{
  grid-column: 1/3 ; // This give the item .one a width that start at 1 and ends at 3rd column.
  grid-row: 1/3 ; // This give the item .one a height that start at 1 and ends at 3rd rows. 

}

```

This is a lesson on a grid layout when building user interfaces that needs a grid look. There are some other layouts that can be used such as a card.


More example are found here: https://www.uxpin.com/studio/blog/web-layout-best-practices-12-timeless-ui-patterns-explained/

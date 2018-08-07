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

## Make a cake-type button

So far there's one cake. In this step, you'll add a **cake-type** button so players can change the cake itself, not just the toppings. It works just like a topping chooser, but it broadcasts a different message.

--- task ---

**Duplicate** one of your chooser button sprites to make a new one.

Change its costume so it looks different from the topping choosers — you could draw a small cake symbol, or a different shape, so players know it changes the cake.

![A cake-type chooser button with its own symbol.](images/cake-type-button.gif)

--- /task ---

--- task ---

Move the new button to a free spot along the top of the stage.

```blocks3
when green flag clicked
go to x: (91) y: (149)
```

--- /task ---

--- task ---

When it's clicked, broadcast a new `layer` message and do the same press animation as your other buttons.

```blocks3
when this sprite clicked
broadcast (layer v)
change y by (1)
play sound (Crank v) until done
change y by (-1)
```

--- /task ---

Click the green flag. Your cake-type button sits along the top with the others and wobbles when clicked. It doesn't change anything yet — you'll make it work next. 🎂

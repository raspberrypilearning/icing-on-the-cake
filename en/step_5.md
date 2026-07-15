## Add a chooser button

In this step, you'll make a **chooser** button and place it at the top of the stage.

--- task ---

In the **toppings** sprite add a new **costume**. Give your new costume a name, like `bow`, so you can find it later.

![Duplicating a topping costume and editing it into a new topping.](images/second-topping.gif)

--- /task ---

Your **toppings** sprite now has more than one costume to stamp.

--- task ---

Create a new sprite for your chooser button. Paint it, or bring in a copy of your topping costume.

![A topping chooser button costume, greyed out to look like a button.](images/chooser-costume.png)

--- /task ---

--- task ---

Click on the **code** tab. Resize and position the chooser near the top of the stage so it's out of the decorating area.

```blocks3
when green flag clicked
go to x: (-135) y: (154)
```
--- /task ---

--- task ---

Add a `broadcast`{:class="block3events"} message block onto a `when this sprite clicked`{:class="block3events"} block and make a new message.

```blocks3
when this sprite clicked
broadcast (bow v)
```

--- /task ---

--- task ---

Make the button feel like it is being clicked by moving it and adding sound.

Add the `change y by ()`{:class="block3motion"} and `play sound () until done`{:class="block3sound"} blocks.

```blocks3
when this sprite clicked
broadcast (bow v)
+change y by (1)
+play sound (Crank v) until done
+change y by (-1)
```

--- /task ---

--- task ---

To make a chooser for your other toppings, **duplicate** this sprite, and change its costume to the matching topping.

Move it to a different spot along the top and change the `broadcast ()`{:class="block3events"} message to match.

![Duplicating a chooser to make another one.](images/duplicate-chooser.gif)

![Your chooser buttons along the top of the stage.](images/chooser-row.png)

--- /task ---

--- task ---

The topping follows the cursor and blocks the button. Make it **hide** when it's up near the choosers so it doesn't block them.

Select the **toppings** sprite.

![The toppings sprite.](images/choose-topping.png)

Add an `if then else`{:class="block3control"} block at the end of the `forever`{:class="block3control"} loop: if the `y position`{:class="block3motion"} is above `125`, it hides; otherwise it shows.

```blocks3
when green flag clicked
erase all
forever
go to (mouse-pointer v)
if <mouse down?> then
if <touching color [#7d3a1f]?> then
play sound (Pop v) until done
stamp
end
end
+if <(y position) > (125)> then
hide
else
show
end
end
```

--- /task ---

**Test:** Click the green flag. The topping hides, and you can click the buttons.

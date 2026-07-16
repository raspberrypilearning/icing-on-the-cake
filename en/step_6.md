## Add a chooser button

In this step, you'll make a button for each cake topping and place it at the top of the stage.

--- task ---

Create a new sprite for the chooser button. Paint it, or bring in a copy of your topping costume.

![A topping chooser button costume, greyed out to look like a button.](images/chooser-costume.png)

--- /task ---

--- task ---

Click on the **code tab**. Resize and position the chooser near the top of the stage so it's out of the decorating area.

```blocks3
when green flag clicked
go to x: (-135) y: (154)
```

![Your first chooser button along the top of the stage.](images/chooser-row.png)
--- /task ---

--- task ---

Add a `broadcast`{:class="block3events"} message onto a `when this sprite clicked`{:class="block3events"} block and name the new message to match your sprite.

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


--- /task ---



**Test:** Click the green flag. The topping hides, and you can click the buttons.

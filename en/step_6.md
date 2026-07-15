## Make a topping chooser

Players need a way to pick which topping to stamp. In this step, you'll make a **chooser** button for a topping and place it at the top of the stage.

--- task ---

Add a new sprite for your chooser button. Paint it, or bring in a copy of your topping costume.

Make it look like a button — for example, give it a grey background or an outline so players can tell it apart from the stamped toppings.

![A topping chooser button costume, greyed out to look like a button.](images/chooser-costume.gif)

--- /task ---

--- task ---

Make the chooser a good button size, then position it near the top of the stage so it's out of the decorating area.

```blocks3
when green flag clicked
go to x: (-135) y: (154)
```

--- /task ---

--- task ---

When the chooser is clicked, it should tell the `toppings` sprite which topping to use by **broadcasting** a message.

Make a new message named after the topping, like `bow`.

```blocks3
when this sprite clicked
broadcast (bow v)
```

--- /task ---

--- task ---

Add a little animation and sound so the button feels like it's being pressed. Add the **Crank** sound to the sprite first.

```blocks3
when this sprite clicked
broadcast (bow v)
+change y by (1)
+play sound (Crank v) until done
+change y by (-1)
```

--- /task ---

--- task ---

Now make a chooser for each of your toppings.

**Duplicate** this chooser sprite, then for the copy:

- change its costume to the matching topping
- move it to a different spot along the top
- change the `broadcast ()`{:class="block3events"} message to match, like `strawberry`

--- /task ---

Click the green flag. Your chooser buttons sit along the top of the stage and wobble with a sound when clicked. 🎀🍓

## Create a stamp

In this step, you'll make your first **topping**. 

--- task ---

Start a new Scratch project and delete the cat sprite.

--- /task ---

--- task ---

In the costume tab, create your topping. A topping can be anything you like — sprinkles, a strawberry, a bow, or a candle. 

- **paint** your own topping with the paintbrush tool
- **upload** a topping picture from your computer
- or **choose** a sprite from the Scratch library


![Choosing a topping sprite in Scratch and renaming it to toppings.](images/choose-topping.png)

--- /task ---

--- task ---

Name the sprite `toppings`, because later it will hold lots of different toppings.

--- /task ---

--- task ---

You need the **Pen** blocks to stamp your topping onto the stage.

Click **Add Extension** in the bottom-left corner, then choose **Pen**.

--- /task ---

--- task ---

Make the `toppings` sprite follow the mouse pointer around the stage.

```blocks3
when green flag clicked
forever
go to (mouse-pointer v)
end
```

--- /task ---

--- task ---

Now make it stamp a copy of itself whenever you click the mouse.

Add an `if then`{:class="block3control"} block inside the `forever`{:class="block3control"} loop that checks `mouse down?`{:class="block3sensing"} and then `stamp`s.

```blocks3
forever
go to (mouse-pointer v)
+if <mouse down?> then
stamp
end
end
```

--- /task ---

--- task ---

Clear the screen when you click the green flag.

```blocks3
when green flag clicked
+erase all
forever
go to (mouse-pointer v)
if <mouse down?> then
stamp
end
end
```

--- /task ---

--- task ---
## Add a sound to your stamp. 

Click the **Sounds** tab and choose a sound a click or popping sound from the sound library.

Add a `play sound () until done`{:class="block3sound"} block so it pops each time you stamp.

```blocks3
when green flag clicked
erase all
forever
go to (mouse-pointer v)
if <mouse down?> then
+play sound (Pop v) until done
stamp
end
end
```

--- /task ---

**Test:** Click the green flag, then click around the stage to see stamps of your topping.

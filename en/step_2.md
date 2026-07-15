## Make a topping

In this step, you'll make your first **topping**. 

--- task ---

Start a new Scratch project.

--- /task ---

--- task ---

In the costume tab, delete the cat and create your topping. A topping can be anything you like — sprinkles, a strawberry, a bow, or a candle. 

--- /task ---

--- task ---

Name the sprite `toppings`, because later it will hold lots of different toppings.

![Choosing a topping sprite in Scratch and renaming it to toppings.](images/choose-topping.png)

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

Now make it stamp itself whenever you click the mouse.

To use the `stamp` block, click **Add Extension** in the bottom-left corner, then choose **Pen**.

Add an `if then`{:class="block3control"} block inside the `forever`{:class="block3control"} loop that checks `mouse down?`{:class="block3sensing"} and then `stamp`s.

```blocks3
when green flag clicked
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

Add a `play sound () until done`{:class="block3sound"} block so it pops each time you stamp.

Click the **Sounds** tab and choose a sound a sound you think will work from the sound library.

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

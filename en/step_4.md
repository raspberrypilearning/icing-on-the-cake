## Decorate the cake

Right now your topping stamps anywhere you click. In this step, you'll make it stamp **only on the cake** by detecting the colour of the cake.

--- task ---

Select the **toppings** sprite.

![The toppings sprite.](images/sprite-toppings.png)

--- /task ---

--- task ---

In the **Code tab**, move the `play sound () until done`{:class="block3sound"} and `stamp` blocks into an `if then`{:class="block3control"} block.

```blocks3
when green flag clicked
erase all
forever
go to (mouse-pointer v)
if <mouse down?> then
+if <> then
play sound (Pop v) until done
stamp
end
end
end
```

--- /task ---

--- task ---

Add a `touching colour` block and use the eyedropper to pick the from your cake.

```blocks3
when green flag clicked
erase all
forever
go to (mouse-pointer v)
if <mouse down?> then
+if <touching color [#7d3a1f]?> then
play sound (Pop v) until done
stamp
end
end
end
```

![Using the eyedropper to pick the cake's colour.](images/eyedropper.gif)

**Tip:** If your cake has more than one colour, you can use an `or`{:class="block3operators"} block to pick two colours.

--- /task ---

**Test:** Click the green flag and see that your topping only stamps when the cursor is over the cake.




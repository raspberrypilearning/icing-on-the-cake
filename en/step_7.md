## Only choose above the cake

In this step, you'll make the topping **hide** when it's up near the choosers, so it doesn't get in the way of clicking the buttons.

--- task ---

Select the `toppings` sprite.

Add an `if then else`{:class="block3control"} block at the end of the `forever`{:class="block3control"} loop. If the sprite's `y position`{:class="block3motion"} is above `100` (up near the buttons), it hides; otherwise it shows.

```blocks3
forever
go to (mouse-pointer v)
if <mouse down?> then
if <touching color [#7d3a1f]?> then
play sound (Pop v) until done
stamp
end
end
+if <(y position) > (100)> then
hide
else
show
end
end
```

--- /task ---

**Test:** Click the green flag and move the mouse up to the choosers. The topping disappears so you can click the buttons, then reappears over the cake.

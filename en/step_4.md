## Stamp only on the cake

Right now your topping stamps anywhere you click. In this step, you'll make it stamp **only on the cake**, with a pop sound.

--- task ---

Select the `toppings` sprite.

Click the **Sounds** tab and add the **Pop** sound from the sound library.

--- /task ---

--- task ---

Go back to the **Code** tab.

Add an `if then`{:class="block3control"} block around the `stamp` block that checks whether the sprite is `touching`{:class="block3sensing"} the colour of your cake. Add a `play sound () until done`{:class="block3sound"} block so it pops each time you stamp.

Click the colour box in the `touching color`{:class="block3sensing"} block, then use the **eyedropper** to pick a colour from your cake.

```blocks3
if <mouse down?> then
+if <touching color [#7d3a1f]?> then
play sound (Pop v) until done
stamp
end
end
```

--- /task ---

--- tip ---

Use the eyedropper to pick your cake's colour exactly, rather than guessing. If your cake has two main colours, you can check for both by joining two `touching color`{:class="block3sensing"} blocks with an `or`{:class="block3operators"} block.

--- /tip ---

**Test:** Click the green flag and try stamping. Your topping only stamps when the mouse is over the cake, and pops as it does.

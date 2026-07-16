## More toppings


--- task ---

In the **costume tab**, duplicate your topping and make more toppings for your cake — like a bow, a strawberry, or a candle. Give each new costume a name so you can find it later.

![Duplicating a topping costume and editing it into a new topping.](images/second-topping.gif)

Your **toppings** sprite now has more than one costume to stamp.

--- /task ---

--- task ---

Your topping follows the cursor all over the stage, even up to the top. Make it **hide** when it's near the top, so it only shows over the cake.

Select the **toppings** sprite.

![The toppings sprite.](images/choose-topping.png)

Add an `if then else`{:class="block3control"} block: if the `y position`{:class="block3motion"} is above `125` it hides; otherwise it shows.

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

**Test:** Click the green flag and move the cursor to the top of the stage — your topping disappears, then comes back when it's over the cake.

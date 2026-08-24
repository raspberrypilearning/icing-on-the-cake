## Add a button

In this step, you'll make a button for one of the toppings.

--- task ---

![A strawberry topping costume, greyed out to look like a button.](images/sprite-strwabbutton.png)

Create a new sprite. 

--- /task ---

--- task ---

In the **costume tab**, make an icon for your button. You can paint it, or copy across your topping costume and edit that. 


![A strawberry topping being copied in Scratch](images/button-make.gif)

--- /task ---

--- task ---

Resize and position the button near the top of the stage.

In the **code tab**, add a `go to x: y:`{:class="block3motion"} block so the button starts in the same place each time. Your numbers should match wherever you placed the button.

```blocks3
when green flag clicked
go to x: (-135) y: (154)
```

![A strawberry topping icon on Scratch](images/button-icon.png)


--- /task ---

--- task ---

Add a `broadcast`{:class="block3events"} message onto a `when this sprite clicked`{:class="block3events"} block and name the new message to match your sprite.

```blocks3
when this sprite clicked
broadcast (strawberry v)
```

--- /task ---

--- task ---

Make the button feel like it is being clicked by moving it and adding sound.

Add the `change y by`{:class="block3motion"} and `play sound until done`{:class="block3sound"} blocks.

```blocks3
when this sprite clicked
broadcast (strawberry v)
+change y by (1)
+play sound (Crank v) until done
+change y by (-1)
```
--- /task ---

--- task ---

If your sound is too long, you can cut it using the sound editing tools.

![Cutting a sound with the sound editing tools.](images/cutting-sound.gif)

--- /task ---

**Test:** Your buttons do not work yet because the topping is in the way. Make it **hide** when it's near the top.

![The topping hiding so it doesn't cover the buttons.](images/behind-button.gif)

--- task ---

Select the **toppings** sprite.

![The toppings sprite.](images/sprite-toppings.png)

Add an `if then else`{:class="block3control"} block so that if the `y position`{:class="block3motion"} is above `125` it hides. Otherwise, it shows. 

```blocks3
when green flag clicked
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

**Test:** Click the green flag and check that the topping hides, and you can click the button.

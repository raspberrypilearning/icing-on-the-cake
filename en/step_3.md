## Make a cake

In this step, you'll add your **cake** sprite.

--- task ---

Add a new sprite using the paint tools to draw your cake. Or you can add the cake sprite from the sprite library, and delete the candles.  

![The cake sprite.](images/sprite-cake.png)

--- /task ---

--- task ---

The topping will use the cake colour in a later step, so use the fill tool to recolour the cake using one main colour.

--- /task ---

--- task ---

Position the cake at the bottom of the stage.

![Making the cake.](images/make-cake.gif)

Add a `go to x: y:`{:class="block3motion"} block and change the x and y to your position.

```blocks3
when green flag clicked
go to x: (0) y: (-100)
```

--- /task ---

--- task ---

Add a `hide`{:class="block3looks"} block to hide the sprite, then **stamp** to draw the cake.

The **erase all** block clears all the stamps, so you can start again by clicking the `green flag`{:class="block3control"}.

```blocks3
when green flag clicked
+erase all
go to x: (0) y: (-100)
+hide
+stamp
```

--- /task ---

**Test:** Click the green flag and see that the cake appears on the stage.


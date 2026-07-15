## Stamp the cake types

In this step, you'll make the cake-type button work, so clicking it switches to the next cake and stamps it.

--- task ---

Click **Make a Variable** and create a variable called `layer type`. This just helps the program remember which cake costume is showing, so **untick** its checkbox to hide it from the stage.

--- /task ---

--- task ---

Select the `cake` sprite.

At the start of its `when green flag clicked`{:class="block3events"} script, set `layer type`{:class="block3variables"} to `1` so it always starts on the first cake.

```blocks3
when green flag clicked
+set [layer type v] to (1)
hide
go to x: (0) y: (0)
stamp
```

--- /task ---

--- task ---

Add a new script so that when the cake receives the `layer` message, it switches to the next cake, stamps it in the middle, and remembers which costume it landed on.

```blocks3
when I receive (layer v)
switch costume to (layer type)
next costume
erase all
go to x: (0) y: (0)
stamp
set [layer type v] to (costume [number v])
```

--- /task ---

--- info ---

`erase all` clears the stage before the new cake is stamped, so you don't see two cakes at once. Any toppings already on the cake are cleared too — players just add them again on the new cake.

--- /info ---

**Test:** Click the green flag, then click your cake-type button. The cake changes to the next one each time.

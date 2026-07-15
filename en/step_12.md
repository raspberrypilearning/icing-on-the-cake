## Add nice comments

In this step, you'll add pop-up **nice comments** that cheer the player on. A comment appears every so often, after enough stamps.

--- task ---

Click **Make a Variable** and create a variable called `click count`. It counts how many toppings have been stamped, so **untick** its checkbox to hide it from the stage.

--- /task ---

--- task ---

Select the `toppings` sprite.

Add a `change () by ()`{:class="block3variables"} block so `click count`{:class="block3variables"} goes up by `1` each time a topping is stamped.

```blocks3
if <touching color [#7d3a1f]?> then
play sound (Pop v) until done
stamp
+change [click count v] by (1)
end
```

--- /task ---

--- task ---

Add a new sprite for your comments. In the **Costumes** tab, make a costume for each message — you can type words like "So sweet!" or "Yum!", or draw little pictures.

![Making costumes for the nice comments, one message per costume.](images/nice-comments.gif)

--- /task ---

--- task ---

Add the **Wand** sound to the comments sprite, then add this script. It hides the comment, and after enough stamps it shows a random message for a couple of seconds before resetting.

Change the `4` in `pick random (1) to (4)`{:class="block3operators"} to match how many comment costumes you made.

```blocks3
when green flag clicked
set [click count v] to (0)
hide
forever
if <(click count) > (pick random (20) to (50))> then
switch costume to (pick random (1) to (4))
show
start sound (Wand v)
wait (2) seconds
set [click count v] to (0)
hide
end
end
```

--- /task ---

**Test:** Click the green flag and decorate. After a while, a nice comment pops up to cheer you on.

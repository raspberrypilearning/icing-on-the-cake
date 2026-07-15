## Receive and switch costume

In this step, you'll make the `toppings` sprite **switch costume** when it receives each message, so clicking a chooser changes which topping you stamp.

--- task ---

Select the `toppings` sprite.

For each topping, add a `when I receive ()`{:class="block3events"} script that `switch costume to ()`{:class="block3looks"} the matching costume.

```blocks3
when I receive (bow v)
switch costume to (bow v)
```

--- /task ---

--- task ---

Add one of these scripts for every topping you made, matching each message to its costume.

```blocks3
when I receive (strawberry v)
switch costume to (strawberry v)
```

--- /task ---

**Test:** Click a chooser to pick a topping, then click on the cake to stamp it. You now have a working cake decorator!

--- tip ---
This is a great point to save your project. You can stop here with a simple decorator, or carry on to add cake types, nice comments, and more.
--- /tip ---

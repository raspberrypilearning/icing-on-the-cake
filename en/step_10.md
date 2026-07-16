## Challenge: more cakes
--- challenge ---

For a challenge, you can let players switch between different **cake types** — layered, wedding or cupcakes! 

--- /challenge ---

--- task ---

Start by making a new button. 

**Duplicate** one of your chooser button sprites and change its costume to make a small cake symbol.

![A cake-type chooser button with its own symbol.](images/cake-type-button.png)

--- /task ---

--- task ---

Move the button to a free spot along the top of the stage.

```blocks3
when green flag clicked
go to x: (91) y: (149)
```

![The cake-type button on the stage.](images/cake-button-stage.png)

--- /task ---

--- task ---

Change the broadcast to a new `type` message.

```blocks3
when this sprite clicked
broadcast (type v)
change y by (1)
play sound (Crank v) until done
change y by (-1)
```

--- /task ---

--- task ---

Select the **cake** sprite.

![The cake sprite.](images/choose-cake.png)

Give the cake more costumes to switch between. In the **Costumes** tab, **duplicate** your cake costume and change it into different cakes. Keep the main colour the same so your toppings still stamp.

![Duplicating the cake costume and editing it into a different cake.](images/different-cakes.gif)

--- /task ---

--- task ---

Create a variable called `cake type`{:class="block3variables"} to remember which cake is showing.
--- /task ---

--- task ---

On the **cake** sprite, set `cake type`{:class="block3variables"} to `1` at the start of its green-flag blocks.

```blocks3
when green flag clicked
+set [cake type v] to (1)
hide
go to x: (0) y: (0)
stamp
```

--- /task ---

--- task ---

Add blocks so that when the cake receives the `type` message, it switches to the next costume and stamps it.

```blocks3
when I receive (type v)
switch costume to (cake type)
next costume
erase all
go to x: (0) y: (0)
stamp
set [cake type v] to (costume [number v])
```

--- /task ---

**Test:** Click the green flag, then click your cake-type button. The cake changes to the next one each time.

--- save ---
